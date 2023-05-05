<!--Javascript-->
<script>
  import { fly } from "svelte/transition";

  let fontSize = 30;
  let displayText = false;
  const pageNum = 2;

  //array of words
  let words = ['"Amazing"', '"Beautiful"', '"Stunning!"', '"Gorgeous"'];

  //if called, displayText becomes true
  const animateText = () => {
    displayText = !displayText;
  };
</script>

<!--HTML-->
<body>
  <section class="picture4">
    <button on:click={animateText}>Click Me!</button>

    <!--if true, animated text is displayed-->
    {#if displayText}
      <p>
        Increase Font Size: <input
          type="range"
          bind:value={fontSize}
          min="20"
          max="45"
        />
      </p>
      <p
        style="margin-top: 5%; font-size: {fontSize}px"
        transition:fly={{ y: 200 }}
      >
        <mark
          >Vogue is one of the most popular fashion magazine since 1892 and has
          played a major role in influencing fashion industries and still even
          today! Known for its <big><q><i>high quality</i></q></big> and
          <big><q><i>sophistication</i></q></big>
          as well as its runway shows.</mark
        > <br /><br />
        <center
          ><mark
            >Vogue has been a source of fashion inspiration for many fashion
            lovers around the world &#x2661</mark
          ></center
        >
      </p>
    {/if}
  </section>

  <section class="picture5">
    {#each words as w}
      <p>{w}</p>
    {/each}
  </section>
</body>

<!--Buttons-->
<section class="BackToTop">
  <a href="#">
    <button>Back to top &uarr;</button>
  </a>
</section>

<section class="button-container">
  <a href="/">
    <button>Go Back</button>
  </a>

  <a href="/thirdPage">
    <button>Next</button>
  </a>
</section>

<section class="pageNumber">
  <p>{pageNum}</p>
</section>

<!--CSS Styling-->
<style>
  /*Pictures*/
  .picture4 {
    background-image: url("images/vogue.jpg");
    background-size: cover;
    background-position: center;
    width: auto;
    height: 120vh;
    padding: 5%;
  }
  .picture4 button {
    margin-top: 15%;
  }
  .picture4 p {
    margin-inline: 5%;
  }
  mark {
    background-color: black;
    color: white;
  }
  .picture5 {
    background-image: url("images/runway.jpg");
    background-size: cover;
    background-position: center;
    width: 45%;
    height: 100vh;
    border-radius: 50%;
    margin: 8%;
    transition: transform 0.5s; /* Animation */
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .picture5:hover {
    transform: scale(1.1); /*Zooms in*/
  }
  .picture5 p {
    font-size: 2.5em;
    margin-left: 140%;
  }
</style>
