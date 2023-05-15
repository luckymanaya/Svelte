<script>
  import Picture from "$lib/Picture.svelte";
  export let pictureDetails;
</script>

<section class="flex-container">
  {#each pictureDetails as pic}
    <Picture {pic} />
  {/each}
</section>
