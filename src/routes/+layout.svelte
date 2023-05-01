<!-- JavaScript -->
<script>
  import "../style.css";
  import Header from "$lib/+header.svelte";
  import Footer from "$lib/+footer.svelte";
</script>

<!-- HTML -->
<section class="main">
  <Header />
  <slot />
  <Footer />
</section>
