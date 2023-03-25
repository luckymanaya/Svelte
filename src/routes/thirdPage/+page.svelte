<!--Flexbox for Picture 6 & 7-->
<section class="flex-container">
  <section class="picture6" />
  <section class="picture7" />
  <section class="picture8" />
</section>

<section class="picture9">
  <img src="images/red.jpg" />
</section>

<section class="flex-container">
  <a href="/secondPage">
    <button>Go Back</button>
  </a>
  <a href="/">
    <button style="margin-left: 140vh">Go Back to 1</button>
  </a>
</section>

<p style="text-align: center; font-size: 2em">3</p>

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
  .picture9 {
    /*Background picture goes behind the image*/
    background-image: url("images/red.jpg");
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 1700px;
  }
  .picture9 img {
    /*Image goes on top of the background picture*/
    max-width: 45%;
    margin: 0 auto;
    padding: 30%;
    display: block;
    border-radius: 35%;
    transition: transform 0.5s; /* Animation */
  }
  .picture9 img:hover {
    transform: scale(1.15);
  }
</style>
