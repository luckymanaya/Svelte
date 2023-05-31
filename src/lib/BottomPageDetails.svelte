<script>
  import { page } from "$app/stores";
</script>

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

  <section class="pageNum">
    <h2>1</h2>
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

  <section class="pageNum">
    <h2>2</h2>
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

  <section class="pageNum">
    <h2>3</h2>
  </section>
{/if}

<style>
  .BackToTop {
    display: flex;
    justify-content: right;
  }
  @media screen and (max-width: 375px) {
    .pageNum h2 {
      font-size: 8vw;
    }
  }
</style>
