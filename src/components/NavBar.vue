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
        <!-- navbar collapse -->
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        </div>
        <!-- shopping cart button that will display whats in the cart and the option to clear the cart -->
        <div class="row">
        <div class="col">
          <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#cart">Cart (<span class="total-count"></span>)</button><button class="clear-cart btn btn-danger">Clear Cart</button></div>
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
  font-size:6rem;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  align-self:center;
  color: rgb(21, 23, 51);
}
</style>