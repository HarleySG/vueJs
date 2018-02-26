<template>
	<section class="c-todo-new">
		<input type="text"
					:placeholder="arrTodos == '' ? placeHolder.default : 'What will you do?'"
					autofocus
					v-model="newTodo"
					@keyup.enter="addTodo"
					class="c-todo-new--input">
	</section>
</template>

<script>
export default {
	props: ['arrTodos'],
	data() {
		return {
			newTodo: '',
			placeHolder: {
				type: String,
				default: 'Nothing todo'
			}
		}
	},
	methods: {
		addTodo () {
			let textInNewTodo = this.newTodo.trim();
			if(textInNewTodo) {
				this.arrTodos.push({
					description: textInNewTodo,
					stateTodo: false
				})
			}
			this.newTodo= ''
		}
	}
}
</script>

<style lang="scss" scoped>
	@import '../assets/TodoList/todoNew.scss';
</style>
