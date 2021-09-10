<template>
    <div class="icons-bar">
        <img class="icons" :src="require('@/assets/IconBar/Finder.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/Chrome.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/AppStore.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/Messages.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/Maps.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/Contacts.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/Mail.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/Podcasts.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/SystemPreferences.png')" @click="openProgram">
        <img class="icons" :src="require('@/assets/IconBar/Bin.png')" @click="openProgram">
    </div>
</template>

<script>
export default {
    name: 'IconBar',
    methods: {
        openProgram(e) {
            e.target.classList.add('icon-bounce');
            setTimeout(() => {
                e.target.classList.remove('icon-bounce');
            }, 3000);
        }
    }
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
    .icon-bounce {
        animation: bounce 0.5s;
        animation-direction: alternate;
        animation-timing-function: cubic-bezier(.5, 0.05, 1, .5);
        animation-iteration-count: infinite;
    }
    @keyframes bounce {
        from {
            transform: translate3d(0, -15px, 0);
        }
        to {
            transform: translate3d(0, 10px, 0);
        }
    }
    @-webkit-keyframes bounce {
        from {
            -webkit-transform: translate3d(0, -15px, 0);
            transform: translate3d(0, -10px, 0);
        }
        to {
            -webkit-transform: translate3d(0, 15px, 0);
            transform: translate3d(0, 10px, 0);
        }
    }


}
</style>