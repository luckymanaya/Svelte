<!--Javascript-->
<script>
  let words = ['"Amazing"', '"Beautiful"', '"Stunning!"', '"Gorgeous"'];
</script>

<!--HTML-->
<body>
  <section class="picture4" />

  <section class="picture5">
    {#each words as w}
      <p><br /><br />{w}<br /><br /></p>
    {/each}
  </section>

  <br />

  <!--Buttons-->
  <section class="button-container">
    <a href="/">
      <button>Go Back</button>
    </a>
    <a href="/thirdPage">
      <button>Next</button>
    </a>
  </section>

  <p style="text-align: center; font-size: 2em">2</p>
</body>

<!--CSS Styling-->
<style>
  /*Pictures*/
  .picture4 {
    background-image: url("images/vogue.jpg");
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 990px;
    padding: 50px;
  }
  .picture5 {
    background-image: url("images/runway.jpg");
    background-size: cover;
    background-position: center;
    width: 45%;
    height: 800px;
    border-radius: 50%;
    margin: 90px;
    transition: transform 0.5s; /* Animation */
  }
  .picture5:hover {
    transform: scale(1.1);
  }
  .picture5 p {
    margin-left: 140%;
    font-size: 2.5em;
  }
</style>
