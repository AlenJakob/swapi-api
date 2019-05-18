<template>
  <div class="row_details-container">
    <div class="column_details-first column_flex">
      <span>Height: {{employee.height}} cm</span>
      <span>Mass: {{employee.mass}} kg</span>
      <span>Birth Year: {{employee.birth_year}} BBY</span>
      <span>Gender: {{employee.gender}}</span>
    </div>
    <div class="column_details-second column_flex">
      <span>Hair: {{employee.hair_color}}</span>
      <span>Birth Year: {{employee.skin_color}}</span>
      <span>Eye: {{employee.eye_color}}</span>
    </div>
    <div class="column_details-img column_flex">
      <ImgExample/>
    </div>
  </div>
</template>

<script>
import ImgExample from "../ImgExample";
export default {
  components: {
    ImgExample
  },
  props: ["employee"],
  computed: {},
  methods: {},
  mounted() {}
};
</script>

<style scoped>
.row_details-container {
  padding: 1rem 0.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.column_flex {
  width: 33.33%;
  display: flex;
  flex-direction: column;
}
</style>
