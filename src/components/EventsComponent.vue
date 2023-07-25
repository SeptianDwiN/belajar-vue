<template>
    <div>
      <h1>Aplikasi Vue.js Gue</h1>
      <my-component
        :nama="nama"
        :umur="umur"
        @greeted="onGreeted"
      ></my-component>
      <slot name="footer"></slot>
    </div>
  </template>
  
  <script>
  export default {
    props: ['nama', 'umur'],
    data() {
      return {
        pesan: 'Halo, ' + this.nama + '!'
      };
    },
    methods: {
      greet() {
        console.log('Halo, bro!');
        this.$emit('greeted');
      }
    },
    computed: {
      pesanSelamat() {
        return 'Selamat datang, ' + this.nama + '!';
      }
    },
    watch: {
      umur(newUmur, oldUmur) {
        console.log('Umur berubah dari', oldUmur, 'menjadi', newUmur);
        
      }
    }
  }
  </script>