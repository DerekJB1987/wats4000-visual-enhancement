<template>
  <div>
    <ul v-if="messages.length > 0">
        <message-item v-for="msg in messages" v-bind:message="msg" v-bind:key="msg.text"></message-item>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';
require('vue2-animate/dist/vue2-animate.min.css');

import CubeSpinner from '@/components/CubeSpinner';
import MessageContainer from '@/components/MessageContainer';

export default {
  name: 'MessageContainer',
  props: {
    messages: []
  },
  components: {
    spinner: CubeSpinner,
    'message-container': MessageContainer
  },
}
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
</style>