<!--Javascript-->
<script>
  import { fly } from "svelte/transition";
  let displayText = false;

  //if called, displayText becomes true
  function animateText() {
    displayText = !displayText;
  }
  //array of words
  let words = ['"Amazing"', '"Beautiful"', '"Stunning!"', '"Gorgeous"'];
</script>

<!--HTML-->
<body>
  <section class="picture4">
    <button on:click={animateText}>Click Me!</button>

    <!--if true, animated text is displayed-->
    {#if displayText}
      <p transition:fly={{ y: 200 }}>
        Vogue is one of the most popular fashion magazine since 1892 and has
        played a major role in influencing fashion industries even today! Known
        for its <big><q><i>high quality</i></q></big> and
        <big><q><i>sophistication</i></q></big>
        as well as its runway shows. <br><br>
        <center>Vogue has been a source of fashion inspiration for many fashion lovers
        around the world &#x2661</center>
      </p>
    {/if}
  </section>

  <section class="picture5">
    <!--displays each word from variable 'words'-->
    {#each words as w}
      <p><br /><br />{w}<br /><br /></p>
    {/each}
  </section>

  <!--Buttons-->
  <section class="button-container">
    <a href="/">
      <button>Go Back</button>
    </a>
    <a href="/thirdPage">
      <button>Next</button>
    </a>
  </section>

  <p style="text-align: center; font-size: 2em">2</p>
</body>

<!--CSS Styling-->
<style>
  /*Pictures*/
  .picture4 {
    background-image: url("images/vogue.jpg");
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 990px;
    padding: 50px;
  }
  .picture4 button {
    margin-top: 15%;
  }
  .picture4 p {
    margin-left: 15%;
    margin-right: 15%;
    font-size: 2em;
  }
  .picture5 {
    background-image: url("images/runway.jpg");
    background-size: cover;
    background-position: center;
    width: 45%;
    height: 800px;
    border-radius: 50%;
    margin: 90px;
    transition: transform 0.5s; /* Animation */
  }
  .picture5:hover {
    transform: scale(1.1);
  }
  .picture5 p {
    margin-left: 140%;
    font-size: 2.5em;
  }
</style>
