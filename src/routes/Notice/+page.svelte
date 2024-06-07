<!-- frontend/src/routes/Notice/+page.svelte -->
<script>
  import { onMount } from 'svelte';
  import axios from 'axios';

  let notices = [];

  onMount(async () => {
    const response = await axios.get(`${import.meta.env.VITE_API_URL}/notices/`);
    notices = response.data;
  });

  function getImageUrl(image) {
    return image ? image : '/default-image.png';
  }
</script>

<style>
  .container {
    max-width: 800px;
    margin: 0 auto;
    padding: 1rem;
  }
  .notice-list {
    list-style-type: none;
    padding: 0;
  }
  .notice-item {
    display: flex;
    align-items: center;
    text-decoration: none;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 1rem;
    margin-bottom: 1rem;
    transition: box-shadow 0.3s ease;
    cursor: pointer;
    color: inherit;
  }
  .notice-item:hover {
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  .notice-image {
    width: 100px;
    height: 100px;
    object-fit: cover;
    border-radius: 8px;
    margin-right: 1rem;
  }
  .notice-title {
    font-size: 1.5rem;
    color: #333;
  }
  .notice-date {
    font-size: 0.9rem;
    color: #999;
  }


  .image {
  width: 100%;
  height: 100px;
  object-fit: cover;
  display: block;
}

.image-container {
  position: relative;
  width: 100%;
  margin: 0 auto;
  margin-top: -17px;
}

.text-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 2em;
  font-weight: bold;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  text-align: center;
}

.custom-line {
  margin-top: -15px; /* 원하는 상단 여백으로 조정 */
}

</style>

<div class="image-container">
  <img src="/images/sky.jpg" class="image" alt="하늘" />
  <div class="text-overlay">공지사항</div>
</div>
<br>
<div class="relative flex items-center custom-line">
  <div class="flex-grow border-t border-gray-300"></div>
  <div class="flex-shrink mx-4 flex space-x-2">
      <div class="w-2 h-2 bg-gray-300"></div>
      <div class="w-2 h-2 bg-gray-300"></div>
      <div class="w-2 h-2 bg-gray-300"></div>
  </div>
  <div class="flex-grow border-t border-gray-300"></div>
</div>

<div class="container">
  <h1>Notices</h1>
  <ul class="notice-list">
    {#each notices as notice}
      <li>
        <a class="notice-item" href="/Notice/{notice.id}">
          <img src="{getImageUrl(notice.image)}" alt="{notice.title}" class="notice-image" />
          <div>
            <div class="notice-title">{notice.title}</div>
            <div class="notice-date">Created on: {new Date(notice.created_at).toLocaleDateString()}</div>
          </div>
        </a>
      </li>
    {/each}
  </ul>
</div>
