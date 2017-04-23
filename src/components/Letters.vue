<template>
<div>
    <div class="letters" v-for="letter in alphabet">
        <div>{{ letter }}</div>
    </div>
</div>
</template>

<script>
export default {
    data () {
        const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
        return {
            alphabet
        };
    }
}
</script>

<style>
.letters {
    float: left;
    height: 100px;
    width: 30%;
    background-color: #dddddd;
    margin: 1.5%;
}

.letters div {
    line-height: 100px;
    text-align: center;
    font-size: 40px;
}
</style>
