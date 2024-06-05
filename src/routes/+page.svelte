<script>
  import { onMount } from 'svelte';
  import images from '/src/imageData/images.json';

  let imageData = [];

  onMount(() => {
    imageData = images;
  });
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;700&display=swap');

  :global(html), :global(body) {
    height: 100%;
    margin: 0;
    font-family: 'Noto Sans KR', sans-serif; /* 폰트 적용 */
  }
  .image-container {
    position: relative;
    width: 100%;
    margin: 0 auto;
  }

  .image {
    width: 100%;
    display: block;
  }

  .text-overlay {
    position: absolute;
    top: 20%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    padding: 10px;
    font-size: 5em; /* Adjust the font size as needed */
    font-weight: bold; /* Make the text bold */
    text-align: center;
    white-space: nowrap;
  }
</style>

<div>
  {#each imageData as image}
    <div class="image-container">
      <img src={image.src} alt={image.alt.replace('<br>', ' ')} class="image" />
      <div class="text-overlay">
        {@html image.alt}
      </div>
    </div>
  {/each}
</div>
