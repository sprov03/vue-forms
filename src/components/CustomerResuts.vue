<template>
  <section>
    <h2>Report</h2>


    <h5>Average Solar Bill</h5>
    <p>{{averageSolarBill}}</p>


    <h5># Years of Free Electricity</h5>
    <p>{{yearsOfFreeElectricity}} years</p>


    <h5>Average Increase in Property Value</h5>
    <p>$4,500.00</p>


    <div>
      <h7>Online Solar Presentation</h7>
      <p>This is an interactive video presentation designed to inform you about solar and help you to decide if you want to go solar.</p>
      <a href="">Solar Presentation</a>
    </div>
    <br>

    <div>
      <h7>Prefer a real person?</h7>
      <p>Setup a time to talk to a real person.</p>
      <a href="">Schedule Appointment</a>
    </div>

    <div>
      <h7>Not ready for a presentation?</h7>
      <p>We completely understand. Please view our Solar Energy Knowledge Base.</p>
      <a href="">Knowledge Base</a>
    </div>
    <br>
  </section>
</template>

<script>
export default {
  name: "CustomerResults",
  props: ['info'],
  computed: {
    averageSolarBill() {
      return '$' + 27.04;
    },
    yearsOfFreeElectricity() {
      return 5;
    },
  }
}
</script>

<style scoped>

</style>
