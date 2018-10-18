<template>
  <d-container fluid class="main-content-container px-4">
    <!-- Page Header -->
    <div class="page-header row no-gutters py-4">
      <div class="col-12 col-sm-4 text-center text-sm-left mb-0">
        <span class="text-uppercase page-subtitle">Components</span>
        <h3 class="page-title">Blog Posts</h3>
      </div>
    </div>

    <!-- First Row of Posts -->
    <d-row>
      <d-col v-for="(post, idx) in PostsListOne" :key="idx" lg="3" md="6" sm="12" class="mb-4">
        <d-card class="card-small card-post card-post--1">
          <div class="card-post__image" :style="{ backgroundImage: 'url(\'' + post.backgroundImage + '\')' }">
            <d-badge pill :class="['card-post__category', 'bg-' + post.categoryTheme ]">{{ post.category }}</d-badge>
            <div class="card-post__author d-flex">
              <a href="#" class="card-post__author-avatar card-post__author-avatar--small" :style="{ backgroundImage: 'url(\'' + post.authorAvatar + '\')' }">Written by {{ post.author }}</a>
            </div>
          </div>
          <d-card-body>
            <h5 class="card-title">
              <a href="#" class="text-fiord-blue">{{ post.title }}</a>
            </h5>
            <p class="card-text d-inline-block mb-3">{{ post.body }}</p>
            <span class="text-muted">{{ post.date }}</span>
          </d-card-body>
        </d-card>
      </d-col>
    </d-row>

    <!-- Second Row of Posts -->
    <d-row>
      <d-col v-for="(post, idx) in PostsListTwo" :key="idx" lg="6" sm="12" class="mb-4">
        <d-card class="card-small card-post card-post--aside card-post--1">
          <div class="card-post__image" :style="{ backgroundImage: 'url(\'' + post.backgroundImage + '\')' }">
            <d-badge pill :class="['card-post__category', 'bg-' + post.categoryTheme ]">{{ post.category }}</d-badge>
            <div class="card-post__author d-flex">
              <a href="#" class="card-post__author-avatar card-post__author-avatar--small" :style="{ backgroundImage: 'url(\'' + post.authorAvatar + '\')' }">Written by Anna Ken</a>
            </div>
          </div>
          <d-card-body>
            <h5 class="card-title">
              <a class="text-fiord-blue" href="#">{{ post.title }}</a>
            </h5>
            <p class="card-text d-inline-block mb-3">{{ post.body }}</p>
            <span class="text-muted">{{ post.date }}</span>
          </d-card-body>
        </d-card>
      </d-col>
    </d-row>

    <!-- Third Row of Posts -->
    <d-row>
      <d-col v-for="(post, idx) in PostsListThree" :key="idx" lg="4">
        <d-card class="card-small card-post mb-4">
          <d-card-body>
            <h5 class="card-title">{{ post.title }}</h5>
            <p class="card-text text-muted">{{ post.body }}</p>
          </d-card-body>
          <d-card-footer class="border-top d-flex">
            <div class="card-post__author d-flex">
              <a href="#" class="card-post__author-avatar card-post__author-avatar--small" :style="{ backgroundImage: 'url(\'' + post.authorAvatar + '\')' }">Written by James Khan</a>
              <div class="d-flex flex-column justify-content-center ml-3">
                <span class="card-post__author-name">{{ post.author }}</span>
                <small class="text-muted">{{ post.date }}</small>
              </div>
            </div>
            <div class="my-auto ml-auto">
              <d-button size="sm" class="btn-white">
                <i class="far fa-bookmark mr-1"></i> Bookmark
              </d-button>
            </div>
          </d-card-footer>
        </d-card>
      </d-col>
    </d-row>

    <!-- Fourth Row of Posts -->
    <d-row>
      <d-col v-for="(post, idx) in PostsListFour" :key="idx" lg="3" md="6" sm="12" class="mb-4">
        <d-card class="card-small card-post h-10">
          <div class="card-post__image" :style="{ backgroundImage: 'url(\'' + post.backgroundImage + '\')' }"></div>
          <d-card-body>
            <h5 class="card-title">
              <a class="text-fiord-blue" href="#">{{ post.title }}</a>
            </h5>
            <p class="card-text">{{ post.body }}</p>
          </d-card-body>
          <d-card-footer class="text-muted border-top py-3">
            <span class="d-inline-block">By <a class="text-fiord-blue" :href="post.authorUrl">{{ post.author }}</a> in <a class="text-fiord-blue" :href="post.categoryUrl">{{ post.category }}</a></span>
          </d-card-footer>
        </d-card>
      </d-col>
    </d-row>
  </d-container>
</template>

<script>
// First Row of Posts
const PostsListOne = [{
  backgroundImage: require('@/assets/images/content-management/1.jpeg'),
  category: 'Business',
  categoryTheme: 'dark',
  author: 'Anna Kunis',
  authorAvatar: require('@/assets/images/avatars/1.jpg'),
  title: 'Conduct at an replied removal an amongst',
  body: 'However venture pursuit he am mr cordial. Forming musical am hearing studied be luckily. But in for determine what would see...',
  date: '28 February 2019',
}, {
  backgroundImage: require('@/assets/images/content-management/2.jpeg'),
  category: 'Travel',
  categoryTheme: 'info',
  author: 'James Jamerson',
  authorAvatar: require('@/assets/images/avatars/2.jpg'),
  title: 'Off tears are day blind smile alone had ready',
  body: 'Is at purse tried jokes china ready decay an. Small its shy way had woody downs power. To denoting admitted speaking learning my...',
  date: '29 February 2019',
}, {
  backgroundImage: require('@/assets/images/content-management/3.jpeg'),
  category: 'Technology',
  categoryTheme: 'royal-blue',
  author: 'Jimmy Jackson',
  authorAvatar: require('@/assets/images/avatars/2.jpg'),
  title: 'Difficult in delivered extensive at direction',
  body: 'Is at purse tried jokes china ready decay an. Small its shy way had woody downs power. To denoting admitted speaking learning my...',
  date: '29 February 2019',
}, {
  backgroundImage: require('@/assets/images/content-management/4.jpeg'),
  category: 'Business',
  categoryTheme: 'warning',
  author: 'John James',
  authorAvatar: require('@/assets/images/avatars/3.jpg'),
  title: 'It so numerous if he may outlived disposal',
  body: 'How but sons mrs lady when. Her especially are unpleasant out alteration continuing unreserved ready road market resolution...',
  date: '29 February 2019',
}];

  // Second Row of posts
const PostsListTwo = [{
  backgroundImage: require('@/assets/images/content-management/5.jpeg'),
  category: 'Travel',
  categoryTheme: 'info',
  author: 'Anna Ken',
  authorAvatar: require('@/assets/images/avatars/0.jpg'),
  title: 'Attention he extremity unwilling on otherwise cars backwards yet',
  body: 'Conviction up partiality as delightful is discovered. Yet jennings resolved disposed exertion you off. Left did fond drew fat head poor jet pan flying over...',
  date: '29 February 2019',
}, {
  backgroundImage: require('@/assets/images/content-management/6.jpeg'),
  category: 'Business',
  categoryTheme: 'dark',
  author: 'John James',
  authorAvatar: require('@/assets/images/avatars/1.jpg'),
  title: 'Totally words widow one downs few age every seven if miss part by fact',
  body: 'Discovered had get considered projection who favourable. Necessary up knowledge it tolerably. Unwilling departure education to admitted speaking...',
  date: '29 February 2019',
}];

  // Third Row of Posts
const PostsListThree = [{
  author: 'John James',
  authorAvatar: require('@/assets/images/avatars/1.jpg'),
  title: 'Had denoting properly jointure which well books beyond',
  body: 'In said to of poor full be post face snug. Introduced imprudence see say unpleasing devonshire acceptance son. Exeter longer wisdom work...',
  date: '29 February 2019',
}, {
  author: 'John James',
  authorAvatar: require('@/assets/images/avatars/2.jpg'),
  title: 'Husbands ask repeated resolved but laughter debating',
  body: 'It abode words began enjoy years no do ﻿no. Tried spoil as heart visit blush or. Boy possible blessing sensible set but margaret interest. Off tears...',
  date: '29 February 2019',
}, {
  author: 'John James',
  authorAvatar: require('@/assets/images/avatars/3.jpg'),
  title: 'Instantly gentleman contained belonging exquisite now direction',
  body: 'West room at sent if year. Numerous indulged distance old law you. Total state as merit court green decay he. Steepest merit checking railway...',
  date: '29 February 2019',
}];

const PostsListFour = [{
  backgroundImage: require('@/assets/images/content-management/7.jpeg'),
  author: 'Alene Trenton',
  authorUrl: '#',
  category: 'News',
  categoryUrl: '#',
  title: 'Extremity so attending objection as engrossed',
  body: 'Pursuit chamber as elderly amongst on. Distant however warrant farther to of. My justice wishing prudent waiting in be...',
  date: '29 February 2019',
}, {
  backgroundImage: require('@/assets/images/content-management/8.jpeg'),
  author: 'Chris Jamie',
  authorUrl: '#',
  category: 'News',
  categoryUrl: '#',
  title: 'Bed sincerity yet therefore forfeited his',
  body: 'Speaking throwing breeding betrayed children my to. Me marianne no he horrible produced ye. Sufficient unpleasing and...',
  date: '29 February 2019',
}, {
  backgroundImage: require('@/assets/images/content-management/9.jpeg'),
  author: 'Monica Jordan',
  authorUrl: '#',
  category: 'News',
  categoryUrl: '#',
  title: 'Object remark lively all did feebly excuse our',
  body: 'Morning prudent removal an letters by. On could my in order never it. Or excited certain sixteen it to parties colonel not seeing...',
  date: '29 February 2019',
}, {
  backgroundImage: require('@/assets/images/content-management/10.jpeg'),
  author: 'Monica Jordan',
  authorUrl: '#',
  category: 'News',
  categoryUrl: '#',
  title: 'His followed carriage proposal entrance',
  body: 'For county now sister engage had season better had waited. Occasional mrs interested far expression directly as regard...',
  date: '29 February 2019',
}];

export default {
  data() {
    return {
      PostsListOne,
      PostsListTwo,
      PostsListThree,
      PostsListFour,
    };
  },
};
</script>

