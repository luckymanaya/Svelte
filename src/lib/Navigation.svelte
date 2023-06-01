<script>
  let isClicked = false;
  const handlePageDropDown = () => {
    isClicked = !isClicked;
  };
</script>

<section class="nav-container">
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li>
        <section class="dropdown">
          <button on:click={handlePageDropDown} class="dropdownBtn"
            >Pages <i class="fa-solid fa-chevron-down fa-xs" />
            {#if isClicked}
              <section class="dropdown-content">
                <a href="/">Page 1</a>
                <a href="/secondPage">Page 2</a>
                <a href="/thirdPage">Page 3</a>
              </section>
            {/if}
          </button>
        </section>
      </li>
      <li><a href="/about">About</a></li>
    </ul>
  </nav>
</section>

<style>
  .nav-container {
    position: fixed;
    width: 100vw;
  }
  nav ul {
    padding: 1rem;
    margin: 0;
    font-size: 2.3vw;
    list-style: none;
    display: flex;
    justify-content: space-evenly;
  }
  nav ul li a{
    color: var(--textColor)
  }
  /*Dropdown Styling*/
  .dropdownBtn {
    background-color: transparent;
    font-size: 2.3vw;
    border: none;
    color: var(--textColor);
    margin: 0;
    padding: 0;
    width: auto;
  }
  .dropdownBtn:hover {
    color: var(--textColor);
  }
  .dropdown-content {
    position: absolute;
    background-color: var(--bgColor);
  }
  .dropdown-content a {
    color: var(--otherColor);
    display: block;
    padding: 1rem;
  }
  .dropdown-content a:hover {
    background-color: var(--otherColor);
    color: var(--textColor);
  }
  .dropdown-content,
  .dropdown-content a:hover {
    border-radius: var(--border-radius);
  }
  @media screen and (max-width: 375px) {
    nav ul,
    .dropdownBtn,
    .dropdown-content a {
      font-size: 4vw;
    }
  }
</style>
