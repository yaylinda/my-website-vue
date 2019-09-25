<template>
  <div class="home">

    <div id="item1" class="column">
      <map-wrapper-component v-on:update-card="updateCard"></map-wrapper-component>      
    </div>

    <div id="item2" class="column">
      <card-holder-component :activeCard="activeCard"></card-holder-component>
    </div>

  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import MapWrapperComponent from '@/components/MapWrapperComponent.vue';
import CardHolderComponent from '@/components/CardHolderComponent.vue';

@Component({
  components: {
    MapWrapperComponent,
    CardHolderComponent,
  },
})
export default class Home extends Vue {

  public activeCard: string = 'default';

  public updateCard(markerId: string) {
    console.log(`updateCard to markerId=${markerId}`);
    this.activeCard = markerId;
  }
}
</script>

<style scoped lang="scss">
  #item1 {
    grid-area: item1;
  }

  #item2 {
    grid-area: item2;
  }

  .home {
    display: grid;
    grid-template-areas: 'item1 item2';
  }
</style>
