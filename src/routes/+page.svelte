<script>
	import { fade, slide } from 'svelte/transition';
    import Counter from './components/Counter.svelte';
    import Reactive from './components/Reactive.svelte';
    import Todo from './components/Todo.svelte';

    let selected = "Counter";
</script>

<div class="body">
    
    <div class="content">
        <h2>Todo:</h2>
        <p>Fix the todo app 2/13/23</p>
        <p>Work on backend cool shit for sveltekit - in progress</p>
        <p>Work on making this into a docker container</p>
        <p>github</p>
        <select bind:value={selected}>
            <option value="Counter">Counter</option>
            <option value="Reactive">Reactive</option>
            <option value="Todo">Todo</option>
          </select>

        {#if selected==="Counter"}
        <div class="wrapper" transition:slide>
            <Counter />
        </div>

        {:else if selected==="Reactive"}
        <div class="wrapper" transition:slide>
            <Reactive />
        </div>

        {:else if selected==="Todo"}
        <div class="wrapper" transition:slide>
            <Todo />
        </div>
        {/if}
    </div>
</div>

<style>
    
.body {

    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: #8458B3;
}

.content {
    flex-direction: column;
    display: flex;
    justify-content: center;
    background-color: white;
    padding: 20px;
    border-radius: 25px;
    text-align: center;
    width: 80%;
    max-width: 800px;
    height: 80vh;
    border: 2px solid black;
}

.wrapper {
  margin: 40px 0;
  border-bottom: 1px solid black;
  padding-bottom: 20px;
}

select {
  font-size: 16px;
  color: white;
  padding: 10px;
  background-color: #8458B3;
  border: 1px solid #ccc;
}



</style>