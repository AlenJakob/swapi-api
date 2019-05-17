<template>
  <div>
    <div class="card_el-employee" v-for="employee in EmployeeList" :key="employee.id">
      <CollapseBtnName :employee="employee"/>
      <EmployeeSword/>
    </div>
  </div>
</template>


<script>
import EmployeeSword from "./EmployeeSword";
import CollapseBtnName from "./CollapseBtnName";
export default {
  props: ["EmployeeList"],
  data() {
    return {};
  },
  components: {
    EmployeeSword,
    CollapseBtnName
  }
};
</script>
