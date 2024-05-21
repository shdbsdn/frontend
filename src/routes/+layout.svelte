<script>
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Dropdown, DropdownItem, DropdownDivider,Footer, FooterCopyright, FooterLinkGroup, FooterBrand, FooterLink } from 'flowbite-svelte';
  import { page } from '$app/stores';
  $: activeUrl = $page.url.pathname;
  let showDropdown = false; // 드롭다운 메뉴의 표시 여부를 제어하는 상태 변수
</script>


<Navbar class="bg-blue-200 mb-4">
  <NavBrand href="/">
    <img src="/images/PNU logo.jpg" class="me-3 h-6 sm:h-9" style="width: 100px; height: auto;" alt="PNU Logo" />
    <div class="self-center whitespace-nowrap dark:text-white" style="font-size: 2em; font-weight: bold; margin-right: 30px;">
      PNU BCE<br>Student Council
    </div>
  </NavBrand>

  <NavHamburger />
  <NavUl {activeUrl}>
    <NavLi class="cursor-pointer" style="font-size: 1.5em; font-weight: bold; margin-left: 100px;">
      소개<span class="w-6 h-6 ms-2 text-primary-800 dark:text-white inline">▽</span>
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/insamal">인사말</DropdownItem>
          <DropdownItem href="/jojikdo">조직도</DropdownItem>
          <DropdownItem href="/yeonheuk">연혁</DropdownItem>
        </Dropdown>
    </NavLi>
    <NavLi href="/Notice" style="font-size: 1.5em; font-weight: bold; margin-left: 100px;">공지</NavLi>
    <NavLi class="cursor-pointer" style="font-size: 1.5em; font-weight: bold; margin-left: 100px;">
      소통<span class="w-6 h-6 ms-2 text-primary-800 dark:text-white inline">▽</span>
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/Q&A">Q&A</DropdownItem>
          <DropdownItem href="/chatbot">챗봇</DropdownItem>
        </Dropdown>
    </NavLi>
    <NavLi href="/convenience information" style="font-size: 1.5em; font-weight: bold; margin-left: 100px;">편의정보</NavLi>
    <NavLi class="cursor-pointer" style="font-size: 1.5em; font-weight: bold; margin-left: 100px;">
      자료실<span class="w-6 h-6 ms-2 text-primary-800 dark:text-white inline">▽</span>
        <Dropdown class="w-44 z-20">
          <DropdownItem href="/pasthangsajeongbo">과거행사정보</DropdownItem>
          <DropdownItem href="/hangsasajin">행사사진</DropdownItem>
        </Dropdown>
    </NavLi>
  </NavUl>
</Navbar>

<div class="px-2 sm:px-4">
  <div class="container mx-auto">
      <slot></slot>
  </div>
</div>

<Footer class="fixed bottom-0 start-0 z-20 w-full">
  <FooterCopyright href="/" by="PNU BCE™" year={2024} />
    <div style="text-align: center"> 
      <p>주소: 경상남도 양산시 물금읍 부산대학로 49 경암공학관 106호</p>
      <p>행정실: 051-510-8544</p>
      <p>이메일: bce.pnu@pusan.ac.kr</p>
    </div> 
</Footer>
