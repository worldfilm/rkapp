<template>
<div class="vip">
  <Paytop/>
  <Paypackge/>
  <Payicons/>
</div>
</template>
<script>
import Paytop from '@/components/Paytop.vue';
import Paypackge from '@/components/Paypackge.vue';
import Payicons from '@/components/Payicons.vue';
export default {
  components: {
    Paytop,Paypackge,Payicons
  }
}
</script>

<style lang="scss" scoped>
.vip {
    overflow: hidden;
}
</style>
