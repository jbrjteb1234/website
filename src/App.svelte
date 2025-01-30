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

<div class="scroll-container">
  <div class="section">
    <div class="border"></div>
    <div class="header-container">
      <h1 class="header-title">
        JAMES BRIGHT
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

    <div class="center-container">
    </div>

    <div class="link-bar">

    </div>
  </div>

  <div class="section">
    <div class="border"></div>
  </div>
</div>
