<template>
    <div id="header">
        <h4 class="tabTitle"><b> {{ tabTitle }} </b></h4>

        <a><img src="../assets/clean.png" id="shine-button"></a>
    </div>
</template>

<script>
export default {
    name: 'Header',
    props: {
        tabTitle: String
    }
}
</script>

<style scoped>

#shine-button {
    width: 40px;
    height: 40px;
}

#header {
    margin: auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border: 1px solid black;
}

h4, a {
    margin-left: 10%;
    margin-right: 10%;
}
</style>