<script>
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Dropdown, DropdownItem, Footer, FooterCopyright, Tooltip } from 'flowbite-svelte';
  import { page } from '$app/stores';
  $: activeUrl = $page.url.pathname;
  let showDropdown = false;

  function toggleDropdown() {
    showDropdown = !showDropdown;
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;700&display=swap');

  :global(html), :global(body) {
    height: 100%;
    margin: 0;
    font-family: 'Noto Sans KR', sans-serif; /* 폰트 적용 */
  }

  :global(body) {
    display: flex;
    flex-direction: column;
  }

  .dropdown {
    display: none;
    position: absolute;
    background-color: white;
    border: 1px solid #ccc;
    padding: 10px;
    z-index: 1000;
    width: 100px; /* Dropdown width */
  }

  .tooltip:hover .dropdown {
    display: block;
  }
  

</style>

<Navbar class="mb-4 border-b-2 border-gray-300">
  <NavBrand href="/">
    <img src="/images/PNU logo.jpg" class="me-3 h-6 sm:h-9" style="width: 50px; height: auto;" alt="PNU Logo" />
    <div class="self-center whitespace-nowrap dark:text-white" style="font-size: 1.4em; font-weight: bold; margin-right: 30px;">
      PNU BCE Student Council
    </div>
  </NavBrand>
  <NavHamburger on:click={toggleDropdown} />
  <NavUl {activeUrl}>
    <div class="tooltip">
      <NavLi class="relative" style="font-size: 1.2em; font-weight: bold; margin-left: 100px;">
        <span class="text-primary-800 dark:text-white inline">소개</span>
        <div class="dropdown">
          <DropdownItem href="/insamal">인사말</DropdownItem>
          <DropdownItem href="/jojikdo">조직도</DropdownItem>
          <DropdownItem href="/yeonheuk">연혁</DropdownItem>
        </div>
      </NavLi>
    </div>
    <NavLi href="/Notice" class="nav-li" style="font-size: 1.2em; font-weight: bold; margin-left: 100px;">공지</NavLi>
    <NavLi href="/FAQ" class="nav-li" style="font-size: 1.2em; font-weight: bold; margin-left: 100px;">FAQ</NavLi>
    <NavLi href="/convenience_information" class="nav-li" style="font-size: 1.2em; font-weight: bold; margin-left: 100px;">편의정보</NavLi>
    <div class="tooltip">
      <NavLi class="relative" style="font-size: 1.2em; font-weight: bold; margin-left: 100px;">
        <span class="text-primary-800 dark:text-white inline">활동</span>
        <div class="dropdown">
          <DropdownItem href="/2023">2023</DropdownItem>
          <DropdownItem href="/2024">2024</DropdownItem>
        </div>
      </NavLi>
    </div>
  </NavUl>
</Navbar>

<div>
  <slot></slot>
</div>

<Footer class="mt-8">
  <FooterCopyright href="/" by="PNU BCE™" year={2024} />
  <div class="text-center mt-2">
    <p>주소: 경상남도 양산시 물금읍 부산대학로 49 경암공학관 106호</p>
    <p>행정실: 051-510-8544</p>
    <p>이메일: bce.pnu@pusan.ac.kr</p>
  </div>
</Footer>

