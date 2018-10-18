<template>
  <d-card class="card-small mb-3">
    <d-card-header class="border-bottom">
      <h6 class="m-0">{{ title }}</h6>
    </d-card-header>

    <d-card-body class="p-0">
      <d-list-group flush>
        <d-list-group-item class="p-3">
          <span class="d-flex mb-2"><i class="material-icons mr-1">flag</i><strong class="mr-1">Status:</strong> Draft <a class="ml-auto" href="#">Edit</a></span>
          <span class="d-flex mb-2"><i class="material-icons mr-1">visibility</i><strong class="mr-1">Visibility:</strong> <strong class="text-success">Public</strong> <a class="ml-auto" href="#">Edit</a></span>
          <span class="d-flex mb-2"><i class="material-icons mr-1">calendar_today</i><strong class="mr-1">Schedule:</strong> Now <a class="ml-auto" href="#">Edit</a></span>
          <span class="d-flex"><i class="material-icons mr-1">score</i><strong class="mr-1">Readability:</strong> <strong class="text-warning">Ok</strong></span>
        </d-list-group-item>

        <d-list-group-item class="d-flex px-3">
          <d-button size="sm" class="btn-outline-accent">
            <i class="material-icons">save</i> Save Draft
          </d-button>

          <d-button size="sm" class="btn-accent ml-auto">
            <i class="material-icons">file_copy</i> Publish
          </d-button>
        </d-list-group-item>
        </d-list-group>
    </d-card-body>
  </d-card>
</template>

<script>
export default {
  name: 'sidebar-actions',
  props: {
    /**
     * The component's title.
     */
    title: {
      type: String,
      default: 'Actions',
    },
  },
};
</script>
