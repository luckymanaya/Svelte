<!-- JavaScript -->
<script>
  let isClicked = false;

  // A function that sets boolean to true when called
  const handleDropDown = () => {
    isClicked = !isClicked;
  };
</script>

<!-- HTML -->
<!--Navigation - List of options-->
<section class="nav-container">
  <nav>
    <ul>
      <a href="/">Home</a>
      <a href="/about">About</a>
      <section class="dropdown">
        <button on:click={handleDropDown} class="dropdownBtn"
          >Pages<small>&#9660</small>
          {#if isClicked}
            <section class="dropdown-content">
              <a href="/">Page 1</a>
              <a href="/secondPage">Page 2</a>
              <a href="/thirdPage">Page 3</a>
            </section>
          {/if}
        </button>
      </section>
      <a href="/contact">Contact Me</a>
    </ul>
  </nav>

  <section class="nav-transparency" />
</section>

<!-- CSS Styling -->
<style>
  /*Navigation Styling*/
  .nav-container {
    width: 100%;
    position: relative;
  }

  nav ul {
    padding: 0;
    margin: 0;
    display: flex;
    font-family: "Arial";
    font-size: 2.5em;
  }

  nav ul a {
    padding: 15px;
  }

  nav ul a:last-of-type {
    margin-left: auto;
  }

  .nav-transparency {
    /*to make header transparent*/
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgb(155, 152, 152);
    opacity: 0.4;
    z-index: -1;
  }

  /*Dropdown Styling*/
  .dropdownBtn {
    background-color: transparent;
    font-size: inherit;
    border: none;
    color: black;
    margin: 0;
    padding: 15px;
  }

  .dropdownBtn:hover {
    color: white;
  }

  .dropdownBtn .dropdown-content {
    display: none;
    z-index: 1;
    position: absolute;
  }

  .dropdown .dropdown-content {
    display: block;
    background-color: lightgray;
    border-radius: 10px;
  }

  .dropdown-content a {
    color: black;
    display: block;
    font-size: 0.95em;
  }

  .dropdown-content a:hover {
    background-color: gray;
    border-radius: inherit;
  }
</style>
