<template>

<Nav />


  <div class="signup">
    <router-view/>
  </div>


</template>

<script>
import Nav from './components/Nav';

export default {
  components: {Nav }
}
</script>


<style >

.signup{
  max-width: 550px;
  margin: 200px auto;
  padding: 20px;
  background-color: #f3f5f7;
  border-radius: 10px;
  box-shadow: 3px 3px 10px whitesmoke,2px 2px 20px black;
}
.signup h3{
  color: black;
  text-align: center;
}
.nav-item{
  background-color: black;
}
.nav-link{
  color: white !important;
}
.log-in{
  color: black;
}
</style>
