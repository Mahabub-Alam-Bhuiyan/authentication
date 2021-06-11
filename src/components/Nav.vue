<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <router-link to="/" class="navbar-brand" ><b>Task management</b></router-link>

      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <router-link to="/login" class="nav-link" >Log In</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/register" class="nav-link" >Sign In</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Nav'

}
</script>

<style >

.nav-item{
  margin-right: 5px;
}

</style>
