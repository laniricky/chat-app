<script>
export default {
  name: 'Message',
  props: [
    'text', // Content of the message
    'author', // Author of the message
    'dark' // Background variant of the box
  ]
}
</script>

<template>
  <form class='chat-box' @submit='onSubmit($event)'>
    <input
        v-model='text'
        placeholder='Write a message'
        type='text'
    />
    <button :disabled='text === ""'>Send</button>
  </form>
</template

<style scoped>
.chat-box {
  width: 100%;
  display: flex;
}

input {
  width: min(100%, 20rem);
  flex-grow: 1;
}

button:disabled {
  opacity: 0.5;
}
</style>
