<!--JavaScript-->
<script>
  let slideImages = [
    "images/flower.jpg",
    "images/black hat.jpg",
    "images/vibes.jpg",
  ];
  let currentSlide = 0;

  //a function to go to next slide
  function nextSlide() {
    currentSlide = (currentSlide + 1) % slideImages.length;
  }

  //a function to go to previous slide
  function previousSlide() {
    currentSlide = (currentSlide - 1 + slideImages.length) % slideImages.length;
  }
</script>

<!--HTML-->
<body>
  <!--Flexbox for Picture 6 & 7-->
  <section class="flex-container">
    <section class="picture6">
      <h1 class="text">Expressive</h1>
    </section>
    <section class="picture7">
      <h1 class="text">Creative</h1>
    </section>
    <section class="picture8">
      <h1 class="text">Influential</h1>
    </section>
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
    <!--if length of images array is not 0, images will be displayed-->
    {#if slideImages.length > 0}
      <section class="flex-container">
        <!--Previous Button for Slideshow-->
        <button on:click={previousSlide}>&#60</button>
        <img src={slideImages[currentSlide]} />
        <!--Next Button for Slideshow-->
        <button on:click={nextSlide}>&#62</button>
      </section>
    {/if}
  </section>

  <!--Buttons-->
  <section class="button-container">
    <a href="/secondPage">
      <button>Go Back</button>
    </a>
    <a href="/">
      <button>Go Back to 1</button>
    </a>
  </section>

  <p style="text-align: center; font-size: 2em">3</p>
</body>

<!--CSS Styling-->
<style>
  /*Pictures*/
  .picture6 {
    background-image: url("images/earring.jpg");
    background-size: cover;
    background-position: center;
    width: 55%;
    height: 990px;
    padding: 50px;
    border-radius: 25px;
    margin: 30px;
    margin-top: 6%;
  }
  .picture7 {
    background-image: url("images/accessories.jpg");
    background-size: cover;
    background-position: center;
    width: 55%;
    height: 990px;
    padding: 50px;
    border-radius: 25px;
    margin: 30px;
    margin-top: 6%;
  }
  .picture8 {
    background-image: url("images/hair.jpg");
    background-size: cover;
    background-position: center;
    width: 55%;
    height: 990px;
    padding: 50px;
    border-radius: 25px;
    margin: 30px;
    margin-top: 6%;
  }
  .text {
    color: black;
    margin-top: 0;
  }
  /*Background picture goes behind the image*/
  .picture9 {
    background-image: url("images/red.jpg");
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 1700px;
  }

  /*Image goes on top of the background picture*/
  .picture9 img {
    max-width: 45%;
    margin: 0 auto;
    padding: 15%;
    display: block;
    transition: transform 0.5s; /* Animation */
  }
  .picture9 img:hover {
    transform: scale(1.15);
  }
  /*Slideshow Styling*/
  .slideshow img {
    width: 30%;
    height: auto;
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 5%;
    border-radius: 25px;
  }
  .flex-container button {
    width: 5%;
    height: 10%;
    margin: auto;
  }
</style>
