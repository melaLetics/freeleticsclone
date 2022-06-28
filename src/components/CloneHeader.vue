<template>
    <div class="d-header-wrapper">
        <div class="d-header">
            <img src="@/assets/Freeletics_Logotype_RGB_White.png" class="image-fluid" />
            <div class="app-font headline"> 
                | Freeletics Clone 
            </div>   
        </div>
    </div>
</template>

<script>
export default {
    name: 'CloneHeader'
}
</script>

<style scoped>
.d-header-wrapper{
    width: 100%;
    z-index: 1000;
    background-color: #161616;
    box-shadow: 0 2px 4px -1px rgb(0 0 0 / 25%);
    backface-visibility: hidden;
    box-sizing: border-box;
    display: grid;
    grid-template-areas: "content";
    grid-template-columns: minmax(0, 1fr);
    gap: 0;
}
.d-header {
    max-width: calc(100% - 16px);
    width: 1110px;
    flex:1;
    box-sizing: border-box;
    background: rgba(22,22,22,0.9);
    margin: auto;
    border-radius: 4px;
    color: white;
}
.headline {
    margin: 5px;
}
.image-fluid {
    height: 50px;
    float: left;
    margin: 5px;
}
</style>