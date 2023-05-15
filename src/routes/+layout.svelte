<!-- JavaScript -->
<script>
  import "../style.css";
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";
  import BottomPageDetails from "$lib/BottomPageDetails.svelte";
</script>

<!-- HTML -->
<section class="main">
  <Header />
  <slot />
  <BottomPageDetails />
  <Footer />
</section>
