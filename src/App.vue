<template>
<transition name="modal">
<div class="wrapper">
<div class="wrapper-content">
<section>

<div class="container">

<button class="btn btnPrimary" @click="modalFirst = !modalFirst">Show first modal</button>

  <modals title="First modal" v-show="modalFirst" @close="modalFirst = !modalFirst">
  <div slot="body">
<p>Text Text</p>
<button class="btn btnPrimary" @click="modalFirst = !modalFirst">Well done</button>
</div>
  </modals>
</div>
</section>

</div>
</div>
</transition>
</template>





<script>
import modals from'@/components/Modal.vue'
export default{
components:{
  modals
},
data(){
  return{
   modalFirst:false
  }
}
}
</script>
