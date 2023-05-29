<script>
  import { browser } from "$app/environment";
  import { pictureDetails } from "$lib/stores";
  import PictureList from "$lib/PictureList.svelte";
  import Greeting from "$lib/Greeting.svelte";

  let greeting = "";
  //If not null, value is returned from the storage. If null, returns empty string
  let name = browser ? window.localStorage.getItem("username") ?? "" : "";
  let img = browser ? window.localStorage.getItem("image") ?? "" : "";

  //The setTimeout here is emulating a delayed response to make the user feel like something is "loading".
  const BASE_URL = "https://api.unsplash.com";
  if (img === "") {
    setTimeout(() => {
      fetch(
        `${BASE_URL}/search/photos?client_id=X7SnFWVw8MCYh7ne-LVwwwwxgi05ikflmFslty1sef4&query=black clothes`
      )
        .then((r) => r.json())
        .then((data) => {
          img = data.results[0].urls.full;
          console.log(img);
        });
    }, 2000);
  }
  // This function creates a smooth scrolling effect and also sets the image and the username
  const scrollFunction = () => {
    localStorage.setItem("image", img);
    localStorage.setItem("username", name);
    document.documentElement.style.scrollBehavior = "smooth";
  };
  //A function that prevents numbers and special characters from displaying in the textbox
  const onlyLetters = (e) => {
    if (/^[^a-zA-Z]*$/.test(e.key)) {
      e.preventDefault();
      return false;
    }
  };
  let subset = [...pictureDetails];
  subset = subset.splice(3);
</script>

<section class="backgroundPic mainPicture" style="background-image:url({img})">
  <input
    bind:value={name}
    on:keydown={onlyLetters}
    placeholder="What is your name?"
    maxlength="20"
  />
  <Greeting {greeting} />
  <h2>
    Welcome {name.charAt(0).toUpperCase() + name.slice(1) || "Stranger"}
    to Lucky's Website! &#x2661
  </h2>

  <section class="button-container">
    <a href="#nextSection">
      <button on:click={scrollFunction}>Continue</button>
    </a>
  </section>
</section>
<section class="firstPageText" id="nextSection">
  <p>Hover Text Below</p>
  <h2>Fashion is a form of <big><i>self-expression</i></big></h2>
  <span class="tooltipText">
    <p>
      When you wear something that is comfortable, cute, or fancy, it makes you
      feel good about yourself. <br />Fashion is in the clothes, but style is in
      the person.
    </p>
  </span>
</section>
<PictureList pictureDetails={subset} />

<style>
  .mainPicture {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  .mainPicture input {
    text-align: center;
    margin-inline: auto;
    font-size: 1.8vw;
  }
  .firstPageText h2 {
    opacity: 0.7;
  }
  .firstPageText h2:hover {
    opacity: 1;
  }
  .firstPageText .tooltipText {
    visibility: hidden;
  }
  .firstPageText:hover .tooltipText {
    visibility: visible;
  }
  @media screen and (max-width: 375px) {
    .mainPicture input {
      font-size: 4vw;
    }
  }
</style>
