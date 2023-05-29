<script>
  const slideImages = [
    "images/flower.jpg",
    "images/black hat.jpg",
    "images/vibes.jpg",
  ];

  let currentSlide = 0;

  //A function that displays next image
  const nextSlide = () => {
    currentSlide = (currentSlide + 1) % slideImages.length;
  };
  //A function that displays previous image
  const previousSlide = () => {
    currentSlide = (currentSlide - 1 + slideImages.length) % slideImages.length;
  };
</script>

<div class="button-container">
  <button on:click={previousSlide}>&#60</button>
  <button on:click={nextSlide}>&#62</button>
</div>

<section class="slideshow">
  {#if slideImages.length > 0}
    <img src={slideImages[currentSlide]} />
  {/if}
</section>

<style>
  .slideshow {
    align-self: center;
  }
  .slideshow img {
    width: 25vw;
    height: 80vh;
    border-radius: 1rem;
  }
  @media screen and (max-width: 375px) {
    .slideshow img {
      width: 75vw;
      height: 70vh;
    }
  }
</style>
