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
    <h1>1</h1>
  </section>
{:else if $page.url.pathname === "/secondPage"}
  <section class="button-container">
    <a href="/">
      <button>Go Back</button>
    </a>
    <a href="/thirdPage">
      <button>Next</button>
    </a>
  </section>

  <section class="pageNum">
    <h1>2</h1>
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
    <h1>3</h1>
  </section>
{/if}

<style>
  .BackToTop {
    display: flex;
    justify-content: right;
  }
  @media screen and (max-width: 375px) {
    .pageNum h1 {
      font-size: 3rem;
    }
  }
</style>
