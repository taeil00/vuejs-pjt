<template>
  <div>
      <div v-for="user in users" :key="user.id">{{ user }}</div>

  </div>
</template>

<script>
import { fetchNewsList} from '../api/index.js';
//import axios from 'axios';

export default {

data(){
    return {
        users: []
    }
},
created(){
    fetchNewsList()
    //axios.get('https://api.hnpwa.com/v0/news/1.json')
    .then(response => this.users = response.data)
    .catch()
}

}
</script>

<style>

</style>