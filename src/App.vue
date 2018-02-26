<template>
	<main id="app" v-cloak class="o-todo">
		<div class="c-todo">
			<header-todo></header-todo>
			<new-todo :arrTodos="arrTodos"></new-todo>
			<list-todo :listTodos="arrTodos"></list-todo>
			<footer class="c-todo-footer" v-if="arrTodos != ''"></footer>
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
			arrTodos: []
		}
	}
}
</script>

<style lang="scss">
	@import 'assets/index.scss';

	.o-todo{
		width: 100%;
		max-width: 64em;
		margin: 0 auto;
	}
	.c-{
		&todo{
			position: relative;
			margin: 0 auto;
			background-color: white;
			box-shadow: 0 2px 4px rgba(black, 0.2),
							0 25px 50px 0 rgba(black, 0.1);
			&-footer{
				min-height: 1.5rem;
				padding: 20px 15px;
				color: var(--color_1);

				&::before{
					content: '';
					position: absolute;
					right: 0;
					bottom: 0;
					left: 0;
					height: 2rem;
					overflow: hidden;
					box-shadow: 0 1px 1px rgba(black, 0.2),
									0 8px 0 -3px rgba(#f5f5f5, 1),
									0 9px 1px -3px rgba(black, 0.2),
									0 16px 0 -6px rgba(#f5f5f5, 1),
									0 17px 2px -6px rgba(black, 0.2),
				}
			}
		}
	}
</style>
