<template>
  <ul>
    <li><a href="#/">Home</a></li>
    <li><a href="#/blog">Blog</a></li>
    <li><a href="#/catalogue">Katalog</a></li>
  </ul>
</template>

<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
}

li {
  float: left;
}

li a {
  display: block;
  padding: 8px;
  background-color: green;
  text-decoration: none;
}

li a:hover {
  text-decoration: none;
  background-color: yellowgreen;

}
</style>
