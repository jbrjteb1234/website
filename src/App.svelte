<script>
  import { onMount } from 'svelte';
  let headerContainer;

  onMount(() => {

      function handleMouseMove(event){
        const mouseX = event.clientX;
        const mouseY = event.clientY;

        const position = headerContainer.getBoundingClientRect();
        const containerX = position.left + position.width/2;
        const containerY = position.top + position.height/2;

        if(headerContainer){
          const differenceX = (mouseX - containerX)/50;
          const differenceY = (mouseY - containerY)/50;

          const newX = Math.max(-50, Math.min(50, differenceX)); 
          const newY = Math.max(-50, Math.min(50, differenceY));
          
          headerContainer.style.transform = `translate(${newX}px, ${newY}px)`;
        }

      }

      window.addEventListener('mousemove', handleMouseMove);

  });
    
</script>

<style>

  :root {
    --font-family: "Poppins", Sans-serif;
    --font-family2: 'Fira Code', monospace;
    --font-size-large: 5rem;
    --font-size-medium: 3rem;
    --font-size-small: 2rem;
    --font-size-text: 1.5rem;
    --font-size-sub-text: 1vw;
    --color-white: rgb(255,255,255);
    --color-blue: rgb(0, 200, 255);
    --color-orange: rgb(255, 170, 0);
    --color-black: rgb(0,0,0);
    --color-grey: rgb(60, 60, 60);
  }

  :global(body) {
    background-color: var(--color-white);
    min-height: 200vh;
  }

  .header-top-container{
    position: absolute; 
    top: 50%; 
    left: 10%; 
    transform: translate(0%, -50%); 
    width: 420px;
    height: 420px;
    background-color: var(--color-grey); 
  }

  .header-container{
    display: flex;
    width: 100%;
    height: 100%;
    flex-direction: column;
    align-items: center;
    background-color: var(--color-black);
  }


  .header-title {
    font-size: var(--font-size-large);
    font-family: var(--font-family);
    color: var(--color-white);
    letter-spacing: 1.8px;
    text-align: left;
    margin-left: 10%;
    width: 100%;
    flex: 1;
  }

  .header-subtitle{
    font-size: var(--font-size-text);
    font-family: var(--font-family2);
    color: var(--color-white);
    font-weight: normal;
    text-align: left;
    margin-left: 10%;
    width: 100%;
    flex: 1;
  }

  .description{
    font-size: var(--font-size-small);
    font-family: var(--font-family);
    color: var(--color-white);
  }

</style>

<div class="header-top-container">
  <div bind:this={headerContainer} class="header-container">
    <h1 class="header-title">
      JAMES<br>BRIGHT
    </h1>

    <h2 class="header-subtitle">
      <span style="color: var(--color-blue)"> &gt </span>
      Aspiring Software Engineer<br>
      <span style="color: var(--color-blue)"> &gt </span>
      Automotive Enthusiast<br>
      <span style="color: var(--color-blue)"> &gt </span> 
      Computer Science Student
    </h2>
  </div>
</div>