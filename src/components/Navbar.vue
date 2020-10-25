<template>
  <nav>
      <link href="https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:wght@700&display=swap" rel="stylesheet">

      <div class="logo">
          <h4>LOGO</h4>
      </div>
      <ul class="nav-links">
          <li>
              <a href="#">HOME</a>
          </li>
          <li>
              <a href="#">MENU</a>
          </li>
          <li>
              <a href="#">ORDER</a>
          </li>
          <li>
              <a href="#">CONTACT</a>
          </li>
      </ul>
      <div @click="onClick()" class="burger">
          <div class="line1"></div>
          <div class="line1"></div>
          <div class="line1"></div>
      </div>
  </nav>
</template>

<script>
export default {
    name: 'Navbar',
    methods: {
        onClick() {
            const nav = document.querySelector('.nav-links');
            const navLinks = document.querySelectorAll('.nav-links li');

            nav.classList.toggle('nav-active');
            //animating the text
            navLinks.forEach((link, index)=> {
                if(link.style.animation){
                    link.style.animation = '';
                } else {
                    link.style.animation = `navLinkFade 0.5s ease forwards ${index/7 + 0.5}s`;
                }
                
            })
        }
    }

}

</script>

<style>

nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    min-height: 8vh;
    background-color: #2F2F2F;

}

.logo {
    font-family: 'Open Sans Condensed', sans-serif;
    color: #FCF200;
    text-transform: uppercase;
    letter-spacing: 5px;
    font-size: 32px;
}

.nav-links {
    display: flex;
    justify-content: space-around;
    width: 40%;
}

.nav-links li {
    list-style: none;
}

.nav-links a {
    font-family: 'Open Sans Condensed', sans-serif;
    color: #FCF200;
    text-decoration: none;
    letter-spacing: 3px;
    font-size: 18px;
}

.burger {
    display: none;
    cursor: pointer;
}

.burger div {
    width: 30px;
    height: 3px;
    background-color: #FCF200;
    margin: 5px;
}

@media screen and (max-width:768px) {

    body{
        overflow-x: hidden;
    }

    .nav-links {
        position: absolute;
        right: 0px;
        height: 92vh;
        top: 8vh;
        background-color: #2F2F2F ;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 90%;
        transform: translateX(100%);
        transition: transform 0.5s ease-in;

    }
    .nav-links li {
        opacity: 0;
    }

    .burger {
        display: block;
    }
}

.nav-active {
    transform: translateX(0%);
}

@keyframes navLinkFade {
    from {
        opacity: 0;
        transform: translateX(50px);
    }
    to {
        opacity: 1;
        transform: translateX(0px);
    }
}


</style>