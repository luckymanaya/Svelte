<script>
  import SocialIcons from "@rodneylab/svelte-social-icons";
</script>

<section class="about-container">
  <h1>About</h1>
  <h2>Hi There!</h2>
  <p>
    Welcome to Lucky's website! where fashion related content is given to you <i
      class="fa-regular fa-heart fa-sm"
    />
  </p>
</section>

<h2>Got any questions? I'd love to hear from you!</h2>
<p>Phone Number: 12345</p>
<p>Email: email@address.com</p>

<h2>Follow my socials! <i class="fa-regular fa-heart fa-sm" /></h2>
<section class="flex-container">
  <a href="#0">
    <SocialIcons
      network="instagram"
      width="85"
      height="85"
      fgColor="#eeeeee"
      bgColor="#111111"
    />
    <a href="#0">
      <SocialIcons
        network="youtube"
        width="85"
        height="85"
        fgColor="#eeeeee"
        bgColor="#111111"
      />
    </a>
    <a href="https://github.com/luckymanaya">
      <SocialIcons
        network="github"
        width="85"
        height="85"
        fgColor="#eeeeee"
        bgColor="#111111"
      />
    </a>
  </a>
</section>

<style>
  a {
    margin: 0 auto 1rem;
  }
  @media screen and (max-width: 375px) {
    h1,
    h2,
    p {
      font-size: 6vw;
    }
  }
</style>
