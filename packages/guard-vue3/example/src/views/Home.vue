<template>
  <div class="home-container">
    <div style="margin-bottom: 30px;">{{ message }}</div>
    <button @click="toLogin">go to login page</button>
    <div id="home-container"></div>
  </div>
</template>

<script scoped setup>
import { useAuthing } from '../../../dist/esm/guard.min.js'

const $authing = useAuthing()

const message = 'This is home page ~~'

$authing.guard.start('#home-container')

// Composition API
// import { useRouter } from 'vue-router'

// const router = useRouter()

// const toLogin = () => {
//   router.push({
//     name: 'Login'
//   })
// }


// // Options API
// export default {
//   data () {
//     return {
//       message
//     }
//   },
//   mounted () {
//     // console.log('this.$authing: ', this.$authing)
//   },
//   methods: {
//     toLogin () {
//       this.$router.push({
//         name: 'Login'
//       })
//     }
//   }
// }
</script>
