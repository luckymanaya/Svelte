<script>
  import "../style.css";
  import Header from "$lib/+header.svelte";
  import Footer from "$lib/+footer.svelte";
</script>

<section class ="main">
  <Header />

  <slot />
  <!--page specific content-->

  <Footer />
</section>
