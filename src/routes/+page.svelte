<!--JavaScript-->
<script>
  let name = "";
  let title = "Lucky's Website";

  //Creates a smooth scrolling effect
  function scrollFunction() {
    document.documentElement.style.scrollBehavior = "smooth";
  }
</script>

<!--HTML-->
<body>
  <!--Creates a new line to separate nav bar and textbox-->
  <br />
  <!--TextBox-->
  <input class="nameText" bind:value={name} placeholder="What is your name?" />
  <!--Displays the user's name with a capitalized first letter-->
  <h2 style="margin-bottom: 10%">
    Welcome {name.charAt(0).toUpperCase() + name.slice(1) || "Stranger"} to {title}!
    &#x2661
  </h2>

  <!--Button for Next Section-->
  <a href="#nextSection">
    <button on:click={scrollFunction}>Continue</button>
  </a>

  <section class="picture1" id="nextSection">
    <h1 style="padding: 26%">
      Scroll Down <br /><span class="scroll-down">&#8595</span>
    </h1>
  </section>

  <!--Text-->
  <section class="firstPageText">
    <p>Hover Text Below</p>
    <h2>Fashion is a form of <big><i>self-expression</i></big></h2>
    <!--Adds extra information-->
    <span class="tooltipText">
      <q
        >When you wear something that is comfortable, cute, or fancy, it makes
        you feel good about yourself. <br />Fashion is in the clothes, but style
        is in the person.</q
      >
    </span>
  </section>

  <!--Flexbox for Picture 2 & 3-->
  <section class="flex-container">
    <section class="picture2" />
    <section class="picture3" />
  </section>

  <!--Button-->
  <section class="button-container">
    <a href="/secondPage">
      <button>Next</button>
    </a>
  </section>

  <p style="text-align: center; font-size: 2em">1</p>
</body>

<!--CSS Styling-->
<style>
  /*TextBox*/
  .nameText {
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    display: block;
    margin-top: 10%;
    margin-bottom: 10%;
    font-size: 1.75em;
  }
  /*Button Styling in Next Section*/
  a button {
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 20%;
  }
  /*Scroll-Down Symbol Styling*/
  .scroll-down {
    font-size: 2.5em;
    color: white;
  }
  /*Pictures*/
  .picture1 {
    background-image: url("images/mannequins.jpg");
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 970px;
  }
  .picture2 {
    background-image: url("images/castle.jpg");
    background-size: cover;
    background-position: center;
    width: 55%;
    height: 990px;
    margin: 10px;
    border-radius: 25px;
  }
  .picture3 {
    background-image: url("images/three women.jpg");
    background-size: cover;
    background-position: center;
    width: 45%;
    height: 990px;
    margin: 10px;
    border-radius: 25px;
  }
  .firstPageText {
    /*makes the tooltip text go to the center*/
    text-align: center;
    margin-bottom: 5%;
  }
  .firstPageText p {
    text-align: center;
  }
  /*Tooltip Text Styling*/
  .firstPageText .tooltipText {
    visibility: hidden;
    border-radius: 10px;
    color: white;
    font-family: "Arial";
    font-size: 1.6em;
  }
  .firstPageText:hover .tooltipText {
    visibility: visible; /*extra info becomes visible*/
  }
</style>
