<!-- JavaScript -->
<script>
  import "../style.css";
  import Header from "$lib/+header.svelte";
  import Footer from "$lib/+footer.svelte";
  import BottomPageDetails from "$lib/+bottomPageDetails.svelte";
</script>

<!-- HTML -->
<section class="main">
  <Header />
  <slot />
  <BottomPageDetails />
  <Footer />
</section>
