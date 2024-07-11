<template>
  <div>
    <PCHome class="pc" />
    <MHome class="mobile" />
  </div>
</template>

<script>
import PCHome from '../components/home/PCHome.vue';
import MHome from '../components/home/MHome.vue';

export default {
  components: {
    PCHome,
    MHome
  },
  mounted() {
    this.$axios.get('http://localhost:1337/api/posts?populate=*').then((response) => {
      console.log(response.data);
    });
    
  }
}

</script>