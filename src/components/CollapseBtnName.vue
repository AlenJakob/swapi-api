<template>
  <div class="collapse_btn-show" @click="show = !show">
    <div class="name_btn-show">{{employee.name}}</div>
    <transition name="slide-fade">
      <div v-if="show" class="card_list-details">
        <p
          class
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi in perspiciatis animi.</p>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  props: ["employee"],
  data() {
    return {
      show: false
    };
  }
};
</script>



<style>
.name_btn-show:hover{
    text-shadow: 0 0 5px rgba(255, 255, 255, 0.582);
}
.collapse_btn-show {
  cursor: pointer;
}
.slide-fade-enter-active {
  transition: all .6s ease;
}
.slide-fade-leave-active {
  transition: all .3s ease-in-out;
}
.slide-fade-enter, .slide-fade-leave-to{
  transform: translatey(-10px);
  opacity: 0;
}
</style>
