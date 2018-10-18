<template>
  <d-card class="card-small blog-comments">

    <!-- Card Header -->
    <d-card-header class="border-bottom">
      <h6 class="m-0">{{ title }}</h6>
    </d-card-header>

    <d-card-body class="p-0">
      <div v-for="(discussion, idx) in discussionsData" :key="idx" class="blog-comments__item d-flex p-3">

        <!-- Avatar -->
        <div class="blog-comments__avatar mr-3">
          <img :src="discussion.author.image" :alt="discussion.author.name" />
        </div>

        <!-- Content -->
        <div class="blog-comments__content">

          <!-- Content - Title -->
          <div class="blog-comments__meta text-muted">
            <a class="text-secondary" :href="discussion.author.url">{{ discussion.author.name }}</a> on <a class="text-secondary" :href="discussion.post.url">{{ discussion.post.title }}</a> <span class="text-muted">– {{ discussion.date }}</span>
          </div>

          <!-- Content - Body -->
          <p class="m-0 my-1 mb-2 text-muted">{{ discussion.body }}</p>

          <!-- Content - Actions -->
          <div class="blog-comments__actions">
            <d-button-group size="small">
              <d-button class="btn-white" @click="handleClick('approve', discussion.id)">
                <span class="text-success"><i class="material-icons">check</i></span> Approve
              </d-button>
              <d-button class="btn-white" @click="handleClick('reject', discussion.id)">
                <span class="text-danger"><i class="material-icons">clear</i></span> Reject
              </d-button>
              <d-button class="btn-white" @click="handleClick('edit', discussion.id)">
                <span class="text-light"><i class="material-icons">more_vert</i></span> Edit
              </d-button>
            </d-button-group>
          </div>
        </div>

      </div>
    </d-card-body>

    <d-card-footer class="border-top">
      <d-row>

        <!-- View All Comments -->
        <d-col class="text-center view-report">
          <d-button type="submit" class="btn-white" @click="handleClick('view-all-comments')">View All Comments</d-button>
        </d-col>

      </d-row>
    </d-card-footer>
  </d-card>
</template>

<script>
const defaultDiscussionsData = [{
  id: 1,
  date: '3 days ago',
  author: {
    image: require('@/assets/images/avatars/1.jpg'),
    name: 'John Doe',
    url: '#',
  },
  post: {
    title: 'Hello World!',
    url: '#',
  },
  body: 'Well, the way they make shows is, they make one show ...',
}, {
  id: 2,
  date: '4 days ago',
  author: {
    image: require('@/assets/images/avatars/2.jpg'),
    name: 'John Doe',
    url: '#',
  },
  post: {
    title: 'Hello World!',
    url: '#',
  },
  body: 'After the avalanche, it took us a week to climb out. Now...',
}, {
  id: 3,
  date: '5 days ago',
  author: {
    image: require('@/assets/images/avatars/3.jpg'),
    name: 'John Doe',
    url: '#',
  },
  post: {
    title: 'Hello World!',
    url: '#',
  },
  body: 'My money\'s in that office, right? If she start giving me...',
}];

export default {
  name: 'discussions',
  props: {
    /**
       * The component's title.
       */
    title: {
      type: String,
      default: 'Discussions',
    },
    /**
       * The discussions data.
       */
    discussionsData: {
      type: Array,
      default() {
        return defaultDiscussionsData;
      },
    },
  },
  methods: {
    /**
       * Emits an action and passes the discussions' ID for reference.
       * @param  {String} action The action type. One of: approve,reject,edit,view-all-comments
       */
    handleClick(action, id) {
      this.$emit(action, id);
    },
  },
};
</script>
