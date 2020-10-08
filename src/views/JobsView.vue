<template>
  <div>
      <div v-for="user in this.$store.state.jobs" :key="user.id">
          {{ user }}
      </div>
  </div>
</template>

<script>
export default {
   
    created(){

        this.$store.dispatch('FETCH_JOBS');

    
    }
}
</script>

<style>

</style>