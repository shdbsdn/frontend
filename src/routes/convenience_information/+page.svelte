<script>
    import { Alert, Li, List } from 'flowbite-svelte';
    import { InfoCircleSolid } from 'flowbite-svelte-icons';
</script>

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