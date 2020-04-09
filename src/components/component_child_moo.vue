<template>
   <div>
      <div class="row">
         <p class="col">Componenet child: moo</p>
         <button class="m-2 col btn btn-primary"
                 @click="modifyValueInMoo()">Send</button>
      </div>
      <h3 class="text-center">{{ anotherRandomVariableName }}</h3>
   </div>
</template>

<script>
    export default {
        props: {
           anotherRandomVariableName: String
        },
        methods: {
            modifyValueInMoo: function () {
                this.anotherRandomVariableName = "Modified by moo";
                this.$emit('dataIsChangedInMoo', this.anotherRandomVariableName)
            }
        }
    }
</script>
