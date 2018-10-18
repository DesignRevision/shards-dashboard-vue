<template>
    <d-card :class="['stats-small', computedVariationClass, 'card', 'card-small']">
        <d-card-body :class="[computedBodyClass]">
            <div :class="['d-flex', computedInnerWrapperClass]">
                <div :class="['stats-small__data', computedDataFieldClass]">
                    <span :class="['stats-small__label', 'text-uppercase', computedLabelClass]">{{ label }}</span>
                    <h6 :class="['stats-small__value', 'count', computedValueClass]">{{ value }}</h6>
                </div>
                <div :class="['stats-small__data', computedInnerDataFieldClass]">
                    <span :class="['stats-small__percentage', `stats-small__percentage--${computedPercentageModifier}`]">{{ percentage }}</span>
                </div>
            </div>
            <canvas :height="computedCanvasHeight" ref="canvas" :class="[computedChartId]"></canvas>
        </d-card-body>
    </d-card>
</template>

<script>
import Chart from '../../utils/chart';
import { nanoid } from '../../utils';

export default {
  name: 'd-small-stats',
  props: {
    /**
     * The element ID.
     */
    id: {
      type: String,
      required: true,
    },
    /**
     * The label.
     */
    label: {
      type: String,
      default: 'Label',
    },
    /**
     * The value.
     */
    value: {
      type: [Number, String],
      default: 0,
    },
    /**
     * The percentage number or string.
     */
    percentage: {
      type: [Number, String],
      default: 0,
    },
    /**
     * Whether is a value increase.
     */
    increase: {
      type: Boolean,
      default: true,
    },
    /**
     * Whether is a value decrease.
     */
    decrease: {
      type: Boolean,
      default: false,
    },
    /**
     * The Chart.js options.
     */
    chartOptions: {
      type: Object,
      default() {
        return {};
      },
    },
    /**
     * The chart dataset.
     */
    chartData: {
      type: Array,
      required: true,
      default() {
        return [];
      },
    },
    /**
     * The chart configuration. This may override every other setting.
     */
    chartConfig: {
      type: Object,
    },
    /**
     * The variation.
     */
    variation: {
      type: String,
      default: null,
    },
  },
  computed: {
    computedChartId() {
      return this.id || `stats-small-${nanoid()}`;
    },
    computedPercentageModifier() {
      return this.increase ? 'increase' : 'decrease';
    },
    computedVariationClass() {
      return this.variation ? `stats-small--${this.variation}` : null;
    },
    computedBodyClass() {
      if (this.variation === '1') {
        return 'p-0 d-flex';
      }

      return 'px-0 pb-0';
    },
    computedInnerWrapperClass() {
      if (this.variation === '1') {
        return 'flex-column m-auto';
      }

      return 'px-3';
    },
    computedDataFieldClass() {
      if (this.variation === '1') {
        return 'text-center';
      }

      return null;
    },
    computedLabelClass() {
      if (this.variation === '1') {
        return null;
      }

      return 'mb-1';
    },
    computedValueClass() {
      if (this.variation === '1') {
        return 'my-3';
      }

      return 'm-0';
    },
    computedInnerDataFieldClass() {
      if (this.variation === '1') {
        return null;
      }

      return 'text-right align-items-center';
    },
    computedCanvasHeight() {
      if (this.variation === '1') {
        return 120;
      }

      return 60;
    },
  },
  mounted() {
    const chartOptions = {
      ...{
        maintainAspectRatio: true,
        responsive: true,
        legend: {
          display: false,
        },
        tooltips: {
          enabled: false,
          custom: false,
        },
        elements: {
          point: {
            radius: 0,
          },
          line: {
            tension: 0.33,
          },
        },
        scales: {
          xAxes: [{
            gridLines: false,
            ticks: {
              display: false,
            },
          }],
          yAxes: [{
            gridLines: false,
            scaleLabel: false,
            ticks: {
              display: false,
              isplay: false,
              // Avoid getting the graph line cut of at the top of the canvas.
              // Chart.js bug link: https://github.com/chartjs/Chart.js/issues/4790
              suggestedMax: Math.max(...this.chartData[0].data) + 1,
            },
          }],
        },
      },
      ...this.chartOptions,
    };

    const chartConfig = {
      ...{
        type: 'line',
        data: {
          ...{ labels: ['Label 1', 'Label 2', 'Label 3', 'Label 4', 'Label 5'] },
          ...{
            datasets: this.chartData,
          },
        },
        options: chartOptions,
      },
      ...this.chartConfig,
    };

    new Chart(this.$refs.canvas, chartConfig);
  },
};
</script>
