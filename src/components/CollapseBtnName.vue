<template>
  <div class="collapse_btn-show" @click="show = !show">
    <div class="name_btn-show">{{employee.name}}</div>
    <transition name="slide-fade">
      <div v-if="show" class="card_list-details">
        <DataDetails :employee="employee"/>
      </div>
    </transition>
  </div>
</template>

<script>
import DataDetails from "./EmployeeDetails/DataDetails";
export default {
  components: {
    DataDetails
  },
  props: ["employee"],
  data() {
    return {
      show: false
    };
  }
};
</script>



<style>
.collapse_btn-show {
  cursor: pointer;
  padding: 0.5rem 0 0 0;
}
.name_btn-show:hover {
  text-shadow: 0 0 5px rgba(255, 255, 255, 0.582);
}

.slide-fade-enter-active {
  transition: all 0.6s ease;
}
.slide-fade-leave-active {
  transition: all 0.3s ease-in-out;
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translatey(-10px);
  opacity: 0;
}
</style>
