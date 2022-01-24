<template>
  <div class="todo-item p-4">
    <div class="todo-item__header">
      <div class="todo-item__header-content">
        <img src="../assets/presentation.svg" alt="presentation">
        <span>Presentation</span>
      </div>

      <div class="todo-item__time">
        <img src="../assets/clock.svg" alt="clock">
        <span>6:00 PM</span>
      </div>
    </div>

    <div class="todo-item__body">
      <span>{{ title }}</span>
    </div>

    <div class="todo-item__footer">
      <div>U</div> <span>User Name</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',

  props: {
    title: String
  }
}
</script>

<style lang="scss" scoped>
.todo-item {
  border-radius: 16px;
  background: #F3FAFA;
  border: 1px solid rgba(171, 217, 218, 0.38);
}

.todo-item__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.todo-item__header-content {
  display: flex;
  justify-content: center;
  align-items: center;

  img {
    width: 22px;
  }

  span {
    color: #293246;
    font-weight: 700;
    font-size: 16px;
    margin-left: 10px;
  }
}

.todo-item__time {
  display: flex;
  align-items: center;

  img {
    width: 12px;
  }

  span {
    font-size: 12px;
    color: #293147;
    margin-left: 10px;
    opacity: 0.5;
  }
}

.todo-item__body {
  margin-top: 14px;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #293246;
}

.todo-item__footer {
  margin-top: 15px;
  display: flex;
  align-items: center;
  font-size: 14px;
  font-weight: 600;

  div {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 28px;
    height: 28px;
    background: #D9EDFA;
    border-radius: 50%;
    color: #75A8D0;
    margin-right: 10px;
  }

  span {
    color: #293147;
    opacity: 0.5;
  }
}
</style>