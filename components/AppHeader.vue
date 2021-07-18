<template>
  <b-navbar type="dark" variant="dark">
    <b-navbar-nav >
      <nuxt-link class="nav-link" to="/">Home</nuxt-link>
      <nuxt-link class="nav-link" to="/about">About me</nuxt-link>
      

      <!-- Navbar dropdowns -->
      <b-nav-item-dropdown text="Lang" right>
        <nuxt-link class="nav-link bg-dark" to="/jokes">Page1</nuxt-link>
        <b-dropdown-item href="#">EN</b-dropdown-item>
        <b-dropdown-item href="#">ES</b-dropdown-item>
        <b-dropdown-item href="#">RU</b-dropdown-item>
        <b-dropdown-item href="#">FA</b-dropdown-item>
      </b-nav-item-dropdown>

      <b-nav-item-dropdown text="User" right>
        <b-dropdown-item href="#">Account</b-dropdown-item>
        <b-dropdown-item href="#">Settings</b-dropdown-item>
      </b-nav-item-dropdown>
    </b-navbar-nav>
  </b-navbar>
</template>

<script>
export default {
  name:'AppHeader'

}
</script>

<style>

</style>
