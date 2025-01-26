<script>

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
    background-color: var(--color-white)
  }

  .header-container{
    display: flex;
    width: 420px;
    margin-left: 10%;
    margin-top: 5%;
    flex-direction: column;
    align-items: center;
    background-color: var(--color-black);
    box-shadow: 25px 25px 12px 0px rgba(0,0,0,0.75);
  }

  .header-title {
    font-size: var(--font-size-large);
    font-family: var(--font-family);
    color: var(--color-white);
    letter-spacing: 1.8px;
    text-align: left;
    margin-top: 5%;
    padding-left: 5%;
    width: 100%;
    flex: 1;
  }

  .header-subtitle{
    font-size: var(--font-size-text);
    font-family: var(--font-family2);
    color: var(--color-white);
    font-weight: normal;
    text-align: left;
    margin-top: 5%;
    padding-left: 5%;
    width: 100%;
    flex: 1;
  }

  .description{
    font-size: var(--font-size-small);
    font-family: var(--font-family);
    color: var(--color-white);
  }

</style>

<div class="header-container">
  <h1 class="header-title">
    JAMES<br>BRIGHT
  </h1>

  <h2 class="header-subtitle">
    <span style="color: var(--font-color-blue)"> &gt </span>
    Aspiring Software Engineer<br>
    <span style="color: var(--font-color-blue)"> &gt </span>
    Automotive Enthusiast<br>
    <span style="color: var(--font-color-blue)"> &gt </span> 
    Computer Science Student
  </h2>
</div>