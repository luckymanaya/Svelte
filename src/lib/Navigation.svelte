<script>
  let isClicked = false;
  const handlePageDropDown = () => {
    isClicked = !isClicked;
  };
</script>

<section class="nav-container">
  <div class="veil">
  </div>
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li>
        <div class="dropdown">
          <button on:click={handlePageDropDown} class="dropdownBtn"
            >Pages <i class="fa-solid fa-chevron-down fa-xs" />
            {#if isClicked}
              <div class="dropdown-content">
                <a href="/">Page 1</a>
                <a href="/secondPage">Page 2</a>
                <a href="/thirdPage">Page 3</a>
              </div>
            {/if}
          </button>
        </div>
      </li>
      <li><a href="/about">About</a></li>
    </ul>
  </nav>
</section>

<style>
  .nav-container {
    position: relative;
    z-index:1000;
  }
  nav ul {
    padding: 1rem;
    margin: 0;
    font-size: 2.3vw;
    list-style: none;
    display: flex;
    justify-content: space-evenly;
  }
  nav ul li a {
    color:var(--bgColor);
  }
  nav ul li a:hover {
    color: var(--textColor);
  }
  .veil{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: var(--otherColor);
    opacity: 0.4;
    z-index: -1;
  }
  /*Dropdown Styling*/
  .dropdownBtn {
    background-color: transparent;
    font-size: 2.3vw;
    border: none;
    color: var(--bgColor);
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
