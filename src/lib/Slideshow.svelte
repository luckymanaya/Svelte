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

<div class="button-container">
  <button on:click={previousSlide}>&#60</button>
  <button on:click={nextSlide}>&#62</button>
</div>

<section class="slideshow">
  <!-- {#if slideImages.length > 0}
    <img src={slideImages[currentSlide]} />
  {/if} -->
  {#each [slideImages[currentSlide]] as src (currentSlide)}
	<img in:fade={{ delay: 200 }} {src}/>	
{/each}
</section>

<style>
  .slideshow {
    align-self: center;
  }
  .slideshow img {
    width: 25vw;
    height: 75vh;
    border-radius: 1rem;
  }
  @media screen and (max-width: 375px) {
    .slideshow img {
      width: 75vw;
      height: 70vh;
    }
  }
</style>
