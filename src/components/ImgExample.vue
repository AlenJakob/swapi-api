<template>
  <div>
    <div class="img-example">
      <span></span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.img-example {
  margin: 0 auto;
  width: 80px;
  height: 80px;
  background: rgba(29, 42, 51, 1);
  position: relative;
}
.img-example span {
  width: 120px;
  height: 3px;
  background: rgba(42, 56, 65, 1);
  display: flex;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%) rotate(45deg);
}
.img-example span:after {
  content: "";
  width: 120px;
  height: 3px;
  background: rgba(42, 56, 65, 1);
  display: flex;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%) rotate(-90deg);
}
</style>

