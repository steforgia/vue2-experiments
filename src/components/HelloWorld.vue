<template>
  <div>
    <slot name="header">Default Header</slot>
    <slot name="body">Default body</slot>

    <form>
      <div>
        <label for="email_input">Email: </label>
        <input id="email_input" placeholder="Enter your email" type="email" v-model="form.email" />
      </div>
      <div>
        <label for="name_input">Name: </label>
        <input id="name_input" placeholder="Enter your name" type="text" v-model="form.name" />
      </div>
      <div>
        <label for="age_input">Age: </label>
        <input id="age_input" placeholder="Enter your Age" type="number" v-model="form.age" />
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'hello-world',
  data() {
    return {
      form: {
        email: '',
        name: '',
        age: undefined,
      },
    }
  },
  created() {
    console.log('Created HelloWorld component. Form values', this.form)
    console.log('Watchers', this.$watch)
  },
  updated() {
    console.log('Updated method called. Form values', this.form)
  },
  watch: {
    form: {
      handler(newForm, oldForm) {
        console.log('WATCH FORM', newForm, oldForm)
      },
      deep: true,
    },
  },
}
</script>
