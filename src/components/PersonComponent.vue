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
        height: 24px;
        width: 24px;
    }

</style>