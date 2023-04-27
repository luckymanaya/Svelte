<!-- JavaScript -->
<script>
  import { page } from "$app/stores";
</script>

<!-- HTML -->
<!--Footer Details-->
<footer>
  {#if $page.url.pathname === "/contact"}
    &copy; Images:
    <a href="https://unsplash.com/">Unsplash Website</a> | Privacy Policy Link:
    <a href="#">Privacy Policy</a>
  {:else}
    &copy; Images:
    <a href="https://unsplash.com/">Unsplash Website</a>
    Contact Link:
    <a href="/contact">Contact Me:</a> | Privacy Policy Link:
    <a href="#">Privacy Policy</a>
  {/if}
</footer>

<!--CSS Styling-->
<style>
  footer {
    font-family: "Arial";
    font-size: 1em;
    margin-top: auto;
    padding: 15px;
    color: white;
  }
  footer a {
    color: gray;
    text-decoration: underline;
  }
  footer a:hover {
    color: white;
  }
</style>
