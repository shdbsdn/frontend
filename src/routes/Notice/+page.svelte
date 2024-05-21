<script>
    import { onMount } from 'svelte';
    import { Notice } from 'flowbite';
    import 'tailwindcss/tailwind.css';
  
    let notices = [];
  
    onMount(async () => {
      // 이 부분에서 실제 공지사항 데이터를 가져오는 API 호출을 수행하실 수 있습니다.
      notices = [
        { id: 1, title: '공지사항 1', content: '공지사항 내용 1' },
        { id: 2, title: '공지사항 2', content: '공지사항 내용 2' },
        // ...
      ];
    });
  </script>
  
  <div class="container mx-auto px-4">
    <h1 class="text-3xl font-bold mb-4">공지사항</h1>
    {#each notices as notice (notice.id)}
      <Notice title={notice.title} content={notice.content} class="mb-4" />
    {/each}
  </div>
  