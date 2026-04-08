<script>
    let todos = $state([
        { title: 'Assignment 1', done: false },
        { title: 'Assignment 2', done: true },
        { title: 'Assignment 3', donez: false }
    ]);
    //array di oggetti, ogni oggetto ha una proprietà title e done
</script>

<h3>My Todos</h3>

<ul>
    {#each todos as todo}
        <li> {todo.title} </li>
        <input type="checkbox" bind:checked={todo.done} />
    {/each}
</ul>