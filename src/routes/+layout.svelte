<!-- JavaScript -->
<script>
  import "../style.css";
  import Header from "$lib/+header.svelte";
  import Footer from "$lib/+footer.svelte";
  import PageDetails from "$lib/+pageDetails.svelte";
</script>

<!-- HTML -->
<section class="main">
  <Header />
  <slot />

  <PageDetails/>
  <Footer />
</section>
