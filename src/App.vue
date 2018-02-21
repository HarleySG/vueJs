<template>
	<main id="app" v-cloak class="o-todo">
		<div class="c-todoApp">
			<header-todo></header-todo>
			<new-todo></new-todo>
			<list-todo :listTodos="arrTodos"></list-todo>
		</div>
	</main>
</template>

<script>
import HeaderTodo from "./components/HeaderTodo.component.vue"
import NewTodo from "./components/NewTodo.component.vue"
import ListTodo from "./components/ListTodo.component.vue"

export default {
	components: {
		HeaderTodo,
		NewTodo,
		ListTodo
	},
	data () {
		return {
			arrTodos: [
				{
					description: 'Todo de ejemplo',
					stateTodo: false
				}
			]
		}
	}
}
</script>

<style lang="scss">
	*, *::before, *::after{
		box-sizing: border-box;
	}
	html{
		font-family: 'Helvetica', Arial, sans-serif;
		font-size: 16px;
	}
</style>
