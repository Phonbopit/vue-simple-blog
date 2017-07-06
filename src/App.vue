<template>
  <div id="app">
    <app-header></app-header>
    <Post></Post>
    <PostList :posts="posts"></PostList>
    <app-footer></app-footer>
  </div>
</template>

<script>
import moment from 'moment'

import AppHeader from './components/Header'
import Post from './components/Post'
import PostList from './components/PostList'
import AppFooter from './components/Footer'

export default {
  name: 'app',

  components: {
    AppHeader,
    Post,
    PostList,
    AppFooter
  },

  data() {
    return {
      posts: [],
      newPost: {
        title: '',
        text: ''
      }
    }
  },

  methods: {
    addPost: function(post) {
      console.log('post', post)
      post.created_at = moment().format('DD MMM, YYYY HH:mm:ss')
      this.posts.push(Object.assign({}, post))
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
