<script>
    import { Heading, P, A } from 'flowbite-svelte';
    import { ChevronRightOutline } from 'flowbite-svelte-icons';
    import { page } from '$app/stores';
    import { Sidebar, SidebarGroup, SidebarItem, SidebarWrapper, SidebarDropdownWrapper, SidebarDropdownItem } from 'flowbite-svelte';
    $: activeUrl = $page.url.pathname;
</script>

<div class="flex h-screen">
    <Sidebar>
    <div class="p-4 text-xl font-bold">
        소개
    </div>
    <SidebarWrapper>
        <SidebarGroup>
        <SidebarItem label="인사말" href="/insamal"/>
        <SidebarItem label="조직도" href="/jojikdo"/>
        <SidebarItem label="연혁" href="/yeonheuk"/>
        </SidebarGroup>
    </SidebarWrapper>
    </Sidebar>
    <div class="flex-1 p-10 text-2xl font-bold">
    <Heading tag="h2" customSize="text-4xl font-extrabold ">조직도</Heading>
    <hr class="my-4 border-t-2 border-blue-200">
    <P class="mb-4">Deliver great service experiences fast - without the complexity of traditional ITSM solutions. Accelerate critical development work, eliminate toil, and deploy changes with ease.</P>
    <Heading tag="h2" customSize="text-4xl font-extrabold ">부서별 업무</Heading>
    <hr class="my-4 border-t-2 border-blue-200">
    <P class="mb-4">Deliver great service experiences fast - without the complexity of traditional ITSM solutions. Accelerate critical development work, eliminate toil, and deploy changes with ease.</P>
    </div>
</div>