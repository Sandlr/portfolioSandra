<template>
  <div class="menu">
    <div class="it">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="Filmin">Filmin</NuxtLink>      
      <NuxtLink to="About">About me</NuxtLink>
    </div>
  </div>
</template>


<style>
.menu {
  text-decoration: none;
  border-bottom: 1px solid black;
  width: 100%;
  height: 50px;
  display: flex;
  flex-direction: row;
  padding: 0rem 4rem;
  background-color: black;
}

.it {
  color: black;
  text-decoration: none;
  display: flex;
  flex-direction: row;
  align-items: center;



  
}


  a{
    text-decoration: none;
    padding:1rem;
    color:white ;
  }
</style>