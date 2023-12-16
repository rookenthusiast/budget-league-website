<template>
  <header class="header">
    <div class="logo pa-3">Budget Ducks</div>
    <nav>
      <a>Decklists</a>
      <a>Standings</a>
      <a>Submissions</a>
    </nav>
    <div class="pa-3">
      <v-btn rounded="xl" size="small">Login</v-btn>
    </div>
  </header>
  <slot />
</template>
<style lang="scss">
.header {
  position: fixed;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #fff;
  padding: 20px 0;

  nav {
    a {
      padding: 12px;
    }
  }
}
</style>
