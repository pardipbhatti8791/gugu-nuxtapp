<template>
  <div>
    <h1>Event #{{ id }}</h1>
  </div>
</template>

<script>
export default {
  computed: {
    id() {
      return this.$route.params.id
    }
  },
  head() {
    return {
      titleTemplate: '%s - Real world events',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content:
            'Where you can find all the events taking place in your neighborhood ' +
            this.id
        }
      ]
    }
  }
}
</script>
