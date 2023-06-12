<script>
  import { page } from "$app/stores";
</script>

{#if $page.url.pathname === "/"}
  <section class="BackToTop">
    <a href="#">
      <button><i class="fa-solid fa-arrow-up fa-xs" /></button>
    </a>
  </section>

  <section class="row-container">
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
      <button><i class="fa-solid fa-arrow-up fa-xs" /></button>
    </a>
  </section>
  <section class="row-container">
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
      <button><i class="fa-solid fa-arrow-up fa-xs" /></button>
    </a>
  </section>
  <section class="row-container">
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
  .BackToTop button {
    border-radius: 4rem;
    width: 4vw;
    font-size: var(--h2Size);
  }
  @media screen and (max-width: 728px) {
    .pageNum h2 {
      font-size: 8vw;
    }
    .BackToTop button {
      width: 12vw;
      font-size: 7vw;
    }
  }
</style>
