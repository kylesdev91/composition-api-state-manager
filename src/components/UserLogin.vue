<template>
  <form @submit.prevent="onSubmit()">
    <label>
      Email:
      <input type="email" v-model="userForm.email" />
    </label>
    <label>
      Password:
      <input type="password" v-model="userForm.password" />
    </label>

    <button type="submit">Submit</button>
  </form>
</template>

<script>
import { ref } from '@vue/reactivity';
export default {
  name: 'UserLogin',
  setup: () => {
    const userForm = ref({
      email: '',
      password: '',
    });

    const onSubmit = () => {
      console.log(userForm.value);
    };

    return {
      userForm,
      onSubmit,
    };
  },
};
</script>

<style></style>
