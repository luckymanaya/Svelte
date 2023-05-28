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
    background: var(--bgColor);
    font-size: 1.3vw;
    margin-top: auto;
    padding: 3rem;
  }
  footer a {
    text-decoration: underline;
  }
  footer a:hover {
    color: var(--textColor);
  }
  @media screen and (max-width: 375px) {
    footer {
      font-size: 5vw;
    }
  }
</style>
