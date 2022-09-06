<script>
import Counter from './components/Counter.vue';
import RadialProgressBar from 'vue-radial-progress'


export default {
  components: {
    Counter,
    RadialProgressBar
  },
  data() {
    return {
      totalCounters: 3,
      countersFinished: 0
    }
  },
  methods: {
    updateCountersFinished() {
      this.countersFinished++;
    }
  }
}

</script>

<template>
  <h1>Contadores</h1> 
  <radial-progress-bar :diameter="200"
                       :completed-steps="countersFinished"
                       :total-steps="totalCounters" 
                       animate-speed="3000"
                       start-color="red"/>
  <h2 v-if="countersFinished!=totalCounters">De los {{ totalCounters }} han finalizado {{ countersFinished }} </h2>
  <h2 v-else>¡Todos los contadores estan a 0!</h2>
  <Counter @counter-finished="updateCountersFinished" initial-value="10" />
  <Counter @counter-finished="updateCountersFinished" initial-value="5" />
  <Counter @counter-finished="updateCountersFinished" initial-value="3" />


</template>

<style scoped>
</style>
