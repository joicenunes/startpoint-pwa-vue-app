<template>
  <div>
    <ul>
      <li v-for='(link, index) in links' :key='index'>
        <router-link :to='link.to'>{{link.name}}</router-link>
      </li>
    </ul>
    <main>
      <router-view />
    </main>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        links: [
          {
            name: 'Home',
            to: '/'
          },
          {
            name: 'Bad Link',
            to: '/bad-url'
          }
        ]
      }
    }
  }
</script>

<style scoped>
  ul {
    list-style: none;
    display: flex;
    padding: 0;
  }
  li {
    padding: 5px 15px 5px 0;
  }
  li a {
    text-decoration: none;
    color: black;
  }
  li a:hover {
    color: #404040;
  }
</style>