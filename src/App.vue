<template>
  
  <!-- Start Header -->
  <header class="text-gray-600 fixed w-full z-50 top-0 left-0">
    <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
      <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
        <!-- TODO: Site logo -->
        <!-- <svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-10 h-10 text-white p-2 bg-indigo-500 rounded-full" viewBox="0 0 24 24">
          <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path>
        </svg> -->
        <span class="ml-3 text-xl">Piotr Szewczyk</span>
      </a>
      <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
        <!-- TODO: Menu -->
        <!-- <a class="mr-5 hover:text-gray-900">->home()</a>
        <a class="mr-5 hover:text-gray-900">->about()</a>
        <a class="mr-5 hover:text-gray-900">->contact()</a> -->
      </nav>
    </div>
  </header>
  <!-- End Header -->

  <!-- <section class="container mx-auto z-1">
    <div class="sm:items-center md:w-2/3 mx-auto">
      <div class="fixed top-1/2 h-full">
        <div class="bg-gray-100 w-2 h-full rounded"></div>
      </div>
    </div>
  </section> -->

  <!-- <section class="z-0 scene-0 fixed flex" style="height:100vh">
    <div class="self-center">Test</div>
  </section> -->

  <section class="h-screen flex">
    <div class="container mx-auto flex px-5 py-24 md:flex-row items-center">
      <div class="flex mx-auto">
        <div class="flex flex-col items-center" data-slide='1'>
          <span class="scene-1-title-1 text-5xl font-black">Piotr Szewczyk</span><br>
          <span class="scene-1-title-3 font-normal text-2xl">PHP Developer / Software Tester</span>
          <a class="a-liquid mt-6" href="/CV.pdf"><span>Zobacz CV</span><div class="liquid"></div></a>
        </div>
      </div>
      <!-- <div class="flex md:w-2/3 mx-auto">
        <div class="md:pl-8 pl-6 flex">
          <div class="self-center">
            
          </div>
        </div>
      </div> -->
    </div>
  </section>

  <!-- <section class="z-0 scene-2 flex" style="height:100vh;">
    <div class="container mx-auto flex">
      <div class="flex md:w-2/3 mx-auto">
        <div class="md:pl-8 pl-6 flex">
          <div class="self-center">
            <div data-slide='2'>
              <span class="scene-1-title-1 text-5xl font-black">MyCV RegEx("\*-x()#")</span>
            </div>
            <div data-slide='3'>
              <span class="scene-1-title-2 font-normal text-3xl">\\\ShowMe\\\\</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="z-0 scene-3 flex" style="height:100vh;">
    <div class="container mx-auto flex">
      <div class="flex md:w-2/3 mx-auto">
        <div class="md:pl-8 pl-6 flex">
          <div class="self-center">
            <div data-slide='4'>
              <span class="scene-1-title-1 text-5xl font-black">Test1 test test test.</span>
            </div>
            <div data-slide='5'>
              <span class="scene-1-title-2 font-normal text-3xl">Test2 test test test test test test.</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="z-0 scene-4 flex" style="height:100vh;">
    <div class="container mx-auto flex">
      <div class="flex md:w-2/3 mx-auto">
        <div class="md:pl-8 pl-6 flex">
          <div class="self-center">
            <div data-slide='6'>
              <span class="scene-1-title-1 text-5xl font-black">tools, modules, integrations, and custom projects</span>
            </div>
            <div data-slide='7'>
              <span class="scene-1-title-2 font-normal text-3xl">for Insurance company.</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section> -->
</template>

<script setup>

import { gsap } from "gsap";
import { Flip } from "gsap/Flip";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import { Observer } from "gsap/Observer";
import { ScrollToPlugin } from "gsap/ScrollToPlugin";
import { Draggable } from "gsap/Draggable";
import { EaselPlugin } from "gsap/EaselPlugin";
import { MotionPathPlugin } from "gsap/MotionPathPlugin";
import { PixiPlugin } from "gsap/PixiPlugin";
import { TextPlugin } from "gsap/TextPlugin";
import {onMounted} from "vue";

gsap.registerPlugin(Flip, ScrollTrigger, Observer, ScrollToPlugin, Draggable, EaselPlugin, MotionPathPlugin, PixiPlugin, TextPlugin);

onMounted(() => {

  // const timeline2 = gsap.timeline({
  //   scrollTrigger: {
  //     trigger: ".scene-1",
  //     start: "top top",
  //     scrub: 0,
  //     pin: ".scene-1",
  //     // markers: true,
  //     pinSpacing: false,
  //     // end: "+=1000",
  //     toggleActions: "play pause play reset",
  //     // smoothOrigin: true,
  //   }
  // });
  // timeline2
  //     .to("[data-slide='1']", {
  //       opacity: 0,
  //       duration: 2,
  //       y: "-30vh"
  //     });

  // const timeline1 = gsap.timeline({
  //   scrollTrigger: {
  //     trigger: ".scene-2",
  //     start: "top top",
  //     scrub: 0,
  //     pin: ".scene-2",
  //     // markers: true,
  //     // pinSpacing: false,
  //     // end: "+=1000",
  //     toggleActions: "play pause play reset"
  //   }
  // });
  // timeline1
  //     .from("[data-slide='2']", {
  //       opacity: 0,
  //       duration: 3,
  //       y: -100,
  //     })
  //     .from("[data-slide='3']", {
  //       opacity: 0,
  //       duration: 3,
  //       y: 100,
  //     }, "-=3");


  //
  // gsap
  //     .timeline({
  //       scrollTrigger: {
  //         trigger: ".img",
  //         // markers: true,
  //         pin: true,
  //         start: "top top",
  //         end: "bottom top",
  //         scrub: true
  //       }
  //     })
  //     .fromTo(
  //         ".img",
  //         {
  //           scale: 1,
  //           y: 0
  //         },
  //         {
  //           scale: 1.1,
  //           y: -200
  //         }
  //     );


});


</script>

<style scoped>


/* CSS Liquid Button */
.a-liquid {
  position: relative;
  padding: 10px 30px;
  display: block;
  width: 200px;
  overflow: hidden;
  border-radius: 40px;
}
.a-liquid span {
  position: relative;
  display: block;
  text-align: center;
  color: #fff;
  font-size: 20px;
  letter-spacing: 2px;
  z-index: 1;
}
.a-liquid .liquid {
  position: absolute;
  top: -90px;
  left: 0;
  width: 200px;
  height: 200px;
  background: #7949ff;
  box-shadow: inset 0 0 50px rgba(0, 0, 0, .5);
  transition: .5s;
}
.a-liquid .liquid::after,
.a-liquid .liquid::before {
  content: '';
  position: absolute;
  top: 0;
  left: 50%;
  width: 200%;
  height: 200%;
  background: #000;
  transform: translate(-50%, -75%);
}

.a-liquid .liquid::before {
  border-radius: 45%;
  background: #401f9c;
  animation: animate 5s linear infinite;
}

.a-liquid .liquid::after {
  border-radius: 40%;
  background: rgba(20, 20, 20, .5);
  animation: animate 10s linear infinite;
}

.a-liquid:hover .liquid {
  top: -120px;
}

@keyframes animate {
  0% {
    transform: translate(-50%, -75%) rotate(0deg);
  }
  100% {
    transform: translate(-50%, -75%) rotate(360deg);
  }
}



</style>
