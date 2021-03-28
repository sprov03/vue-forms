<template>
  <div id="app">
    <h1>Value Solar Power Pre Qualifier</h1>
    <p>This is a quick 7 question question prequalifies</p>
    <p>Step: {{step}}</p>


    <step-one   v-if="step === 1" v-model="info.electricCompany"></step-one>
    <step-two   v-if="step === 2" v-model="info.electricCompany"></step-two>
    <step-three v-if="step === 3" v-model="info.electricCompany"></step-three>
    <step-four  v-if="step === 4" v-model="info.electricCompany"></step-four>

    <customer-results v-if="step === 7" info="info"></customer-results>


    <button @click="step--" :disabled="step === 1">
      Prev
    </button>

    <button @click="step++" :disabled="step === 7">
      <template v-if="step === 7">View Results</template>
      <template v-else>Next</template>
    </button>

    <pre>{{info | json}}</pre>
  </div>
</template>

<script>
import StepOne from "@/components/StepOne";
import StepThree from "@/components/StepThree";
import StepFour from "@/components/StepFour";
import CustomerResults from "@/components/CustomerResuts";
export default {
  name: 'HelloWorld',
  components: {CustomerResults, StepFour, StepThree, StepOne},
  props: {
    msg: String
  },
  data() {
    return {
      step: 1,
      info: {
        electricCompany: '',
        homeUpgrades: {
          radiantBarrier: false,
          R24MinimumInsulation: false,
          smartThermostat: false,
          solarVentilationFan: false,
          ledLightBulbs: false
        },
        averageElectricBill: 150.00,
        annualUsage: 30,
        annualBill: 30,
        sqftOfHome: 1300,
        atticOverGarage: false,
        whenWasHomeBuild: 1986,
        roofShaded: false,
      }
    }
  },
  methods: {
    submitData() {
      alert('Send off api call here');
    }
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
