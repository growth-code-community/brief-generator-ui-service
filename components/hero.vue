<template>
    <div class="hero">
        <Banner />
        <div class="container mt-3">
            <Form />
            <Brief />
        </div>
    </div>
</template>

<script>
import Banner from './Banner'
import Form from './Form'
import Brief from './Brief.vue';

export default {
    components:{
        Banner,
        Form,
        Brief
    }
}
</script>

<style scoped>
.hero {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    margin: 150px 250px 0px;
}

.container {
    display: flex;
    justify-content: space-between;
    gap: 30px;
    margin-bottom: 50px
}

</style>