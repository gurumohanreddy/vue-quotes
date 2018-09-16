<template>
  <div class="row my-4">
    <div class="card col-md">
      <div class="card-body">
        <div class="card-title">Add a Quote</div>
        <form>
          <div class="form-row">
            <div class="col-md-9">
              <input type="text" class="form-control" placeholder="Add a Quote" v-model='quote'>
            </div>
            <div class="col-md-3">
              <button type="submit" class="btn btn-block btn-primary" @click.prevent="createNew">Add Quote</button>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data:function() {
    return { quote: '' }
  },
  methods: {
    createNew() {
      this.$emit('addedQuote', this.quote);
      this.quote = '';
    }
  }
}
</script>
<style>
</style>
