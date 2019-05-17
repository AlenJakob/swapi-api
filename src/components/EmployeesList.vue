<template>
  <div class="card_list-container">
    <div>
      <HeaderSword/>
      <Card :EmployeeList="EmployeeList" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Card from "./Card";
import HeaderSword from "./HeaderSword";
import EmployeeSword from "./EmployeeSword";
export default {
  components: {
    Card,
    HeaderSword,
    EmployeeSword
  },
data() {
    return {
      msg: "Swapi Api App",
      EmployeeList: []
    };
  },
  methods: {
    test() {
      console.log(this.EmployeeList, "employee are empty damn");
    }
  },
  async mounted() {
    const listUsers = await axios
      .get("https://swapi.co/api/people")
      .then(res => (this.EmployeeList = res.data.results))
      .catch(err => new err());
  }
};


</script>

<style scoped>
.card_list-container {
  padding: 2rem 1rem 1rem 1rem;
  border-radius: 5px;
  margin: 0 auto;
  background: rgba(42, 56, 65, 1);
  color: rgba(159, 170, 175, 1);
  box-shadow: 0 0 2rem rgba(0, 0, 0, 1);
  width: 600px;
  min-height: 500px;
}

</style>
