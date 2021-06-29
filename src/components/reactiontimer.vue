<template>
    <div>
        <h1 class="dec">{{score}} ms</h1>
    </div>
</template>
<script>
export default {
    name:'reactiontimer',
    props:['score']
}
</script>
<style scoped>
.dec{
    color: red;
    text-align: center;
}
</style>