<template>
  <div>
    <div class="f1 code">
      Hello World
    </div>
    <ul>
      <li v-for="user in users" :key="user.id">{{ user.login }}</li>
    </ul>
  </div>
</template>

<script>
  import axios from '~/plugins/axios';
  import { mapState } from 'vuex'

  export default {
    computed: mapState([
      "users"
    ])
  }
</script>
