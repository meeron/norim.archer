<template>
  <nav>
    <div class="nav-wrapper">
      <ul class="right">
        <li v-for="r in routes"
          :key="r.path"
          :class="{ active: $route.path === r.path }">
          <router-link :to="r.path">{{r.title}} {{r.isActive}}</router-link>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  data: function() {
    return {
      routes: [
        { path: '/', title: 'Home' },
        { path: '/login', title: 'Login' },
        { path: '/about', title: 'About' }
      ]
    };
  }
};
</script>

