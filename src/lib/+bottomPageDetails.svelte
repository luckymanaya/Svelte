<!-- JavaScript -->
<script>
  import { page } from "$app/stores";
</script>

<!-- HTML -->
{#if $page.url.pathname === "/"}
  <section class="BackToTop">
    <a href="#">
      <button>Back to top &uarr;</button>
    </a>
  </section>

  <section class="button-container">
    <a href="/secondPage">
      <button>Next</button>
    </a>
  </section>

  <section class="pageNumber">
    <p>1</p>
  </section>
{:else if $page.url.pathname === "/secondPage"}
  <section class="BackToTop">
    <a href="#">
      <button>Back to top &uarr;</button>
    </a>
  </section>

  <section class="button-container">
    <a href="/">
      <button>Go Back</button>
    </a>

    <a href="/thirdPage">
      <button>Next</button>
    </a>
  </section>

  <section class="pageNumber">
    <p>2</p>
  </section>
{:else if $page.url.pathname === "/thirdPage"}
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

  <section class="pageNumber">
    <p>3</p>
  </section>
{/if}

<!-- CSS Styling -->
<style>
  .pageNumber p {
    text-align: center;
    font-size: 2em;
  }
</style>
