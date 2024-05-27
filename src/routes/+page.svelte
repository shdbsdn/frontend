<script>
  import { Carousel } from 'flowbite-svelte';
  import images from '/src/imageData/images.json';

  let image = images[0];  // 초기 이미지 설정
</script>

<style>
  .carousel-image img {
    width: 100%;
    object-fit: cover; 
  }
</style>

<div class="carousel-image w-full">
  <Carousel {images} let:image let:Indicators let:Controls class="w-full">
    <Controls />
    <Indicators />
    <div slot="item" class="w-full">
      {#each images as img}
        <img src={img.src} alt={img.alt} class="w-full" />
      {/each}
    </div>
  </Carousel>

  <div class="rounded h-12 dark:bg-gray-700 dark:text-white p-2 my-2 text-center text-xl font-bold">
    {image?.alt}
  </div>
</div>