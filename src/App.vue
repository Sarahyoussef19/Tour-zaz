
<script>
import Menu from './components/Menu.vue';
import Carousel from './components/Carousel.vue'
import { useMessage, NMessageProvider } from 'naive-ui'
import { defineComponent } from 'vue'
import SignupFormVue from './components/SignupForm.vue';
import AlbumCollection from './components/AlbumCollection.vue'
import myvideo from './components/Video.vue'
import DownloadJsonVue from './components/DownloadJson.vue';
import { darkTheme } from 'naive-ui'
import { NConfigProvider } from 'naive-ui'


import { NThemeEditor } from 'naive-ui'


export default defineComponent({
  setup() {
    return {

    }
  },
  components: {
    Menu, Carousel, NMessageProvider, SignupFormVue, AlbumCollection, myvideo, DownloadJsonVue, NThemeEditor, darkTheme, NConfigProvider
  }
})
const themeOverrides = {
  "Timeline": {
    "titleFontSizeMedium": "12px",
    "iconSizeMedium": "10px",
    "titleMarginMedium": "-10px"
  }
}







</script>

<template>
  <n-config-provider :theme="darkTheme">
    <n-theme-editor>
      <n-message-provider>
        <DownloadJsonVue></DownloadJsonVue>
        <Menu></Menu>
        <Carousel></Carousel>
        <signup-form-vue></signup-form-vue>
        <myvideo></myvideo>
        <AlbumCollection></AlbumCollection>

      </n-message-provider>
    </n-theme-editor>
  </n-config-provider>
</template>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: white;

  color: #2c3e50;
  margin-top: 30px;
}
</style>
