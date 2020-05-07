<template>
<div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
	<p>
		<input type="checkbox" v-on:change="markCompleted" > {{ todo.title }}
		<button @click="$emit('delete-todo', todo.id)" style="cursor: pointer; margin-left: 15px;">❌</button>
	</p>
</div>
</template>

<script>
export default{
	name: "TodoItem",
	props: ["todo"],
	methods: {
		markCompleted(){
			this.todo.completed = !this.todo.completed;
		}
	}
}
</script>

<style scoped>
	.todo-item{
		background: #f4f4f4;
		padding: 10px;
		border-bottom: 1px #ccc dotted;
		text-align: center;
	}

	.is-complete{
		text-decoration: line-through;
	}
</style>