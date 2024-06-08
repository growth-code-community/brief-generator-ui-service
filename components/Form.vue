<template>
    <form>
        <div class="top">
            <p class="weight-5 mb-1">Create Brief</p>
            <hr>
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
}

form .top {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

form .top hr {
    border: .5px solid #FFFFFF;
}

form .container {
    display: flex;
    align-items: center;
    gap: 24px;
}

form .container .content {
    display: flex;
    flex-direction: column;
    gap: 12px;
}

form .container .content select {
    display: flex;
    padding: 8px;
    background: url(@/assets/icons/dropdown_arrow.svg) 97% center no-repeat #ffffff5c !important;
    border-radius: 4px;
    color: #FFFFFF;
    font-weight: 500;
    width: 200px;
    -webkit-appearance: none;
}   

form .prompt {
    display: flex;
    flex-direction: column;
    gap: 12px;
    align-items: stretch;
}

form .prompt textarea {
    background-color: #ffffff5c ;    
    color: #FFFFFF;
    height: 50px;
    font-size: 16px;
    font-weight: 500;
}
</style>