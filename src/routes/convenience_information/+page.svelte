<script>
    import { Alert, Li, List } from 'flowbite-svelte';
    import { InfoCircleSolid } from 'flowbite-svelte-icons';
</script>

<style>
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
    <div class="text-overlay">편의정보</div>
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
  
<br>

<Alert class="!items-start">
<span slot="icon">
    <InfoCircleSolid slot="icon" class="w-5 h-5" />
    <span class="sr-only">Info</span>
</span>
<p class="font-medium">학생회실 내 비치된 도서 대출</p>
<ul class="mt-1.5 ms-4 list-disc list-inside">
    <li>At least 10 characters (and up to 100 characters)</li>
    <li>At least one lowercase character</li>
    <li>Inclusion of at least one special character, e.g., ! @ # ?</li>
</ul>
</Alert>
<Alert color="blue" class="!items-start">
<span slot="icon">
    <InfoCircleSolid slot="icon" class="w-5 h-5" />
    <span class="sr-only">Info</span>
</span>
<p class="font-medium">우천시 우산 대여 서비스</p>
<List class="mt-1.5 ms-4">
    <Li>At least 10 characters (and up to 100 characters)</Li>
    <Li>At least one lowercase character</Li>
    <Li>Inclusion of at least one special character, e.g., ! @ # ?</Li>
</List>
</Alert>