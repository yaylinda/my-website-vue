<template>
  <div class="home">
    <div class="column">
      <map-component></map-component>      
    </div>
    <div class="column">
      <card-holder-component></card-holder-component>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import MapComponent from '@/components/MapComponent.vue';
import CardHolderComponent from '@/components/CardHolderComponent.vue';

@Component({
  components: {
    MapComponent,
    CardHolderComponent,
  },
})
export default class Home extends Vue {

}
</script>

<style scoped lang="scss">
  .home {
    display: flex;
  }
  .column {
    flex: 50%;
  }
</style>
