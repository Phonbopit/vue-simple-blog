<template>
	<div class="media-content columns">
    <div class="column is-10">
      <p><strong>{{post.title}}</strong>
      <br>
      {{post.text}}
      </p>
      <br>
      <span class="date">On {{post.created_at}}</span>
    </div>
    <div class="column is-2 is-centered">
      <a class="button is-danger is-outlined is-pulled-right" v-on:click="removePost(index)">Delete</a>
    </div>
  </div>
</template>

<script>
	export default {
		name: 'postitem',
		props: ['post', 'index'],
	  methods: {
	  	removePost: function(index) {
	  		this.$parent.removePost(index)
	  	}
	  }
	}
</script>

<style>
	
</style>