<template>
  <nav class="nav">
    <ul>
      <li>
        <NuxtLink active-class="active" class="link" to="/">
          Home
        </NuxtLink>
      </li>
      <li>
        <NuxtLink active-class="active" class="link" to="/products">
          Products
        </NuxtLink>
      </li>
      <li>
        <NuxtLink active-class="active" class="link" to="/about">
          About
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style>
  nav{
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background: black;
    z-index: 9;
  }
  ul{
    list-style: none;
    padding: 20px 0;
    margin: 0;
    display: flex;
    align-items: center;
  }
  ul li {
    margin: 0 10px;
    padding: 5px;
  }
  ul li a{
    font-size: 18px;
    color: white;
    text-decoration: none;
  }
  ul li a.active{
    color: green;
  }
  ul li a:hover{
    opacity: .8;
  }
</style>