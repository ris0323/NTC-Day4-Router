<template>
    Product Id is {{ $route.params.productId}}
    {{ info }}
    <router-link :to="`/products/${route.params.productId}/comments`">products comments</router-link>
    <router-view></router-view>
</template>
<script>
import axios from 'axios'
export default {

  data () {
    return { info: null }
  },
  mounted () {
    axios.get('http://jsonplaceholder.typicode.com/todos/1')
      .then(response => (this.info = response.data))
  }
}
</script>
