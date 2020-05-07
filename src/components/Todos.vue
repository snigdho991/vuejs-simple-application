<template>
<div>
	<div v-bind:key="todo.id" v-for="todo in todos">
		<h3><TodoItem v-bind:todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)" /></h3>
	</div>
</div>
</template>

<script>
import TodoItem from './TodoItem.vue'

export default {
  name: "Todos",
  components: {
	TodoItem
  },
  props: ["todos"]
}
</script>

<style lang="css" scoped>

</style>