<template>
	<div>
		<section class="posts">
      <div class="container">
        <div class="columns">
          <div class="column is-half is-offset-one-quarter">
            <h2 class="title">Posts</h2>
            <div class="box" v-for="(post, index) in posts">
              <PostItem :post="post" :index="index"></PostItem>
            </div>
          </div>
        </div>
      </div>
    </section>
	</div>
</template>

<script>
  import PostItem from './PostItem'

	export default {
		name: 'postlist',
		props: ['posts'],
		components: {
			PostItem
		},
		methods: {
			removePost: function(index) {
				this.posts.splice(index, 1)
			}
		}
	}
</script>

<style>
.posts {
	margin: 2em 0;
}

.posts .date {
  font-size: 0.75rem;
}
</style>