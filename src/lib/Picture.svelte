<script>
  export let pic;
</script>


  <div class="item">
    <div class="picture" style="background-image:url({pic.image})">
      <h1 class="text">{pic.text}</h1>
    </div>
  </div>

<style>
  .picture {
    background-size: cover;
    background-position: center;
    width: 20vw;
    height: 100vh;
    padding: 50px;
    border-radius: 25px;
    margin-inline: auto;
    margin-top: 15vh;
    transition: transform 0.5s;
  }
  .picture:hover {
    transform: scale(1.1);
  }
  .text {
    color: black;
    margin-top: -2vh;
    transition: transform 0.5s;
    word-wrap: break-word;

  }
  .text:hover {
    transform: scale(1.1);
  }
</style>
