<script>
  import { page } from "$app/stores";
</script>

<footer>
  {#if $page.url.pathname === "/contact"}
    Images:
    <a href="https://unsplash.com/">Unsplash Website</a> | Privacy Policy Link:
    <a href="#0">Privacy Policy</a>
    <br />
    &copy; 2023, Lucky Manaya
  {:else}
    Images:
    <a href="https://unsplash.com/">Unsplash Website</a> | Contact Link:
    <a href="/contact">Contact Me</a> | Privacy Policy Link:
    <a href="#0">Privacy Policy</a>
    <br />
    &copy; 2023, Lucky Manaya
  {/if}
</footer>

<style>
  footer {
    background: rgb(155, 152, 152);
    font-family: "Arial";
    font-size: 1em;
    margin-top: auto;
    padding: 50px;
    color: black;
  }
  footer a {
    color: black;
    text-decoration: underline;
  }
  footer a:hover {
    color: white;
  }
  @media screen and (max-width: 375px) {
    footer {
      font-size: 9vw;
      width: 144vw;
    }
  }
</style>
