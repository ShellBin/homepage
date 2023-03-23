<template>
    <div class="footer-info">
        <span>什么样的魔法技巧我全都会！</span>
         <span>Visual design by bento.me</span>
        <span>© 2013-{{new Date().getFullYear()}} ShellBin. All rights reserved.</span>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'FooterInfo'
})
</script>

<style scoped lang="scss">
.footer-info {
    display: flex;
    flex-direction: column;

    span {
        display: block;
        color: #616161;
    }
}
</style>
