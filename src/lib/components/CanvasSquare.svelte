<script>
    let Size = $state(50);
    let Color = $state('#ff3e00');
    let canvas = document.querySelector('canvas');

    const context = canvas.getContext('2d');
    context?.clearRect(0, 0, canvas.width, canvas.height);

    context.fillStyle = Color;
</script>

<h3>Canvas Square</h3>


<article>
    <canvas width="100" height="100"></canvas>
   
    <nav>
        <label> 
            Size:
            <input type="range" />
        </label>

        <label> 
            Size:
            <input type="color" />
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