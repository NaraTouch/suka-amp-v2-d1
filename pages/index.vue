<template>
  <section >
    <div class="container">
      <div class="header">
        <Header />
      </div>

      <!-- <div class="test"> -->
        <main class="main container-div">
            <RunningText />
            <NavImageGame />
            <RunningImage />
            <!-- <MultipleCarousel /> -->
        </main>
        
         <div class="tab-winner">
           <TabWinner />
        </div>
        <div class="image-slider"> 
          <Slider />
        </div>
        <div class="connection">
          <Connection />
        </div>
        <div class="content-text">
          <ContentText />
        </div>
        <div class="sidebar-right container-div">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusamus, beatae perferendis animi eveniet maxime voluptatibus sapiente suscipit provident? Magni beatae laboriosam eos blanditiis doloribus atque aspernatur magnam voluptatum ea ipsum!</p>
        </div>
       
      <!-- </div> -->

      <footer>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio voluptate possimus placeat repellendus a officiis, est temporibus laborum reiciendis reprehenderit vel veritatis perspiciatis, quod in, rerum quae natus earum tempore.</p>
      </footer>
    </div>
  </section>
</template>

<script>
export default {
  components: {
    Navigation: () => import('../components/Navigation'),
    RunningImage: () => import('../components/RunningImage'),
    MultipleCarousel: () => import('../components/MultipleCarousel'),
    Header: () => import('../components/header/Header'),
    RunningText: () => import('../components/RunningText'),
    NavImageGame: () => import('../components/body/NavImageGame'),
    TabWinner: () => import('../components/Tab/TabWinner'),
    Slider: () => import('../components/slider/Slider'),
    Connection: () => import('../components/connection/Connection'),
    ContentText: () => import('../components/content/ContentText'),
  },
  data() {
    return {
       count: 0,
       src: "../static/images/images.jpg",
    }
  },
  methods: {
    say: function (message) {
      alert(message)
    }
  },
  watch: {
     say: function (count) {
      alert(this.count)
    }
  },
}
</script>


<style lang="scss" scoped>

// slide menu
  .hamburger {
    padding-left: 10px;
    .sidebar {
      padding: 10px;
      margin: 0;
      .sidebar > li {
        list-style: none;
        margin-bottom:10px;
      }
      .sidebar a {
        text-decoration: none;
      }
      .close-sidebar {
        font-size: 1.5em;
        padding-left: 5px;
      }
      p {
        color: red;
      }
    }
  }

  .container {
    display: grid;        
    grid-template-columns: repeat(4, 1fr); 
    grid-template-rows: 0.1fr 0.5fr 1.2fr 1.2fr; 
    grid-template-areas:
    "header header header header"
    "main main main main"
    "tab-winner sidebar-right sidebar-right sidebar-right"
    "image-slider sidebar-right sidebar-right sidebar-right"
    "connection sidebar-right sidebar-right sidebar-right"
    "content-text sidebar-right sidebar-right sidebar-right"
    "footer footer footer footer";
    gap: 0.5rem;
    height: 100vh;
    font-weight: 800;
    font-size: 12px;
    color: #004d40;
    text-align: center;
    .header{
      background-color: #3770F6;
      grid-area: header;
    }
    .main{
      // background-color: red;
      grid-area: main;
    }
    .sidebar-right {
      background: #D3D4D7;
      grid-area: sidebar-right;
    }
    .tab-winner {
      background: $color-gray;
      grid-area: tab-winner;
      border-radius: 5px;
    }
    .image-slider {
      background: #BDBCBB;
      grid-area: image-slider;
      border-radius: 5px;
    }
    .connection {
      background: #BDBCBB;
      grid-area: connection;
      border-radius: 5px;
    }
    .content-text {
       background: #BDBCBB;
      grid-area: content-text;
      border-radius: 5px;
    }
    .body {
      margin: 0px 20px;
    }
    footer {
      background-color: #3770F6;
      grid-area: footer;
      color: #ffffff;
    }
    .container-div {
      margin: 0px 20px;
    }
  }

</style>
