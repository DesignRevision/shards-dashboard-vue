<template>
  <div class="card card-small country-stats">

    <!-- Card Header -->
    <div class="card-header border-bottom">
      <h6 class="m-0">{{ title }}</h6>
      <div class="block-handle"></div>
    </div>

    <div class="card-body p-0">

      <!-- Map Container -->
      <div ref="mContainer" width="100%" height="100%" style="width: 100%; height: 180px;"></div>

      <!-- Countries Table List -->
      <table class="table m-0">
        <tbody>
          <tr v-for="(country, idx) in countries" :key="idx">
            <td><img class="country-flag mr-1" :src="country.flag" :alt="country.title"> {{ country.title }}</td>
            <td class="text-right">{{ country.visitorsAmount }}</td>
            <td class="text-right">{{ country.visitorsPercentage }}</td>
          </tr>
        </tbody>
      </table>

    </div>
    <d-card-footer class="border-top">
      <d-row>

        <!-- Time Frame -->
        <d-col>
          <d-select size="sm" value="last-week" style="max-width: 130px;">
            <option value="last-week">Last Week</option>
            <option value="today">Today</option>
            <option value="last-month">Last Month</option>
            <option value="last-year">Last Year</option>
          </d-select>
        </d-col>

        <!-- View Full Report -->
        <d-col class="text-right view-report">
          <a href="#">View full report &rarr;</a>
        </d-col>

      </d-row>
    </d-card-footer>
  </div>
</template>

<script>
const defaultCountriesData = [{
  flag: require('@/assets/images/flags/flag-us.png'),
  title: 'United States',
  visitorsAmount: '12,291',
  visitorsPercentage: '23.32%',
}, {
  flag: require('@/assets/images/flags/flag-uk.png'),
  title: 'United Kingdom',
  visitorsAmount: '11,192',
  visitorsPercentage: '18.8%',
}, {
  flag: require('@/assets/images/flags/flag-au.png'),
  title: 'Australia',
  visitorsAmount: '9,291',
  visitorsPercentage: '12.3%',
}, {
  flag: require('@/assets/images/flags/flag-jp.png'),
  title: 'Japan',
  visitorsAmount: '2,291',
  visitorsPercentage: '8.14%',
}];

const defaultMapsData = [
  ['Country', 'Users'],
  ['United States', 12219],
  ['United Kingdom', 11192],
  ['Australia', 9291],
  ['Japan', 2291],
];

export default {
  name: 'ao-users-by-country',
  props: {
    /**
       * The component title.
       */
    title: {
      type: String,
      default: 'Users by Country',
    },
    /**
       * The countries data.
       */
    countries: {
      type: Array,
      default() {
        return defaultCountriesData;
      },
    },
    /**
       * The maps data.
       */
    mapsData: {
      type: Array,
      default() {
        return defaultMapsData;
      },
    },
  },
  mounted() {
    this.createGoogleMaps()
      .then(this.initCountriesMap);
  },
  methods: {
    createGoogleMaps() {
      if (window.__SDPGoogleChartLoaded__) {
        return new Promise((resolve) => {
          resolve();
        });
      }

      window.__SDPGoogleChartLoaded__ = true;

      return new Promise((resolve, reject) => {
        const gmap = document.createElement('script');
        gmap.src = 'https://www.gstatic.com/charts/loader.js';
        gmap.type = 'text/javascript';
        gmap.onload = resolve;
        gmap.onerror = reject;
        document.body.appendChild(gmap);
      });
    },
    initCountriesMap() {
      const { mapsData } = this;
      const { mContainer } = this.$refs;

      // eslint-disable-next-line
      google.charts.load('current', {
        packages: ['geochart'],
        mapsApiKey: 'AIzaSyD-9tSrke72PouQMnMX-a7eZSW0jkFMBWY',
      });

      // eslint-disable-next-line
      google.charts.setOnLoadCallback(() => {
        // eslint-disable-next-line
        const data = google.visualization.arrayToDataTable(mapsData);

        const options = {
          colorAxis: {
            colors: ['#B9C2D4', '#E4E8EF'],
          },
          legend: false,
          width: '100%',
        };

        // eslint-disable-next-line
        const chart = new google.visualization.GeoChart(mContainer);

        function drawGeochart() {
          chart.draw(data, options);
        }

        drawGeochart();
        window.addEventListener('resize', drawGeochart);
      });
    },
  },
};
</script>
