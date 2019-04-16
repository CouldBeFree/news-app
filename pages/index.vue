<template>
  <div>
    <div class="code">
      Hello World
    </div>
    <ul>
      <li v-for="item in items" :key="item.id">{{ item.title }}</li>
    </ul>
  </div>
</template>

<script>
  import axios from '~/plugins/axios';
  import { mapState } from 'vuex'

  export default {
    computed: mapState([
      "items",
      "ids"
    ])
  }
</script>
