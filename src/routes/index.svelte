<script>
  import { onMount } from 'svelte';
import Layout from './__layout.svelte';

  onMount(async () => {    
    var scrollpos = window.scrollY;
    var header = document.getElementById("header");
    // var navcontent = document.getElementById("nav-content");
    // var navaction = document.getElementById("navAction");
    var toToggle = document.querySelectorAll(".toggleColour");

    document.addEventListener("scroll", function () {
      scrollpos = window.scrollY;

      if (scrollpos > 10) {
        header.classList.add("bg-white");
        // navaction.classList.remove("bg-white");
        // navaction.classList.add("gradient");
        // navaction.classList.remove("text-gray-800");
        // navaction.classList.add("text-white");
        //Use to switch toggleColour colours
        for (var i = 0; i < toToggle.length; i++) {
          toToggle[i].classList.add("text-gray-800");
          toToggle[i].classList.remove("text-white");
        }
        header.classList.add("shadow");
        // navcontent.classList.remove("bg-gray-100");
        // navcontent.classList.add("bg-white");
      } else {
        header.classList.remove("bg-white");
        // navaction.classList.remove("gradient");
        // navaction.classList.add("bg-white");
        // navaction.classList.remove("text-white");
        // navaction.classList.add("text-gray-800");
        //Use to switch toggleColour colours
        for (var i = 0; i < toToggle.length; i++) {
          toToggle[i].classList.add("text-white");
          toToggle[i].classList.remove("text-gray-800");
        }

        header.classList.remove("shadow");
        // navcontent.classList.remove("bg-white");
        // navcontent.classList.add("bg-gray-100");
      }
    });
  });
</script>

<nav id="header" class="fixed w-full z-30 top-0 text-white">
  <div class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2">
    <div class="pl-4 flex items-center">
      <a class="toggleColour text-white no-underline hover:no-underline font-bold text-2xl lg:text-4xl" href="#">
        LiviaAI
      </a>
    </div>
    
    <!--div class="block lg:hidden pr-4">
      <button id="nav-toggle" class="flex items-center p-1 text-pink-800 hover:text-gray-900 focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out">
        <svg class="fill-current h-6 w-6" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
      </button>
    </div -->
    <div class="w-full flex-grow lg:flex lg:items-center lg:w-auto hidden mt-2 lg:mt-0 bg-white lg:bg-transparent text-black p-4 lg:p-0 z-20" id="nav-content">
      <ul class="list-reset lg:flex justify-end flex-1 items-center">
        <li class="mr-3">
          <a class="inline-block py-2 px-4 text-black font-bold no-underline" href="/">Home</a>
        </li>
        <li class="mr-3">
          <a class="inline-block text-black no-underline hover:text-gray-800 hover:text-underline py-2 px-4" href="/blog/sample">Blog</a>
        </li>
      </ul>
      <!-- button
        id="navAction"
        class="mx-auto lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-full mt-4 lg:mt-0 py-4 px-8 shadow opacity-75 focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out"
      >
        Home
      </button -->
    </div>
  </div>
  <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
</nav>
<!--Hero-->
<div class="pt-24">
  <div class="container px-3 mx-auto flex flex-wrap flex-col md:flex-row items-center">
    <!--Left Col-->
    <div class="mb-8 flex flex-col w-full md:w-3/5 justify-center items-start text-center md:text-left">
      <p class="uppercase mt-10 tracking-loose w-full">Research Project</p>
      <h1 class="my-4 text-5xl font-bold leading-tight">
        Linking Viennese Art through AI
      </h1>
      <p class="leading-normal text-2xl mb-8">
        A research collaboration that investigates how Artificial Intelligence 
        can help interlink, navigate and analyse art collections.
      </p>
      <!-- button class="mx-auto lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-full my-6 py-4 px-8 shadow-lg focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out">
        Read more
      </button -->
    </div>
  </div>
</div>
<div class="relative -mt-12 lg:-mt-24">
  <svg viewBox="0 0 1428 174" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
    <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
      <g transform="translate(-2.000000, 44.000000)" fill="#FFFFFF" fill-rule="nonzero">
        <path d="M0,0 C90.7283404,0.927527913 147.912752,27.187927 291.910178,59.9119003 C387.908462,81.7278826 543.605069,89.334785 759,82.7326078 C469.336065,156.254352 216.336065,153.6679 0,74.9732496" opacity="0.100000001"></path>
        <path
          d="M100,104.708498 C277.413333,72.2345949 426.147877,52.5246657 546.203633,45.5787101 C666.259389,38.6327546 810.524845,41.7979068 979,55.0741668 C931.069965,56.122511 810.303266,74.8455141 616.699903,111.243176 C423.096539,147.640838 250.863238,145.462612 100,104.708498 Z"
          opacity="0.100000001"
        ></path>
        <path d="M1046,51.6521276 C1130.83045,29.328812 1279.08318,17.607883 1439,40.1656806 L1439,120 C1271.17211,77.9435312 1140.17211,55.1609071 1046,51.6521276 Z" id="Path-4" opacity="0.200000003"></path>
      </g>
      <g transform="translate(-4.000000, 76.000000)" fill="#FFFFFF" fill-rule="nonzero">
        <path
          d="M0.457,34.035 C57.086,53.198 98.208,65.809 123.822,71.865 C181.454,85.495 234.295,90.29 272.033,93.459 C311.355,96.759 396.635,95.801 461.025,91.663 C486.76,90.01 518.727,86.372 556.926,80.752 C595.747,74.596 622.372,70.008 636.799,66.991 C663.913,61.324 712.501,49.503 727.605,46.128 C780.47,34.317 818.839,22.532 856.324,15.904 C922.689,4.169 955.676,2.522 1011.185,0.432 C1060.705,1.477 1097.39,3.129 1121.236,5.387 C1161.703,9.219 1208.621,17.821 1235.4,22.304 C1285.855,30.748 1354.351,47.432 1440.886,72.354 L1441.191,104.352 L1.121,104.031 L0.457,34.035 Z"
        ></path>
      </g>
    </g>
  </svg>
</div>
<section class="bg-white py-8">
  <div class="container max-w-5xl mx-auto m-8">
    <h1 class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-800">
      LiviaAI
    </h1>
    <div class="w-full mb-4">
      <div class="h-1 mx-auto gradient w-64 opacity-25 my-0 py-0 rounded-t"></div>
    </div>
    <div class="flex flex-wrap">
      <div class="w-6/6 sm:w-2/2 p-6">
        <p class="text-gray-600 mb-12">
          LiviaAI is a research collaboration to investigate the potential of artificial intelligence (AI) 
          to identify patterns, connections and associations between digitized objects in three Viennese 
          art collections: the <strong>Belvedere</strong>, the <strong>Wien Museum</strong>, and the 
          <strong>Museum für Angewandte Kunst</strong> The goal of the project is three-fold: 
        </p>
        
        <ol class="text-gray-600 list-decimal list-inside mb-12">
          <li>
            <strong>to explore the use of AI as a tool</strong> for Digital Humanists and museum curators to study the use of
            classification systems and vocabularies across museum collections
          </li>
          
          <li>
            <strong>to establish connections</strong> between online collections so that the associations between them and
            their individual objects become more visible
          </li> 
          
          <li>
            <strong>to demonstrate how AI can support new online exhibition formats</strong> that emphasize serendipitous 
            browsing, exploration of contextual connections, and playful engagement with Vienna's collected
            heritage
          </li> 
        </ol>
          
        <p class="text-gray-600 mb-12">
          Building on cutting-edge <strong>deep learning</strong> and
          <strong>natural language processing</strong> - most notably representation learning,
          triplet loss networks and word embeddings - LiviaAI will explore ways for museum 
          professionals to design their own AI processes without the need for the prohibitive 
          manual data annotation work normally required to train AI models.
        </p>
        
      </div>
      <!-- div class="w-full sm:w-1/2 p-6"></div -->
    </div>
  </div>
</section>

<section class="bg-white py-8">
  <div class="container mx-auto flex flex-wrap">
    <h2 class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-800">
      Partners
    </h2>
    <div class="w-full mb-4">
      <div class="h-1 mx-auto gradient w-64 opacity-25 my-0 py-0 rounded-t"></div>
    </div>

    <div class="flex justify-center w-full pt-10 pb-20">
      <div class="flex justify-center items-center">
        <div class="pr-10">
          <a href="https://www.donau-uni.ac.at" class="flex flex-wrap no-underline hover:no-underline" title="Universität für Weiterbildung Krems">
            <img class="splash-logo" src="logos/donau-universitaet-krems.svg" alt="Logo der Universität für Weiterbildung Krems"/>
          </a>
        </div>

        <div class="pl-10 pr-10">
          <a href="https://www.ait.ac.at" class="flex flex-wrap no-underline hover:no-underline" title="AIT Austrian Institute of Technology">
            <img class="splash-logo" src="logos/ait.jpg" alt="Logo des Austrian Instiute of Technology"/>
          </a>
        </div>

        <div>
          <a href="https://www.belvedere.at/" class="flex flex-wrap no-underline hover:no-underline"title="Belvedere Museum Wien">
            <img class="splash-logo-small" src="logos/belvedere.jpg" alt="Logo des Belvedere Museum Wien"/>
          </a>
        </div>

        <div class="pl-10">
          <a href="https://www.mak.at/" class="flex flex-wrap no-underline hover:no-underline"title="MAK Museum Wien">
            <img class="splash-logo-small" src="logos/mak.jpg" alt="Logo des MAK Museum Wien"/>
          </a>
        </div>

        <div class="pl-10">
          <a href="https://www.wienmuseum.at/" class="flex flex-wrap no-underline hover:no-underline"title="Wien Museum">
            <img class="splash-logo-small" src="logos/wien-museum.png" alt="Logo des Wien Museum"/>
          </a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- section class="bg-white border-b py-8">
  <div class="container mx-auto flex flex-wrap pt-4 pb-12">
    <h1 class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-800">
      Title
    </h1>
    <div class="w-full mb-4">
      <div class="h-1 mx-auto gradient w-64 opacity-25 my-0 py-0 rounded-t"></div>
    </div>
    <div class="w-full md:w-1/3 p-6 flex flex-col flex-grow flex-shrink">
      <div class="flex-1 bg-white rounded-t rounded-b-none overflow-hidden shadow">
        <a href="#" class="flex flex-wrap no-underline hover:no-underline">
          <p class="w-full text-gray-600 text-xs md:text-sm px-6">
            GETTING STARTED
          </p>
          <div class="w-full font-bold text-xl text-gray-800 px-6">
            Lorem ipsum dolor sit amet.
          </div>
          <p class="text-gray-800 text-base px-6 mb-5">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam at ipsum eu nunc commodo posuere et sit amet ligula.
          </p>
        </a>
      </div>
      <div class="flex-none mt-auto bg-white rounded-b rounded-t-none overflow-hidden shadow p-6">
        <div class="flex items-center justify-start">
          <button class="mx-auto lg:mx-0 hover:underline gradient text-white font-bold rounded-full my-6 py-4 px-8 shadow-lg focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out">
            Action
          </button>
        </div>
      </div>
    </div>
    <div class="w-full md:w-1/3 p-6 flex flex-col flex-grow flex-shrink">
      <div class="flex-1 bg-white rounded-t rounded-b-none overflow-hidden shadow">
        <a href="#" class="flex flex-wrap no-underline hover:no-underline">
          <p class="w-full text-gray-600 text-xs md:text-sm px-6">
            GETTING STARTED
          </p>
          <div class="w-full font-bold text-xl text-gray-800 px-6">
            Lorem ipsum dolor sit amet.
          </div>
          <p class="text-gray-800 text-base px-6 mb-5">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam at ipsum eu nunc commodo posuere et sit amet ligula.
          </p>
        </a>
      </div>
      <div class="flex-none mt-auto bg-white rounded-b rounded-t-none overflow-hidden shadow p-6">
        <div class="flex items-center justify-center">
          <button class="mx-auto lg:mx-0 hover:underline gradient text-white font-bold rounded-full my-6 py-4 px-8 shadow-lg focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out">
            Action
          </button>
        </div>
      </div>
    </div>
    <div class="w-full md:w-1/3 p-6 flex flex-col flex-grow flex-shrink">
      <div class="flex-1 bg-white rounded-t rounded-b-none overflow-hidden shadow">
        <a href="#" class="flex flex-wrap no-underline hover:no-underline">
          <p class="w-full text-gray-600 text-xs md:text-sm px-6">
            GETTING STARTED
          </p>
          <div class="w-full font-bold text-xl text-gray-800 px-6">
            Lorem ipsum dolor sit amet.
          </div>
          <p class="text-gray-800 text-base px-6 mb-5">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam at ipsum eu nunc commodo posuere et sit amet ligula.
          </p>
        </a>
      </div>
      <div class="flex-none mt-auto bg-white rounded-b rounded-t-none overflow-hidden shadow p-6">
        <div class="flex items-center justify-end">
          <button class="mx-auto lg:mx-0 hover:underline gradient text-white font-bold rounded-full my-6 py-4 px-8 shadow-lg focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out">
            Action
          </button>
        </div>
      </div>
    </div>
  </div>
</section -->
<!-- Change the colour #f8fafc to match the previous section colour -->
<svg class="wave-top" viewBox="0 0 1439 147" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
  <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
    <g transform="translate(-1.000000, -14.000000)" fill-rule="nonzero">
      <g class="wave" fill="#fff">
        <path
          d="M1440,84 C1383.555,64.3 1342.555,51.3 1317,45 C1259.5,30.824 1206.707,25.526 1169,22 C1129.711,18.326 1044.426,18.475 980,22 C954.25,23.409 922.25,26.742 884,32 C845.122,37.787 818.455,42.121 804,45 C776.833,50.41 728.136,61.77 713,65 C660.023,76.309 621.544,87.729 584,94 C517.525,105.104 484.525,106.438 429,108 C379.49,106.484 342.823,104.484 319,102 C278.571,97.783 231.737,88.736 205,84 C154.629,75.076 86.296,57.743 0,32 L0,0 L1440,0 L1440,84 Z"
        ></path>
      </g>
      <g transform="translate(1.000000, 15.000000)" fill="#FFFFFF">
        <g transform="translate(719.500000, 68.500000) rotate(-180.000000) translate(-719.500000, -68.500000) ">
          <path d="M0,0 C90.7283404,0.927527913 147.912752,27.187927 291.910178,59.9119003 C387.908462,81.7278826 543.605069,89.334785 759,82.7326078 C469.336065,156.254352 216.336065,153.6679 0,74.9732496" opacity="0.100000001"></path>
          <path
            d="M100,104.708498 C277.413333,72.2345949 426.147877,52.5246657 546.203633,45.5787101 C666.259389,38.6327546 810.524845,41.7979068 979,55.0741668 C931.069965,56.122511 810.303266,74.8455141 616.699903,111.243176 C423.096539,147.640838 250.863238,145.462612 100,104.708498 Z"
            opacity="0.100000001"
          ></path>
          <path d="M1046,51.6521276 C1130.83045,29.328812 1279.08318,17.607883 1439,40.1656806 L1439,120 C1271.17211,77.9435312 1140.17211,55.1609071 1046,51.6521276 Z" opacity="0.200000003"></path>
        </g>
      </g>
    </g>
  </g>
</svg>
<section class="container mx-auto text-center py-6 mb-12">
  <!--
  <h1 class="w-full my-2 text-5xl font-bold leading-tight text-center text-white">
    Call to Action
  </h1>
  <div class="w-full mb-4">
    <div class="h-1 mx-auto bg-white w-1/6 opacity-25 my-0 py-0 rounded-t"></div>
  </div>
  <h3 class="my-4 text-3xl leading-tight">
    Main Hero Message to sell yourself!
  </h3>
  <button class="mx-auto lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-full my-6 py-4 px-8 shadow-lg focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out">
    Action!
  </button>
  -->
</section>
<!--Footer-->
<!-- footer class="bg-white">
  <div class="container mx-auto px-8">
    <div class="w-full flex flex-col md:flex-row py-6">
      <div class="flex-1 mb-6 text-black">
        <a class="text-pink-600 no-underline hover:no-underline font-bold text-2xl lg:text-4xl" href="#">
          LANDING
        </a>
      </div>
      <div class="flex-1">
        <p class="uppercase text-gray-500 md:mb-6">Links</p>
        <ul class="list-reset mb-6">
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">FAQ</a>
          </li>
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Help</a>
          </li>
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Support</a>
          </li>
        </ul>
      </div>
      <div class="flex-1">
        <p class="uppercase text-gray-500 md:mb-6">Legal</p>
        <ul class="list-reset mb-6">
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Terms</a>
          </li>
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Privacy</a>
          </li>
        </ul>
      </div>
      <div class="flex-1">
        <p class="uppercase text-gray-500 md:mb-6">Social</p>
        <ul class="list-reset mb-6">
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Facebook</a>
          </li>
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Linkedin</a>
          </li>
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Twitter</a>
          </li>
        </ul>
      </div>
      <div class="flex-1">
        <p class="uppercase text-gray-500 md:mb-6">Company</p>
        <ul class="list-reset mb-6">
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Official Blog</a>
          </li>
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">About Us</a>
          </li>
          <li class="mt-2 inline-block mr-2 md:block md:mr-0">
            <a href="#" class="no-underline hover:underline text-gray-800 hover:text-pink-500">Contact</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
  <a href="https://www.freepik.com/free-photos-vectors/background" class="text-gray-500">Background vector created by freepik - www.freepik.com</a>
</footer -->