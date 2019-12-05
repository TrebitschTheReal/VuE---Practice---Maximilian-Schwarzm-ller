<template>
   <div id="app">
      <div class="p-2 m-2 border border-secondary bg-secondary text-light">
         <p>Main component</p>
         <div class="text-center">
            <img alt="Vue logo" src="./assets/logo.png">
         </div>
         <div class="p-2 m-2">
            <button class="btn btn-dark btn-block"
                    @click="setToDefault">Set to default
            </button>
         </div>
         <div class="p-5 row">
            <component_foo class="bg-warning text-dark m-2 p-3 col"
                           :message="message"
                           @dataIsChangedInFoo="message = $event"/>
            <component_moo class="bg-success m-2 p-3 col"
                           :message="message"
                           @dataIsChangedInMoo="message = $event"></component_moo>
         </div>
         <div class="p-5">
            <component_practice_1 class="m-2 p-3 bg-primary"></component_practice_1>
         </div>
         <div class="p-5">
            <component_practice_2 class="m-2 p-3 bg-dark"></component_practice_2>
         </div>
      </div>
   </div>
</template>

<script>
    import component_foo from './components/component_child_foo.vue'
    import component_moo from './components/component_child_moo.vue'
    import component_practice_1 from './components/component_practice_v-model';
    import component_practice_2 from './components/component_practice_two_way_binding';

    export default {
        name: 'app',
        components: {
            component_foo,
            component_moo,
            component_practice_1,
            component_practice_2,
        },
        data: function () {
            return {
                message: "default value",
            };
        },
        methods: {
            setToDefault: function () {
                this.message = "default value"
            }
        }
    }
</script>