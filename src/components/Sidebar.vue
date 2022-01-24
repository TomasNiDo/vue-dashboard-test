<template>
  <div class="sidebar">
    <aside class="menu">
      <ul class="menu-list">
        <li class="px-4"><button class="button is-primary">HOME BASE</button></li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  name: 'Sidebar'
}
</script>

<style lang="scss" scoped>
.menu-list li button {
    font-family: 'Montserrat';
    color: #ffffff !important;
    font-size: 14px;
    font-weight: 600;
    padding: 24px 58px;
  }
</style>