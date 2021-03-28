<template>
  <section>
    <h2>Home Upgrades</h2>
    <p>
      Have done the following upgrades to your home?
      -radiant barrier
      -R42 minimum insulation
      -Smart Thermostat
      -Solar Powered Venthiliation Fan
      -LED Light Bulbs
    </p>

    <div class="field">
      <label class="label">What is the name of you Electric Company</label>
      <div class="control">
        <input class="input" type="text" :vlaue="value" @input="$emit('input', $event.target.value)" placeholder="You Electric Company">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "StepTwo",
  props: ['value'],
}
</script>

<style scoped>

</style>
