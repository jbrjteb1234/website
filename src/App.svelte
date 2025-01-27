<script>
  import { onMount } from 'svelte';
  let headerContainer;

  onMount(() => {

      function handleMouseMove(event){
        const mouseX = event.clientX;
        const mouseY = event.clientY;

        const position = headerContainer.getBoundingClientRect();
        const containerX = position.left + position.width/2;

        if(headerContainer){
          const differenceX = (mouseX - containerX)/25;

          const newX = Math.max(-50, Math.min(50, differenceX)); 
          
          headerContainer.style.transform = `translate(${newX}px, ${0}px)`;
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
    --header-box-height: 380px;
  }

  :global(body) {
    background-color: var(--color-white);
    margin: 0;
    padding: 0;
  }

  .scroll-container {
    height: 100vh;
    overflow-y: scroll; 
    scroll-snap-type: y mandatory; 
  }

  .section {
    height: 100vh;
    width: 100%;
    overflow: hidden;
    scroll-snap-align: start;
  }

  .section:nth-child(1){
    display: flex;
    align-items: center; 
    height: 100vh;
    width: 100%;
    background-color: aliceblue;
    justify-content: space-between;
  }

  .section:nth-child(2){
    background-color: aquamarine;
  }

  .header-top-container{
    margin-left: 10%;
    height: var(--header-box-height);
    background-color: var(--color-grey); 
    align-items: center;
    justify-content: center;
    display: flex;
    flex: 0 0 420px;
    z-index: 5;
  }

  .header-container{
    display: flex;
    width: 110%;
    height: 110%;
    flex-direction: column;
    align-items: center;
    background-color: var(--color-black);
    clip-path: polygon(0 10%, 100% 0%, 100% 90%, 0% 100%);
  }


  .header-title {
    font-size: var(--font-size-large);
    font-family: var(--font-family);
    color: var(--color-white);
    letter-spacing: 1.8px;
    text-align: left;
    margin-left: 10%;
    width: 100%;
    height: 35%;
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

  .center-container{
    flex: 1;
    width: 100%;
  }

  .blue-line{
    width: 100%;
    background-color: var(--color-blue);
    transform: translate(0, calc(var(--header-box-height)/2 - 0.05 * var(--header-box-height) - 5px));
    height: 2px;
    z-index: 2;
  }

  .description{
    font-size: var(--font-size-small);
    font-family: var(--font-family);
    color: var(--color-white);
  }

</style>

<div class="scroll-container">
  <div class="section">
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

    <div class="center-container">
      <div class="blue-line">
      </div>  
    </div>

    <div class="link-bar">

    </div>
  </div>

  <div class="section">

  </div>
</div>