<template>
  <div class="hello">
    <div :class="{newbkg:scrolled}" ref="navbar" class="navbar">
      <nav>
        <div class="navbar-wrapper container">
          <div class="logo">
            <img
              src="data:image/svg+xml;base64,PHN2ZyBkYXRhLW5hbWU9ImxvZ28iIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgd2lkdGg9IjI2Ljg4MiIgaGVpZ2h0PSIzMCI+PGRlZnM+PGxpbmVhckdyYWRpZW50IGlkPSJhIiB4Mj0iMSIgeTI9IjEiIGdyYWRpZW50VW5pdHM9Im9iamVjdEJvdW5kaW5nQm94Ij48c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiM3NzYzY2QiLz48c3RvcCBvZmZzZXQ9Ii4xODQiIHN0b3AtY29sb3I9IiM3YjY4ZDAiLz48c3RvcCBvZmZzZXQ9Ii40OTEiIHN0b3AtY29sb3I9IiM4NjczZDYiLz48c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiNiOWFmZTciLz48L2xpbmVhckdyYWRpZW50PjwvZGVmcz48ZyBkYXRhLW5hbWU9IkxheWVyIDEiPjxwYXRoIGRhdGEtbmFtZT0iJmx0O1BhdGgmZ3Q7IiBkPSJNMjYuODgyIDEzLjQxNlYzMEgxMS4yNjNhMTUuMjQ2IDE1LjI0NiAwIDAgMCAxMi44MjktNi45OTRsLjAzNy0uMDU1YTE0LjU3MiAxNC41NzIgMCAwIDAgMi40MjMtOC4wNTFjMC0uNDI0LS4wMTctLjg0My0uMDU1LTEuMjU3cS0uMDA3LS4xMTItLjAxOS0uMjI0YTkuMzcgOS4zNyAwIDAgMC0uMDU5LS40NzYgOC45MDggOC45MDggMCAwIDAtLjAyNS0uMTgySDE0LjF2NC40MjNoNi45ODRBMTAuNjIxIDEwLjYyMSAwIDAgMSAyMC4xIDE5LjRhOS4zIDkuMyAwIDAgMS0xLjQ3NyAxLjk4NHEtLjI3NC4yODMtLjU3MS41MzlsLS4wMTMuMDA5YTEwLjggMTAuOCAwIDAgMS0zLjIgMi4wMjIgMTAuNTcxIDEwLjU3MSAwIDAgMS0xLjk1OC41ODUgMTAuODI2IDEwLjgyNiAwIDAgMS0yLjA5MS4yMDZjLS4xNDYgMC0uMjkxIDAtLjQzNS0uMDExQTEwLjc4OCAxMC43ODggMCAwIDEgMCAxMy45NTNhMTEuMDkgMTEuMDkgMCAwIDEgLjA2Ny0xLjE3NkExMy40MjMgMTMuNDIzIDAgMCAxIDE2LjEuMjZhMTMuNDE4IDEzLjQxOCAwIDAgMSAxMC43ODIgMTMuMTU2eiIgZmlsbD0idXJsKCNhKSIvPjwvZz48L3N2Zz4="
              alt
            />
          </div>
          <div class="nav-items">
            <ul>
              <li>
                <a href>Home</a>
              </li>
              <li>
                <a href>Ride</a>
              </li>
              <li>
                <a href>Fare Estimate</a>
              </li>
              <li>
                <a href>Features</a>
              </li>
              <li>
                <a href>News</a>
              </li>
            </ul>
          </div>
          <div class="auth">
            <ul>
              <li>
                <a href>Login</a>
              </li>
              <li>
                <a href>Sign Up</a>
              </li>
            </ul>
          </div>
          <div v-if="showBurger" @click="showMobileMenu" class="Burger">
            <div class="bug1"></div>
            <div class="bug2"></div>
            <div class="bug3"></div>
          </div>
          <div
            :class="{'slideInRight':this.mobileMenu,'mobileSlideLeft':this.mobileMenu,'slideOutRight':this.mobileOut,'mobileOut':this.mobileOut}"
            class="animated mobile-menu"
          >
            <div class="mobile-container">
              <div @click="hideMobileMenu" class="cross">
                <div class="cross1"></div>
                <div class="cross2"></div>
              </div>
              <ul>
                <li>
                  <a href>Home</a>
                </li>
                <li>
                  <a href>Ride</a>
                </li>
                <li>
                  <a href>Fare Estimate</a>
                </li>
                <li>
                  <a href>Features</a>
                </li>
                <li>
                  <a href>News</a>
                </li>
                <li>
                  <a href>Login</a>
                </li>
                <li>
                  <a href>Sign Up</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
import "../animate.css";
export default {
  props: {},
  data() {
    return {
      scrolled: false,
      mobileMenu: false,
      mobileOut:false,
      showBurger:true,
    };
  },
  methods: {
    handleScroll: function(event) {
      if (
        document.body.scrollTop > 45 ||
        document.documentElement.scrollTop > 45
      ) {
        console.log("down");
        this.scrolled = true;
      } else {
        this.scrolled = false;
      }
    },
    showMobileMenu() {
      console.log(this.mobileMenu);
      this.showBurger=false
      this.mobileMenu = true;
      this.mobileOut=false;
      console.log(this.mobileMenu);
    },
    hideMobileMenu(){
      this.showBurger=true

      this.mobileMenu=false;
      this.mobileOut=true;
    },
    // hideMobileOnBigScreen() {
    //   console.log(this.mobileMenu);
    //   window.addEventListener("resize", function() {
    //     this.mobileMenu = false;
    //     if (window.innerWidth > 990) {
    //       console.log(this.mobileMenu);
    //       this.mobileMenu = false;
    //       console.log(this.mobileMenu);
    //     }
    //   });
    // }
  },

  created: function() {
    // this.hideMobileOnBigScreen();
    window.addEventListener("scroll", this.handleScroll);
    console.log("created");
  },
  destroyed: function() {
    window.removeEventListener("scroll", this.handleScroll);
    console.log("destroyed");
  }
};
</script>
<style scoped>
.newbkg {
  background: white;
  height: 8.5vh !important;
  -webkit-box-shadow: 0px 3px 5px 0px rgba(176, 176, 176, 0.19);
  -moz-box-shadow: 0px 3px 5px 0px rgba(176, 176, 176, 0.19);
  box-shadow: 0px 3px 5px 0px rgba(176, 176, 176, 0.19);
}
.navbar {
  width: 100%;
  height: 10.5vh;
  position: fixed;
  top: 0;
  transition: 0.4s;
  left: 0;
  z-index: 100;
}
.navbar nav {
  width: 100%;
  height: 100%;
}
.navbar-wrapper {
  /* width: 1200px;
  margin: 0 auto; */
  height: 100%;
  display: flex;
  align-items: center;
}
.logo {
  width: auto;
  height: auto;
}
.logo img {
  width: 30px;
  height: 30px;
}
.nav-items {
  width: auto;
  height: auto;
  margin-right: auto;
  margin-left: 95px;
}
.nav-items ul {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
.nav-items ul li {
  list-style-type: none;
  padding: 0px 30px;
  font-weight: 500;
  cursor: pointer;
}
.nav-items ul li a {
  text-decoration: none;
  color: black;
  padding: 8px 0;
  position: relative;
}
.nav-items ul li a::before,
.auth ul li a::before {
  content: "";
  width: 0;
  height: 10px;
  background-image: linear-gradient(
    to right,
    rgb(191, 192, 245),
    rgb(185, 176, 232)
  );
  position: absolute;
  bottom: 8px;
  left: 5px;
  content: "";
  display: inline-flex;
  transition: 0.3s all linear;
  z-index: -1;
}
.nav-items ul li a:hover::before,
.auth ul li a:hover::before {
  width: 100%;
}
.auth {
  margin-right: 45px;
  margin-left: auto;
}
.auth ul {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}
.auth ul li {
  list-style-type: none;
  padding: 0px 30px;
  font-weight: 500;
}
.auth ul li a {
  text-decoration: none;
  color: black;
  padding: 8px 0px;
  position: relative;
}
.Burger {
  width: 35px;
  height: 35px;
  margin-left: auto;
  direction: rtl;
  display: none;
}
.bug1 {
  width: 100%;
  height: 3px;
  background: #8454ff;
  margin: 5px 0;
  border-radius: 10px;
}
.bug2 {
  width: 100%;
  height: 3px;
  background: #8454ff;
  margin: 5px 0;
  border-radius: 10px;
}
.bug3 {
  width: 75%;
  height: 3px;
  background: #8454ff;
  margin: 5px 0;
  border-radius: 10px;
}
.mobile-menu {
  height: 100vh;
  position: fixed;
  top: 0;
  right: -400px;
  background: white;
  width: 400px;
 -webkit-box-shadow: -2px 0px 14px 0px rgba(191,191,191,0.3);
-moz-box-shadow: -2px 0px 14px 0px rgba(191,191,191,0.3);
box-shadow: -2px 0px 14px 0px rgba(191,191,191,0.3);
  /* display: none; */
}
.mobileSlideLeft { 
   right: 0; 
}
.mobileOut{
  right: 0; 
  /* display: none; */
}
.mobile-container {
  width: 100%;
  height: 100%;
  padding-top: 50px;
  padding-left: 50px;
  position: relative;
}
.mobile-container ul {
  padding: 0;
  margin: 0;
}
.mobile-container ul li {
  list-style: none;
  padding: 0px 16px;
}
.mobile-container ul li a {
  text-decoration: none;
  padding: 18px 0;
  color: rgb(51, 51, 51);
  display: inline-block;
  position: relative;
}
.mobile-container ul li a::before {
  content: "";
  width: 0;
  height: 10px;
  background-image: linear-gradient(
    to right,
    rgb(191, 192, 245),
    rgb(185, 176, 232)
  );
  position: absolute;
  bottom: 18px;
  left: 5px;
  content: "";
  display: inline-flex;
  transition: 0.3s all linear;
  z-index: -1;
}
.mobile-container ul li a:hover::before {
  width: 100%;
}
.cross {
  position: absolute;
    top: 20px;
    right: 20px;
    width: 25px;
    height: 25px;
    cursor: pointer;
}
.cross1 {
  width: 100%;
  height: 2px;
  transform: rotate(-45deg);
  background: #8454ff;
  position: absolute;
  top: 50%;
  left: 0;
}
.cross2 {
  width: 100%;
  height: 2px;
  transform: rotate(45deg);
  background: #8454ff;
  position: absolute;
  top: 50%;
  right: 0;
}
@media screen and (max-width: 1180px) {
  .nav-items {
    margin-left: 55px;
  }
  .auth {
    margin-right: 25px;
  }
}
@media screen and (max-width: 1050px) {
  .nav-items {
    margin-left: 25px;
  }
  .auth {
    margin-right: 5px;
  }
  .nav-items ul li {
    padding: 0 25px;
  }
}

@media screen and (max-width: 990px) {
  .nav-items,
  .auth {
    display: none;
  }
  .Burger {
    display: block;
  }
}
@media screen and (max-width:800px){
  .mobile-container{
    padding-left: 40px;
  }
}
@media screen and (max-width: 750px) {
  .mobile-menu{
    width: 350px;
  }
  
}
@media screen and (max-width: 600px) {
  .mobile-menu{
    width: 300px;
  }
}
@media screen and (max-width: 500px) {
  .mobile-menu{
    width:65%;
  }
}
@media screen and (max-width: 400px) {
  .mobile-menu{
    width:70%;
  }
}
</style>


