<!-- Kaylee Martin -->
<!-- NavBar Template -->

<!-- bootstrap navbar for landing page -->
<template>
    <nav class="navbar navbar-expand-lg " >
      <div class="container-fluid">
        <!-- title for the site -->
        <a class="navbar-brand">The Movie Emporium</a>
        <!-- toggle button -->
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        </div>
      </div>
    </nav>
  </template>
  
  <!-- navbar script  makes sure navbar shows up on the page -->
  <script>
  export default {
    name: "NavBar",
  };
  </script>

<!-- navbar styles for the moving cinema tape and title of page -->
<style>
.navbar{
  background-image:url("cinema-tape.jpg");
  background-position:center;
  background-repeat:repeat;
  height:12rem;
  opacity:85%;
}
.navbar-brand{
  font-size:9.25rem;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  align-self:center;
  color: rgb(21, 23, 51);
}
</style>