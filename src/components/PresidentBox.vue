<template>
    <div class="car-box">
        <div v-for="president of pDetails" :key="president._id" class="car-item">
            <SPresident :president=president />
        </div>
    </div>
</template>


<script>
import SPresident from './SPresident.vue';

export default {
    name: 'PresidentBox',
    props: {
        pDetails: Array
    },
    components: {
        SPresident
    }

}
</script>
<style scoped>
.car-box {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.car-item {
    margin: 10px;
}
</style>
