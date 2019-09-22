<template>
    <div class="person">
        <img src="../assets/pikachu-female.gif" />
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class PersonComponent extends Vue {

}
</script>

<style scoped lang="scss">

    .person {
        position: absolute;
        z-index: 10;
        background-size: contain;
    }

</style>