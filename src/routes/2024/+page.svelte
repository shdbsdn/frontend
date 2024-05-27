<script>
    import { Timeline, TimelineItem } from 'flowbite-svelte';
    import { CalendarWeekSolid } from 'flowbite-svelte-icons';
    import { Sidebar, SidebarGroup, SidebarItem, SidebarWrapper, SidebarDropdownWrapper, SidebarDropdownItem } from 'flowbite-svelte';
</script>

<div class="flex h-screen">
<Sidebar>
    <div class="p-4 text-xl font-bold">
        활동
    </div>
    <SidebarWrapper>
        <SidebarGroup>
        <SidebarItem label="2023" href="/2023"/>
        <SidebarItem label="2024" href="/2024"/>
        </SidebarGroup>
    </SidebarWrapper>
</Sidebar>
    <div class="flex-1 p-10 text-2xl font-bold">
    <Timeline order="vertical">
    <TimelineItem title="중간고사 간식행사" date="23_4_10">
        <svelte:fragment slot="icon">
        <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-primary-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-primary-900">
            <CalendarWeekSolid class="w-4 h-4 text-primary-600 dark:text-primary-400" />
        </span>
        </svelte:fragment>
        <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">중간고사 간식행사를 진행했습니다! 중간고사 화이팅!</p>
    </TimelineItem>
    <TimelineItem title="MT" date="23_5_11">
        <svelte:fragment slot="icon">
        <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-primary-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-primary-900">
            <CalendarWeekSolid class="w-4 h-4 text-primary-600 dark:text-primary-400" />
        </span>
        </svelte:fragment>
        <p class="text-base font-normal text-gray-500 dark:text-gray-400">청도로 MT를 다녀왔습니다!</p>
    </TimelineItem>
    <TimelineItem title="기말고사 간싱행사" date="23_6_10">
        <svelte:fragment slot="icon">
        <span class="flex absolute -start-3 justify-center items-center w-6 h-6 bg-primary-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-primary-900">
            <CalendarWeekSolid class="w-4 h-4 text-primary-600 dark:text-primary-400" />
        </span>
        </svelte:fragment>
        <p class="text-base font-normal text-gray-500 dark:text-gray-400">기말고사 간식행사를 진행했습니다! 기말고사 화이팅!</p>
    </TimelineItem>
    </Timeline>
    </div>
</div>