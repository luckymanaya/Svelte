<script>
  export let pic;
</script>

<div class="item">
  <div class="backgroundPic picture" style="background-image:url({pic.image})">
    <h1 class="text">{pic.text}</h1>
  </div>
</div>

<style>
  .picture {
    width: 25vw;
    height: 100vh;
    padding: 3rem;
    border-radius: 1rem;
    margin-inline: auto;
    margin-top: 2rem;
    transition: transform 0.5s;
  }
  .picture:hover {
    transform: scale(1.1);
  }
  .text {
    color: var(--textColor);
    -webkit-text-stroke-width: 0.12vw;
    -webkit-text-stroke-color: var(--otherColor);
    transition: transform 0.5s;
    word-wrap: break-word;
  }
  .text:hover {
    transform: scale(1.1);
  }
  @media screen and (max-width: 375px) {
    .picture {
      height: 30vh;
    }
    .text {
      font-size: 4vw;
    }
  }
</style>
