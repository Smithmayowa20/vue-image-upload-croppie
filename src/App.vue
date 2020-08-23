<template>
  <div id="app" style="text-align: center">
    <img :src="defaultImage" style="width: 100px;height: 100px">
    <VueImageUploadCroppiee :defaultImage.sync="defaultImage" :height="100" :width="100" :circle="true" :trans="trans"></VueImageUploadCroppie>
  </div>
</template>

<script>
import VueImageUploadCroppiee from './components/VueImageUploadCroppiee'
export default {
  name: 'app',
  data() {
  	return {
  		'defaultImage': '',
      'trans': { 
          'cropImage': '裁剪图片', 
          'chooseImage':'选择图片', 
          'confirmCutting': '确认裁剪'
      }
  	}
  },
  watch: {
      'defaultImage': function(value) {
          if (value) {
            // do whatever you want with image value,(upload ..)
          }
      }
  },
  components: {
    VueImageUploadCroppiee
  }
}
</script>
