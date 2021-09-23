<template>
  <div class="container">
      <Header title="Tasker Chase"/>
      <Tasks :tasks="tasks" />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Tasks from './components/Tasks.vue'



export default {
  name: 'App',
  components: {
    Header,
    Tasks,
  },
  data() {
    return {
      tasks: []
    }
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: 'Solat-ul fajr',
        day: 'Febuary 26th at 5:45am',
        reminder: true,
      },
      {
        id: 1,
        text: 'Bath',
        day: 'March 2nd at 7:09am',
        reminder: true,
      },
      {
        id: 1,
        text: 'Hangout',
        day: 'December 16th at 2:00pm',
        reminder: false,
      },
    ]
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}


body {
  font-family: 'Poppins', sans-serif;
}


.container{
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px dashed rgb(247, 123, 7);
  padding: 30px;
  border-radius: 5px;
}
</style>
