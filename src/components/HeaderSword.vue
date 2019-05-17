<template>
  <div class="container_sword-blue">
    <div class="sword-blue"></div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container_sword-blue {
  
}
.sword-blue {
  border: 1px solid rgba(0, 0, 0, 0.1);
  background-image: url("https://i.ibb.co/Bn6Ds5c/blue-Sword.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  min-width: 540px;
  height: 35px;
  position: relative;
}
.sword-blue:before {
  content: "Employees list";
  position: absolute;
  left: 7%;
  top: -20px;
}
</style>
