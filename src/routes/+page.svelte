<script lang="ts">
  import Todo from "../components/Todo.svelte";

  // define todo items 
  let todos = [
    { id: 1, title: 'Task 1', completed: false },
    { id: 2, title: 'Task 2', completed: true }
  ]
</script>

<style>

</style>

<div>
  { #each todos as todo (todo.id) }
  <Todo title={todo.title} completed={todo.completed} />  
  {/each}
</div>