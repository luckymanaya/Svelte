<!--JavaScript-->
<script>
  const slideImages = [
    "images/flower.jpg",
    "images/black hat.jpg",
    "images/vibes.jpg",
  ];

  let currentSlide = 0;
  const pageNum = 3;

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
  <!--Flexbox for Picture 6 & 7-->
  <section class="flex-container">
    {#each Array(3) as _, index (index)}
      <section class="item">
        <section id="picture{index + 6}" class="picture" />
      </section>
    {/each}
  </section>

  <h1 style="margin-top: 5%">A new <big>DO</big>, for a new <big>YOU</big>!</h1>

  <section class="picture9">
    <img src="images/red.jpg" />
  </section>

  <h2 style="margin-top: 5%">
    Showcase your creativity through clothing choices<br />...and have fun with
    it!
  </h2>

  <!--Slideshow Images-->
  <section class="slideshow">
    {#if slideImages.length > 0}
      <section class="flex-container">
        <button on:click={previousSlide}>&#60</button>
        <img src={slideImages[currentSlide]} />
        <button on:click={nextSlide}>&#62</button>
      </section>
    {/if}
  </section>
</body>

<!--Buttons-->
<section class="BackToTop">
  <a href="#">
    <button>Back to top &uarr;</button>
  </a>
</section>

<section class="button-container">
  <a href="/">
    <button>Go Back to 1</button>
  </a>

  <a href="/secondPage">
    <button>Go Back</button>
  </a>
</section>

<!--Page Number Text-->
<section class="pageNumber">
  <p>{pageNum}</p>
</section>

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

  #picture6 {
    background-image: url("images/earring.jpg");
  }
  #picture6:hover {
    transform: scale(1.1);
  }
  #picture7 {
    background-image: url("images/accessories.jpg");
  }
  #picture7:hover {
    transform: scale(1.1);
  }
  #picture8 {
    background-image: url("images/hair.jpg");
  }
  #picture8:hover {
    transform: scale(1.1);
  }
  /*Background picture goes behind the image*/
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

  /*Image goes on top of the background picture*/

  .picture9 img {
    max-width: 30vw;
    margin: 0 auto;
    transition: transform 0.5s;
  }
  .picture9 img:hover {
    transform: scale(1.2);
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
