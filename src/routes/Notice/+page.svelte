<script>
    let posts = [
      { id: 1, title: '중간고사 간식행사', content: '내용 1' },
      { id: 2, title: '행림제 관련 공지사항', content: '내용 2' },
      { id: 3, title: '전치제 관련 주의사항', content: '내용 3' },
      { id: 4, title: '전치제 관련 주의사항', content: '내용 3' },
      { id: 5, title: '전치제 관련 주의사항', content: '내용 3' },
      { id: 6, title: '전치제 관련 주의사항', content: '내용 3' },
      { id: 7, title: '전치제 관련 주의사항', content: '내용 3' },
      { id: 8, title: '전치제 관련 주의사항', content: '내용 3' },
      { id: 9, title: '전치제 관련 주의사항', content: '내용 3' },
      { id: 10, title: '전치제 관련 주의사항', content: '내용 3' }
      // ...
    ];
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
    margin-top: -13px;
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

<br>

<div class="container mx-auto px-4">
<div class="border rounded-lg overflow-hidden">
    {#each posts as post (post.id)}
    <div class="border-b p-4">
        <h2 class="text-xl font-bold">{post.title}</h2>
        <p>{post.content}</p>
    </div>
    {/each}
</div>
</div>
  
  
