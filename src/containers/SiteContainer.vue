<template>
  <div class="c-app">
    
    <router-view :key="$route.path"></router-view>
            
  </div>
</template>

<script>

export default {
    name: 'SiteContainer',
    data(){
        return {};
    }
}

</script>

<style scoped>

</style>
