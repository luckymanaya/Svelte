<!--HTML Structure-->
<body>
  <section class="picture1" />

  <!--Text-->
  <section class="firstPageText">
    <p>Fashion is a form of <big><i>self-expression</i></big></p>
    <!--Adds extra information-->
    <span class="tooltipText">
      <center>
        <q
          >When you wear something that is comfortable, cute, or fancy, it makes
          you feel good about yourself. <br>Fashion is in the clothes, but style is
          in the person.</q
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

  <!--Flexbox for the Bottom Details-->
  <section class="flex-container">
    <a href="/secondPage">
      <button>Next</button>
    </a>
  </section>
  <p style="text-align: center; font-size: 2em">1</p>
</body>

<!--CSS Styling-->
<style>
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

  /*Text in First Page Styling*/
  .firstPageText p {
    text-align: center;
    font-family: "Arial";
    font-size: 2.5em;
    color: white;
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
    visibility: visible;
  }
</style>
