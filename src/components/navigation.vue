<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container">

        <!-- Toggler/collapsible button -->
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Navbar links -->
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <router-link :to="{ name: 'Home' }" class="nav-link">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="{ name: 'About' }" class="nav-link">About</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="{ name: 'Resume' }" class="nav-link">Education</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="{ name: 'Projects' }" class="nav-link">Projects</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="{ name: 'Testimonials' }" class="nav-link">Reviews</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="{ name: 'Contact' }" class="nav-link">Contact</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- <router-view/> -->
  </div>
</template>


<style scoped>
.navbar {
  padding: 10px;
  text-align: center;
}

.nav-link {
  color: rgb(81, 206, 210);
  margin: 0 10px;
  padding: 5px 10px;
  font-family: Black Ops One;
}

.nav-item {
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav-link:hover {
  border-bottom: 2px solid #9732ac;
}

@media screen and (max-width: 420) {
  .nav-item {
    margin: 10px;
  }
}
</style>
