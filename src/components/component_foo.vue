<template>
  <div class="hello">
     <button class="btn btn-primary">Liter</button>
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    message: String
  }
}
</script>
