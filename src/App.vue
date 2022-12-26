<template>
  <div class="app">
    <HeaderComponent />

    <HomeView />

    <FooterComponent />
  </div>
</template>

<script>
import './assets/css/global.css';
import HeaderComponent from './components/HeaderComponent';
import HomeView from './views/HomeView';
import FooterComponent from './components/FooterComponent';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    HomeView,
    FooterComponent
  }
}
</script>

<style>
</style>