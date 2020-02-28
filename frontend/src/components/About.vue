<template>
  <div ref="ref" id="about" class="glow">
    <Heading anchor=".images" wrapper="#about" :speed="-5"
      >Guess Who's Back</Heading
    >
    <div class="info container">
      <div class="row">
        <div
          class="col-md-12 text-center d-flex justify-content-center align-items-center"
        >
          <div class="temp">
            <span>#</span>
            <span>T</span>
            <span>C</span>
            <span>20</span>
          </div>
        </div>
        <!-- <div
          class="col-md-6 text-center d-flex justify-content-center align-items-center"
        >
          <div class="date">
            Back in
            <br />{{ days }} Day...
          </div>
        </div> -->
      </div>
    </div>

    <div class="container-fluid images">
      <section class="image" style="position: relative">
        <div class="row mt-5 aboutInfox">
          <div class="collage1">
            <div class="i1">
              <img src="../assets/eventImgs/DSC_0180.jpg" />
            </div>
            <div class="i2">
              <img src="../assets/eventImgs/DSC_0017.jpg" />
            </div>
            <div class="i3">
              <img src="../assets/eventImgs/DSC_0175.jpg" />
            </div>
            <div class="i4">
              <img src="../assets/eventImgs/DSC_0189.jpg" />
            </div>
            <div class="i5">
              <img src="../assets/eventImgs/DSC_0199.jpg" />
            </div>
            <div class="i6">
              <img src="../assets/eventImgs/DSC_0272.jpg" />
            </div>
            <div class="i7">
              <img src="../assets/eventImgs/DSC_0288.jpg" />
            </div>
            <div class="i8">
              <img src="../assets/eventImgs/DSC_0389.jpg" />
            </div>
          </div>
          <div
            class="collageDescription"
            v-rellax="{ speed: 3, wrapper: '.image', relativeToWrapper: true }"
          >
            <p>
              After 5 successful and enjoyable techfests, we are here
              presenting our <b>6th Grand Tech Event <u>Tachyon</u> </b>.
            </p>
            <p>
              Tachyon 2020 has been initiated by the
              <b>Mozilla Phoenix Club</b>
              and the
              <b
                >CSE Department JUET Guna</b
              >.
            </p>
            <p>
              Tachyon is an endeavor to provide an outstanding platform for the students to showcase their talent and skillsets in fiercest of competitions. Tachyon strives for one and all to get inspired and make an effort to change the world.
            </p>
          </div>
          <!-- <div class="text p-5">
            


          </div> -->
        </div>
      </section>
      <section class="videoPlayer">
        <div class="container embed-responsive embed-responsive-16by9">
          <iframe
            src="https://www.youtube.com/embed/wYAFdwIOyW8"
            frameborder="0"
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
      
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      days: 0
    };
  },

  mounted() {
    setInterval(() => {
      var today = new Date().getTime();
      var date = new Date("April 10, 2020 00:00:00").getTime();
      var dist = date - today;
      this.days = Math.ceil(dist / (1000 * 60 * 60 * 24));
    }, 1000);
  }
};
</script>

<style lang="scss" scoped>
#about * {
  z-index: 3;
}
#about {
  margin-top: -30em;
}
.glow h1,
h2 {
  /* // font-size: 15em; */
  filter: drop-shadow(0px 0px 10px rgba(255, 255, 255, 0.6));
}

.aboutInfox {
  justify-content: center;
  width: 97%;
  margin-left: auto;
  margin-right: auto;
}

.date {
  font-size: 48px;
  font-weight: 600;
  color: #0575e6;
  filter: drop-shadow(0px 0px 10px rgba(4, 117, 229, 0.6));
}
.temp {
  font-size: 200px;
  font-weight: 900;
  letter-spacing: -0.07em;
  color: #0575e6;
  filter: drop-shadow(0px 0px 10px rgba(4, 117, 229, 0.6));
}
/* // .para p {
//   font-size: 1.2em;
//   &.right {
//     text-align: right;
//   }
//   &.left {
//     text-align: left;
//   }
// } */
.para p {
  font-size: 1.2em;
  text-align: right;
}

.info-card {
  position: absolute;
  bottom: 0;
  right: 0;
  z-index: 2;
  width: 40%;
  background: rgb(15, 15, 15);
  /* // box-shadow: 0 0 50px rgba(255, 255, 255, 0.2); */
  padding: 10px 30px;
}

.image {
  position: relative;
}
.collage1 {
  width: 60%;
  height: 600px;
  background: rgb(234, 234, 255);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  display: grid;
  grid-template-rows: auto auto auto auto;
  grid-template-columns: auto auto auto auto;
  grid-gap: 10px;
  background: transparent;
}

.collage1 > div {
  position: relative;
  overflow: hidden;
  box-shadow: 0 0 5px gray;
  transition: transform 0.2s ease-in-out;
}
.collage1 > div > img {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: scale(1) translate(-50%, -50%);
  transition: transform 0.2s ease-in-out;
}
// .collage1 > div:hover {

//   outline: 10px solid #0575e6;
//   transform: scale(1.1);
//   outline-offset: 10px;
//   img {
//     transform: scale(1.2) translate(-50%, -50%);
//   }

// }

// .collage1>div>img:hover {
//   transform: scale(1.2) translate(-50%, -50%);
//   z-index: 5;
// }

.collage1 .i1 {
  grid-area: 1/1/3/3;
}
.collage1 .i1 > img {
  height: 100%;
}
.collage1 .i2 {
  grid-area: 1/3/2/4;
}
.collage1 .i2 > img {
  height: 100%;
}
.collage1 .i3 {
  grid-area: 1/4/2/5;
}
.collage1 .i3 > img {
  height: 100%;
}
.collage1 .i4 {
  grid-area: 2/3/3/5;
}
.collage1 .i4 > img {
  width: 100%;
}
.collage1 .i5 {
  grid-area: 3/1/4/3;
}
.collage1 .i5 > img {
  width: 100%;
}
.collage1 .i6 {
  grid-area: 4/1/5/2;
}
.collage1 .i6 > img {
  height: 100%;
}
.collage1 .i7 {
  grid-area: 4/2/5/3;
}
.collage1 .i7 > img {
  height: 100%;
}
.collage1 .i8 {
  grid-area: 3/3/5/5;
}
.collage1 .i8 > img {
  height: 100%;
}
/* 
.collage1 img:hover{transform:scale(1.2) translate(-50%,-50%);} */

.collageDescription {
  /* position: relative; */
  /* top: 30%; */
  position: relative;
  /* width: 50%; */
  height: 70vh;
  border-radius: 10px;
  // border: 1px solid #0576e6;
  box-shadow: 7px 7px 30px #1768b86b;
  background: linear-gradient(#dddddd, #bdbdbd);
  padding: 20px;
  color: rgb(1, 2, 7);
  display: flex;
  flex-direction: column;
  font-size: 22px;
  text-align: center;
  // border: 1px solid rgba(255, 255, 255, 0.8);
  width: 500px;
  /* box-shadow: 0 0 10px rgba(0, 0, 0, 0.2); */
  /* display: grid; */
  /* grid-template-columns: auto auto; */
  /* grid-template-rows: auto auto auto; */
  /* grid-gap: 10px; */
  /* background: transparent; */
}

/* .collageDescription>p::first-letter{
  color:blue;
  font-size:28px;
} */

.image.second .collageDescription {
  /* left: 10%; */
}
.text {
  width: 50%;
  font-size: 1.5em;
}

.videoPlayer {
  margin-top: 150px;
}
.videoPlayer > div {
  box-shadow: 0 0 50px #0e66be6e;
}

/* // .image {
//   width: 75%;
//   height: 300px;
//   overflow: hidden;
//   box-shadow: 10px 10px 10px rgba(10, 7, 160, 0.507);
//   // transition: all 550ms ease-out;
// }
// .image:hover {
//   outline-offset: 10px;
//   outline: 5px solid #0575e6;
//   transform: scale(1.05) !important;
// } */

[data-aos="text-fade-down"] {
  transform: translateY(-30px);
  opacity: 0;
}
[data-aos="text-fade-down"].aos-animate {
  transform: translateY(0);
  opacity: 1;
}
[data-aos="image"] {
  height: 0;
  transition-property: height;
}
[data-aos="image"].aos-animate {
  height: fit-content;
}

@media only screen and (max-width: 576px) {
  .temp {
    font-size: 150px;
  }
  #about .date {
    font-size: 32px;
  }
  /* .collage1 .i5,.collage1 .i6,
  .collage1 .i7,.collage1 .i8,
  .collageDescription .i5,.collageDescription .i6,
  .collageDescription .i7,.collageDescription .i8{
    display:none;
  } */

  .collage1 {
    margin: 0 auto;
  }

  .collage1 .i1 {
    grid-area: 1/1/2/5;
  }
  .collage1 .i1 > img {
    width: 100%;
    height: auto;
  }
  .collage1 .i2 {
    grid-area: 2/1/3/3;
  }
  .collage1 .i2 > img {
    height: 100%;
  }
  .collage1 .i3 {
    grid-area: 2/3/3/5;
  }
  .collage1 .i3 > img {
    height: 100%;
  }
  .collage1 .i4 {
    grid-area: 3/1/4/5;
  }
  .collage1 .i4 > img {
    width: 100%;
  }
  .collage1 .i5 {
    grid-area: 4/1/5/3;
  }
  .collage1 .i5 > img {
    height: 100%;
    width: auto;
  }
  .collage1 .i6 {
    grid-area: 4/3/5/5;
  }
  .collage1 .i6 > img {
    height: 100%;
  }
  .collage1 .i7 {
    grid-area: 4/2/5/3;
    display: none;
  }
  .collage1 .i7 > img {
    height: 100%;
  }
  .collage1 .i8 {
    grid-area: 3/3/5/5;
    display: none;
  }
  .collage1 .i8 > img {
    height: 100%;
  }
}

@media only screen and (max-width: 768px) {
  .display-4 {
    font-size: 2em !important;
  }
  .image {
    width: 100%;
  }

  .collageDescription {
    left: 0%;
    width: 85vw;
    font-size: 16px;
  }

  .info-card {
    position: relative;
    width: 100%;
  }
  .collage1 {
    width: 100%;
    height: 600px;
    background: transparent;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  }
  .collageDescription {
    margin-left: auto;
    margin-right: auto;
    height: auto;
  }

  .text {
    width: 100%;
  }
}

@media only screen and (max-width: 576px) {
  #about {
    margin-top: -40em;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
}

@media only screen and (max-width: 1078px) {
  .aboutInfox {
    /* flex-direction: column; */
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (max-width: 1267px) {
  .collage1 {
    width: 100%;
  }

  .collageDescription {
    width: 95%;
    height: auto;
  }
  .videoPlayer {
    margin-top: -40px;
  }
}
</style>