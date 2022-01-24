<template>
  <card :padding="38">
    <div class="todo-wrapper">
      <div class="todo-header">
        <span>YOUR TO-DOS FOR TODAY</span>
      </div>

      <div class="todo-content">
        <clip-loader :loading="loading" color="#81C4EE"></clip-loader>
        
        <ul class="todo-list">
          <li class="todo-list__item" v-for="item in items" :key="item.id">
            <todo-item :title="item.title" />
          </li>
        </ul>
      </div>

      <div class="todo-footer">
        <a href="#">SEE ALL</a>
      </div>
    </div>
  </card>
</template>

<script>
import Card from './Card.vue'
import TodoItem from './TodoItem.vue'
import ClipLoader from 'vue-spinner/src/ClipLoader.vue'
import axios from 'axios'

export default {
  name: 'TodoList',

  components: { 
    Card, 
    TodoItem,
    ClipLoader
  },

  data: () => ({
    loading: true,
    items: [],
  }),

  mounted() {
    this.fetchTodo()
  },

  methods: {
    async fetchTodo() {
      try {
        const { data } = await axios.get('https://jsonplaceholder.typicode.com/todos')

        this.items = data.slice(0, 5)
        this.loading = false;
      } catch (error) {
        console.log(error)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.todo-header {
  color: #04446B;
  font-weight: 700;
  font-size: 22px;
  margin-bottom: 40px;
}

.todo-list {
  list-style-type: none;
  margin: 0;

  li:not(:last-child) {
    margin-bottom: 16px;
  }
}

.todo-footer {
  text-align: right;
  font-weight: bold;
  font-size: 14px;
  line-height: 17px;
  margin-top: 40px;

  a { 
    color: #81C4EE; 
  }
}
</style>