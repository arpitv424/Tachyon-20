<template>
  <div ref="glimpses" id="glimpses">
    <Heading anchor=".glimpses" wrapper="#glimpses" :speed="-3"
      >Glimpses</Heading
    >
    <div class="glimpses">
      <div class="container">
        <div class="row m-0 mx-auto justify-content-around text-center">
          <div class="glimpse-card blue col-md-12 col-lg-3">
            <div class="stat">
              <p class="number m-0">2000+</p>
              <p>Participations</p>
            </div>
          </div>
          <div class="glimpse-card white col-md-12 col-lg-3">
            <div class="stat">
              <p class="number m-0">10+</p>
              <p>Renowned Speakers</p>
            </div>
          </div>
          <div class="glimpse-card blue col-md-12 col-lg-3">
            <div class="stat">
              <p class="number m-0">40+</p>
              <p>Events</p>
            </div>
          </div>
        </div>
        <div class="gdata">
        <p class="text my-5 p-5 text-center">
         With a footfall of <b>2000+</b> in 2k19, Tachyon had been a huge success in the past years. 
           
        </p>
        <p class="text my-5 p-3 text-center">
          This year, we expect a gathering close to over <b>3000</b>.
        </p>
        
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#glimpses * {
  z-index: 3;
}
#glimpses {
  margin-top: 10em;
}

.glimpse-card {
  border-radius: 10px;
  width: 100%;
  margin: 0;
  // padding: 10%;
  padding: 2vw 5vh;
  &.blue {
    box-shadow: 8px 8px 50px #1768b86c;
    background: linear-gradient(#0575e6, #044483);
    color: white;
  }
  &.white {
    box-shadow: 8px 8px 50px #bbbbbb6c;
    background: linear-gradient(#dddddd, #bdbdbd);
    color: #0575e6;
  }
}
.glimpses {
  // margin-top: 60%;
  color: white;
}
.number {
  font-size: 4em;
  font-weight: bold;
}
.text {
  font-size: 2.5em;
  margin:0;
}

@media only screen and (max-width: 992px){
  .glimpse-card{
    margin-top:20px;
    margin-bottom:20px;
  }
}

@media screen and (max-width: 768px) {
  #glimpses {
    margin-top: -40em;
  }
}

@media only screen and (max-width: 576px) {
  #glimpses .text {
    font-size: 1.5em;
  }

  .glimpse-card{
    margin-top:20px;
    margin-bottom:20px;
  }
}
</style>