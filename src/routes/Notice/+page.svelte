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

<div class="container mx-auto px-4">
<h1 class="text-3xl font-bold mb-4">공지사항</h1>
<div class="border rounded-lg overflow-hidden">
    {#each posts as post (post.id)}
    <div class="border-b p-4">
        <h2 class="text-xl font-bold">{post.title}</h2>
        <p>{post.content}</p>
    </div>
    {/each}
</div>
</div>
  
  