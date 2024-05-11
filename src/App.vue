<template>
  <div id="app">
    <Header :name=headerTopic :corporation=corporation :barner=barnerSentence></Header>
    <!-- ↓こいつが必要 -->
    <router-view :newsList=setNewsList />    
    <Footer :name=headerTopic :corporation=corporation></Footer>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/HeaderComponent.vue'
import Footer from './components/FooterComponent.vue'
import 'normalize.css'

export default {
  name: 'App',
  data:function(){
    return {
      corporation:"株式会社 DXPRO",
      // headerTopic:"お問い合わせ"
      headerTopic:["トップページ","会社案内","お問い合わせ","事業紹介","掲示板","会社実績"],
      // footerTopic:{contact:"お問い合わせ",aboutUs:"私たちの活動",diary:"プログラミング日記",result:"開発実績"}
      barnerSentence:"当サイトにお越しいただき、誠にありがとうございます.",
      setNewsList:[{date:"2022/05/13",category:"お知らせ",title:"ブログを作成いたしました"},{date:"2022/11/16",category:"お知らせ",title:"ブログを更新いたしました"}]
      //router-viewにpropするのは大丈夫でした
    }
  },
  components: {
    Header,Footer
  }
}

</script>

<style>
    p {
        margin:0;
    }
    li{
      list-style: none;
      
    }
    a{
      text-decoration:none;
    }

</style>
