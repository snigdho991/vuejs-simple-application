<template>
	<header class="header">
		<h1>Todo List</h1>
		<div id="nav">
			<router-link to="/">Home</router-link> |
			<router-link to="/about">About</router-link> |
			<router-link to="/contact">Contact</router-link>
		</div>
	</header>
</template>

<script>
export default {

  name: "Header",

}
</script>

<style lang="css" scoped>
	.header{
		background: #333;
		color: #fff;
		text-align: center;
		padding: 10px;
	}

	.header{
		color: #fff;
		padding-right: 5px;
	}
</style>