<template>
   <div class="p-2">
      <p>component exercise one - use v-model in input with a constant text variable</p>
      <!-- 5) Pre-Populate this input with your name (set the "value" attribute) -->
      <div>
         <input type="text" v-model="text" @keypress="blockInputWithConstantlyRefreshableText">
      </div>
   </div>
</template>

<script>
   export default {
       data: function () {
           return {
               text: 'Constant text'
           }
       },
       methods: {
         blockInputWithConstantlyRefreshableText: function () {
             this.text = 'Constant text';
         }
       }
   }
</script>