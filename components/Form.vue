<template>
    <form>
        <div class="top">
            <p class="weight-5 mb-1">Create Brief</p>
        </div>

        <div class="container mt-2">
            <div class="content">
                <p>Type</p>
                <select name="" id="">
                    <option value="">Logo</option>
                </select>
            </div>

            <div class="content">
                <p>Industry</p>
                <select name="" id="">
                    <option value="">Technology</option>
                </select>
            </div>
        </div>

        <div class="prompt mt-2">
            <textarea name="" id="" placeholder="Result should be focused on making logo better to improve customer retention"></textarea>
        </div>
    </form>
</template>

<script>
export default {

}
</script>

<style scoped>
form {
    background-color: #FAFAFA1A;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    padding: 32px;
    border-radius: 8px;

    @media (width < 700px) {
        padding: 16px;
    }
}

form .top {
    display: flex;
    flex-direction: column;
    gap: 8px;
    border-bottom: .5px solid #ffffff7f;
}

form .container {
    display: flex;
    align-items: center;
    gap: 24px;
    align-items: stretch;
    width: 100%;
}

form .container .content {
    display: flex;
    flex-direction: column;
    gap: 12px;
    align-items: stretch;
    width: 100%;
}

form .container .content select {
    display: flex;
    padding: 8px;
    background: url(@/assets/icons/dropdown_arrow.svg) 95% center no-repeat #ffffff5c !important;
    border-radius: 4px;
    color: #FFFFFF;
    font-size: 16px;
    font-weight: 500;
    width: 100%;
    -webkit-appearance: none;
    outline: none;
}   

form .prompt {
    display: flex;
    flex-direction: column;
    gap: 12px;
    align-items: stretch;
    height: 100%;
}

form .prompt textarea {
    background-color: #ffffff5c ;    
    color: #FFFFFF;
    height: 100%;
    padding: 10px;
    font-size: 16px;
    font-weight: 500;
    border-radius: 4px;
    outline: 0px;
}
</style>