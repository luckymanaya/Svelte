<script>
  import { fly } from "svelte/transition";
  import Slideshow from "$lib/Slideshow.svelte";
  import { slideImages } from "$lib/stores";

  let fontSize = 30;
  let displayText = false;

  const animateText = () => {
    displayText = !displayText;
  };

  let subsetSlides = [...slideImages];
  subsetSlides = subsetSlides.splice(3);
</script>

<section class="backgroundPic voguePic">
  <button on:click={animateText}>Click Me!</button>

  {#if displayText}
    <p>
      Increase Font Size: <input
        type="range"
        bind:value={fontSize}
        min="20"
        max="100"
      />
    </p>
    <p style="font-size: {fontSize}px" transition:fly={{ y: 200 }}>
      <mark
        >Vogue is one of the most popular fashion magazine since 1892 and has
        played a major role in influencing fashion industries and still even
        today! Known for its <i>high quality</i> and
        <i>sophistication</i>
        as well as its runway shows.</mark
      > <br /><br />
      <center
        ><mark
          >Vogue has been a source of fashion inspiration for many fashion
          lovers around the world <i class="fa-regular fa-heart fa-sm" /></mark
        ></center
      >
    </p>
  {/if}
</section>

<Slideshow slideImages={subsetSlides} />

<style>
  .voguePic {
    background-image: url("images/vogue.jpg");
    padding: 3rem;
  }
  mark {
    background-color: var(--otherColor);
    color: var(--textColor);
  }
</style>
