<template>
    <div class="card-holder">
        <card-component title="Select a POI"></card-component>
        <card-component title="Background"></card-component>
        <card-component title="Education"></card-component>
        <card-component title="Internships"></card-component>
        <card-component title="At Capital One (Part I)"></card-component>
        <card-component title="At Capital One (Part II)"></card-component>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import CardComponent from '@/components/CardComponent.vue';

@Component({
  components: {
    CardComponent,
  },
})
export default class CardHolderComponent extends Vue {

}
</script>

<style scoped lang="scss">

    .card-holder {
      
    }

</style>