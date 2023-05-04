<template>
    <div class="president-box">
        <div v-for="president of pDetails" :key="president._id" class="president-item">
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
.president-box {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.president-item {
    margin: 10px;
}
</style>
