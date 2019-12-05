<template>
   <div class="hello">
      <div class="row">
         <p class="col">Componenet foo</p>
         <button class="col m-2 btn btn-primary"
                 @click="modifyValue">Send
         </button>
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
                this.message = 'Modified by foo';
                this.$emit('dataIsChanged', this.message)
            }
        }
    }
</script>
