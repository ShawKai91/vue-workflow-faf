<template>
  <div>
    <h1>DevWorkflow</h1>
     <p>{{ subtitle }}</p>
    <p>{{ marketingMessage }}</p>
    <!-- <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas error sequi pariatur adipisci nisi enim excepturi consequuntur, vitae ipsum porro!</p> -->
  </div>
</template> 

<script>
export default {
  name: "HomepageContent",
  props: {
    subtitle: String,
    marketingMessage: String
  }
}
</script> 