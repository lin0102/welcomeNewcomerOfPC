<template>
    <div class="bar">
        <div class="side-bar">
            <div
                :class="['button', {active: currentComponent===list}]"
                v-for="list of barList"
                :key="list.title"
                @click="currentComponent=list">{{ list.title }}</div>
        </div>
        <transition enter-active-class="animated fadeIn faster" leave-active-class="animated fadeOut faster" mode="out-in">
            <component :is="currentComponent.component"></component>
        </transition>
    </div>
</template>

<script>
export default {
    props: {
        barList: {
            type: Array
        }
    },
    data() {
        return {
            currentComponent: this.barList[0]
        }
    }
}
</script>

<style lang="less" scoped>
    .bar {
        width: 100%;
        height: 100%;
        display: flex;
    }
    .side-bar {
        width: 120px;
        height: 100%;
        display: flex;
        flex-flow: column;
    }
    .button {
        min-width: 100%;
        flex: 1;
        background: #baefff;
        margin: -4.5px;
        border: solid 4.5px #432a92;
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
        cursor: pointer;
        color: #432a92;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 15px;
        font-weight: 600;
        letter-spacing: 2px;
        transition: all .5s;
        &:last-child {
            border-bottom: solid 1px #432a92;
        }
    }
    .active {
        background: #fff5a7;
        min-width: 120%;
        margin: 0 0 0 -4px;
    }
</style>
