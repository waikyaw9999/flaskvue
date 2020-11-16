<template>
  <div class="home">
    <Ping/>
  </div>
</template>

<script>
// @ is an alias to /src
import Ping from '@/components/Ping.vue';

export default {
  name: 'Home',
  components: {
    Ping,
  },
};
</script>
