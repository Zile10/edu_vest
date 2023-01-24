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
  background-image: url('https://i.postimg.cc/05dBYjBh/towfiqu-barbhuiya-joq-WSI9u-XM-unsplash.jpg');
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
</style>
