<template>
  <div class="social-icon-container">
    <a href="https://www.instagram.com/bitcamp" class="social-icon-chip">
      <img src="/assets/img/icons/instagram.svg" class="social-icon" />
    </a>
    <a href="https://www.facebook.com/bitcmp" class="social-icon-chip">
      <img src="/assets/img/icons/facebook.svg" class="social-icon" />
    </a>
    <a href="https://twitter.com/bitcmp" class="social-icon-chip">
      <img src="/assets/img/icons/twitter.svg" class="social-icon" />
    </a>
    <a href="https://www.tiktok.com/@bitcamp_umd" class="social-icon-chip">
      <img src="/assets/img/icons/tiktok.svg" class="social-icon tiktok-icon" />
    </a>
  </div>
</template>

<script lang="ts">
export default {
  name: 'SocialIcons',
};
</script>

<style>

.social-icon-container {
  display: flex;
  gap: 1vw;
  z-index: 10;
}

.social-icon-chip {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 3.9vw;
  height: 3.9vw;
  min-width: 44px;
  min-height: 44px;
  border-radius: 18px;
  background-color: rgba(255, 255, 255, 0.1);
  transition: transform 0.3s, background-color 0.3s;
}

.social-icon-chip:hover {
  transform: scale(1.1);
  background-color: rgba(255, 255, 255, 0.18);
}

.social-icon {
  width: 1.9vw;
  min-width: 20px;
  display: inline-block;
  transition: transform 0.3s;
}

.tiktok-icon {
  margin-left: -0.15vw;
}

/* mobile view - icon size */
@media (max-width: 768px) {
  .social-icon-container {
    gap: 3vw;
  }

  .social-icon-chip {
    width: 11vw;
    height: 11vw;
  }

  .social-icon {
    width: 5.5vw;
  }
}
</style>
