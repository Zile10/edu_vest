<template>
  <section class="sec-1">
    <div><p>.</p></div>
    <div class="banner">
      <h2>Welcome!</h2>
      <h4>To The Greatest Investment of Your Life</h4>
    
      <h3>EduVest! Investing into your future!</h3>

    </div>

    <div class="container">
			<h2>Why Invest:</h2>
			<p>Not everyone saves for retirement, and even those who do may not be putting away nearly enough to last through the retirement years. A 2020 Federal Reserve study showed that about 25% of non-retirees were not saving for retirement.1 However, everyone needs to invest to create wealth, beat inflation, and save for retirement and other financial goals.
      <br>
      Investing does not need to involve saving large sums of money. Due to compound interest, you can earn money on your initial amount invested plus all the accumulated interest from previous periods. While everyone should be investing, each person has a different investment strategy that fits their personal and financial goals.
      </p>
		</div>

  </section>
    <div></div>
  <section class="sec-2">

    <div>
    <div class="row">
      <div class="col-md-6">
        <h2>Investment Resources</h2>
        <ul>
          <li><a href="https://www.easyequities.co.za/">easyEquities</a></li>
          <li><a href="https://www.investor.co.za/">Investor.co.za</a></li>
          <li><a href="https://www.moneyweb.co.za/">Moneyweb</a></li>
        </ul>
      </div>
      <div class="col-md-6">
        <h2>JSE Top 100 Companies</h2>
        <ul>
          <li v-for="company in topCompanies" :key="company.id">{{ company.name }}</li>
        </ul>
      </div>
    </div>
    <div class="row">
      <div class="col-md-12">
        <h2>Recent Investment News and Trends</h2>
        <div id="news-carousel" class="carousel slide" data-ride="carousel">
          <div class="carousel-inner">
            <div v-for="(article, index) in recentNews" :key="article.id" :class="{ 'carousel-item': true, 'active': index === 0 }">
              <h3>{{ article.title }}</h3>
              <p>{{ article.description }}</p>
              <a :href="article.url">Read more</a>
            </div>
          </div>
          <a class="carousel-control-prev" href="#news-carousel" role="button" data-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="sr-only">Previous</span>
          </a>
          <a class="carousel-control-next" href="#news-carousel" role="button" data-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="sr-only">Next</span>
          </a>
        </div>
      </div>
    </div>
  </div>

    
  </section>

  <section class="sec-3">

  </section>

</template>

<script>
import Resources from '@/components/Resources.vue';
export default {
  name: "HomeView",
  component: {
    Resources
  },
  data() {
    return {
      topCompanies: [
        { id: 1, name: 'Company 1' },
        { id: 2, name: 'Company 2' },
        { id: 3, name: 'Company 3' },
        { id: 4, name: 'Company 4' },
        { id: 5, name: 'Company 5' },
      ],
      recentNews: [
        { id: 1, title: 'Article 1', description: 'Lorem ipsum dolor sit amet.', url: '#' },
        { id: 2, title: 'Article 2', description: 'Lorem ipsum dolor sit amet.', url: '#' },
        { id: 3, title: 'Article 3', description: 'Lorem ipsum dolor sit amet.', url: '#' },
      ],
    }
  }
}
</script>

<style scoped>
section {
  width: 100%;
  min-height: calc(100vh - 60px);
  scroll-margin-top: 100px;

  /* background-image: url('https://i.postimg.cc/SsKq5rC7/top-view-dark-modern-workplace-open-laptop.jpg'); */
  background-attachment: fixed;
  background-size: cover;
}
.section-overlay {
  width: 100%;
  min-height: inherit;
  height: 100%;
}
section:nth-child(odd) .section-overlay {
  background-color: rgba(0, 0, 0, 0.5);
}
section:nth-child(even) .section-overlay {
  background-color: rgba(0, 0, 0, 0.35);
}
section.sec-1 {
  background-image: url('https://i.postimg.cc/05dBYjBh/towfiqu-barbhuiya-joq-WSI9u-XM-unsplash.jpg');
  background-attachment: fixed;
  background-size: cover;
}
section.sec-2{
  /* background-image: url('https://i.postimg.cc/4dcKMWXH/jeshoots-com-unsplash-white-desk.jpg'); */
  background-attachment: fixed;
  background-size: cover;
}
section.sec-3 {
  background: url('https://i.postimg.cc/Dz84Q2Dg/georgie-cobbs-unsplash-white-wall-desk.jpg') no-repeat center center;
  background-attachment: fixed;
  background-size: cover;
}

div.banner {
  background-color: rgba(255, 255, 255, 0.6);
  width: 80%;
  height: 300px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin: 5px auto;
}
div.banner>* {
  padding: 5px;
}

div.col-md-6:first-child {
  background-color: #f2f2f2;
  padding: 20px;
}

/* Style the JSE Top 100 Companies section */
div.col-md-6:last-child {
  background-color: #f2f2f2;
  padding: 20px;
}

/* Style the Recent Investment News and Trends section */
div.col-md-12 {
  background-color: #f2f2f2;
  padding: 20px;
}

/* Style the carousel */
div#news-carousel {
  margin-top: 20px;
}

/* Style the carousel items */
div.carousel-item {
  text-align: center;
}

/* Style the carousel controls */
div.carousel-control-prev,
div.carousel-control-next {
  width: auto;
  height: auto;
  background-color: transparent;
}
</style>
