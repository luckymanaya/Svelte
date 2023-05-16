<!--JavaScript-->
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

<!--HTML-->
<PictureList pictureDetails={subset} />

<section class="bgPic">
  <h1>A new <big>DO</big>, for a new <big>YOU</big>!</h1>
  <img src="images/red.jpg" />
</section>

<h2>
  Showcase your creativity through clothing choices<br />...and have fun with
  it!
</h2>

<section class="slideshow">
  {#if slideImages.length > 0}
    <div class="flex-container">
      <button on:click={previousSlide}>&#60</button>
      <img src={slideImages[currentSlide]} />
      <button on:click={nextSlide}>&#62</button>
    </div>
  {/if}
</section>

<!--CSS Styling-->
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
  }
  .bgPic h1 {
    font-size: 3em;
    text-shadow: 2px 5px 4px black;
  }
  /*Image goes on top of the background picture*/
  .bgPic img {
    max-width: 30vw;
    margin: 0 auto;
    transition: transform 0.5s;
  }
  .bgPic img:hover {
    transform: scale(1.1);
  }
  /*Slideshow Styling*/
  .slideshow {
    display: flex;
    flex-direction: column;
  }
  .slideshow img {
    width: 25vw;
    border-radius: 25px;
  }
  .flex-container button {
    font-size: 2.5em;
    width: 5vw;
    height: 7vh;
    margin: auto;
  }
</style>
