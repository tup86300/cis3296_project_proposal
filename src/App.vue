<template>
  <header>
    <div class="wrapper">
      <nav id="nav">
        <div id="nav-title-container">
          <h1 class="nav-title">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
              <g clip-path="url(#clip0_9_26)">
                <path
                  d="M19.914 11.105C19.9706 10.7394 19.9994 10.37 20 10C20 7.87827 19.1571 5.84344 17.6569 4.34315C16.1566 2.84285 14.1217 2 12 2C9.87827 2 7.84344 2.84285 6.34315 4.34315C4.84285 5.84344 4 7.87827 4 10C4 14.993 9.539 20.193 11.399 21.799C11.5723 21.9293 11.7832 21.9998 12 21.9998C12.2168 21.9998 12.4277 21.9293 12.601 21.799C12.8799 21.5578 13.1546 21.3117 13.425 21.061"
                  stroke="#D4B77A" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                <path
                  d="M12 13C13.6569 13 15 11.6569 15 10C15 8.34315 13.6569 7 12 7C10.3431 7 9 8.34315 9 10C9 11.6569 10.3431 13 12 13Z"
                  stroke="#D4B77A" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                <path
                  d="M19.0003 15C19.3225 15 19.5837 14.7761 19.5837 14.5C19.5837 14.2239 19.3225 14 19.0003 14C18.6782 14 18.417 14.2239 18.417 14.5C18.417 14.7761 18.6782 15 19.0003 15Z"
                  stroke="#D4B77A" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                <path d="M17.25 22L19 19L20.75 22" stroke="#D4B77A" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
                <path d="M15.5 16L19 17L22.5 16" stroke="#D4B77A" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round" />
                <path d="M19 17V19" stroke="#D4B77A" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
              </g>
              <defs>
                <clipPath id="clip0_9_26">
                  <rect width="24" height="24" fill="white" />
                </clipPath>
              </defs>
            </svg>
            Access Atlas
          </h1>
        </div>
        <div id="nav-link-container">
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
        </div>
      </nav>
    </div>
  </header>
  <div id="content">
    <RouterView />
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<style>
body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
  background-color: #EFEBEA;
  font-family: "Open Sans", sans-serif;
  font-size: 17px;
}

#nav {
  background-color: #0B6342;
  position: sticky;
  top: 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: .5rem 2rem;
  white-space: nowrap;
}

.nav-title {
  margin: 0;
  padding: 0;
  font-family: "Open Sans", sans-serif;
  font-size: 2rem;
  font-weight: bold;
  color: #D4B77A;
  white-space: nowrap;
}

#nav-link-container {
  display: flex;
  gap: 1rem;
}

.dropDown a {
  text-decoration: none;
  white-space: nowrap;
  color: white;

}

#nav-link-container a:hover {
  color: #D4B77A;

}

#nav-link-container a {
  text-decoration: none;
  white-space: nowrap;
  color: white;

}

#content {
  padding: 20px 2rem 50px 2rem;
}

@media only screen and (min-width: 40rem) {
  #nav {
    flex-direction: row;
    align-items: center;
  }

  #nav-link-container {
    flex-direction: row;
  }
}
</style>