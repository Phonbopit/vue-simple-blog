<template>
	<header class="header">
		<section class="hero is-success">
			<div class="hero-body">
				<div class="container">
					<h1 class="title">{{ title }}</h1>
					<h2>{{ subtitle }}</h2>
				</div>
			</div>
		</section>
	</header>
</template>

<script>
	export default {
		name: 'super-header',
		data() {
			return {
				title: 'Vue Chat',
				subtitle: 'Simple Chat Application with Vue.js'
			}
		}
	}
</script>