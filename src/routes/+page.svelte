<!--JavaScript-->
<script>
  import { browser } from "$app/environment";

  // Unsplash Website URL
  const BASE_URL = "https://api.unsplash.com";

  let img = "";
  // Fetches picture based on ID
  setTimeout(
    () =>
      fetch(
        `${BASE_URL}/photos/jNKv4QohAk0?client_id=X7SnFWVw8MCYh7ne-LVwwwwxgi05ikflmFslty1sef4`
      )
        .then((r) => r.json())
        .then((data) => {
          console.log(data);
          img = data.urls.full;
          console.log(img);
        }),
    2000
  );

  //If not null, value is returned from the storage. If null, returns empty string
  let name = browser ? window.localStorage.getItem("username") ?? "" : "";

  let title = "Lucky's Website";
  const pageNum = 1;

  const today = new Date();
  const time = today.getHours();
  let greeting = "";

  //If and else statements for displaying greetings based on local time
  if (time >= 5 && time < 12) greeting = "Good Morning!";
  else if (time >= 12 && time < 18) greeting = "Good Afternoon!";
  else greeting = "Good Evening!";

  //Creates a smooth scrolling effect
  const scrollFunction = () => {
    //Sets the name to the storage with a paired key of username after clicking the button
    localStorage.setItem("username", name);
    document.documentElement.style.scrollBehavior = "smooth";
  };
</script>

<!--HTML-->
<body>
  <section class="mainPicture" style="background-image:url({img})">
    <!--TextBox-->
    <input bind:value={name} placeholder="What is your name?" maxlength="20" />
    <!-- Displays greeting based on local time -->
    <h2>{greeting}</h2>
    <!--Displays the user's name with a capitalized first letter-->
    <h2 style="margin-bottom: 5%">
      Welcome {name.charAt(0).toUpperCase() + name.slice(1) || "Stranger"}
      to {title}! &#x2661
    </h2>

    <!--Button for Next Section-->
    <a href="#nextSection">
      <button on:click={scrollFunction}>Continue</button>
    </a>
  </section>

  <!-- Next Section -->
  <section class="picture1" id="nextSection">
    <h1>
      Scroll Down <br /><span class="scroll-down">
        <a href="#nextSection2"
          ><button on:click={scrollFunction}>&#8595</button></a
        ></span
      >
    </h1>
  </section>

  <section id="nextSection2" />

  <!--Text-->
  <p style="text-align:center; margin-top: 10%">Hover Text Below</p>
  <section class="firstPageText">
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
    <section class="item">
      <section class="picture2" />
    </section>
    <section class="item">
      <section class="picture3" />
    </section>
  </section>
</body>

<!--Buttons-->
<section class="button-container">
  <a href="/secondPage">
    <button>Next</button>
  </a>
</section>

<!--Page Number Text-->
<section class="pageNumber">
  <p>{pageNum}</p>
</section>

<!--CSS Styling-->
<style>
  /*Main Picture*/
  .mainPicture {
    background-size: cover;
    background-position: center;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  /*TextBox*/
  .mainPicture input {
    text-align: center;
    margin-inline: auto;
    margin-bottom: 2%;
    display: block;
    font-size: 1.75em;
  }
  /*Button Styling in Next Section*/
  a button {
    display: block;
    margin-left: auto;
    margin-right: auto;
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
    width: auto;
    height: 100vh;
    display:flex;
    flex-direction: column;
    justify-content:center;
  }
  .picture1 button {
    padding: 20px;
    margin-top: 50px;
    width: auto;
    font-size: 50%;
  }
  .picture2 {
    background-image: url("images/castle.jpg");
    background-size: cover;
    background-position: center;
    width: auto;
    height: 150vh;
    margin: 10px;
    border-radius: 25px;
  }
  .picture3 {
    background-image: url("images/three women.jpg");
    background-size: cover;
    background-position: center;
    width: auto;
    height: 150vh;
    margin: 10px;
    border-radius: 25px;
  }
  .firstPageText {
    /*makes the tooltip text go to the center*/
    text-align: center;
    margin-bottom: 2%;
  }
  .firstPageText h2 {
    color: gray;
  }
  .firstPageText h2:hover {
    color: white;
    /*Cursor won't change to textbox cursor*/
    cursor: default;
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
