<script>
  import { fly } from "svelte/transition";

  let fontSize = 30;
  let displayText = false;

  const animateText = () => {
    displayText = !displayText;
  };
</script>

<section class="backgroundPic voguePic">
  <button on:click={animateText}>Click Me!</button>

  {#if displayText}
    <p>
      Increase Font Size: <input
        type="range"
        bind:value={fontSize}
        min="20"
        max="35"
      />
    </p>
    <p style="font-size: {fontSize}px" transition:fly={{ y: 200 }}>
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
