<template>
  <section>
    <h2>Electric Bill</h2>
    <p>
      What is your average electricity bill?  (The more accurate this information, the more accurate the information we can give you)
    </p>

    <div class="field">
      <label class="label">
        What is your average electricity bill?  (The more accurate this information, the more accurate the information we can give you)
      </label>
      <div class="control">
        <input class="input" type="text" :vlaue="value" @input="$emit('input', $event.target.value)" placeholder="You Electric Company">
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "StepThree",
  props: ['value'],
}
</script>

<style scoped>

</style>
