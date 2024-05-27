<script>
    let posts = [
      { id: 1, title: '학생회비 납부 확인은 어떻게 하나요?', content: '내용 1' },
      { id: 2, title: '차량 등록은 어떻게 하나요?', content: '내용 2' },
      { id: 3, title: '출석 인정은 어떻게 받나요?', content: '내용 3' }
      // ...
    ];
</script>

<div class="container mx-auto px-4">
<h1 class="text-3xl font-bold mb-4">Q&A</h1>
<div class="border rounded-lg overflow-hidden">
    {#each posts as post (post.id)}
    <div class="border-b p-4">
        <h2 class="text-xl font-bold">{post.title}</h2>
        <p>{post.content}</p>
    </div>
    {/each}
</div>
</div>
  
  