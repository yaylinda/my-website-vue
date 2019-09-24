<template>
    <div class="marker" :style="position" v-on:click="$emit('marker-click', position)">
        <img class="gray" src="../assets/circle-icon.svg" />
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class MarkerComponent extends Vue {
    @Prop() markerId!: string;
    @Prop() position!: string;
}
</script>

<style scoped lang="scss">

    .marker {
        height: 24px;
        width: 24px;
        z-index: 100;
        position: absolute;
    }

    .marker :hover {
        cursor: pointer;
    }

</style>