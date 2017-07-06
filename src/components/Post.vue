<template>
	<section class="new-post">
		<div class="container">
			<div class="columns">
			  <div class="column is-half is-offset-one-quarter">
			    <h2 class="title">Create new post</h2>
			    <form id="form" v-on:submit.prevent="addPost">
			      <div class="field">
			        <label class="label">Title</label>
			        <p class="control">
			          <input class="input" type="text" placeholder="Title" v-model="newPost.title">
			        </p>
			      </div>
			      <div class="field">
			        <label class="label">Content</label>
			        <p class="control">
			          <textarea class="textarea" placeholder="Put your content here." v-model="newPost.text"></textarea>
			        </p>
			      </div>
			      <div class="field">
			        <input type="submit" class="button is-primary" value="Add Post" :disabled="newPost.title === '' && newPost.text === ''">
			      </div>
			    </form>
			  </div>
			</div>
		</div>
  </section>
</template>

<script>
	export default {
		name: 'post',

		data() {
	    return {
	      newPost: {
	        title: '',
	        text: ''
	      }
	    }
	  },

	  methods: {
	  	addPost: function() {
	  		this.$parent.addPost(this.newPost)

	  		this.newPost.title = ''
	  		this.newPost.text = ''
	  	}
	  }
	}
</script>

<style>
	
</style>