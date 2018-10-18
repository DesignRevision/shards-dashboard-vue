<template>
  <d-card class="card-small">

    <!-- Card Header -->
    <d-card-header class="border-bottom">
      <h6 class="m-0">{{ title }}</h6>
      <div class="block-handle"></div>
    </d-card-header>

    <d-card-body class="p-0">

      <!-- Top Referrals List Group -->
      <d-list-group flush class="list-group-small">
        <d-list-group-item v-for="(item, idx) in referralData" :key="idx" class="d-flex px-3">
          <span class="text-semibold text-fiord-blue">{{ item.title }}</span>
          <span class="ml-auto text-right text-semibold text-reagent-gray">{{ item.value }}</span>
        </d-list-group-item>
      </d-list-group>

    </d-card-body>

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

  </d-card>
</template>

<script>
const defaultTopReferrals = [{
  title: 'GitHub',
  value: '19,291',
}, {
  title: 'Stack Overflow',
  value: '11,201',
}, {
  title: 'Hacker News',
  value: '9,291',
}, {
  title: 'Reddit',
  value: '8,281',
}, {
  title: 'The Next Web',
  value: '7,128',
}, {
  title: 'Tech Crunch',
  value: '6,218',
}, {
  title: 'YouTube',
  value: '1,218',
}, {
  title: 'Adobe',
  value: '1,171',
},
];

export default {
  name: 'ao-top-referrals',
  props: {
    /**
       * The component's title.
       */
    title: {
      type: String,
      default: 'Top Referrals',
    },
    /**
       * The referral datasets.
       */
    referralData: {
      type: Array,
      default() {
        return defaultTopReferrals;
      },
    },
  },
};
</script>
