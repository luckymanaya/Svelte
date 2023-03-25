<!--JavaScript-->
<script>
  let name = "";

  //Creates a smooth scrolling effect
  function scrollFunction() {
    document.documentElement.style.scrollBehavior = "smooth";

  }
</script>

<!--HTML-->
<body>
  <br />
  <!--TextBox-->
  <input
    class="nameText"
    bind:value={name}
    placeholder="Enter Name"
    style="margin-top: 10%; margin-bottom: 10%"
  />
  <!--Displays the user's name with a capitalized first letter-->
  <h2 style="margin-bottom: 10%">Welcome {name.charAt(0).toUpperCase() + name.slice(1) || "Stranger"} &#x2661</h2> 

  <!--Button for Next Section-->
  <a href="#nextSection">
    <button
      style="display: block; margin-left: auto; margin-right: auto; margin-bottom: 20%"
      on:click={scrollFunction}>Continue</button
    >
  </a>

  <section class="picture1" id="nextSection" />
  <!--Text-->
  <section class="firstPageText">
    <h2>Fashion is a form of <big><i>self-expression</i></big></h2>
    <!--Adds extra information-->
    <span class="tooltipText">
      <center>
        <q
          >When you wear something that is comfortable, cute, or fancy, it makes
          you feel good about yourself. <br />Fashion is in the clothes, but
          style is in the person.</q
        >
      </center>
    </span>
  </section>

  <!--Flexbox for Picture 2 & 3-->
  <section class="flex-container">
    <section class="picture2" />
    <section class="picture3" />
  </section>

  <br />

  <!--Button-->
  <a href="/secondPage">
    <button style="margin-left: 85%">Next</button>
  </a>

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
  }
  /*Pictures*/
  .picture1 {
    background-image: url("images/mannequins.jpg");
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 900px;
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

  /*Tooltip Text Styling*/
  .firstPageText .tooltipText {
    visibility: hidden;
    border-radius: 10px;
    color: white;
    font-family: Arial;
    font-size: 1.6em;
  }
  .firstPageText:hover .tooltipText {
    visibility: visible; /*extra info becomes visible*/
  }
</style>
