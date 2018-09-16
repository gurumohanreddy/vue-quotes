<template>
  <div class="row">
    <div class="card col-md my-4">
      <div class="card-body">
        <div class="card-title">Quotes Addded</div>
        <div class="progress">
          <div class="progress-bar" role="progressbar" :style="{width: (quotesCount/maxQuotes)*100+'%'}" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">{{quotesCount}}/{{maxQuotes}}</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ['quotesCount', 'maxQuotes']
}
</script>

