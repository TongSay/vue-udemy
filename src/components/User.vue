<template>
    <button @click="onClickAge()">Upadate Age Event</button>
    <button @click="ageChangeFn(3)">Upadate Age CB</button>
    <p>The user is {{ age }} years old </p>
    <p>Age x 2 is {{ ageDouble }}</p>
</template>

<script>
    export default {
    name: 'User',
    props: {
      age: {
        type: Number,
        //require: true,
        // default: 20,
        validator(value) {
          return value < 130
        }
      },
      ageChangeFn: Function
    },
    emits: ["age-change"],
    computed: {
        ageDouble () {
        return this.age * 2;
    }
    },
    
    methods: {
      onClickAge() {
        this.$emit("age-change",3);
      }
    }
  }
</script>