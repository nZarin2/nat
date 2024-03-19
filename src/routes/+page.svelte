<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>


<script> import '../style.css'
let todoItem = '';
let todoList = [];
function addToArray() {
     todoList.push(todoItem);
     todoList = todoList;
     console. log(todoList);
     todoItem= '';
}
</script>
<h1>To do</h1>
<form on:submit={addToArray}>
     <input type="text" bind:value={todoItem}>
<input type="Submit"><button> Add </button>
</form>
<ul>
     {#each todoList as item}
 <li>
<input type="checkbox">
{item}


</li>

{/each}
</ul>
<style>
     ul{
          list-style: none;
     }
</style>