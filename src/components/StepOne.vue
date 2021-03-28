<template>
  <section>
    <h2>Electric Company</h2>

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
  name: "StepOne",
  props: ['value'],
}
</script>

<style scoped>

</style>
