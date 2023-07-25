<template>
    <div>

        <!--Props-->
        <h2>Nama :{{ nama }}</h2>
        <p>Umur :{{ umur }}</p>
    </div>
</template>

<script>

    export default {
        name: "MyComponent",
        props:['nama','umur'],

    }
</script>

<style>
h1{
    color: blue;
}

p{
    size: 16px;
}
</style>