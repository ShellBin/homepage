<template>
    <div class="bento">
      <div class="bento-row">
        <div class="twitter"></div>
        <div class="twitter"></div>
      </div>
    </div>
</template>
<script lang="ts">
// import axios from 'axios'

export default {
  name: 'BentoLinks',
  data () {
    return {
      twitterData: null
    }
  }
}
</script>

<style scoped lang="scss">
.bento {
  display: flex;
  justify-content: center;
  justify-items: center;
  max-width: 100rem;
}

@media (max-width: 82rem) {
  .bento {

  }
}

.bento-row {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  // margin-bottom: ;
}

@mixin bento-block {
  display: flex;
  border-radius: 24px;
  border: #E2E6EA solid 1px;
}

@mixin bento-standard {
  @include bento-block();
  height: 13vw; width: 13vw;
  min-height: 8rem; min-width: 8rem;
  max-height: 12rem; max-width: 12rem;
}

@mixin bento-banner {
  @include bento-block();
}

@mixin bento-taller {
  @include bento-block();
}

@mixin bento-fatter {
  @include bento-block();
}

@mixin bento-huge {
  @include bento-block();
}

// 元素样式
.twitter {
  @include bento-standard();
  background-color: #F5FAFE;
}
</style>
