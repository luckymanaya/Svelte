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
    padding: 3rem;
    border-radius: var(--border-radius);
    margin-inline: auto;
    margin-top: 2rem;
    transition: transform 0.5s;
  }
  .picture:hover {
    transform: scale(1.1);
  }
  .text {
    color: var(--textColor);
    text-shadow: 1px 1px 3px black;
  }
  @media screen and (max-width: 375px) {
    .picture {
      height: 30vh;
      width: 50vw;
    }
    .text {
      font-size: 6vw;
    }
  }
</style>
