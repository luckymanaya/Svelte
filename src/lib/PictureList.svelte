<script>
  import Picture from "$lib/Picture.svelte";
  export let pictures;
</script>

<section class="flex-container">
  {#each pictures as pic}
    <Picture {pic} />
  {/each}
</section>
