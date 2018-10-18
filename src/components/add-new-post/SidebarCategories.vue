<template>
  <d-card class="card-small mb-3">

    <!-- Card Header -->
    <d-card-header class="border-bottom">
      <h6 class="m-0">{{ title }}</h6>
    </d-card-header>

    <d-card-body class="p-0">
      <d-list-group flush>

        <!-- Categories -->
        <d-list-group-item class="px-3 pb-2">
          <d-checkbox class="mb-1" value="uncategorized">Uncategorized</d-checkbox>
          <d-checkbox class="mb-1" value="design">Design</d-checkbox>
          <d-checkbox class="mb-1" value="development">Development</d-checkbox>
          <d-checkbox class="mb-1" value="writing">Writing</d-checkbox>
          <d-checkbox class="mb-1" value="books">Books</d-checkbox>
        </d-list-group-item>

        <!-- Add New Category -->
        <d-list-group-item class="px-3 pb-2">
          <d-input-group class="mb-2">
            <d-input placeholder="New category" />
            <d-input-group-addon append>
              <d-button class="btn-white px-2"><i class="material-icons">add</i></d-button>
            </d-input-group-addon>
          </d-input-group>
        </d-list-group-item>

      </d-list-group>
    </d-card-body>
  </d-card>
</template>

<script>
export default {
  name: 'sidebar-categories',
  props: {
    /**
     * The component's title.
     */
    title: {
      type: String,
      default: 'Categories',
    },
  },
};
</script>

