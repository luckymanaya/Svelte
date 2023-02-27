<script>
    import Navigation from '$lib/navigation.svelte';
    import Footer from '$lib/footer.svelte';
</script>

<input type = "text" />

<Navigation/>

<slot/> <!--page specific content-->

<Footer/>

This is the footer.