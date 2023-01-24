<template>
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
</template>

<script>
export default {
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
  /* Style the Investment Resources section */
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