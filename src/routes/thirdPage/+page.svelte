<script>
  import { pictureDetails } from "$lib/stores.js";
  import PictureList from "$lib/PictureList.svelte";

  const slideImages = [
    "images/flower.jpg",
    "images/black hat.jpg",
    "images/vibes.jpg",
  ];

  let currentSlide = 0;

  const nextSlide = () => {
    currentSlide = (currentSlide + 1) % slideImages.length;
  };

  const previousSlide = () => {
    currentSlide = (currentSlide - 1 + slideImages.length) % slideImages.length;
  };

  let subset = [...pictureDetails];
  subset = subset.splice(0, 3);
</script>

<PictureList pictureDetails={subset} />

<section class="bgPic">
  <h2>A new <big>DO</big>, for a new <big>YOU</big>!</h2>
  <img src="images/red.jpg" />
</section>

<h2>
  Showcase your creativity through clothing choices... and have fun with it!
</h2>

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
  .bgPic {
    background-image: url("images/red.jpg");
    background-size: cover;
    background-position: center;
    width: auto;
    height: 130vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-top: 2rem;
  }
  .bgPic h2 {
    text-shadow: 2px 5px 4px black;
  }
  /*Image goes on top of the background picture*/
  .bgPic img {
    width: 35vw;
    align-self: center;
    transition: transform 0.5s;
  }
  .bgPic img:hover {
    transform: scale(1.1);
  }
  /*Slideshow Styling*/
  .slideshow {
    align-self: center;
  }
  .slideshow img {
    width: 25vw;
    border-radius: 1rem;
  }
  .button-container button {
    font-size: 2vw;
    margin: 1rem;
  }
  @media screen and (max-width: 375px) {
    h2 {
      font-size: 8vw;
    }
    .bgPic {
      width: 170vw;
    }
    .slideshow img {
      width: 100vw;
    }
    .button-container button {
      font-size: 10vw;
    }
  }
</style>
