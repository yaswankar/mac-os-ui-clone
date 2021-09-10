<template>
    <div class="popover" v-click-outside="handleClose">
        <div class="option">About this Mac</div>
        <div class="seperator" style="position: absolute; height: 1px; left: 10px; right: 10px; top: 32px; background-color: rgba(0,0,0, 0.1); margin: 2px 0 0 4px;"></div>
        <div class="option">System Preferences</div>
        <div class="option">App Store</div>
        <div class="seperator" style="position: absolute; height: 1px; left: 10px; right: 10px; top: 95px; background-color: rgba(0,0,0, 0.1); margin: 2px 0 0 4px;"></div>
        <div class="option">Recent Items</div>
        <div class="seperator" style="position: absolute; height: 1px; left: 10px; right: 10px; top: 127px; background-color: rgba(0,0,0, 0.1); margin: 2px 0 0 4px;"></div>
        <div class="option">Force Quit</div>
        <div class="seperator" style="position: absolute; height: 1px; left: 10px; right: 10px; top: 160px; background-color: rgba(0,0,0, 0.1); margin: 2px 0 0 4px;"></div>
        <div class="option">Sleep</div>
        <div class="option">Restart</div>
        <div class="seperator" style="position: absolute; height: 1px; left: 10px; right: 10px; top: 255px; background-color: rgba(0,0,0, 0.1); margin: 2px 0 0 4px;"></div>
        <div class="option">Shut Down</div>
        <div class="option">Lock Screen</div>
    </div>
</template>

<script>
export default {
    name: 'ApplePopover',
    methods: {
        handleClose(e) {
            console.log(e.target.className);
            if(e.target.className !== 'apple-btn' && e.target.className !== 'apple-icon') this.$emit('close-popover');
            return;
        }
    }
}
</script>

<style lang="scss">
.popover {
    position: absolute;
    width: 260px;
    height: auto;
    left: 0;
    top: 25px;
    background: rgba(245, 245, 245, 0.5);
    background-blend-mode: luminosity;
    backdrop-filter: blur(81.5485px);
/* Note: backdrop-filter has minimal browser support */
    border-radius: 6px;
    .option {
        margin: 6px 3px 0 3px;
        font-style: normal;
        font-weight: 500;
        font-size: 13px;
        text-align: left;
        color: #232526;
        box-sizing: border-box;
        height: 26px;
        padding: 3px 10px;
        &:hover {
            background: #017AFF;
            color: #fff;
            box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
            border-radius: 4px;
        }
    }
    .option:first-child {
        margin-top: 5px;
    }
    .option:last-child {
        margin: 6px 3px 3px 3px;
    }
}
</style>