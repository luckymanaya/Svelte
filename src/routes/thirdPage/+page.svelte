<script>
  import { pictureDetails } from "$lib/stores.js";
  import PictureList from "$lib/PictureList.svelte";
  import Slideshow from "$lib/Slideshow.svelte";

  let subset = [...pictureDetails];
  subset = subset.splice(0, 3);
</script>

<PictureList pictureDetails={subset} />

<h2>
  Showcase your creativity through clothing choices... and have fun with it!
</h2>
<Slideshow />