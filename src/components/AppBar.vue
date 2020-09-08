<template>
    <div class="center">
      <vs-navbar center-collapsed v-model="active">
        <template #left>
          <img class="icon" src="../assets/logo.png" alt="">
        </template>
        
        <template #right>
      <vs-avatar-group max="4">
        <vs-avatar>
          <img src="../assets/avatars/avatar-1.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-6.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-2.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-7.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-3.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-8.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-4.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-9.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-5.png" alt="">
        </vs-avatar>
        <vs-avatar>
          <img src="../assets/avatars/avatar-10.png" alt="">
        </vs-avatar>
      </vs-avatar-group>
        </template>
      </vs-navbar>
    </div>
</template>

<script>
  export default {
    data: () => ({
      active: 'primary'
    })
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .icon{
    height: 40px;
  }
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
  .vs-navbar-content{
    position: relative;
  }
</style>