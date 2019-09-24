<template>
  <div class="map-wrapper">
    <div class="background">
      <div class="points">Visited:</div>
      <marker-component markerId="childhood" position="top: 203px; left: 137px;" v-on:marker-click="goToMarker"></marker-component>
      <marker-component markerId="education" position="top: 145px; left: 233px;" v-on:marker-click="goToMarker"></marker-component>
      <marker-component markerId="internships" position="top: 187px; left: 353px;" v-on:marker-click="goToMarker"></marker-component>
      <marker-component markerId="capitalone" position="top: 161px; left: 433px;" v-on:marker-click="goToMarker"></marker-component>
      <person-component :position="personPosition"></person-component>
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

  personPosition: string = 'top: 280px; left: 93px';

  goToMarker(position: string) {
    console.log(`clicked on marker with position=${position}`);
    this.personPosition = position;
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
