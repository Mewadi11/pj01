<template>
  <div>
    <input :value="value" type="text" placeholder="name" @input="createtodo" />

    <button @click="Todo">สร้างtodo</button>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: ["value", "createtodo", "todo"],
};
</script>