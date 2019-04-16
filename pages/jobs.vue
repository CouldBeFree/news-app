<template>
    <div>
        <h1>Jobs</h1>
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
      await store.dispatch("LOAD_ITEMS", "jobstories.json")
    }
  }

</script>
