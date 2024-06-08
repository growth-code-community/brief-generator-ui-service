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
    components: {
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
    align-items: center;
    margin: 150px 120px 0px;
    padding: 0px;

    @media (width < 700px) {
        margin: 90px 20px;
    }
}

.container {
    display: grid;
    grid-template-columns: 2fr 3fr;
    /* Replace percentages with fr units */
    gap: 20px;
    margin-bottom: 50px;
    width: inherit;

    @media (width < 1000px) {
        grid-template-columns: 1fr;
    }
}
</style>