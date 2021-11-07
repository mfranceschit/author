<template>
  <div class="container">
    <div class="book">
      <div class="front">
        <div
          class="cover"
          :class="[book.category === 'stories' ? 'story-book' : 'thought-book']"
        >
          <section class="title">
            <h2>{{ book.title }}</h2>
          </section>

          <p class="author">{{ book.author }}</p>
        </div>
      </div>
      <div
        class="left-side"
        :class="[book.category === 'stories' ? 'story-book' : 'thought-book']"
      >
        <h3>
          <span>{{ book.author }}</span>
          <span>{{ book.title }}</span>
        </h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    book: {
      author: String,
      category: String,
      title: String,
      slug: String,
      coverUrl: String,
    },
  },
}
</script>

<style>
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
  -webkit-transform: rotate3d(0, 1, 0, -90deg);
  -moz-transform: rotate3d(0, 1, 0, -90deg);
  transform: rotate3d(0, 1, 0, -90deg);
}

.cover > figure {
  height: 400px;
  overflow: hidden;
  margin: 1em 40px;
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
  color: white;
  font-family: acumin-pro, sans-serif;
  font-weight: 400;
  position: absolute;
  top: 475px;
  right: 50px;
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

.container .book .cover:after {
  content: '';
  position: absolute;
  top: 0;
  left: 10px;
  bottom: 0;
  width: 3px;
  background: rgba(0, 0, 0, 0.1);
  box-shadow: 1px 0 3px rgba(255, 255, 255, 0.1);
}

.container .book h2 {
  text-align: center;
  font-style: italic;
}

.container .book h3 {
  width: 500px;
  height: 40px;
  color: #fff;
  font-size: 1em;
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

.container .book-spine h3 {
  width: 500px;
  height: 40px;
  color: #fff;
  padding-right: 10px;
  text-align: right;
  -webkit-transform-origin: 0 0;
  -moz-transform-origin: 0 0;
  transform-origin: 0 0;
  -webkit-transform: rotate(90deg) translateY(-40px);
  -moz-transform: rotate(90deg) translateY(-40px);
  transform: rotate(90deg) translateY(-40px);
}

.cover,
.left-side {
  background-image: url('~assets/images/leather.png');
}

.cover .title {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2.5em;
  font-family: 'Parisienne';
}

.title h2 {
  background: linear-gradient(
    to right,
    #cfc09f 22%,
    #634f2c 24%,
    #cfc09f 26%,
    #cfc09f 27%,
    #ffecb3 40%,
    #cfc09f 78%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  color: #fff;
}

.thought-book {
  background-color: #000000;
  color: #c0c0c0;
}

.story-book {
  background-color: #ba0000;
  color: #ffd700;
}

.left-side h3 span:first-child {
  font-weight: 400;
  font-size: 13px;
  padding-right: 20px;
}

.left-side h3 span:last-child {
  font-family: acumin-pro, sans-serif;
}
</style>
