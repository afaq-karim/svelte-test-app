<script lang="ts">
  import { onMount } from "svelte";

  export let title: string;
  export let completed: boolean;

  onMount(() => {
    console.log(title, completed);
  })
</script>

<style>
  .container {
    max-width: 500px;
    margin: 0 auto;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 10px;
  }

  h2 {
    margin: 0;
  }

  .completed {
    text-decoration: line-through;
    opacity: 0.5;
  }
</style>

<div class="container">
  <h2 class:completed={completed}>{title}</h2>
  {#if completed}
    <input type="checkbox" name="todo" id={title} value={true} checked>
  {:else}
    <input type="checkbox" name="todo" id={title} value={true}>
  {/if}
</div>






