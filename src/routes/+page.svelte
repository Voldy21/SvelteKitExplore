<script>
    import Counter from './components/Nested.svelte';

</script>

<div class="body">
    
    <div class="content">
        <div class="wrapper">
            <Counter />
        </div>
        <div class="wrapper">
            
        </div>
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
    background-color: white;
    padding: 20px;
    border-radius: 25px;
    text-align: center;
    width: 80%;
    max-width: 800px;
    border: 2px solid black;
}

.wrapper {
  margin: 40px 0;
  border-bottom: 1px solid black;
  padding-bottom: 20px;
}



</style>