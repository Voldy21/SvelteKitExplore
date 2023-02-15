<script>
    let count = 0;
    let rounded = false;

    function floorHalve(){
        if(count % 2 == 1){
        rounded = true;
        setTimeout(()=>rounded=false, 1000);
    }

    count = Math.round( count / 2)
    }

    function Halve(){
        count /= 2;
    }
</script>

<button on:click={() => count++}>
    Increment
</button>

<button on:click={() => count--}>
    Decrement
</button>

<button on:click={() => count*=2}>
    Double
</button>

<button on:click={Halve}>
    Halve
</button>

<button on:click={floorHalve}>
    Floor the half
</button>

<div class="center">
    <div class="Rounded">
        {#if rounded}
            <span>Rounded</span>
        {/if}
    </div>

</div>



<p>Clicked {count} {count === 1 ? 'time' : "times"}</p>

<style>
    p{
        font-family: Arial, Helvetica, sans-serif;
    }

    button {
        background-color: blue;
        color: white;
        border-radius: 25px;
        border: none;
        padding: 10px 20px;
        font-size: 16px;
        cursor: pointer;
        transition: all 0.3s ease;
    }

    button:hover {
        background-color: darkblue;
    }

    button:active {
        transform: translateY(2px);
    }

    .Rounded {
        display:flex;
        justify-content: center;
        font-weight: bold;
        font-size: 1.3rem;
        padding-top: 10px;
        height: 30px;
        width: 85px
}
    .Rounded:after {
        content: '\200b';
    }

    .center {
        display: flex;
        justify-content: center;
    }
</style>