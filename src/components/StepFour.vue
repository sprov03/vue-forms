<template>
  <section>
    <h2>Annual Usage</h2>

    <div class="field">
      <label class="label">Annual Usage</label>
      <div class="control">
        <input class="input" type="text" :vlaue="value" @input="$emit('input', $event.target.value)" placeholder="30 GW">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "StepFour",
  props: ['value'],
}
</script>

<style scoped>

</style>
