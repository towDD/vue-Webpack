<template>
	<div class="main">
        <router-view
          keep-alive
          transition="fade"
          transition-mode='out-in'></router-view>
  </div>
</template>
<script>
import store from './vuex/store.js';

(function () {
    document.addEventListener('DOMContentLoaded', function () {
        var html = document.documentElement;
        var windowWidth = html.clientWidth;
        html.style.fontSize = windowWidth / 7.2 + 'px';
        // 等价于html.style.fontSize = windowWidth / 640 * 100 + 'px';
    }, false);
})();

export default {
  store:store
}


require("./st/css/app.scss");
</script>


<style lang="sass">


</style>
