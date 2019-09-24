<template>
    <div class="card-holder">
        <card-component :activeCard="activeCard" cardId="default" title="Select a POI"></card-component>
        <card-component :activeCard="activeCard" cardId="childhood" title="Childhood"></card-component>
        <card-component :activeCard="activeCard" cardId="education" title="Education"></card-component>
        <card-component :activeCard="activeCard" cardId="internships" title="Internships"></card-component>
        <card-component :activeCard="activeCard" cardId="capitalone" title="At Capital One"></card-component>
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
  @Prop() public activeCard!: string;
}
</script>

<style scoped lang="scss">

    .card-holder {
      
    }

</style>