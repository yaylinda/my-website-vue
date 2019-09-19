<template>
  <div class="map">
    <div class="background-wrapper">
      <div class="points">Visited:</div>
      <img class="background" src="../assets/background.png" />
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
export default class MapComponent extends Vue {
  public goToMarker(x: number, y: number) {
    console.log(`goToMarker: x=${y}, y=${y}`);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
