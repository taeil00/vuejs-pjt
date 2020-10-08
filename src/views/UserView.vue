<template>
<div>
  <p>
     {{ userInfo.id }}
  </p>
  <p>
     {{ userInfo.karma }}
  </p>
  <p>
     {{  this.$store.state.user.created }}
  </p>
  </div>
</template>

<script>



export default {
  computed:{
    userInfo(){
      return this.$store.state.user;
    }
  },
  created(){
    const userName = this.$route.params.id;
    console.log(this.$route.params.id);

    this.$store.dispatch('FETCH_USER', userName);
  }
}
</script>

<style>

</style>