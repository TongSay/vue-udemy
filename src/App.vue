<template>
  <h3> Hey!</h3>
  <greeting></greeting>
  <user :age="20"></user>
</template>

<script>
import  Greeting  from "@/components/Greeting.vue"
import User from "@/components/User.vue"	

export default {
  name: 'App',
  components: {
    Greeting,
    User,
  }
}
</script>