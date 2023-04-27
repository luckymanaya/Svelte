<!-- JavaScript -->
<script>
  import { page } from "$app/stores";
</script>

<!-- HTML -->
<!--Footer Details-->
<footer>
  {#if $page.url.pathname === "/contact"}
    Images:
    <a href="https://unsplash.com/">Unsplash Website</a> | Privacy Policy Link:
    <!-- Link goes nowhere -->
    <a href="#0">Privacy Policy</a>
    <br />
    &copy; 2023, Lucky Manaya
  {:else}
    Images:
    <a href="https://unsplash.com/">Unsplash Website</a> | Contact Link:
    <a href="/contact">Contact Me:</a> | Privacy Policy Link:
    <!-- Link goes nowhere -->
    <a href="#0">Privacy Policy</a>
    <br />
    &copy; 2023, Lucky Manaya
  {/if}
</footer>

<!--CSS Styling-->
<style>
  footer {
    background-color: gray;
    font-family: "Arial";
    font-size: 1em;
    margin-top: auto;
    padding: 30px;
    color: black;
  }
  footer a {
    color: black;
    text-decoration: underline;
  }
  footer a:hover {
    color: white;
  }
</style>
