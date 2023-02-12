<script>
    import "../app.css"
    import TodoForm from "../components/TodoForm.svelte";
    import Todo from "../components/Todo.svelte";
    import {todos} from "../stores/todoStores.js";
</script>

<div class="container mx-auto my-6 max-w-lg">
    <h1 class="text-2xl font-bold text-center text-gray-800 md:text-3xl">My Todo List</h1>
    <TodoForm/>
    {#each $todos as todo}
        <Todo todo={todo} index={todo.id}/>
    {/each}
</div>
