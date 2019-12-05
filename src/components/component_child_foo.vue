<template>
   <div>
      <div class="row">
         <p class="col">Componenet child: foo</p>
         <button class="col m-2 btn btn-primary"
                 @click="modifyValueInFoo()">Send</button>
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
            modifyValueInFoo: function () {
                this.message = 'Modified by foo';
                this.$emit('dataIsChangedInFoo', this.message)
            }
        }
    }
</script>
