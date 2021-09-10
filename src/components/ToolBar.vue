<template>
    <div class="toolbar">
        <button class="apple-btn"  @click="$emit('trigger-popover', 'ApplePopover')"><img class="apple-icon" :src="require('@/assets/apple.png')" /></button>
        <button class="toolbar__options">Finder</button>
        <button class="toolbar__options">File</button>
        <button class="toolbar__options">Edit</button>
        <button class="toolbar__options">View</button>
        <button class="toolbar__options">Go</button>
        <button class="toolbar__options">Window</button>
        <button class="toolbar__options">Help</button>
    </div>
</template>

<script>
export default {
    name: 'ToolBar',
}
</script>

<style lang="scss" scoped>
.toolbar {
    display: flex;
    position: absolute;
    background-color: rgba(0,0,0, 0.1);
    height: 24px;
    left: 0px;
    right: 0px;
    top: 0px;
    &__options {
        margin-left: 5px;
        padding: 3px 10px;
        font-size: 14px;
        font-weight: 600;
        text-align: center;
        background-color: rgba(0,0,0, 0);
        outline: none;
        border: none;
        color: #fff;
        &:focus {
        background-color: rgba(0,0,0, 0.1);
        border-color: transparent;
        border-radius: 4px;
        }
    }
    .apple-icon {
        height: 18px;
    }
    .apple-btn {
        margin-left: 20px;
        padding-top: 2px;
        text-align: center;
        background-color: rgba(0,0,0, 0);
        outline: none;
        border: none;
        color: #fff;
    }
    .apple-btn:focus {
        background-color: rgba(0,0,0, 0.1);
        border-color: transparent;
        border-radius: 4px;
    }
}
</style>