<template>
    <div class="card">
        <div class="title">{{title}}</div>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class CardComponent extends Vue {
    @Prop() private title!: string;
}
</script>

<style scoped lang="scss">

</style>