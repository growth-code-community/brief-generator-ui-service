<template>
    <nav>
        <span class="logo">
            <img src="@/assets/icons/menu.svg" alt="">
            <p class="font-size-24 weight-5">Generate Brief</p>
        </span>

        <p class="weight-5 about">About <br>Hackday Build</p>
    </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
nav {
    position: fixed;
    top: 0px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 28px 40px;
    width: 100%;
    background-color: #121212;

    @media (width < 700px) {
        padding: 16px 20px;
    }
}

nav .logo {
    display: flex;
    align-items: center;
    gap: 32px;

    @media (width < 700px) {
        gap: 10px;
    }
}

nav .logo p {
    @media (width < 700px) {
        font-size: 18px !important;
    }
}

nav .logo img {
   @media (width < 700px) {
        width: 25px;
   } 
}

nav .about {
    @media (width < 700px) {
        font-size: 14px;
    }
}
</style>