<template>
	<header>
		<input type="text"
					autofocus
					v-model="newTodo">
	</header>
</template>

<script>
export default {
	props: {
		arrTodos: [
			{
				description: String,
				stateTodo: Boolean
			}
		]
	},
	data() {
		return {
			newTodo: ''
		}
	}
}
</script>
