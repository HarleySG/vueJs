<template>
	<section class="c-todo-section">
		<ul class="c-todoApp-list">
			<li class="c-todoApp-todo" v-for="(todo, indice) of listTodos" :key="indice">
				<input type="checkbox"
					name="descriptionTodo"
					id="'thisTodo_'+indice"
					:checked="(todo.stateTodo == true) ? 'checked' : ''"
					class="c-todoApp-checkTodo">

				<label for="'thisTodo_'+indice"
					@click="todo.stateTodo = !todo.stateTodo"
					v-text="todo.description"></label>
			</li>
		</ul>
	</section>
</template>

<script>
export default {
	props: ['listTodos']
}
</script>
