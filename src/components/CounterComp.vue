<template>
    <div>
        <p class="timer">{{time}} Second</p>
    </div>
</template>
<script>
export default{
    props:{
        time:Number
    }
}
</script>
<style>
.timer{
    font-size: 12px;
    font-weight: bold;
}
</style>