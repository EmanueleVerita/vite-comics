<script>
import HeaderComponent from './components/HeaderComponent.Vue';
import MainComponent from './components/MainComponent.Vue';
import FooterComponent from './components/FooterComponent.Vue';


export default {
  name: 'App',
  components:{
    HeaderComponent,
    MainComponent,
    FooterComponent
  },
  data() {
    return {
     
    }
  }
  
}
</script>

<template>

<div>
  <HeaderComponent></HeaderComponent>
  <MainComponent></MainComponent>
  <FooterComponent></FooterComponent>
</div>

</template>

<style lang="scss">
 
</style>
