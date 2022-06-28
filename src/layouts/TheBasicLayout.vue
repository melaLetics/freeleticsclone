<template>
    <div class="background">
        <clone-header></clone-header>
        <clone-body>
            <template v-slot>
                <slot></slot>
            </template>
        </clone-body>
    </div>
</template>

<script>

import CloneHeader from '@/components/CloneHeader.vue';
import CloneBody from '@/components/CloneBody.vue';

export default {
    name: 'TheBasicLayout',
    components: {
        CloneHeader,CloneBody
    },
}
</script>

<style scoped>
.background {
  background-color:rgba(22,22,22,0.9);
  background-image: url(@/assets/freeletics_08.jpg);  
  background-size: cover;
  opacity: 0.9;
  position: absolute;
  z-index: -1000;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;   
  height: 100%;
}
</style>