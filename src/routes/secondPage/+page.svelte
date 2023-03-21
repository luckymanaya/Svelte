<!--Javascript Coding-->
<script>
  let words = ['"Amazing"', '"Beautiful"', '"Stunning!"', '"Gorgeous"'];
</script>

<!--HTML coding-->
<body>
  <section class="picture4" />

  <section class="picture5">
    {#each words as w}
      <p><br /><br />{w}<br /><br /></p>
    {/each}
  </section>

  <br />

  <!--Flexbox for the Bottom Details-->
  <section class="flex-container">
    <a href="/">
      <button>Go Back</button>
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
    width: 50%;
    height: 990px;
    border-radius: 50%;
    margin: 40px;
  }
  .picture5 p {
    margin-left: 140%;
    font-size: 2.5em;
  }
</style>
