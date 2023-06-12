<script>
  import { fade } from "svelte/transition";
  export let slideImages;

  let currentSlide = 0;

  //These functions displays the next and previous images
  const nextSlide = () => {
    currentSlide = (currentSlide + 1) % slideImages.length;
  };
  const previousSlide = () => {
    currentSlide = (currentSlide - 1 + slideImages.length) % slideImages.length;
  };
</script>

<div class="row-container">
  <button on:click={previousSlide}>&#60</button>
  <button on:click={nextSlide}>&#62</button>
</div>

<section class="slideshow">
  {#each [slideImages[currentSlide]] as src (currentSlide)}
    <img in:fade={{ delay: 200 }} {src} />
  {/each}
</section>

<style>
  .slideshow {
    align-self: center;
  }
  .slideshow img {
    width: 100%;
    height: 75vh;
    border-radius: 1rem;
  }
  .row-container button {
    width: 5vw;
    font-size: var(--h2Size);
    margin: 5rem 5rem 2rem;
  }
  @media screen and (max-width: 728px) {
    .slideshow img {
      height: 50vh;
    }
    .row-container button {
      width: 15vw;
      font-size: 5vw;
    }
  }
</style>
