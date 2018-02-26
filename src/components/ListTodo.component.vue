<template>
	<section class="c-todo-body">
		<ul class="c-todo-list">
			<li class="c-todo-list--item"
				v-for="(todo, indice) of listTodos"
				:key="indice"
				:class="{'u-complete' : todo.stateTodo}">

				<input type="checkbox"
					name="descriptionTodo"
					:id="'thisTodo_'+indice"
					:checked="(todo.stateTodo == true) ? 'checked' : ''"
					class="c-todo-checkTodo">

				<label :for="'thisTodo_'+indice"
					@click="todo.stateTodo = !todo.stateTodo"
					v-text="todo.description"
					class="c-todo-checkTodo"></label>
			</li>
		</ul>
	</section>
</template>

<script>
export default {
	props: ['listTodos']
}
</script>

<style lang="scss" scoped>
	@import '../assets/TodoList/todoList.scss';
</style>
