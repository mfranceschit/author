<template>
  <div class="container">
    <div class="book">
      <div class="front">
        <div class="cover">
          <p class="num-up"></p>
          <svg
            id="eye-left"
            xmlns="http://www.w3.org/2000/svg"
            width="75"
            height="100"
            version="1.0"
          >
            <path
              d="m 72.520861,60.915859 v 0 C 69.385207,53.011396 61.908243,46.570093 55.74346,42.387465 49.578631,38.204905 40.408101,36.818968 33.679899,37.051071 c -1.597953,0.05517 -2.931531,0.451253 -4.000736,1.188245 -0.738155,0.570053 -1.097854,1.127016 -1.079089,1.670881 0.02949,0.854739 0.93486,2.69053 2.716108,5.507379 0.805175,1.372521 1.234574,2.83577 1.288193,4.389751 0.131362,3.807345 -0.983571,6.879734 -3.344801,9.217182 -2.361227,2.337476 -5.686459,3.580206 -9.975699,3.728183 C 15.162859,62.894893 11.580282,61.559887 8.5361375,58.747669 5.4920363,55.935482 3.8975877,52.431474 3.7527937,48.235627 c -0.1769131,-5.1282 2.0835359,-9.776522 6.7813483,-13.944986 4.697855,-4.168379 11.041643,-6.390426 19.031387,-6.666142 8.662566,-0.298838 16.811229,2.201105 24.446015,7.499833 7.634738,5.298806 13.804506,13.895976 18.509317,25.791527 z"
              id="text2161"
              fill="#000"
              fill-opacity="1"
              stroke="none"
              stroke-width=".72233355px"
              stroke-linecap="butt"
              stroke-linejoin="miter"
              stroke-opacity="1"
            />
          </svg>
          <svg
            id="eye-right"
            xmlns="http://www.w3.org/2000/svg"
            width="75"
            height="100"
            version="1.0"
          >
            <path
              d="m 72.520861,60.915859 v 0 C 69.385207,53.011396 61.908243,46.570093 55.74346,42.387465 49.578631,38.204905 40.408101,36.818968 33.679899,37.051071 c -1.597953,0.05517 -2.931531,0.451253 -4.000736,1.188245 -0.738155,0.570053 -1.097854,1.127016 -1.079089,1.670881 0.02949,0.854739 0.93486,2.69053 2.716108,5.507379 0.805175,1.372521 1.234574,2.83577 1.288193,4.389751 0.131362,3.807345 -0.983571,6.879734 -3.344801,9.217182 -2.361227,2.337476 -5.686459,3.580206 -9.975699,3.728183 C 15.162859,62.894893 11.580282,61.559887 8.5361375,58.747669 5.4920363,55.935482 3.8975877,52.431474 3.7527937,48.235627 c -0.1769131,-5.1282 2.0835359,-9.776522 6.7813483,-13.944986 4.697855,-4.168379 11.041643,-6.390426 19.031387,-6.666142 8.662566,-0.298838 16.811229,2.201105 24.446015,7.499833 7.634738,5.298806 13.804506,13.895976 18.509317,25.791527 z"
              id="text2161"
              fill="#000"
              fill-opacity="1"
              stroke="none"
              stroke-width=".72233355px"
              stroke-linecap="butt"
              stroke-linejoin="miter"
              stroke-opacity="1"
            />
          </svg>
          <p class="num-down">1</p>
          <p class="author">George Orweell</p>
        </div>
      </div>
      <div class="left-side">
        <h2>
          <span>George Orwell</span>
          <span>r</span>
        </h2>
      </div>
    </div>
  </div>
</template>

<style>
html,
body {
  background-color: #c4bec6;
  display: border-box;
}

.container {
  z-index: 1;
  perspective: 3000px;
}

.container .book {
  position: relative;
  display: block;
  width: 400px;
  height: 550px;
  margin: 5% auto;
  border-radius: 2px 4px 4px 2px;
  background: linear-gradient(45deg, #dad5dc 0%, #f2ebf4 100%);
  font-family: acumin-pro, sans-serif;
  -webkit-box-shadow: 13px 13px 8px 0px rgba(151, 146, 153, 0.6);
  -moz-box-shadow: 13px 13px 8px 0px rgba(151, 146, 153, 0.6);
  box-shadow: 13px 13px 8px 0px rgba(151, 146, 153, 0.6);
  font-weight: 400;
  color: #2b2b2b;
  -webkit-transform-style: preserve-3d;
  -moz-transform-style: preserve-3d;
  transform-style: preserve-3d;
  -webkit-transition: -webkit-transform 0.5s;
  -moz-transition: -moz-transform 0.5s;
  transition: transform 0.5s;
}

.container .book:hover {
  -webkit-transform: rotate3d(0, 1, 0, 35deg);
  -moz-transform: rotate3d(0, 1, 0, 35deg);
  transform: rotate3d(0, 1, 0, 35deg);
}

.container .book > div,
.container .front > div {
  display: block;
  position: absolute;
}

.container .front {
  -webkit-transform-style: preserve-3d;
  -moz-transform-style: preserve-3d;
  transform-style: preserve-3d;
  -webkit-transform-origin: 0% 50%;
  -moz-transform-origin: 0% 50%;
  transform-origin: 0% 50%;
  -webkit-transition: -webkit-transform 0.5s;
  -moz-transition: -moz-transform 0.5s;
  transition: transform 0.5s;
  -webkit-transform: translate3d(0, 0, 20px);
  -moz-transform: translate3d(0, 0, 20px);
  transform: translate3d(0, 0, 20px);
  z-index: 10;
}

.container .front > div {
  width: 400px;
  height: 550px;
}

.container .left-side {
  width: 40px;
  left: -20px;
  height: 550px;
  background-color: rgba(232, 229, 234);
  -webkit-transform: rotate3d(0, 1, 0, -90deg);
  -moz-transform: rotate3d(0, 1, 0, -90deg);
  transform: rotate3d(0, 1, 0, -90deg);
}

.cover svg {
  position: absolute;
  top: 50%;
  left: 45%;
  margin-top: -100px;
  margin-left: -110px;
  width: 300px;
}

#eye-right {
  padding-left: 185px;
}

.cover .num-up {
  position: absolute;
  top: 64px;
  left: 47px;
  letter-spacing: 50px;
  transform: rotate(-90deg);
}

.cover .num-down {
  position: relative;
  top: 65px;
  left: -95px;
  transform: rotate(-90deg);
}

.author {
  font-family: acumin-pro, sans-serif;
  font-weight: 400;
  position: absolute;
  top: 475px;
  left: 50px;
  opacity: 0.8;
}

.container .front > div {
  border-radius: 0 3px 3px 0;
  box-shadow: inset 4px 0 10px rgba(0, 0, 0, 0.1);
}

.container .front:after {
  content: '';
  position: absolute;
  top: 1px;
  bottom: 1px;
  left: -1px;
  width: 1px;
}

.container .cover:after {
  content: '';
  position: absolute;
  top: 0;
  left: 10px;
  bottom: 0;
  width: 3px;
  background: rgba(0, 0, 0, 0.1);
  box-shadow: 1px 0 3px rgba(255, 255, 255, 0.1);
}

.container h2 {
  width: 500px;
  height: 40px;
  color: #2b2b2b;
  font-size: 15px;
  line-height: 40px;
  padding-right: 10px;
  text-align: right;
  -webkit-transform-origin: 0 0;
  -moz-transform-origin: 0 0;
  transform-origin: 0 0;
  -webkit-transform: rotate(90deg) translateY(-40px);
  -moz-transform: rotate(90deg) translateY(-40px);
  transform: rotate(90deg) translateY(-40px);
}

.cover {
  background: linear-gradient(45deg, #dad5dc 0%, #f2ebf4 100%);
}

.left-side h2 span:first-child {
  font-weight: 400;
  font-size: 13px;
  padding-right: 20px;
}

.left-side h2 span:last-child {
  font-family: acumin-pro, sans-serif;
}
</style>
