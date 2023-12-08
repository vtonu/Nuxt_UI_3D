<script setup>
const colorMode = useColorMode();
const isDark = computed({
  get() {
    return colorMode.value === 'dark';
  },
  set() {
    colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark';
  },
});
// Accordion dropdowns
const items = [
  {
    label:
      'Project 1 - [Assignment] UV Map Brick & Slate Roof Tiling Textures onto Basic House Model',
    icon: 'i-heroicons-information-circle',
    defaultOpen: true,
    slot: 'project-1',
    /* content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.', */
  },
  {
    label: 'Project 2 - [Assignment] Model a House',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-2',
  },
  {
    label: 'Project 3 - [Assignment] Model a 3D Bridge',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-3',
  },
  {
    label:
      'Project 4 - [Assignment] Create a Floor Tiling & Terrain Tiling Texture. Diffuse and Normal Maps. No AI generated textures.',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-4',
  },
  {
    label: 'Project 5 - [Assignment] Model a 3D Barrel in Maya & Unity',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-5',
  },
  {
    label: 'Project 6 - [Assignment] Stained Glass - Alpha Transparency & Normal Map',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-6',
  },
  {
    label: 'Project 7 - [Assignment] Create Materials for the Barrel with Substance Painter',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-7',
  },
  {
    label: 'Project 8 - [Assignment] Model and UV a Hard Surface Mech Sphere',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-8',
  },
  {
    label: 'Project 9 - [Assignment] Build and Texture a Plant',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-9',
  },
  {
    label: '[Final Assignment] - One game ready, pro game model',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'final-project',
  },
];
</script>

<template>
  <UCard class="m-16 ring ring-green-500 ring-offset-2">
    <template #header>
      <ClientOnly>
        <UButton
          :icon="isDark ? 'i-heroicons-moon-20-solid' : 'i-heroicons-sun-20-solid'"
          color="gray ring ring-green-500 ring-offset-2"
          variant="outline"
          aria-label="Theme"
          @click="isDark = !isDark" />

        <template #fallback>
          <div class="w-8 h-8" />
        </template> </ClientOnly
    ></template>
    <h3 class="text-xl font-bold text-gray-900 dark:text-white pt-2">
      GAME 134 - 3D Materials & Textures<br /><br />
    </h3>
    <p>
      This course covers the elements of creating portfolio quality Material Shaders/Textures
      applied to a 3D model. Best practices for creating realistic looking textures will be applied.
      Students will use techniques learned in class and build realistic 3D props/assets. Emphasis
      will be placed on creating procedural and file textures. Diffuse, Alpha, Roughness/Metallic,
      Emissive, Bump/ Normal mapping will be learned and how these materials work in different
      renderers such as Maya or Unity’s real-time PBR (Physical Based Renderer using Roughness and
      Metallic maps).
      <br /><br />
    </p>
    <UAccordion color="primary" variant="outline" size="sm" :items="items">
      <template #project-1>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            In this assignment, we will go over the basics of making materials, UVing tiling
            textures, and applying and aligning and projecting UVs. The purpose is to learn to align
            UVs. Using the default UVs of a primitive model is not acceptable. <br /><br />
          </p>
          <!-- <img class="object-cover" src="./media/P1/project1.jpg" alt="Project Image" /> -->
          <img class="object-cover" src="./media/P1/project1_1.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-2>
        <div class="flex flex-col justify-center items-center gap-2">
          <p class="text-sm text-gray-500 dark:text-gray-400"><br /><br /></p>
          <img class="object" src="./media/P2/project2.jpg" alt="Project Image" />
          <img class="object" src="./media/P2/project2_2.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-3>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400"></p>
          <!-- <img class="object" src="./media/P3/project3.jpg" alt="Project Image" /> -->
          <img class="object" src="./media/P3/project3_3.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-4>
        <div class="flex flex-col justify-center items-center gap-2">
          <p class="text-sm text-gray-500 dark:text-gray-400"></p>
          <img class="object" src="./media/P4/project4.jpg" alt="Project Image" />
          <img class="object" src="./media/P4/project4_4.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-5>
        <div class="flex flex-col justify-center items-center gap-2">
          <p class="text-sm text-gray-500 dark:text-gray-400"></p>
          <img class="object" src="./media/P5/project5.jpg" alt="Project Image" />
          <img class="object" src="./media/P5/project5_5.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-6>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400"></p>
          <img class="object" src="./media/P6/project6.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-7>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400"></p>
          <!-- <img class="object" src="./media/P7/project7.jpg" alt="Project Image" /> -->
          <img class="object" src="./media/P7/project7_7.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-8>
        <div class="flex flex-col justify-center items-center gap-2">
          <p class="text-sm text-gray-500 dark:text-gray-400"></p>
          <img class="object" src="./media/P8/project8.jpg" alt="Project Image" />
          <img class="object" src="./media/P8/project8_8.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-9>
        <div class="flex flex-col justify-center items-center gap-2">
          <p class="text-sm text-gray-500 dark:text-gray-400"></p>
          <!-- <video src="./media/P9/project9.mp4" alt="Project Video Bouncing Ball" controls></video> -->
          <img class="object" src="./media/P9/project9.jpg" alt="Project Image" />
          <img class="object" src="./media/P9/project9_9.jpg" alt="Project Image" />
        </div>
      </template>
      <template #final-project>
        <div class="flex flex-col justify-center items-center gap-2">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            The final project will be one object that represents 3 or 4 different looks (glossy,
            metal, wood, rubber, steel, glass, etc.). Final should be PBR based Metallic/Roughness
            workflow (Physically Based Rendering). Aesthetics matter. <br /><br />
          </p>
          <img src="./media/P10/project10.jpg" alt="Project Image" />
          <img src="./media/P10/project10_10.jpg" alt="Project Image" />
          <img src="./media/P10/project10_10_10.jpg" alt="Project Image" />
          <img src="./media/P10/project10_10_10_10.jpg" alt="Project Image" />
          <img src="./media/P10/project10_10_10_10_10.jpg" alt="Project Image" />
        </div> </template
    ></UAccordion>
    <!-- <template #footer /> -->
  </UCard>
</template>
