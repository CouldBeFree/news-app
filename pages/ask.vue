<template>
    <div>
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
      await store.dispatch("LOAD_ITEMS", "askstories.json")
    }
  }

</script>
