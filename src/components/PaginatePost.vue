<template>
  <div class="btn-group" role="group" aria-label="Basic example">
     <button 
          @click="$emit('prev')"
            type="button" 
            class="btn btn-outline-primary"
            :disabled="inicio <= 0"
            > Previus
            {{inicio}}
            </button>  
            
      <button 
          @click="$emit('next')"
             type="button" 
            class="btn btn-outline-primary"
            :disabled="fin >= maxlength" 
            >Next 
            {{fin}}
             </button>
  </div>
</template>

<script setup>
// const emit = defineEmits(['next' , 'prev'])
defineProps(["inicio","fin" , "maxlength"]);
</script>
