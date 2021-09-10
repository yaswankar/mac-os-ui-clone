<template>
  <div class="icons-bar">
      <img class="icons" :src="require('@/assets/IconBar/Finder.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/Chrome.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/AppStore.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/Messages.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/Maps.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/Contacts.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/Mail.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/Podcasts.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/SystemPreferences.png')" alt="">
      <img class="icons" :src="require('@/assets/IconBar/Bin.png')" alt="">
  </div>
</template>

<script>
export default {
    name: 'IconBar'
}
</script>

<style lang="scss" scoped>
.icons-bar {
    position: absolute;
    padding: 5px;
    display: flex;
    width: 690px;
    height: 72px;
    left: calc(50% - 690px/2);
    bottom: 10px;
    box-shadow: 0px 4px 4px 0px #00000040;
    background: rgba(245, 245, 245, 0.15);
    background-blend-mode: luminosity;
    /* #03 Blur/Background #03 */
    backdrop-filter: blur(81.5485px);
    /* Note: backdrop-filter has minimal browser support */
    border-radius: 20px;
    .icons {
        height: 60px;
        margin-left: 8px;
    }


}
</style>