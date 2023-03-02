<template>
 <div>
    <navbar/>
    <Nuxt/>
<hfooter/>
</div>
</template>

<script>
import navbar from '~/components/sections/navbar.vue'
import hfooter from '~/components/sections/hfooter.vue';
export default {
    name: 'default',
components: {
    navbar, 
    hfooter
}
}
</script> 