<template>
  <d-card class="card-small h-100">

    <!-- Component Header -->
    <d-card-header class="border-bottom">
      <h6 class="m-0">{{ title }}</h6>
    </d-card-header>

    <d-card-body class="d-flex flex-column">
      <d-form class="quick-post-form">

        <!-- Title -->
        <div class="form-group">
          <d-input class="form-control" placeholder="Brave New World" />
        </div>

        <!-- Body -->
        <div class="form-group">
          <d-textarea class="form-control" placeholder="Words can be like X-rays if you use them properly..." />
        </div>

        <!-- Create Draft -->
        <div class="form-group">
          <d-button class="btn-accent" type="submit">Create Draft</d-button>
        </div>

      </d-form>
    </d-card-body>

  </d-card>
</template>

<script>
export default {
  name: 'new-draft',
  props: {
    /**
       * The component's title.
       */
    title: {
      type: String,
      default: 'New Draft',
    },
  },
};
</script>
