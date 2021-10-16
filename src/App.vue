<template>
  <div id="app">
        <nav class="navbar navbar-expand navbar-dark bg-dark">
            <a href="/" class="navbar-brand">Ứng dụng Quản lý danh bạ</a>
            <div class="mr-auto navbar-nav">
                <li class="nav-item">
                  <router-link to='/contactbook' class='nav-link'>
                  Danh bạ <i class='fas fa-address-book'></i>
                  </router-link>
                </li>
            </div>
        </nav>

        <div class="container mt-3">
           <router-view/>
        </div>
    </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
