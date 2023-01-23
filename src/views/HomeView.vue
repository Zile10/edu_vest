<template>
  <section class="sec-1">
    <h2>Welcome!</h2>
    <h4>To The Greatest Investment of Your Life</h4>
  
    <h3>EduVest! Investing into your future!</h3>

    <h1>{{ this.newsData.data }}</h1>

  </section>
    <div></div>
  <section class="sec-2">

  </section>

  <section class="sec-3">

  </section>

</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      newsData: []
    }
  },
  mounted(){
    let myHeaders = new Headers();
    myHeaders.append("apikey", "ZPISKsnKbSIuqu7h2V3QN5hfCafJQYWd");

    let requestOptions = {
      method: 'GET',
      redirect: 'follow',
      headers: myHeaders
    };

    fetch("https://api.apilayer.com/financelayer/news?tickers=btc&tags=money&sources=default&sort=desc&offset=0&limit=25&keywords=investment&fallback=on&date=thismonth", requestOptions)
      .then(response => response.text())
      .then(result => this.newsData = JSON.parse(result))
      .catch(error => console.log('error', error));
    
  }
};
</script>

<style>
section {
  width: 100%;
  min-height: calc(100vh - 60px);
  scroll-margin-top: 100px;

  background-image: url('https://i.postimg.cc/SsKq5rC7/top-view-dark-modern-workplace-open-laptop.jpg');
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
  background-image: url('https://i.postimg.cc/7LdGmFry/lauren-mancke-unsplash-white-desk.jpg');
  background-attachment: fixed;
  background-size: cover;
}
section.sec-2{
  background-image: url('https://i.postimg.cc/4dcKMWXH/jeshoots-com-unsplash-white-desk.jpg');
  background-attachment: fixed;
  background-size: cover;
}
section.sec-3 {
  background: url('https://i.postimg.cc/Dz84Q2Dg/georgie-cobbs-unsplash-white-wall-desk.jpg') no-repeat center center;
  background-attachment: fixed;
  background-size: cover;
}
</style>
