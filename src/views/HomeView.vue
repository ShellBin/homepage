<template>
  <div class="home">
    <div class="info">
      <AvatarContainer />
      <FooterInfo class="desktop-footer" />
    </div>
    <div class="main-panel">
      <BentoLinks/>
    </div>
    <FooterInfo class="mobile-footer" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AvatarContainer from '@/components/HomeView/AvatarContainer.vue'
import BentoLinks from '@/components/HomeView/BentoLinks.vue'
import FooterInfo from '@/components/HomeView/FooterInfo.vue'

export default defineComponent({
  name: 'HomeView',
  components: {
    AvatarContainer, BentoLinks, FooterInfo
  }
})
</script>

<style scoped lang="scss">
.home {
  display: flex;
  justify-content: space-between;
}

.info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 4rem;
  min-width: 30rem;
  position: fixed;
  // height: -webkit-fill-available;
  height: calc(100% - 4rem * 2);
}

.main-panel {
  margin: 4rem 4rem 4rem 40rem;
  width: 100%;
}

.desktop-footer {
  margin-left: 1rem;
}

.mobile-footer {
  margin-bottom: 2rem;
  display: none;
}

@media (max-width: 82rem) {

  /* styles for mobile devices */
  .desktop-footer {
    display: none;
  }

  .mobile-footer {
    display: block;
    padding-bottom: 2rem;
  }

  .home {
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
  }

  .info {
    margin-bottom: 2rem;
    position: relative;
    min-width: auto;
  }

  .main-panel {
    // height: 100%;
    width: 30vw;
    min-width: 18rem;
    max-width: 25rem;
    margin: 0 0 2rem;
    overflow-y: visible;
  }
}
</style>
