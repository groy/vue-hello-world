<template lang="pug">
  div(class="deeper")
    h2 Welcome to VueJs
</template>

<script>

export default {
  name: 'Deeper',
  components: {},
  props: {},
  data(){
    return {
      sampleData: null,
    };
  },
  computed: {},
  asyncComputed: {},
  methods: {},
  watch: { // Defined functions execute when changes happen to the corresponding data variables
    sampleData() {
      // Do the thing
    }
  },
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},
  beforeUpdate() {}, // Triggered immediately before ANY DOM updates
  updated() {}, // Triggered immedaitely after ANY DOM updates
  beforeDestroy() {}, // Going, going, going!
  destroyed() {}, // Uh-oh all gone
}
</script>

<style lang="sass">
.deeper
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center 
</style>
