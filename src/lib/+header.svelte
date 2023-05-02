<!-- JavaScript -->
<script>
  import Navigation from "./+navigation.svelte";
  import SocialIcons from "@rodneylab/svelte-social-icons";
</script>

<!-- HTML -->

<!--Icons-->
<section class="icon-container">
  <a href="#0">
    <SocialIcons network="instagram" />
  </a>
  <a href="#0">
    <SocialIcons network="facebook" />
  </a>
  <a href="#0">
    <SocialIcons network="youtube" />
  </a>
  <a href="#0">
    <SocialIcons network="spotify" />
  </a>
  <a href="#0">
    <SocialIcons network="snapchat" />
  </a>
  <a href="#0">
    <SocialIcons network="pinterest" />
  </a>
  <a href="#0">
    <SocialIcons network="discord" />
  </a>
  <a href="https://github.com/luckymanaya">
    <SocialIcons network="github" />
  </a>
  <a href="#0">
    <SocialIcons network="twitter" />
  </a>
</section>

<Navigation />

<style>
  .icon-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 4rem;
    background-color: black;
    padding: 1rem;
  }
  a {
    transition: transform 0.5s; /* Animation */
  }
  a:hover {
    transform: scale(1.4); /*Zooms in*/
  }
</style>
