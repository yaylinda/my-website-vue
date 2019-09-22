<template>
  <div class="map-wrapper">
    <div class="background">
      <div class="points">Visited:</div>
      <marker-component></marker-component>
      <person-component></person-component>
    </div>
    
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import MarkerComponent from '@/components/MarkerComponent.vue';
import PersonComponent from '@/components/PersonComponent.vue';


@Component({
  components: {
    MarkerComponent,
    PersonComponent,
  },
})
export default class MapWrapperComponent extends Vue {
  public goToMarker(x: number, y: number) {
    console.log(`goToMarker: x=${y}, y=${y}`);
  }
}
</script>

<style scoped lang="scss">

  .points {
    position: absolute;
  }

  .background {
    position: relative;
    background-image: url("../assets/background.png");
    height: 335px;
    width: 562px;
  }

</style>
