<!-- JavaScript -->
<script>
  import SocialIcons from "@rodneylab/svelte-social-icons";
  let isClicked1 = false;
  let isClicked2 = false;

  const handlePageDropDown = () => {
    isClicked1 = !isClicked1;
  };

  const handleSocialsDropDown = () => {
    isClicked2 = !isClicked2;
  };
</script>

<!-- HTML -->
<section class="nav-container">
  <nav>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/about">About</a></li>
      <section class="dropdown">
        <button on:click={handlePageDropDown} class="dropdownBtn"
          >Pages&#9660
          {#if isClicked1}
            <section class="dropdown-content">
              <a href="/">Page 1</a>
              <a href="/secondPage">Page 2</a>
              <a href="/thirdPage">Page 3</a>
            </section>
          {/if}
        </button>
      </section>
      <section class="dropdown">
        <button on:click={handleSocialsDropDown} class="dropdownBtn"
          >Socials&#9660
          {#if isClicked2}
            <section class="dropdown-content">
              <a href="#0">
                <SocialIcons network="instagram" />
              </a>
              <a href="#0">
                <SocialIcons network="facebook" />
              </a>
              <a href="#0">
                <SocialIcons network="youtube" />
              </a>
              <a href="https://github.com/luckymanaya">
                <SocialIcons network="github" />
              </a>
            </section>
          {/if}
        </button>
      </section>
      <li><a href="/contact">Contact Me</a></li>
    </ul>
  </nav>
</section>

<!-- CSS Styling -->
<style>
  .nav-container {
    width: 100%;
    background: gray;
  }
  nav ul {
    padding: 5px;
    margin: 0;
    display: flex;
    font-family: "Arial";
    font-size: 2.3vw;
    list-style: none;
    justify-content: space-evenly;
  }
  /*Dropdown Styling*/
  .dropdownBtn {
    background-color: transparent;
    font-size: 2.3vw;
    border: none;
    color: black;
    margin: 0;
    padding: 0;
  }
  .dropdownBtn:hover {
    color: white;
  }
  .dropdown-content {
    position: absolute;
    background-color: lightgray;
    border-radius: 1rem;
  }
  .dropdown-content a {
    color: black;
    display: block;
    padding: 1rem;
  }
  .dropdown-content a:hover {
    background-color: black;
    border-radius: inherit;
    color: white;
  }

  @media screen and (max-width: 375px){
    .nav-container {
    width: 170vw;
  }
  nav ul {
    padding: 40px;
    font-size: 5vw;
  }
  .dropdownBtn{
    font-size: 5vw;
  }
  .dropdown-content a {
    font-size: 10vw;
    width: 60vw;

  }
}
</style>
