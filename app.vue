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
    label: 'Project 1 - Basic Navigation and Object Manipulation',
    icon: 'i-heroicons-information-circle',
    defaultOpen: true,
    slot: 'project-1',
    /* content:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed neque elit, tristique placerat feugiat ac, facilisis vitae arcu. Proin eget egestas augue. Praesent ut sem nec arcu pellentesque aliquet. Duis dapibus diam vel metus tempus vulputate.', */
  },
  {
    label: 'Project 2 - Component Editing',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-2',
  },
  {
    label: 'Project 3 - Editing with Modeling Tools',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-3',
  },
  {
    label: 'Project 4 - Practice Modeling From Reference Images',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-4',
  },
  {
    label: 'Project 5 - Modeling Project',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-5',
  },
  {
    label: 'Project 6 - Lighting Basics',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-6',
  },
  {
    label: 'Project 7 - Material Practice',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-7',
  },
  {
    label: 'Project 8 - Unwrap and Texture',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-8',
  },
  {
    label: 'Project 9 - Simple Bouncing Ball Animation',
    icon: 'i-heroicons-information-circle',
    defaultOpen: false,
    slot: 'project-9',
  },
  {
    label: 'Final Project',
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
      GAME 124 - Introduction to 3D with Maya<br /><br />
    </h3>
    <p>
      This course is an introduction to the 3D content creation process as practiced in Maya. Best
      practices for 3D modeling, texturing, file management, and animation will be examined.
      Students will build several small scenes and render those scenes into movies. Emphasis will be
      placed on 3D as it relates to the video game industry.
      <br /><br />
    </p>
    <UAccordion color="primary" variant="outline" size="sm" :items="items">
      <template #project-1>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Using the scene provided, create and position all necessary objects required to recreate
            each of the object groups. Each group must be created to be within .1 units (set to
            centimeters) of accuracy. <br /><br />The purpose of this assignment is to give ample
            exposure to the basic Maya navigation control, object creation tools, and basic
            manipulation tools.<br /><br />
          </p>
          <img class="object-cover" src="./media/P1/project1.png" alt="Project Image" />
        </div>
      </template>
      <template #project-2>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Using the provided scene, recreate each of the objects by creating objects, and editing
            their components. Each object should be recreated to within .01 units of accuracy. Each
            object should be modeled from a single contiguous starting object, and should not be
            built using multiple separate objects. <br /><br />Combine and group objects to match
            the provided formations. Name groups and objects, center their pivots, freeze
            transformations and delete all construction history. <br /><br />The purpose of this
            assignment is to allow the student to practice modeling by editing an objects
            components.<br /><br />
          </p>
          <img class="object" src="./media/P2/project2.png" alt="Project Image" />
        </div>
      </template>
      <template #project-3>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Using the provided scene, recreate each of the objects using whichever modeling tools
            and techniques that work best for you. Each object should be recreated to within .01
            units of accuracy. There are two groups of objects providing differing degrees of
            difficulty. Start with the simpler shapes, and then work your way to the more advanced
            shapes. <br /><br />Each object should be modeled from a single contiguous starting
            object, and should not be built using multiple separate objects. Group or combined each
            of your two object groups, and make sure to Freeze all Transformations, and Delete
            Construction History. <br /><br />The purpose of this assignment is to allow the student
            to practice using different modeling tools to create specific abstract shapes from
            simple primitives.<br /><br />
          </p>
          <img class="object" src="./media/P3/project3.png" alt="Project Image" />
        </div>
      </template>
      <template #project-4>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Working from reference images create an object of your choice (or, if you prefer, use
            the provided references). The object should be moderately complex and be clearly
            identifiable. Use the reference images as image planes to model from within Maya. Make
            any adjustments necessary to the images so that they properly align in Maya.
            <br /><br />Use this assignment to practice your modeling skills while applying them
            toward an artistic purpose.<br /><br />
          </p>
          <img class="object" src="./media/P4/project4.png" alt="Project Image" />
        </div>
      </template>
      <template #project-5>
        <div class="flex flex-col justify-center items-center gap-1">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Choose one of the following to model: <br /><br />Humanoid Figure - not necessarily
            human <br /><br />Interior Environment - a room with a entry or exit and at least 5
            supporting props <br /><br />Exterior Environment - one large focal point and at least 5
            supporting props Vehicle <br /><br />Use polygonal and/or NURBs modeling techniques to
            create your model. The model should be created as realistic as possible. Focus on
            modeling in passes - start with the big simple shapes, and work toward more and more
            detailed shapes, adding geometry only when and where needed, and removing excess and
            unneeded geometry.<br /><br />
          </p>
          <img class="object" src="./media/P5/project5.png" alt="Project Image" />
        </div>
      </template>
      <template #project-6>
        <div class="flex justify-center items-center gap-1">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Using the provided Maya file, set up the scene with proper 3 point lighting: create and
            name a key, fill and rim light; light the scene as realistically as possible; create and
            name a shot camera; using the shot camera render the scene from 3 unique angles using
            the Arnold renderer.
          </p>
          <img class="object-cover h-48 w-96" src="./media/P6/Render1.jpg" alt="Project Image" />
          <img class="object-cover h-48 w-96" src="./media/P6/Render2.jpg" alt="Project Image" />
          <img class="object-cover h-48 w-96" src="./media/P6/Render3.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-7>
        <div class="flex justify-center items-center gap-1">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Using the scene provided, assign and adjust materials for each object in the scene. Name
            all materials and their respective shading groups. Similar objects can share materials.
            Adjust each materials attributes to make each object appear as lifelike as possible.
            Create a shot camera, light(s) and render the scene from 3 various angles. Always clean
            up your scenes and organize the outliner before submitting.
          </p>
          <img class="object-cover h-48 w-96" src="./media/P7/Render1.jpg" alt="Project Image" />
          <img class="object-cover h-48 w-96" src="./media/P7/Render2.jpg" alt="Project Image" />
          <img class="object-cover h-48 w-96" src="./media/P7/Render3.jpg" alt="Project Image" />
        </div>
      </template>
      <template #project-8>
        <div class="flex justify-center items-center gap-1">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Unwrap each of the polygonal models contained within the scene provided. The UV's should
            be laid out to maximize coverage of the UV space. <br /><br />Create and apply texture
            maps for each of your models. The resulting texture map or maps should be created with a
            reasonable level of detail. Put equal effort into making the textures as you do making
            the UV layouts. The maximum texture size for each texture is 1024 x 1024. All bitmaps
            must be in powers of 2 (e.g. 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024). Light and render
            at least 3 views of your project. Renders should be at least 720 HD resolution.
            <br /><br />This project will only work properly if you work inside of a Maya project
            directory and save it out correctly.
          </p>
          <img
            class="object-cover h-48 w-96"
            src="./media/P8/GAME124_Tonu_P8_Render1.png"
            alt="Project Image" />
          <img
            class="object-cover h-48 w-96"
            src="./media/P8/GAME124_Tonu_P8_Render2.png"
            alt="Project Image" />
          <img
            class="object-cover h-48 w-96"
            src="./media/P8/GAME124_Tonu_P8_Render3.png"
            alt="Project Image" />
        </div>
      </template>
      <template #project-9>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Create a simple bouncing ball animation that moves the ball in 2 Directions - Vertical
            and horizontal. The ball should decelerate horizontally from an initial speed to a stop.
            The Ball should bounce vertically at least 3 times. Use key frame animation to Animate
            the ball's change through time. Use the graph editor to edit the animation curves to
            achieve the proper motion.<br /><br />
          </p>
          <video src="./media/P9/project9.mp4" alt="Project Video Bouncing Ball" controls></video>
        </div>
      </template>
      <template #final-project>
        <div class="">
          <p class="text-sm text-gray-500 dark:text-gray-400">
            Using all the skills you have learned up to this point create visually interesting 3D
            model/scene, texture it, light the scene, and render the scene.<br /><br />Final Polygon
            Budget: 200,000 QUADS Max in scene; keep in mind all objects should be modeled as low
            poly as possible and have clean edge flow and QUAD topology whenever possible.
            <br /><br />Texturing: Maximum texture map resolution of 2048 px by 2048 px (you may use
            as many textures as necessary for your scene) All textures must be in a Power of 2
            dimension. Utilizing tiling textures is recommended. <br /><br />Rendering: Use Maya to
            Compose, light and render a scene containing the 3D Model Render in Arnold (preferred)
            or Maya Software from at least 3 various angles. Image size no less than HD_720
            resolution.<br /><br />
          </p>
          <img src="./media/P10/GAME124_Tonu_FinalProject_Render2.png" alt="Project Image" />
          <img src="./media/P10/GAME124_Tonu_FinalProject_Render3.png" alt="Project Image" />
          <img src="./media/P10/GAME124_Tonu_FinalProject_Render1.png" alt="Project Image" />
        </div> </template
    ></UAccordion>
    <!-- <template #footer /> -->
  </UCard>
</template>
