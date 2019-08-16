<template>
    <div class="col-lg-6 col-m-6">
    <div class="quote">
        <slot></slot>
    </div>
        </div>
</template>

<script>

</script>

<style scoped>
.quote {
    font-family: 'Roboto', sans-serif;
    border: 4px solid blueviolet;
    padding: 30px;
    margin: 20px;
    color: #555;
    font-size: 20px;
    text-align: center;
    transition: 0.3s
}

.quote:hover {
 border: 4px solid red;  
 cursor: pointer
}
</style>