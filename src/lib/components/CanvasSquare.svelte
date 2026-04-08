<script>
import { untrack } from 'svelte';

    let size = $state(50);
    let color = $state('#ff3e00');

    let canvas 

    $effect(() => {
        const context = canvas.getContext('2d');
        context.clearRect(0, 0, canvas.width, canvas.height);

        context.fillStyle = untrack(() => color);
        context.fillRect(0, 0, size, size);
    });

// Con `onMount` il codice genera X numeri **solo all’inizio** al montaggio del componente, es componente che prende dati api dal meteo.
// Con `$:` (reactive statement) i numeri vengono aggiornati **solo quando cambiano** `size` o `color`, non automaticamente all’inizio, prende dati continuamente.

   ;
</script>

<h3>Canvas Square</h3>


<article>
    <canvas bind:this={canvas} width="100" height="100"></canvas>
   
    <nav>
        <label> 
            Size:
            <input type="range" bind:value={size} />
        </label>

        <label> 
            Color:
            <input type="color" bind:value={color} />
        </label>
    </nav>
</article>



<style>

    article {
        display: flex;
        gap: 1em;
        align-items: end;
    }
    canvas {
    border: 1px solid rgb(255, 255, 255);
  }   

  nav {
    display: flex;
     gap: 1 em;
    flex-direction: column;
  }
  </style>