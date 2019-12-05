<template>
   <div>
      <div class="row">
         <p class="col">Componenet child: moo</p>
         <button class="m-2 col btn btn-primary"
                 @click="modifyValueInMoo()">Send</button>
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
            modifyValueInMoo: function () {
                this.message = "Modified by moo";
                this.$emit('dataIsChangedInMoo', this.message)
            }
        }
    }
</script>
