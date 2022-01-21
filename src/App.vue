<template>
<label>
  <div class="daybox">
    <input id=switch_night type="checkbox">
    <div class="top">
      <div class="moon"></div>
      <div class="cloud">
        <div class="rain"></div>
        <div class="rain rain2"></div>
        <div class="rain rain3"></div>
      </div>
      <svg class="temsvg">
        <circle cx="0" cy="100" r="3"></circle>
        <text x=0 y=100>26°</text>
        <circle cx="70" cy="80" r="3"></circle>
        <text x=70 y=80>28°</text>
        <circle cx="140" cy="120" r="3"></circle>
        <text x=140 y=120>24°</text>
        <circle cx="210" cy="90" r="3"></circle>
        <text x=210 y=90>27°</text>
        <circle cx="280" cy="110" r="3"></circle>
        <text x=280 y=110>25°</text>
        <circle cx="350" cy="80" r="3"></circle>
        <text x=350 y=80>29°</text>
        <circle cx="420" cy="120" r="3"></circle>
        <text x=420 y=120>26°</text>
        <circle cx="490" cy="100" r="3"></circle>
        <text x=490 y=100>26°</text>
        <polyline points="0,100 70,80 140,120 210,90 280,110 350,80 420,120  "></polyline>
      </svg>
      <div class="text">
        <div class="temperature">29°C</div>
        <div class="info">
          <div class="address">New Taipei City,Taiwan</div>
          <div class="time">Friday, July 2 9:00PM</div>
        </div>
      </div>

    </div>
    <div class="bottom">
      <div class="dayweather">
        <h3>MON</h3>
        <svg viewbox="-25 -25 100 100">
          <circle class="sun" cx="20" cy="15" r="8"></circle>
        </svg>
      </div>
      <div class="dayweather">
        <h3>TUE</h3>
        <svg viewbox="-25 -25 100 100">
          <circle class="sun" cx="20" cy="11" r="8"></circle>
          <circle class="cloud" cx="20" cy="25" r="8"></circle>
          <circle class="cloud" cx="9" cy="20" r="8"></circle>
          <circle class="cloud" cx="6" cy="25" r="8"></circle>
          <circle class="cloud" cx="-7" cy="20" r="6"></circle>
          <circle class="cloud" cx="-6" cy="0" r="6"></circle>
        </svg>
      </div>
      <div class="dayweather">
        <h3>WED</h3>
        <svg viewbox="-65 -25 100 100">
          <line class="rain" x1="-25" y1="15" x2="-25" y2="35"></line>
          <line class="rain" x1="-14" y1="5" x2="-14" y2="30"></line>
          <line class="rain" x1="-5" y1="20" x2="-5" y2="45"></line>
          <circle class="cloud" cx="0" cy="30" r="20"></circle>
          <circle class="cloud" cx="-15" cy="30" r="20"></circle>
          <circle class="cloud" cx="-30" cy="30" r="20"></circle>
          <circle class="cloud" cx="-25" cy="10" r="15"></circle>
          <circle class="cloud" cx="-5" cy="15" r="15"></circle>
          
        </svg>
      </div>
      <div class="dayweather">
        <h3>THU</h3>
        <svg viewbox="-50 -50 100 100">
          <circle class="sun" cx="0" cy="0" r="22"></circle>
          <circle class="cloud" cx="0" cy="30" r="20"></circle>
          <circle class="cloud" cx="-15" cy="30" r="20"></circle>
          <circle class="cloud" cx="-30" cy="30" r="20"></circle>
          <circle class="cloud" cx="-25" cy="10" r="15"></circle>
          <circle class="cloud" cx="-5" cy="15" r="15"></circle>
        </svg>
      </div>
      <div class="dayweather">
        <h3>FRI</h3>
        <svg viewbox="-50 -50 100 100">
          <circle class="sun" cx="0" cy="0" r="22"></circle>
        </svg>
      </div>
      <div class="dayweather">
        <h3>SAT</h3>
        <svg viewbox="-65 -35 100 100">
          <circle class="cloud" cx="0" cy="30" r="20"></circle>
          <circle class="cloud" cx="-15" cy="30" r="20"></circle>
          <circle class="cloud" cx="-30" cy="30" r="20"></circle>
          <circle class="cloud" cx="-25" cy="10" r="15"></circle>
          <circle class="cloud" cx="-5" cy="15" r="15"></circle>
        </svg>
      </div>
      <div class="dayweather">
        <h3>SUN</h3>
        <svg viewbox="-50 -50 100 100">
          <circle class="sun" cx="0" cy="0" r="22"></circle>
        </svg>
      </div>
    </div>
  </div>
</label>



    
</template>

<script>


export default {
  
}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Yomogi&display=swap");
@mixin size($w, $h) {
  width: $w;
  height: $h;
}
$color_white: #f3f3f3;
$color_yellow: #FFD633;
$color_black: #333;
$color_blue_start: #19283D;
$color_blue_end: #1D678F;
$color_rain: #4DACFF;
$color_white_cloud: #f2f9fe;
$color_grey_cloud: #ccc;
  
* {
  // border: solid 1px;
  position: relative;
  font-family: "Yomogi", cursive;
}

html,body {
  width: 100%;
  height: 100%;
  margin:0;
  padding:0;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: $color_black;
}

label {
  cursor: pointer;
}

.daybox {
  width: 150%;
  max-width: 400px;
  background-color: $color_white;
  box-shadow: 0px 0px 20px rgba(black,0.3);
  border-radius: 8px;
  cursor: pointer;
  
  &:hover {
    .bottom {
      height: 100px;
    } 
    .dayweather {
    opacity: 1;
    top: 0px;
   
    }
  }
}
.dayweather:nth-child(1) {
  transition-delay: 0.2s;
}
.dayweather:nth-child(2) {
  transition-delay: 0.4s;
}
.dayweather:nth-child(3) {
  transition-delay: 0.6s;
}
.dayweather:nth-child(4) {
  transition-delay: 0.8s;
}
.dayweather:nth-child(5) {
  transition-delay: 1s;
}
.dayweather:nth-child(6) {
  transition-delay: 1.2s;
}
.dayweather:nth-child(7) {
  transition-delay: 1.4s;
}
.temsvg {
  width: 100%;
  polyline {
    stroke: $color_white;
    fill: none;
    opacity:0.2;
  }
  text {
    transform: translateX(-10px) translateY(20px);
    font-size: 14px;
    fill: $color_white;
    opacity:0;
  }
  circle {
    fill: $color_white;
    opacity:0.2;
  }
}

.rain {
  @include size(2px, 10px);
  left: 45px;
  bottom: 15px;
  position: absolute;
  animation: raindrop 1s infinite linear;
  background: $color_white;
}

@keyframes raindrop {
  0% {
    transform: translateY(0px);
  }
  100% {
    transform: translateY(50px);
    opacity: 0;
  }
}

.rain2 {
  left: 70px;
  bottom: 20px;
  animation-delay: -0.3s;
}

.rain3 {
  left: 30px;
  bottom: 20px;
  animation-delay: -0.6s;
}

.top {
  height: 330px;
  background: linear-gradient(25deg,$color_blue_start,$color_blue_end);
  background-size: 100% 300%;
  animation: daylight 5s both;
  border-radius: 5px 5px 0px 0px;
  
  @keyframes daylight {
    0% {background-position: 100% 30%;}
    100% {background-position: 100% 100%;}    
  }
 .text {
    display: flex;
    flex-direction: column;
    position: absolute;
    bottom: 25px;
    left: 25px;
    color: $color_white;
   
    .temperature {
      font-size: 60px;
      line-height: 70px;
    }
    .info {
      font-size: 12px;
      padding: 1px;
      opacity: 0.6;
    }
    .address,
    .time {
      bottom: -40%;
      left: 0%;
    }
  }

}

.cloud {
  @include size(100px, 40px);
  position: absolute;
  left: 220px;
  bottom: 100px;
  border-radius: 20px;
  background:$color_white;
  box-shadow: 0px 0px 20px rgba(black,0.3);
  &::before,
  &::after {
    content: "";
    display: block;
    // border: solid 1px;
    @include size(50px, 50px);
    border-radius: 100%;
    position: absolute;
    background: $color_white;
  }
  &::before {
    left: 16px;
    top: -28px;
  }
  &::after {
    left: 35px;
    top: -20px;
  }
  animation: cloudmove 1.8s infinite linear;
}

@keyframes cloudmove {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
  100% {
    transform: translateY(0px);
  }
}

.moon {
  @include size(50px, 50px);
  border-radius: 100%;
  box-shadow: 15px -15px ;
  position: absolute;
  left: 50px;
  top: 100px;
  animation: moonmove 16s infinite;
}

@keyframes moonmove {
  0% {
    box-shadow: 15px -15px $color_yellow;
    transform: translateX(-15px) translateY(15px);
  }
  100% {
    box-shadow: -30px 30px $color_yellow;
    transform: translateX(30px) translateY(-30px);
  }
}

.bottom {
  height: 10px;
  display: flex;
  align-items: start;
  justify-content: center;
  box-shadow: 0px 0px 20px rgba(black,0.3);
  overflow: hidden;
  transition-duration:1.5s;

  .dayweather {
    width: calc(100% / 7 - 5px);
    text-align: center;
    opacity: 0;
    top: 18px;
    transition-duration: 1.5s;
    
    h3 {
      font-size: 8px;
      color :rgba($color_black,0.8);
      letter-spacing: 1px;
    }
  }
  
  svg {
    width: 100%;
    height: 30px;
    max-width: 40px;
    .sun {
      fill: $color_yellow;
      stroke: rgba($color_yellow,0.5);
      stroke-width: 15px;
      stroke-dasharray: 3px;
    }
    .cloud {
      fill: $color_grey_cloud;
    }
    .rain {
      stroke: blue;
    }
  }
}

.moon,.cloud {
   transition-duration: 0.5s; 
  }
circle {
   transition-duration: 0.5s; 
  }
text,polyline{
  transition: 0.5s 0.8s;
}

#switch_night {
  display: none;
}
#switch_night:checked + .top{
  .moon,.cloud{
    opacity: 0.2;
  }
  .temsvg {
    circle,polyline,text {
      opacity: 1;
    }
  }
}

</style>
