<template>
  <div class="avatar-container">
    <img class="avatar" alt="avatar" src="@/assets/avatar.jpg">
    <div class="info">
      <p class="name">ShellBin</p>
      <p class="bio">A computer-loving person who enjoys everything.</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'AvatarContainer'
})
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.avatar {
  width: 11.5rem;
  border-radius: 50%;
}

.info {
  margin-left: 1rem;

  .name {
    margin: 2rem 0 1rem;
    font-weight: bold;
    line-height: 2rem;
    font-size: 2.6rem;
  }

  .bio {
    word-break: break-word;
    color: #565656;
    font-size: 1.3rem;
  }
}

@media (max-width: 82rem) {

  /* styles for mobile devices */
  .avatar {
    width: 9.35rem;
  }

  .info {
    max-width: min(31.25rem, 100%);

    .name {
      font-size: 2rem;
    }

    .bio {
      font-size: 1rem;
    }
  }
}
</style>
