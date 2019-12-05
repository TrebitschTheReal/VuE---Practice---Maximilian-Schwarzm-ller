<template>
   <div class="hello">
      <div class="row">
         <p class="col">Componenet moo</p>
         <button class="m-2 col btn btn-primary" @click="modifyValue">Send</button>
      </div>
      <h3 class="text-center">{{ message }}</h3>
   </div>
</template>

<script>
    export default {
        props: {
            message: String
        },
        methods: {
            modifyValue: function () {
                this.message = "Modified by moo";
                this.$emit('dataIsChanged', this.message)
            }
        }
    }
</script>
