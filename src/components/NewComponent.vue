<template>
 
  <my-component nama ="sptn" umur="40"></my-component>
  <latihan-component name="septian" age="21"></latihan-component>
  <latihan-dua-component></latihan-dua-component>
  <WatchersComponent nama="aasu" umur="19"></WatchersComponent>
  <EventsComponent :nama="nama" :umur="umur" @greeted="onGreeted">
  <template #footer>
    <div>
      <p>Ini adalah footer latihan</p>
    </div>
  </template>
  </EventsComponent>


  
</template>

<script setup>

import MyComponent from './MyComponent.vue';
import LatihanComponent from './LatihanComponent.vue';
import LatihanDuaComponent from './LatihanDuaComponent.vue';
import WatchersComponent from './WatchersComponent.vue';
import EventsComponent from './EventsComponent.vue'

//event
import { ref } from 'vue';
const nama = ref('john');
const umur = ref(25);

const onGreeted = () => {
  console.log('Kamu Udah Di Sapa,Bro!')
}


</script>