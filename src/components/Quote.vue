<template>
  <div class="col-md-6 mb-3">
    <div class="card">
      <div class="card-body">
        <slot></slot>
      </div>
    </div>
  </div>
</template>
<script>
</script>
<style lang='scss' scoped>
  .card {
    cursor: pointer;

    &:hover{
      background-color: lighten($color: red, $amount: 40%)
    }
  }
</style>
