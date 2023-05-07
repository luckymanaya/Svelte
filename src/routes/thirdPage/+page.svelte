<!--JavaScript-->
<script>
  const slideImages = [
    "images/flower.jpg",
    "images/black hat.jpg",
    "images/vibes.jpg",
  ];

  const pictureDetails = [
    {
      image: "images/earring.jpg",
      text: "Expressive",
    },
    {
      image: "images/accessories.jpg",
      text: "Creative",
    },
    {
      image: "images/hair.jpg",
      text: "Influential",
    },
  ];

  let currentSlide = 0;

  //A function to go to next slide
  const nextSlide = () => {
    currentSlide = (currentSlide + 1) % slideImages.length;
  };

  //A function to go to previous slide
  const previousSlide = () => {
    currentSlide = (currentSlide - 1 + slideImages.length) % slideImages.length;
  };
</script>

<!--HTML-->
<body>
  <section class="flex-container">
    {#each pictureDetails as pic}
      <div class="item">
        <div class="picture" style="background-image:url({pic.image})">
          <h2 class="text">{pic.text}</h2>
        </div>
      </div>
    {/each}
  </section>

  <section class="picture9">
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
</body>

<!--CSS Styling-->
<style>
  /*Pictures*/
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
    opacity: 0.5;
    transition: transform 0.5s;
  }
  .text:hover {
    opacity: 1;
    transform: scale(1.1);
  }
  .picture9 {
    background-image: url("images/red.jpg");
    background-size: cover;
    background-position: center;
    width: auto;
    height: 130vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .picture9 h1 {
    font-size: 3em;
    text-shadow: 2px 5px 4px black;
  }
  /*Image goes on top of the background picture*/
  .picture9 img {
    max-width: 30vw;
    margin: 0 auto;
    transition: transform 0.5s;
  }
  .picture9 img:hover {
    transform: scale(1.1);
  }
  /*Slideshow Styling*/
  .slideshow {
    display: flex;
  }
  .slideshow img {
    width: 25%;
    margin-bottom: 5%;
    border-radius: 25px;
  }
  .flex-container button {
    width: 5vw;
    height: 8vh;
    margin: auto;
    font-size: 2.5em;
  }
</style>
