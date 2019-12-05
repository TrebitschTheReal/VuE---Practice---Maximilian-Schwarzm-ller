<template>
   <div class="p-2">
      <p>component practice - use two way binding</p>
      <!-- 5) Pre-Populate this input with your name (set the "value" attribute) -->
      <div class="row">
         <input class="col mx-1" type="text" v-model="text"/>
         <input disabled class="col mx-1" type="text" :value="text"/>
      </div>
   </div>
</template>

<script>
    export default {
        data: function () {
            return {
                text: ''
            }
        },
    }
</script>