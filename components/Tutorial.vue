<!-- Please remove this file from your project -->
<template>
  <div>
    <div class="w-full h-full min-h-screen sm:px-6 lg:px-8 bg-gray-100">
      <div class="grid grid-cols-3">
        <p class="self-center text-blue-500 text-3xl font-bold">cVizard</p>
        <div></div>
        <button class="justify-self-end rounded-full mb-4 mt-4 bg-blue-400 p-2 px-4 text-white" @click="createPdf2">
          Create pdf
        </button>
      </div>

      <!-- <a class="flex justify-center pt-8 sm:pt-0" href="https://nuxtjs.org" target="_blank">
        <svg width="218" height="45" viewBox="0 0 159 30" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M55.5017 6.81866H60.1727L70.0719 22.9912V6.81866H74.3837V29.7345H69.7446L59.8135 13.5955V29.7345H55.5017V6.81866Z" fill="#003543" /> <path d="M93.657 29.7344H89.6389V27.1747C88.7241 28.9761 86.8628 29.9904 84.5113 29.9904C80.7869 29.9904 78.3684 27.3059 78.3684 23.4423V13.2339H82.3865V22.5976C82.3865 24.8566 83.7594 26.4276 85.8171 26.4276C88.0712 26.4276 89.6389 24.6598 89.6389 22.2377V13.2339H93.657V29.7344Z" fill="#003543" /> <path d="M107.64 29.7344L103.784 24.2342L99.9291 29.7344H95.6492L101.596 21.1242L96.1074 13.2339H100.485L103.784 17.9821L107.051 13.2339H111.461L105.94 21.1242L111.886 29.7344H107.64Z" fill="#003543" /> <path d="M120.053 8.25848V13.2339H124.627V16.6063H120.053V24.7974C120.053 25.0725 120.162 25.3363 120.356 25.531C120.55 25.7257 120.813 25.8353 121.087 25.8357H124.627V29.728H121.98C118.386 29.728 116.035 27.6323 116.035 23.9687V16.6095H112.801V13.2339H114.83C115.776 13.2339 116.327 12.6692 116.327 11.7349V8.25848H120.053Z" fill="#003543" /> <path d="M134.756 24.5446V6.81866H139.066V23.1864C139.066 27.6067 136.943 29.7345 133.349 29.7345H128.332V25.8421H133.461C133.804 25.8421 134.134 25.7054 134.377 25.4621C134.619 25.2188 134.756 24.8888 134.756 24.5446Z" fill="#003543" /> <path d="M141.649 22.0409H145.799C146.029 24.6006 147.728 26.2308 150.472 26.2308C152.923 26.2308 154.623 25.2501 154.623 23.2199C154.623 18.3085 142.331 21.7129 142.331 12.9395C142.334 9.17515 145.568 6.55945 150.215 6.55945C155.05 6.55945 158.317 9.34153 158.516 13.6306H154.388C154.193 11.6341 152.632 10.2918 150.207 10.2918C147.953 10.2918 146.548 11.3397 146.548 12.9427C146.548 18.0173 159 14.2226 159 23.1576C159 27.4131 155.504 30 150.474 30C145.279 30 141.882 26.8563 141.654 22.0441" fill="#003543" /> <path d="M24.7203 29.704H41.1008C41.6211 29.7041 42.1322 29.5669 42.5828 29.3061C43.0334 29.0454 43.4075 28.6704 43.6675 28.2188C43.9275 27.7672 44.0643 27.2549 44.0641 26.7335C44.0639 26.2121 43.9266 25.6999 43.6662 25.2485L32.6655 6.15312C32.4055 5.70162 32.0315 5.32667 31.581 5.06598C31.1305 4.8053 30.6195 4.66805 30.0994 4.66805C29.5792 4.66805 29.0682 4.8053 28.6177 5.06598C28.1672 5.32667 27.7932 5.70162 27.5332 6.15312L24.7203 11.039L19.2208 1.48485C18.9606 1.03338 18.5864 0.658493 18.1358 0.397853C17.6852 0.137213 17.1741 0 16.6538 0C16.1336 0 15.6225 0.137213 15.1719 0.397853C14.7213 0.658493 14.3471 1.03338 14.0868 1.48485L0.397874 25.2485C0.137452 25.6999 0.000226653 26.2121 2.8053e-07 26.7335C-0.000226092 27.2549 0.136554 27.7672 0.396584 28.2188C0.656614 28.6704 1.03072 29.0454 1.48129 29.3061C1.93185 29.5669 2.44298 29.7041 2.96326 29.704H13.2456C17.3195 29.704 20.3239 27.9106 22.3912 24.4118L27.4102 15.7008L30.0986 11.039L38.1667 25.0422H27.4102L24.7203 29.704ZM13.0779 25.0374L5.9022 25.0358L16.6586 6.36589L22.0257 15.7008L18.4322 21.9401C17.0593 24.2103 15.4996 25.0374 13.0779 25.0374Z" fill="#00DC82" /></svg>
      </a> -->
      <!-- <div ref="pdf"
        class="h-full max-w-xl align-middle tracking-normal bg-gray-100 sm:pt-0 font-sans items-center min-h-screen sm:items-center justify-center overflow-hidden shadow sm:rounded-lg">
        <Header v-bind="getCV.header" />
        <div class="p-3">
          <div class="grid grid-cols-3 sm:grid-cols-4 gap-3">
            <div class="flex-col col-span-1">
              <Skills class="mb-3" v-for="skill in getCV.skills" v-bind="skill"></Skills>
            </div>
            <div class="col-span-3">
              <ContactInfo v-bind="getCV.contact" />
              <div class="bg-white rounded-xl shadow mt-4">
                <h2 class="font-semibold text-lg px-4 pt-2">Work Experience</h2>
                <Experience :key="id" v-for="experience, id of getCV.experiences" v-bind="experience" />
              </div>

            </div>
          </div>
        </div>
      </div> -->
      <div ref="pdf" class="bg-white text-gray-800">

        <div class="container mx-auto p-6">
          <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
            <!-- Left Column: Contact, Skills, Education, etc. -->
            <div class="space-y-6 col-span-3">
              <div>
                <h1 class="text-3xl font-bold text-blue-500 ">Efe Güre</h1>
                <h2 class="text-xl font-semibold">Senior Frontend Engineer / Team Lead</h2>

              </div>

              <div class="space-y-4">
                <p>Highly skilled Frontend Developer with extensive experience leading teams and delivering
                  user-friendly web applications using JavaScript frameworks such as Vue, React, and Angular. Expert in
                  creating dynamic, responsive UIs, with a strong focus on problem-solving and attention to detail.
                  Fluent in English and Turkish, committed to continuous learning, and staying current with industry
                  trends.</p>
              </div>
              <h2 class="text-2xl font-bold text-blue-500 border-b pb-4">Work Experience</h2>

              <div class="grid grid-cols-4">
                <h3 class="text-xl font-semibold text-blue-400 col-span-2">Team Lead \ Senior Developer</h3>
                <h3 class="text-xl font-semibold text-blue-400 col-span-2 text-right">June 2019 - August 2024</h3>
                <p class="col-span-4 mt-4"><strong>Company:</strong> Ezlo Innovation</p>
                <p class="col-span-4 mt-4"><strong>Product:</strong> Dashboard Configurator</p>
                <p class="col-span-4 mt-4"><strong>Location:</strong> Turkey / Remote</p>
                <ul class="list-disc list-inside col-span-4 mt-4">
                  <li>Led the development of a dynamic UI template application allowing users to create and interact
                    with customized dashboards for home-automation devices.</li>
                  <li>Oversaw all aspects of the project including development, sprint planning, estimation, code
                    review, and build management.</li>
                  <li>Implemented a drag-and-drop designer for creating custom UI elements and data binding to these
                    elements.</li>
                  <li>Developed a flexible solution for storing and displaying the UIs created by end-users.</li>
                  <li>Reduced app bundle size by 40%.</li>
                  <li>Identified and resolved a significant memory leakage issue.</li>
                  <li>Implemented web workers for non-blocking API communication.</li>
                  <li>Integrated telemetry logging data.</li>

                </ul>
                <p class="col-span-4 mt-4"><strong>Tech Stack:</strong> Vue, JavaScript, HTML/CSS, SCSS, Vuex, webpack,
                  ESLint, Git</p>
              </div>

              <div class="grid grid-cols-4">
                <h3 class="text-xl font-semibold text-blue-400 col-span-2">Senior Frontend Developer(Contractor)</h3>
                <h3 class="text-xl font-semibold text-blue-400 col-span-2 text-right"> November 2022 - April 2023</h3>
                <p class="col-span-4 mt-4"><strong>Company:</strong> Ginoa</p>
                <p class="col-span-4 mt-4"><strong>Product:</strong> Ginoa.io </p>
                <p class="col-span-4 mt-4"><strong>Location:</strong> Turkey / Remote</p>
                <ul class="list-disc list-inside col-span-4 mt-4">
                  <li>Contracted for a web3 application focused on NFT bartering and trading.</li>
                  <li>Deciding the tech stack and general app layout.</li>
                  <li>Creating responsive UI elements.</li>
                  <li>Implementing data binding from APIs.</li>
                  <li>Integrated virtualization to render numerous NFTs efficiently with advanced paging/loading
                    capabilities.</li>
                </ul>
                <p class="col-span-4 mt-4"><strong>Tech Stack:</strong> React, TypeScript, Tailwind, react-query,
                  Recharts,
                  Headless UI, Vite</p>
              </div>

              <div class="grid grid-cols-4">
                <h3 class="text-xl font-semibold text-blue-400 col-span-2">Frontend Developer</h3>
                <h3 class="text-xl font-semibold text-blue-400 col-span-2 text-right">Oct 2018 - June 2019</h3>
                <p class="col-span-4 mt-4"><strong>Company:</strong> Nurd Innovation</p>
                <p class="col-span-4 mt-4"><strong>Product:</strong> NuMessage</p>
                <p class="col-span-4 mt-4"><strong>Location:</strong> Turkey / Izmir</p>
                <ul class="list-disc list-inside col-span-4 mt-4">
                  <li>Contributed to a 'Skype-like' cross-platform and web messaging project.</li>
                  <li>Developed new components.</li>
                  <li>Wrote documentation.</li>
                  <li>Conducted unit testing.</li>
                  <li>Tech Stack: NativeScript-Vue, Vue, JavaScript, HTML/CSS, SCSS</li>
                </ul>
              </div>

              <div class="grid grid-cols-4">
                <h3 class="text-xl font-semibold text-blue-400 col-span-2">Frontend Developer</h3>
                <h3 class="text-xl font-semibold text-blue-400 col-span-2 text-right">Jun 2017 - Mar 2018</h3>
                <p class="col-span-4 mt-4"><strong>Company:</strong> Univera</p>
                <p class="col-span-4 mt-4"><strong>Product:</strong> E-commerce Platform</p>
                <p class="col-span-4 mt-4"><strong>Location:</strong> Turkey / Izmir</p>
                <ul class="list-disc list-inside col-span-4 mt-4">
                  <li>Developed and documented several plugins for an e-commerce application using Google Analytics.
                  </li>
                </ul>
                <p class="col-span-4 mt-4"><strong>Tech Stack:</strong> NopCommerce, C#, .NET, JavaScript, Google
                  Analytics
                </p>
              </div>

              <div class="grid grid-cols-4">
                <h3 class="text-xl font-semibold text-blue-400 col-span-2">Junior Frontend Developer</h3>
                <h3 class="text-xl font-semibold text-blue-400 col-span-2 text-right"> Jan 2017 - Jun 2017 / Mar 2018 -
                  Jun 2018
                </h3>
                <p class="col-span-4 mt-4"><strong>Company:</strong> Delta Smart Technologies (startup)</p>
                <p class="col-span-4 mt-4"><strong>Product:</strong> Pincident</p>
                <p class="col-span-4 mt-4"><strong>Location:</strong> Turkey / Urla</p>

                <ul class="list-disc list-inside col-span-4">
                  <li>Created a web-based admin panel for an incident management application used by city halls to
                    receive reports from citizens.</li>
                  <li>Worked within a small development team, collaborating closely with backend and cross-platform
                    developers.</li>
                </ul>
                <p class="col-span-4 mt-4"><strong>Tech Stack:</strong> Angular, TypeScript, rxjs, HTML/CSS
                </p>
              </div>


            </div>

            <!-- Right Column: Work Experience -->
            <div class="space-y-6 bg-gray-100 p-4 rounded-xl">
              <h3 class="text-xl font-semibold text-blue-300 border-b pb-4">Contact Info</h3>
              <p class="mt-2"><strong>Location:</strong> Istanbul, Turkey</p>
              <p><strong>Phone:</strong> +905392757576</p>
              <p><strong>Email:</strong> efegure@gmail.com</p>
              <p><strong>LinkedIn:</strong> https://www.linkedin.com/in/efe-g%C3%BCre-5a47b0b9/</p>
              <div class="space-y-4">
                <h3 class="text-xl font-semibold text-blue-300 border-b pb-4">Technologies</h3>
                <ul class="list-disc list-inside">
                  <li>JavaScript, TypeScript</li>
                  <li>Vue.js, React.js, AngularJS</li>
                  <li>Tailwind, Bootstrap</li>
                  <li>HTML, CSS, SCSS</li>
                  <li>Vuex, redux</li>
                  <li>rtk-query, react-window, virtualization</li>
                  <li>webpack, Jenkins, ESLint</li>
                  <li>GitHub, npm</li>
                  <li>Jira, Figma</li>
                  <li>NativeScript</li>
                </ul>
              </div>

              <div class="space-y-4">
                <h3 class="text-xl font-semibold text-blue-300 border-b pb-4">Languages</h3>
                <ul class="list-disc list-inside">
                  <li>Turkish - Native</li>
                  <li>English - Fluent</li>
                  <li>French - Limited</li>
                </ul>
              </div>

              <div class="space-y-4">
                <h3 class="text-xl font-semibold text-blue-300 border-b pb-4">Soft Skills</h3>
                <ul class="list-disc list-inside">
                  <li>Problem-solving</li>
                  <li>Attention to Detail</li>
                  <li>Time management</li>
                  <li>Leadership</li>
                  <li>Communication</li>
                  <li>Adaptability</li>
                </ul>
              </div>

              <div class="space-y-4">
                <h3 class="text-xl font-semibold text-blue-300 border-b pb-4">Education</h3>
                <ul class="list-disc list-inside">
                  <li>Izmir Institute of Technology, Computer Engineering (2012-2017)</li>
                  <li>Izmir Atatürk High School (2007-2012)</li>
                </ul>
              </div>

            </div>
          </div>
        </div>


      </div>
      <div class="flex justify-center pt-4 space-x-2">
        <a href="https://github.com/nuxt/nuxt.js" target="_blank"><svg
            class="w-6 h-6 text-gray-600 hover:text-gray-800 button--github" xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="32" height="32"
            preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
            <path
              d="M12 2.247a10 10 0 0 0-3.162 19.487c.5.088.687-.212.687-.475c0-.237-.012-1.025-.012-1.862c-2.513.462-3.163-.613-3.363-1.175a3.636 3.636 0 0 0-1.025-1.413c-.35-.187-.85-.65-.013-.662a2.001 2.001 0 0 1 1.538 1.025a2.137 2.137 0 0 0 2.912.825a2.104 2.104 0 0 1 .638-1.338c-2.225-.25-4.55-1.112-4.55-4.937a3.892 3.892 0 0 1 1.025-2.688a3.594 3.594 0 0 1 .1-2.65s.837-.262 2.75 1.025a9.427 9.427 0 0 1 5 0c1.912-1.3 2.75-1.025 2.75-1.025a3.593 3.593 0 0 1 .1 2.65a3.869 3.869 0 0 1 1.025 2.688c0 3.837-2.338 4.687-4.563 4.937a2.368 2.368 0 0 1 .675 1.85c0 1.338-.012 2.413-.012 2.75c0 .263.187.575.687.475A10.005 10.005 0 0 0 12 2.247z"
              fill="currentColor" />
          </svg></a>
        <a href="https://twitter.com/nuxt_js" target="_blank"><svg class="w-6 h-6 text-gray-600 hover:text-gray-800"
            xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img"
            width="32" height="32" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
            <path
              d="M22.46 6c-.77.35-1.6.58-2.46.69c.88-.53 1.56-1.37 1.88-2.38c-.83.5-1.75.85-2.72 1.05C18.37 4.5 17.26 4 16 4c-2.35 0-4.27 1.92-4.27 4.29c0 .34.04.67.11.98C8.28 9.09 5.11 7.38 3 4.79c-.37.63-.58 1.37-.58 2.15c0 1.49.75 2.81 1.91 3.56c-.71 0-1.37-.2-1.95-.5v.03c0 2.08 1.48 3.82 3.44 4.21a4.22 4.22 0 0 1-1.93.07a4.28 4.28 0 0 0 4 2.98a8.521 8.521 0 0 1-5.33 1.84c-.34 0-.68-.02-1.02-.06C3.44 20.29 5.7 21 8.12 21C16 21 20.33 14.46 20.33 8.79c0-.19 0-.37-.01-.56c.84-.6 1.56-1.36 2.14-2.23z"
              fill="currentColor" />
          </svg></a>
      </div>
    </div>
  </div>
</template>

<script>
import cv from "static/efegurecv.json";
import html2pdf from "html2pdf.js";
import { jsPDF, fromHTML, split_text_to_size } from "jspdf";

export default {
  name: "NuxtTutorial",
  computed: {
    getCV() {
      console.log("CV", cv);
      return cv;
    },
  },
  methods: {
    createPdf() {
      // your JS code here like >> jsPlumb.ready(function () {})
      var opt = {
        margin: 0,
        filename: "cv.pdf",
        html2canvas: {
          scale: 4,
          useCORS: true,
          allowTaint: true,
          letterRendering: true,
        },
        // format here is in inches A4 format is 8,5 * 11 inches
        jsPDF: { unit: "in", format: "letter", orientation: "portrait" },
      };

      // New Promise-based usage:

      // Old monolithic-style usage:
      html2pdf(this.$refs.pdf, opt);
    },
    createPdf2() {
      let doc = new jsPDF({
        unit: 'pt',
      });
      const elementHandler = {
        '#ignorePDF': function (element, renderer) {
          return true;
        }
      };
      document.body.style.zoom = 1;
      doc.html(this.$refs.pdf, {
        x: 0, y: 0, autoPaging: "text", html2canvas: {
          scale: 0.6, // default is window.devicePixelRatio
          dpi: 192,  // Reduces dots per inch for faster rendering
          useCORS: true  // Ensures that resources are handled efficiently
        },
        doc,
        callback: function (doc_e) {
          doc_e.save("ats-resume-2024.pdf");
        }
      });

    }
  },
};
</script>
<style>
body {
  /* display: inline-block; */
  /* ! https://github.com/niklasvh/html2canvas/issues/2775 */
  /* line-height: 0.5!important; */
}
</style>
