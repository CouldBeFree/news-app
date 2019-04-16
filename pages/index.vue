<template>
    <div>
        <h1>Top</h1>
        <items/>
    </div>
</template>

<script>
import Items from '~/components/Items.vue';

export default {
  components: {
    'items': Items
  },
  async fetch({store}) {
    await store.dispatch("LOAD_ITEMS", "topstories.json")
  }
}

</script>
