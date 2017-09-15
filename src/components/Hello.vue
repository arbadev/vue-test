<template>
  <div>
    <ul>
      <li v-for='name in names' v-text='name'></li>
    </ul>
    <input v-model='newName'>
    <button @click='addName'>add name</button>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      names: ['putanga', 'tuki', 'cabeza'],
      newName: '',
    };
  },
  methods: {
    addName() {
      this.names.push(this.newName)
      this.newName = ''
    },
  },
};
</script>
