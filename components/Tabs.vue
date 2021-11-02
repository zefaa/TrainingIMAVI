<template>
  <div class = "container">
  <ul class="menu">
    <li> <router-link to="/"> Home </router-link> </li>
    <li> <router-link to="/profil/procob">Data Diri </router-link> </li>
    <li> <router-link to="/pendidikan/edu">Pendidikan</router-link> </li>
    <li> <router-link to="/pengalaman/exp">Pengalaman</router-link> </li>
   </ul> 
  </div>
 </template>
 <script>
 export default {
 }
 </script>
 <style scoped>
 .container {
  width: 75%;
  margin: 100px auto;
  text-align: center;
 }
 .menu {
  list-style: none;
  margin-bottom: 20px;
 }
 .menu li {
  display: inline;
 }
.menu ul{
  display: center;
}
 .menu li a {
  padding: 20px;
  text-decoration: none;
 }
 </style>