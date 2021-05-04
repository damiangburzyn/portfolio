<template>
  <router-view/>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@600;700;800&display=swap');
*{
  margin: 0;
  padding:0;
  box-sizing: border-box;
}

#app {
  font-family: poppins, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

#nav {
padding: 30px;
position: fixed;
z-index: 1;
background-color: #fFF;
width:100%;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
