<template>
  <div id="main_layout" :class="$mq">
    <div id="main_header_container">
      <MainHeader :isWhiteBG="isWhiteBG" />
    </div>

    <div id="main_content">
      <slot></slot>
    </div>

    <div id="main_footer_container">
      <MainFooter />
    </div>
  </div>
</template>

<script>
import MainHeader from './MainHeader'
import MainFooter from './MainFooter'

export default {
  name: 'MainLayout',
  components: {
    MainHeader,
    MainFooter
  },

  props : {
    section : {
      type : String,
      required : true
    },
    isWhiteBG: Boolean
  }
}
</script>

<style scoped>
#main_layout{
  position: relative;
  min-height: 100%;
}

#main_content{
  position: relative;
}

#main_header_container{
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 100;
}

#main_footer_container{
  width: 100%;
  position: relative;
}
</style>
