<template>
    <div class="bento">
      <!-- <h1>There are Bento here</h1> -->
      <div class="twitter"></div>
      <div class="twitter"></div>
      <div class="twitter"></div>
      <div class="twitter"></div>
      <div class="twitter"></div>
      <div class="twitter"></div>
      <div class="twitter"></div>
    </div>
</template>
<script lang="ts">
import axios from 'axios'

export default {
  name: 'BentoLinks',
  data () {
    return {
      twitterData: null
    }
  },

  mounted () {
    this.fetchData()
  },

  methods: {
    fetchData () {
      console.log('Test')
    }
  }
}
</script>

<style scoped lang="scss">
.bento {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(5rem, 10rem));
  grid-gap: 1.5rem;
  justify-content: center;
  max-width: 500rem;
  flex-grow: 1;
}

@mixin bento-block {
  display: flex;
  border-radius: 24px;
  border: #E2E6EA solid 1px;
}

@mixin bento-standard {
  @include bento-block();
  height: 10vw; width: 10vw;
  min-height: 8rem; min-width: 8rem;
  max-height: 10rem; max-width: 10rem;
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
