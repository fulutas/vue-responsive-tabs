<template>

  <div v-if="isSelected">
      <div class="mt-3">
          
      <slot></slot>

      </div>
  </div>
  
</template>

<script>
export default {
    props : {

        isSelected : {
            type : Boolean
        }
        
    }
}
</script>

<style scoped>

</style>