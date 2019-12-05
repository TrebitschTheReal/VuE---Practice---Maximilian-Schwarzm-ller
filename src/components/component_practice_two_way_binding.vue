<template>
   <div class="p-2">
      <p>component practice - use two way binding</p>
      <!-- 5) Pre-Populate this input with your name (set the "value" attribute) -->
      <div class="row">
         <input class="col m-1" type="text" v-model="text" placeholder="Type here"/>
         <input disabled class="col m-1" type="text" :value="text"/>
      </div>
      <div class="row">
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
         <textarea disabled class="col m-1" name="" cols="10" rows="5" v-model="text"></textarea>
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