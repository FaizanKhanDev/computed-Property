<template>
  <div>
    <div style="border: 1px solid #fff;">
      <NuxtTutorial />
    </div>
    <br />
    <br />
    <br />

    <div style="border: 1px solid #fff;">
      <ForLoop />

    </div>
    
  </div>

</template>

<script>
import NuxtTutorial from '@/components/Tutorial';
import ForLoop from '@/components/ForLoop'

export default {
  name: 'IndexPage',
  components:{
    NuxtTutorial,
    ForLoop,
  } 
}
</script>
