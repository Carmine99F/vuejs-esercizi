<script>
export default {
  data() {
    return {
      myName: 'Carmine',
      cognome: 'Fierro',
      myObject: {
        esame: 'java',
        cfu: 9,
      },
      myText: 'esempio',
      message: '<span style="color: red;">Hello, Vue!</span>',
      newElement: '<div>Ciao</div>',
      isVisible: true,
    };
  },
  methods: {
    avviso() {
      if (this.myName === 'Carmine') this.myName = 'Silvia';
      else {
        this.myName = 'Carmine';
      }
    },
    hideh1() {
      this.isVisible = !this.isVisible;
    },
  },
};
</script>

<template>
  <h1 v-show="isVisible" @mouseover="hideh1" @mouseout="hideh1">Show</h1>
  <p>Piacere sono {{ myName }}</p>
  <p>{{ myObject.cfu }}</p>
  <button @click="avviso">Cliccami</button>
  <p v-text="message"></p>
  <p>{{ message }}</p>
  <p v-html="newElement"></p>
</template>

<style scoped>
p {
  color: red;
}
</style>
