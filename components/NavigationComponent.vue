<template>
    <nav>
        <span class="logo">
            <img src="@/assets/icons/menu.svg" alt="">
            <p class="font-size-24 weight-5">Generate Brief</p>
        </span>

        <p class="weight-5">About <br>Hackday Build</p>
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
}

nav .logo {
    display: flex;
    align-items: center;
    gap: 32px;
}
</style>