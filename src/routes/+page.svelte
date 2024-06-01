<script>
  import { Carousel } from 'flowbite-svelte';
  import images from '/src/imageData/images.json';

  let index = 0;
  let image = images[0];  // Initialize with the first image
</script>

<style>
  :global(body), :global(html) {
    margin: 0;
    padding: 0;
    width: 100%;
  }

  .carousel-container {
  position: relative;
  width: calc(100vw - 16px); /* Full viewport width minus 16px for padding/margin */
  overflow: hidden;
  }

  .carousel-image img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }
  .carousel-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .alt-text {
    position: absolute; /* Set position to absolute */
    bottom: 10px; /* Adjust as necessary for your design */
    right: 10px; /* Adjust as necessary for your design */
    z-index: 9999; /* Ensure it's above other content */
    background-color: rgba(255, 255, 255, 0.8); /* Semi-transparent background */
    padding: 8px;
    border-radius: 8px;
  }
</style>

<div class="carousel-wrapper">
  <div class="carousel-container">
    <Carousel {images} let:Indicators let:Controls on:change={({ detail }) => (image = detail)}>
      <Controls />
      <Indicators />
      <div slot="item" class="carousel-image">
        {#each images as img}
          <img src={img.src} alt={img.alt} />
        {/each}
      </div>
    </Carousel>
    <div class="alt-text">
      {image?.alt}
    </div>
  </div>
</div>

