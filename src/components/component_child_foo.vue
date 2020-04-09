<template>
   <div>
      <div class="row">
         <p class="col">Componenet child: foo</p>
         <button class="col m-2 btn btn-primary"
                 @click="modifyValueInFoo()">Send</button>
      </div>
      <h3 class="text-center">{{ randomVariableName }}</h3>
   </div>
</template>

<script>
    export default {
        props: {
           randomVariableName: String
        },
        methods: {
            modifyValueInFoo: function () {
                this.randomVariableName = 'Modified by foo';
                this.$emit('dataIsChangedInFoo', this.randomVariableName)
            }
        }
    }
</script>
