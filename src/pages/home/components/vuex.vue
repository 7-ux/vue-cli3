<template>
  <div class="">
      <h3>vuex 组件</h3>
      <p>{{count}}</p>
      <button type="button" @click="increment(2)">plus</button>
      <button type="button" @click="decrement">delete</button>
  </div>
</template>

<script>
import { mapState, mapActions } from 'vuex'
export default {
    computed: {
        ...mapState([
            'count'
        ])
    },
    methods: mapActions([
        'increment',
        'decrement'
    ])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
