<template>
    <div class="main-outlet-wrapper" >
        <div class="main-outlet app-font">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CloneBody'
}
</script>
<style scoped>

.main-outlet-wrapper {
    box-sizing: border-box;
    width: 100%;
    display: grid;
    grid-template-areas: "content";
    grid-template-columns: minmax(0, 1fr);
    gap: 0;
}

.background {
  background-color:rgba(22,22,22,0.9);
  background-image: url(@/assets/freeletics_08.jpg);  
  background-repeat: repeat-x repeat-y;
  opacity: 0.9;
  position: absolute;
  z-index: -1000;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;   
  height: 100%;
}

.main-outlet {
    max-width: calc(100% - 16px);
    width: 1110px;
    flex: 1;
    box-sizing: border-box;
    padding-left: 16px;
    padding-right: 16px;
    margin: 32px auto;
    border-radius: 4px;
    color: white;
}

</style>