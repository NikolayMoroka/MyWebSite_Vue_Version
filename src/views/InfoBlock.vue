<template>
    <div class="info_block mt-15 px-4">
        <v-row v-for="(items, index) in infoBlocks" :key="index">
            <v-col cols="12">
                <h3 class="title_block mb-5">
                    {{ items.title }}
                </h3>
                <div v-for="text in items.text" :key="text.index" class="text-left">
                    <span class="text_block"> {{ text }} </span> 
                    <span 
                    @click="dialog = true"
                    style="font-weight: 500; font-size: 18px; text-decoration: underline;">
                     (more)
                    </span>
                </div>

                <ul v-if="items.list" class="text-left">
                    <li v-for="item in items.list" :key="item.index" class="text_block">
                        {{ item }}
                    </li>
                </ul>

            </v-col>

            <v-col cols="12">
                <img width="90%" :src="items.image" alt="">
            </v-col>
        </v-row>
        <v-dialog
        v-model="dialog"
        fullscreen
        style="background-color: white"
        >
            <div style="height: 100vh; background-color: #fff">
                <v-app-bar color="#290653">
                    <v-btn icon @click="dialog = false">
                        <v-icon x-large color="#fff">
                            mdi-chevron-left
                        </v-icon>
                    </v-btn>
                </v-app-bar>

                <v-container>
                    <v-row>
                        <v-col>
                            <p style="color: #290653;" class="text_block">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Reiciendis at ratione quia dolorem aliquid fugiat consectetur ullam repudiandae aperiam. Ab iusto iure fugiat ut dolorem, aperiam placeat repudiandae dolor neque.</p>
                        </v-col>
                    </v-row>
                </v-container>
            </div>
        </v-dialog>
    </div>
</template>

<script>
export default {
  name: 'InfoBlock',
  data: () => ({
      infoBlocks: [
      {
        title: 'ABOUT ME',
        text: [
            "Hello! My name is Nikolay Moroka and I'm a Front-end developer.",
            "For several years I have been studying website and application development. I successfully participate in various projects.",
            "I'm constantly improving and developing my skills, complementing them with new technologies."
        ],
        image: require('../assets/I_am_dev.png')
      },
       {
        title: 'MY SKILLS',
        text: [
            "I am fluent in technologies such as:"
        ],
        list: [
            "HTML5",
            "CSS",
            "SASS / SCSS preprocessors",
            "Bootstrap",
            "JavaScript (ES5, ES6, ES6+)",
            "Vue.js and jQuery"
        ],
        image: require('../assets/skills.png')
      },
       {
        title: 'OTHER TECHNOLOGI',
        text: [
            "I have experience with:"
        ],
        list: [
            "Gulp / Webpack",
            "Photoshop / Figma / Avocode",
            "GIT",
            "CMS WordPress / Tilda",
            "CSS Grid",
            "CSS animation",
            "Basic knowledge of React.js",
            "Basic knowledge of PHP"
        ],
        image: require('../assets/other_technologi.png')
      },
       {
        title: 'ADAPTIVE and CROSS-BROWSER',
        text: [
            "In the course of my work, I pay a lot of attention to the adaptability and cross-browser compatibility of their projects. This will allow you to avoid errors and ensure the correct operation of the site / application on different devices and browsers."
        ],
        image: require('../assets/adaptive.png')
      },
       {
        title: 'СREATIVE APPROACH',
        text: [
            "In my work, not only technical knowledge is important, but also creative solutions to each problem. I love creative work and look for an individual approach to each job"
        ],
        image: require('../assets/creativity.png')
      },
       {
        title: 'QUALITY of WORK',
        text: [
            "I treat my projects with great responsibility and guarantee the quality of the work done."
        ],
        image: require('../assets/quality.png')
      },
    ],
    dialog: false
  }),  
}
</script>

<style scoped>
.info_block {
    color: white;
}
</style>