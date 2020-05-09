<template>
   <div>
      <div id="app">
         <div class="container">
            <nav class="navbar navbar-expand-lg navbar-light">
               <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
                  <img src="../src/assets/images/navbar/logos.png" alt="" />
                  <div class="navbar-logos">
                     Waxom
                  </div>
                  <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
                     <li
                        v-for="list in lists"
                        :key="list"
                        class="nav-item active"
                     >
                        <a class="nav-link" href="#">{{ list }} </a>
                     </li>
                     <div class="navbar-icons">
                        <img
                           src="../src/assets/images/navbar/icon-cart.png"
                           alt=""
                        />
                        <img
                           style="padding-left: 30px"
                           src="../src/assets/images/navbar/icon-search.png"
                           alt=""
                        />
                     </div>
                  </ul>
               </div>
            </nav>
         </div>
         <div>
            <b-carousel
               id="carousel-1"
               v-model="slide"
               :interval="4000"
               controls
               indicators
               background="none"
               img-width="1024"
               img-height="480"
               style="text-shadow: 1px 1px 2px #333;"
               @sliding-start="onSlideStart"
               @sliding-end="onSlideEnd"
            >
               <b-carousel-slide
                  v-for="text in sliders"
                  :key="text.title"
                  caption="Unique and modern design"
                  img-blank
               >
                  <p class="carousel-title">{{ text.title }}</p>
                  <p class="carousel-text">
                     {{ text.description }}
                  </p>
                  <button>Get started</button>
               </b-carousel-slide>
            </b-carousel>
         </div>
      </div>
      <b-row cols="1" cols-sm="2" cols-md="2" cols-lg="6">
         <b-col v-for="bodyc in bodycontent" :key="bodyc.src">
            <div>
               <div class="d-flex justify-content-center">
                  <img class="mb-3" :src="bodyc.src" alt="" />
               </div>
               <p class="text-center bodycname">
                  {{ bodyc.name }}
               </p>
               <p class="text-center bodycsubname">
                  {{ bodyc.subname }}
               </p>
            </div>
         </b-col>
      </b-row>
      <div>
         <div
            style="background-color: #fbfaf8; position: relative"
            class="pt-5"
         >
            <h1 class="text-center poop1">
               Waxom is Realization of yours ideals.
            </h1>

            <p class="text-center poop2">
               Lorem, ipsum dolor sit amet consectetur adipisicing elit. Minus
               tempore vitae natus quibusdam aliquid harum nihil quae facilis
               cum incidunt.
            </p>

            <div class="hand-carousel">
               <b-img-lazy
                  v-bind="mainProps"
                  :src="getImageUrl(80)"
                  alt="Image 1"
               ></b-img-lazy>
            </div>
         </div>
      </div>
      <div class="Waxom-multipress d-flex justify-content-around w-100">
         <div style="width: 93%" class=" d-flex justify-content-around">
            <div>
               <h1>
                  <span style="color: brown">Waxom</span> multipurpose WordPress
                  Theme
               </h1>
               <p>
                  Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                  Ipsa, nesciunt!
               </p>
            </div>

            <button>Purchase now</button>
         </div>
      </div>
      <div style="background-color: white; " class="pt-5">
         <h1 class="text-center poop1">
            Our Latest Projects.
         </h1>

         <p class="text-center poop2">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Minus
            tempore vitae natus quibusdam aliquid harum nihil quae facilis cum
            incidunt.
         </p>
         <div class="d-flex justify-content-center latest-project">
            <button>All</button>
            <button>Web Design</button>
            <button>Mobile App</button>
            <button>Illustration</button>
            <button>Photography</button>
         </div>
         <div class="d-flex justify-content-center">
            <b-card-group deck>
               <div>
                  <b-row class="card-row" cols="1" cols-md="4" cols-sm="1">
                     <b-col v-for="n of projects" :key="n">
                        <b-card
                           :title="n.titleimage"
                           :img-src="n.image"
                           img-alt="Image"
                           img-top
                        >
                           <b-card-text>
                              {{ n.subtitleimage }}
                           </b-card-text>
                        </b-card></b-col
                     >
                  </b-row>
                  <b-row class="card-row" cols="1" cols-md="4" cols-sm="1">
                     <b-col v-for="t of projectssame" :key="t">
                        <b-card
                           :title="t.titleimage"
                           :img-src="t.image"
                           img-alt="Image"
                           img-top
                        >
                           <b-card-text>
                              {{ t.subtitleimage }}
                           </b-card-text>
                        </b-card></b-col
                     >
                  </b-row>
                  <div class="d-flex justify-content-center mt-5 mb-5">
                     <button>Load more</button>
                  </div>
               </div>
            </b-card-group>
         </div>
         <div class="w-100">
            <youtube
               player-width="100%"
               player-height="705px;"
               :video-id="youtubeID"
            ></youtube>
         </div>
         <div class="handmobile ">
            <div class="d-flex justify-content-center align-items-center">
               <div class="handmobiletext" style="width: 80%">
                  <b-row cols="1" cols-sm="12" cols-md="2" cols-lg="12">
                     <b-col>
                        <img :src="iPhoneinhand" width="350" height="500" />
                     </b-col>

                     <b-col>
                        <h1>Exellent for Mobile Devices.</h1>

                        <p>
                           Lorem ipsum dolor sit, amet consectetur adipisicing
                           elit. Quos veniam officiis provident a? Qui,
                           molestiae. Perferendis tempora sed, molestias nihil
                           voluptates ducimus cumque blanditiis, asperiores
                           rerum et cupiditate quod voluptatibus. Nihil ab a ex
                           nostrum facilis fugiat aliquam quam consectetur!
                        </p>
                        <ul class="mt-5">
                           <li>
                              <img :src="iconarrow" alt="" />
                              Lorem ipsum dolor sit amet, consectetur
                              adipisicing elit.
                           </li>
                           <li>
                              <img :src="iconarrow" alt="" />
                              Lorem ipsum dolor sit amet, consectetur
                              adipisicing elit. Cupiditate?
                           </li>
                           <li>
                              <img :src="iconarrow" alt="" />
                              Lorem ipsum dolor sit amet, consectetur
                              adipisicing elit. Cup.
                           </li>
                           <li>
                              <img :src="iconarrow" alt="" />
                              Lorem ipsum dolor sit amet, consectetur
                              adipisicing.
                           </li>
                        </ul>
                     </b-col>
                  </b-row>
               </div>
            </div>
         </div>
         <div
            class="eat d-flex justify-content-center "
            style="padding-bottom: 70px"
         >
            <b-row
               cols="2"
               cols-sm="3"
               cols-md="3"
               cols-lg="5"
               style="width: 80%"
            >
               <b-col>
                  <div class="d-flex justify-content-center">
                     <img
                        class="mb-3 ttt"
                        src="../src/assets/images/body-icons/person.png"
                        alt=""
                     />
                  </div>
                  <div>
                     <p class="cifr">3578</p>
                     <p class="cifrtext">Suticfacted clients</p>
                  </div>
               </b-col>
               <b-col>
                  <div class="d-flex justify-content-center">
                     <img
                        class="mb-3"
                        src="../src/assets/images/body-icons/caffe.png"
                        alt=""
                     />
                  </div>
                  <div>
                     <p class="cifr">3578</p>
                     <p class="cifrtext">Suticfacted clients</p>
                  </div>
               </b-col>
               <b-col>
                  <div class="d-flex justify-content-center">
                     <img
                        class="mb-3"
                        src="../src/assets/images/body-icons/message.png"
                        alt=""
                     />
                  </div>
                  <div>
                     <p class="cifr">3578</p>
                     <p class="cifrtext">Suticfacted clients</p>
                  </div>
               </b-col>
               <b-col>
                  <div class="d-flex justify-content-center">
                     <img
                        class="mb-3"
                        src="../src/assets/images/body-icons/heart.png"
                        alt=""
                     />
                  </div>
                  <div>
                     <p class="cifr">3578</p>
                     <p class="cifrtext">Suticfacted clients</p>
                  </div>
               </b-col>
               <b-col>
                  <div class="d-flex justify-content-center">
                     <img
                        class="mb-3"
                        src="../src/assets/images/body-icons/ringar.png"
                        alt=""
                     />
                  </div>
                  <div>
                     <p class="cifr">3578</p>
                     <p class="cifrtext">Suticfacted clients</p>
                  </div>
               </b-col>
            </b-row>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   data() {
      return {
         iconarrow: require("./assets/images/01.png"),
         iPhoneinhand: require("./assets/images/iPhoneinhand.png"),
         youtubeID: "ynz3eMM73Jg",
         projects: [
            {
               titleimage: "Claritas Etiam Processus",
               subtitleimage: "Photography Nature",
               image: require("./assets/images/projects/project01.png"),
            },
            {
               titleimage: "Quam Nutamus Farum",
               subtitleimage: "Grachic Design mark Up",
               image: require("./assets/images/projects/project02.png"),
            },
            {
               titleimage: "Usus Ligentis Vidtntur",
               subtitleimage: "Photography Holiday",
               image: require("./assets/images/projects/project03.png"),
            },
         ],
         projectssame: [
            {
               titleimage: "Claritas Etiam Processus",
               subtitleimage: "Photography Nature",
               image: require("./assets/images/projects/project04.png"),
            },
            {
               titleimage: "Quam Nutamus Farum",
               subtitleimage: "Grachic Design mark Up",
               image: require("./assets/images/projects/project05.png"),
            },
            {
               titleimage: "Usus Ligentis Vidtntur",
               subtitleimage: "Photography Holiday",
               image: require("./assets/images/projects/project06.png"),
            },
         ],

         mainProps: {
            center: true,
            fluidGrow: true,
            blank: true,
            blankColor: "#bbb",
            width: 900,
            height: 400,
            class: "my-5",
         },
         slide: 0,

         sliding: null,
         bodycontent: [
            {
               name: "Web & App Design",
               subname:
                  " Lorem ipsum, dolor sit amet consectetur adipisici elit. Doloribus velit, illum ab provident.",
               src: require("./assets/images/body-icons/pencil.png"),
            },
            {
               name: "Development",
               subname:
                  " Lorem ipsum, dolor sit amet consectetur adipisici elit. Doloribus velit, illum ab provident.",
               src: require("./assets/images/body-icons/development.png"),
            },
            {
               name: "Web Design",
               subname:
                  " Lorem ipsum, dolor sit amet consectetur adipisici elit. Doloribus velit, illum ab provident.",
               src: require("./assets/images/body-icons/customization.png"),
            },
            {
               name: "Customization",
               subname:
                  " Lorem ipsum, dolor sit amet consectetur adipisici elit. Doloribus velit, illum ab provident.",
               src: require("./assets/images/body-icons/marketing.png"),
            },
         ],
         sliders: [
            {
               title: "Marketing",
               description:
                  "Lorem ipsum dolor sit amet, consectetur adipiscing elit.Suspendisse eros felis, tincidunt a tincidunt eget, convalli vel est. Ut pellentesque ut lacus vel interdum.",
            },
            {
               title: "Portfolio pcd template1",
               description:
                  "1Lorem ipsum dolor sit amet, consectetur adipiscing elit.Suspendisse eros felis, tincidunt a tincidunt eget, convalli vel est. Ut pellentesque ut lacus vel interdum.",
            },
            {
               title: "Portfolio pcd template2",
               description:
                  "2Lorem ipsum dolor sit amet, consectetur adipiscing elit.Suspendisse eros felis, tincidunt a tincidunt eget, convalli vel est. Ut pellentesque ut lacus vel interdum.",
            },
            {
               title: "Portfolio pcd template3",
               description:
                  "3Lorem ipsum dolor sit amet, consectetur adipiscing elit.Suspendisse eros felis, tincidunt a tincidunt eget, convalli vel est. Ut pellentesque ut lacus vel interdum.",
            },
            {
               title: "Portfolio pcd template4",
               description:
                  "4Lorem ipsum dolor sit amet, consectetur adipiscing elit.Suspendisse eros felis, tincidunt a tincidunt eget, convalli vel est. Ut pellentesque ut lacus vel interdum.",
            },
            {
               title: "Portfolio pcd template5",
               description:
                  "5Lorem ipsum dolor sit amet, consectetur adipiscing elit.Suspendisse eros felis, tincidunt a tincidunt eget, convalli vel est. Ut pellentesque ut lacus vel interdum.",
            },
         ],
         lists: [
            "Home",
            "About us",
            "Portfolio",
            "Features",
            "Blog",
            "Pricing",
            "Shortcodes",
            "Contact",
         ],
      };
   },

   methods: {
      onSlideStart(slide) {
         this.sliding = true;
      },
      onSlideEnd(slide) {
         this.sliding = false;
      },
      getImageUrl(imageId) {
         const { width, height } = this.mainProps;
         return `https://picsum.photos/${width}/${height}/?image=${imageId}`;
      },
   },
};
</script>

<style lang="scss">
.row {
   background: transparent !important;
}
.cifr {
   font-size: 48px;
   line-height: 36px;
   color: #ffffff;
   font-family: "Montserrat";
   font-weight: 300;
   text-align: center;
}
.cifrtext {
   font-size: 14px;
   line-height: 20px;
   color: #c7b299;
   font-family: "Montserrat";
   font-weight: 300;
   text-align: center;
   position: relative;
}

.cifrtext:after {
   content: "";
   position: absolute;
   width: 30px;
   height: 2px;
   background-color: #ffffff;
   top: 40px;

   right: 50px;
   background: white;
}

@media (max-width: 991px) {
   .cifrtext:after {
      display: none;
   }
}
.eat {
   background: linear-gradient(90deg, #211b19 0%, #4e3326 100%);
}
li {
   list-style: none;
}
.bodycname {
   font-size: 22px;
   color: #555555;

   font-weight: 600;
   text-align: center;
}
.bodycsubname {
   font-size: 14px;
   line-height: 24px;
   color: #8c8c8c;
   font-family: "Montserrat";
   font-weight: 300;
   text-align: center;
}
.card-row .col {
   margin-top: 30px !important;
}
.latest-project button {
   margin-left: 10px;
   font-size: 14px;
   line-height: 21px;
   color: #8c8c8c;
   font-family: "Montserrat";
   font-weight: 300;
   text-align: center;
   display: inline-block;
   height: 32px !important;
   border-radius: 3px;
   background-color: transparent;
}
.latest-project button:focus {
   color: white;
   outline: none;
   background-color: #998575;
}
@media (min-width: 992px) {
   .row-cols-lg-6 > * {
      -ms-flex: 0 0 16.666667%;
      flex: 0 0 17.5%;
      max-width: 19%;
   }
}
.Waxom-multipress {
   position: relative;
   background-image: linear-gradient(90deg, #211b19 0%, #4e3326 100%);
   padding: 20px 0;
   align-items: center;
}
.Waxom-multipress h1 {
   font-size: 28px;
   color: #c7b299;
   font-family: "Raleway";
   font-weight: 400;
}
.Waxom-multipress p {
   font-size: 18px;
   color: #615855;
   font-family: "Montserrat";
   font-weight: 300;
}
.hand-carousel {
   position: relative;
   justify-content: center;
   display: flex;
}

.hand-carousel .img-fluid {
   position: relative;
   max-width: 1000px;

   cursor: pointer;
}

.col {
   margin-top: 100px;
}

.row {
   background: white;
   display: flex;
   justify-content: center;
   align-items: center;
}
@media (min-width: 1200px) {
   .container,
   .container-lg,
   .container-md,
   .container-sm,
   .container-xl {
      max-width: 1240px;
      position: relative;
   }
}
body {
   overflow-x: hidden;
}
.carousel-control-prev-icon {
   background-image: url("../src/assets/images/left.png");
   display: inline-block;
   width: 40px;
   height: 73px;
   border-radius: 36px;
   color: #d3c1ac;
}
.carousel-control-next-icon {
   background-image: url("../src/assets/images/right.png");
   display: inline-block;
   width: 40px;
   height: 73px;
   border-radius: 36px;
   color: #d3c1ac;
}
#app {
   position: relative;
   background-image: url("../src/assets/images/bg.png");
   background-position: center;
   background-repeat: no-repeat;
   background-size: cover;
}

.next {
   position: absolute;
   width: 1150px;
   margin-top: 100px;
}

.carousel-indicators li {
   border-radius: 100%;
   -ms-flex: 0 1 auto;
   flex: 0 1 auto;
   width: 10px;
   height: 10px;
   margin-right: 3px;
   margin-left: 3px;
   text-indent: -999px;
   cursor: pointer;
   background-color: #fff;
   background-clip: padding-box;
   border-top: none;

   border-bottom: none;
   opacity: 0.5;
   transition: opacity 0.6s ease;
}

.nav-link {
   color: white !important;
}

.nav-link:hover {
   color: #918474 !important;
}

@media (min-width: 992px) {
   .navbar-expand-lg .navbar-nav .nav-link {
      padding-right: 15px;
      padding-left: 15px;
   }
}

.navbar-logos {
   padding-right: 180px;
   font-size: 34px;
   letter-spacing: -1px;
   color: #ffffff;
   font-family: "Raleway";
   font-weight: 400;
   text-align: right;
}

li a {
   font-size: 15px;
}
li a:hover {
   color: #918474;
}

.nav-item .nav-link:focus {
   color: #918474 !important;
}

.navbar-icons {
   margin-left: 61px;
}

.carousel-caption {
   position: absolute;
   bottom: 230px;
   left: 30.5%;
   z-index: 10;
   width: 596px;
   height: 317px;
   color: #fff;
   text-align: center;
}

.carousel-title {
   font-size: 52px;
   color: #ffffff;
   font-family: "Raleway";
   font-weight: 800;
   text-align: center;
}
.carousel-text {
   font-size: 16px;
   line-height: 24px;
   color: #ffffff;
   font-family: "Montserrat";
   font-weight: 300;
   width: 571px;
   height: 58px;
   text-align: center;
}

button {
   width: 170px;
   height: 53px;
   border-radius: 3px;
   background-color: #988574;
}

.poop1 {
   font-size: 30px;
   color: #555555;
   font-family: "Raleway";
   font-weight: 600;
}

.poop2 {
   font-size: 16px;
   line-height: 28px;
   color: #8c8c8c;
   font-family: "Montserrat";
   font-weight: 300;
}
</style>
