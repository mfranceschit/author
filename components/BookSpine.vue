<template>
  <div class="container">
    <div class="book-spine">
      <div class="front">
        <div
          class="cover"
          :class="[book.category === 'stories' ? 'story-book' : 'thought-book']"
        >
          <h3>
            <span>{{ book.author }}</span>
            <span>{{ book.title }}</span>
          </h3>
        </div>
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
.container .book-spine {
  position: relative;
  display: block;
  width: 100px;
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

.container .book-spine .front > div {
  width: 100px;
  height: 550px;
}

.cover {
  background-image: url('~assets/images/leather.png');
  display: flex;
}

.cover h3 span:first-child {
  font-weight: 400;
  font-size: 13px;
  padding-right: 20px;
}

.cover h3 span:last-child {
  font-family: acumin-pro, sans-serif;
}
</style>
