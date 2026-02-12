<script>
export default {};
</script>

<template>
  <nav class="flex-row d-flex">
    <a href="/" class="navbar-brand"> Ứng dụng Quản lý danh bạ</a>
    <div class="mr-auto navbar-nav">
      <li>
        <router-link :to="{ name: 'contactbook' }" class="nav-link">
          Danh bạ <i class="fas fa-address-book"></i>
        </router-link>
      </li>
    </div>
  </nav>
</template>
