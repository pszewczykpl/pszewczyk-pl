<template>
  <header class="text-gray-600 body-font top-0 fixed z-50 w-full items-center insert-x-0">
    <div class="flex">
      <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center insert-x-0 items-center w-full">
        <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
          <span class="ml-3 text-xl">.ps</span>
        </a>
        <div class="md:ml-auto md:mr-auto">

        </div>
        <div class="flex flex-wrap items-center text-base justify-center">
          <nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
            <a class="mr-5 hover:text-gray-900" style="color: royalblue">.o_mnie()</a>
            <a class="mr-5 hover:text-gray-900">.kontakt()</a>
            <a class="mr-5 hover:text-gray-900">.email()</a>
            <a class="mr-5 hover:text-gray-900">GH</a>
          </nav>
        </div>
      </div>
    </div>
  </header>

  <section class="container mx-auto z-1">
    <div class="sm:items-center md:w-2/3 mx-auto">
      <div class="fixed top-1/2 h-full">
        <div class="bg-gray-100 w-2 h-full rounded"></div>
      </div>
    </div>
  </section>

  <section class="z-0 scene-0 fixed flex" style="height:100vh">
    <div class="self-center">Test</div>
  </section>

  <section class="z-0 scene-1 flex" style="height:100vh;">
    <div class="container mx-auto flex">
      <div class="flex md:w-2/3 mx-auto">
        <div class="md:pl-8 pl-6 flex">
          <div class="self-center">
            <div data-slide='1'>
              <span class="scene-1-title-1 text-5xl font-black">pszewczyk.pl()</span><br>
              <span class="scene-1-title-2 font-normal text-3xl">Piotr Szewczyk</span><br>
              <span class="scene-1-title-3 font-normal text-3xl">PHP Developer / QA Tester</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="z-0 scene-2 flex" style="height:100vh;">
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
  </section>
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

  const timeline2 = gsap.timeline({
    scrollTrigger: {
      trigger: ".scene-1",
      start: "top top",
      scrub: 0,
      pin: ".scene-1",
      // markers: true,
      pinSpacing: false,
      // end: "+=1000",
      toggleActions: "play pause play reset",
      // smoothOrigin: true,
    }
  });
  timeline2
      .to("[data-slide='1']", {
        opacity: 0,
        duration: 2,
        y: "-30vh"
      });

  const timeline1 = gsap.timeline({
    scrollTrigger: {
      trigger: ".scene-2",
      start: "top top",
      scrub: 0,
      pin: ".scene-2",
      // markers: true,
      // pinSpacing: false,
      // end: "+=1000",
      toggleActions: "play pause play reset"
    }
  });
  timeline1
      .from("[data-slide='2']", {
        opacity: 0,
        duration: 3,
        y: -100,
      })
      .from("[data-slide='3']", {
        opacity: 0,
        duration: 3,
        y: 100,
      }, "-=3");


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

</style>
