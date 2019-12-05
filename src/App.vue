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
                           @dataIsChanged="message = $event"/>
            <component_moo class="bg-success m-2 p-3 col"
                           :message="message"
                           @dataIsChanged="message = $event"></component_moo>
         </div>
         <div class="p-5">
            <component_practice class="bg-primary m-2 p-3 col"></component_practice>
         </div>
      </div>
   </div>
</template>

<script>
    import component_foo from './components/component_foo.vue'
    import component_moo from './components/component_moo.vue'
    import component_practice from './components/component_practice';

    export default {
        name: 'app',
        components: {
            component_foo,
            component_moo,
            component_practice
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