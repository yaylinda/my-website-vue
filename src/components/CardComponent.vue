<template>
    <div class="card" v-show="activeCard === cardId">
        <div class="title">{{title}}</div>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class CardComponent extends Vue {
    @Prop() private activeCard!: string;
    @Prop() private cardId!: string;
    @Prop() private title!: string;
}
</script>

<style scoped lang="scss">

</style>