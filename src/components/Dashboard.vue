<template>
  <div class="dashboard">
    <navbar />

    <div class="wrapper py-4">
      <sidebar />

      <div class="container">
        <greeting username="Christy" />

        <div class="content mt-5 columns">
          <div class="column is-two-thirds-desktop is-half-tablet">
            <card>
              <div class="p-6"></div>
            </card>
          </div>

          <div class="todo column is-one-third-desktop is-half-tablet">
            <todo-list />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from './Navbar.vue'
import Sidebar from './Sidebar.vue'
import Greeting from './Greeting.vue'
import TodoList from './TodoList.vue'
import Card from './Card.vue'

export default {
  name: 'Dashboard',

  components: { 
    Navbar, 
    Sidebar, 
    Greeting, 
    TodoList,
    Card
  }
}
</script>

<style scoped>
.wrapper {
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
}
</style>