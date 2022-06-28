<template>
    <div class="upload-container center">
        <img src="@/assets/Freeletics_Logotype_RGB_White.png" class="image-fluid center"/>
        
        <div class="center">Upload your profile data here:</div>
        <button class="btn btn-info" @click="onPickFile">Select your data....</button>
        <input
        type="file"
        style="display: none"
        ref="fileInput"
        @change="onFilePicked"/>
        <div class="footer-note">In order to get your profile data, send an email to support@freeletics.com</div>
    </div>
</template>

<script>
//import {ref} from 'vue'
export default {
    name: 'HomeView',
    data() {
        return {image: null}
    },
    methods: {
        onPickFile() {
            this.$refs.fileInput.click();
        },
        onFilePicked(event) {
            console.log(event);
            const files = event.target.files
            let filename = files[0].name
            const fileReader = new FileReader()
            fileReader.addEventListener('load', () => {
            this.file = fileReader.result;
            console.log(filename);
  })
        }
    }
}
</script>

<style scoped>

.image-fluid {
  height: 250px;
  margin-top: 50px;
  margin-bottom: 50px;
}
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}
.footer-note{
  margin-top: 30px;
  font-size: 12px;
  text-align: center;
}
</style>