<template>
<footer>
  <div class="footer">
    <div class="container">
      <div class="row m-0 mx-auto justify-content-around">
        <section>
          <h4>TACHYON</h4>
        </section>
        <section class="list">
          <div class="row m-0">
            <ul class="links font-sm">
              <li class="list-item mb-2">
                <a href="#hero" 
                  v-scroll-to="{
                    el: '#hero',
                    offset: 0
                  }"
                    >HOME</a>
              </li>
              <li class="list-item mb-2">
                <a href="#about"
                  v-scroll-to="{
                    el: '#about',
                    offset: 900
                  }"
                  >ABOUT US</a>
              </li>
              <li class="list-item mb-2">
                <a href="#sponsors"
                  v-scroll-to="{
                    el: '#sponsors',
                    offset: 900
                  }"
                  >SPONSORS</a>
              </li>
              <li class="list-item mb-2">
                <a href="#glimpses"
                  v-scroll-to="{
                    el: '#glimpses',
                    offset: 900
                  }"
                  >GLIMPSES</a>
              </li>
              <li class="list-item mb-2">
                <a href="/ourTeam" 
                  
                    >DEVELOPED BY</a>
              </li>
            </ul>

            <ul class="links font-sm">
              <li class="list-item mb-2">
                <a href="#contact"
                  v-scroll-to="{
                    el: '#contact',
                    offset: 900
                  }"
                  >CONTACT US</a>
              </li>
              <li class="list-item mb-2">
                <a href="https://hackcodeofconduct.org/1369-tachyon_20" target="_blank" 
                  
                    >CODE OF CONDUCT</a>
              </li>
            </ul>
          </div>
        </section>
        <section>
          <p class="font-weight-bold font-sm mb-2">ADDRESS</p>
          <p class="font-sm">
            Jaypee University of Engineering and Technology <br />
            Agra Bombay Road, Raghogarh, Guna - 473226
          </p>
        </section>
        <section class="tex-center">
          <p class="font-weight-bold font-sm mb-1">FOLLOW US</p>
          <div class="social-row row m-0 py-2">
            <a href="https://www.facebook.com/juetfirefoxclub/?ref=br_rs" target="_blank" style="color:white;"><i class="fab fa-facebook-square fa-lg"></i></a>
            <i></i>
            <a href="https://www.instagram.com/mpcjuet/"  target="_blank" style="color:white;"><i class="fab fa-instagram fa-lg"></i></a>
            
            
          </div>
        </section>
      </div>
    </div>
  </div>
</footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  z-index: 10;
  z-index: 3;
  position: relative;
  
}
.footer {
  height: fit-content;
  background: linear-gradient(0deg, #0576e696 0%, black 100%);
  color: white;
  padding: 20px;
  padding-top: 50px;
  text-align: center;
  margin-top:50px;
}
.footer section {
  margin: 10px 20px;
}
.font-sm {
  font-size: 0.85em;
}
.glow {
  filter: drop-shadow(0px 0px 10px rgba(255, 255, 255, 0.2));
}
.list {
  display: none;
}
.links {
  list-style-type: none;
  font-weight: bold;
  margin: 0 5px;
}
.list-item {
  opacity: 0.5;
  cursor: pointer;
  transition: opacity 100ms ease-out;
}
.list-item a {
  text-decoration: none;
  color: white;
}
.list-item:hover {
  opacity: 1;
}
.social-row i {
  margin: 0 15px;
  font-size: 2em;
  opacity: 0.6;
  cursor: pointer;
  transition: opacity 100ms ease-out;
}
.social-row i:hover {
  opacity: 1;
}

@media only screen and (min-width: 768px) {
  .list {
    display: block;
  }
  .footer {
    text-align: left;
  }
}
</style>