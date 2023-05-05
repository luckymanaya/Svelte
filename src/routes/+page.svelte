<!--JavaScript-->
<script>
  import { browser } from "$app/environment";

  const BASE_URL = "https://api.unsplash.com";

  let img = "";

  /*
    The setTimeout here is emulating a delayed response - it makes the user feel like something is actually 'loading'.
  */
  setTimeout(
    () =>
      fetch(
        `${BASE_URL}/search/photos?client_id=X7SnFWVw8MCYh7ne-LVwwwwxgi05ikflmFslty1sef4&query=black clothes`
      )
        .then((r) => r.json())
        .then((data) => {
          img = data.results[0].urls.full;
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

  if (time >= 5 && time < 12) greeting = "Good Morning!";
  else if (time >= 12 && time < 18) greeting = "Good Afternoon!";
  else greeting = "Good Evening!";

  //Creates a smooth scrolling effect
  const scrollFunction = () => {
    localStorage.setItem("username", name);
    document.documentElement.style.scrollBehavior = "smooth";
  };

  //A function that prevents numbers and special characters from displaying in the textbox
  const changeName = (e) => {
    if (
      /^[0-9(~|`|!|@|#|$|%|^|&|\*|\(|\)|{|}|\[|\]|;|:|\"|'|<|,|\.|>|\?|\/|\\|\||-|_|\+|=)]*$/.test(
        e.key
      )
    ) {
      e.preventDefault();
      return false;
    }
  };
</script>

<!--HTML-->
<body>
  <section class="mainPicture" style="background-image:url({img})">
    <input
      bind:value={name}
      on:keydown={changeName}
      placeholder="What is your name?"
      maxlength="20"
    />

    <h2>{greeting}</h2>
    <h2 style="margin-bottom: 5%">
      Welcome {name.charAt(0).toUpperCase() + name.slice(1) || "Stranger"}
      to {title}! &#x2661
    </h2>

    <a href="#nextSection">
      <button on:click={scrollFunction}>Continue</button>
    </a>
  </section>

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

  <p style="text-align:center; margin-top: 10%">Hover Text Below</p>
  <section class="firstPageText">
    <h2>Fashion is a form of <big><i>self-expression</i></big></h2>
    <span class="tooltipText">
      <q>
        When you wear something that is comfortable, cute, or fancy, it makes
        you feel good about yourself. <br />Fashion is in the clothes, but style
        is in the person.
      </q>
    </span>
  </section>

  <section class="flex-container">
    {#each Array(2) as _, index (index)}
      <section class="item">
        <section id="picture{index + 2}" class="picture" />
      </section>
    {/each}
  </section>
</body>

<!--Buttons-->
<section class="BackToTop">
  <a href="#">
    <button on:click={scrollFunction}>Back to top &uarr;</button>
  </a>
</section>

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
  .mainPicture {
    background-size: cover;
    background-position: center;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .mainPicture input {
    text-align: center;
    margin-inline: auto;
    margin-bottom: 2%;
    display: block;
    font-size: 1.75em;
  }
  a button {
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
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
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .picture1 button {
    padding: 20px;
    margin-top: 50px;
    width: auto;
    font-size: 50%;
  }
  .picture {
    background-size: cover;
    background-position: center;
    width: auto;
    height: 150vh;
    margin: 10px;
    border-radius: 25px;
  }
  #picture2 {
    background-image: url("images/castle.jpg");
  }
  #picture3 {
    background-image: url("images/three women.jpg");
  }
  .firstPageText {
    text-align: center;
    margin-bottom: 2%;
  }
  .firstPageText h2 {
    color: gray;
  }
  .firstPageText h2:hover {
    color: white;
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
    visibility: visible;
  }
</style>
