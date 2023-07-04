# Artikel 1, Diving Deeper into 3D Graphics and three.js

## Introduction
During my exploration of the digital universe, I've discovered the significant role that 3D graphics play in transforming a multitude of applications, ranging from video games to animated films, and even website design. Amidst the vast array of tools available, I've found the JavaScript library, three.js, to be an invaluable ally in navigating the 3D world. I was intrigued by the talk of Servin, a freelancer and full-stack developer who founded his own company called Level 30 Wizards, which is a creative digital studio. This inspired me to write this article. Even though I am still relatively new to JavaScript, 3D modelling was always interesting to me, and being able to implement this into my own future designs would be amazing.

## Understanding the 3D Graphics World
In my quest to understand the magic behind three-dimensional graphics, I've learned that they provide a sense of depth and perspective - something that their two-dimensional cousins lack. Every 3D object lives in a space defined by length, breadth, and depth (or x, y, and z coordinates for the mathematically inclined).

My research led me to understand how 3D graphics spring to life: by transforming and rendering geometric data, often polygons, in this three-dimensional space. The final touches - lighting, shading, texturing - are then applied to make these polygons appear as realistic, tangible objects.

## A Deeper Look into three.js
three.js emerged on my radar as a veritable life-saver, a JavaScript library that allows us to create and display these 3D graphics in a web browser. It simplifies the intimidating complexity of WebGL (Web Graphics Library), the standard technology behind 3D web graphics.

After working with it, I've realized that three.js strikes the perfect balance, simplifying WebGL without compromising on its power. Thus, it provides an accessible gateway for both 3D graphics novices and experts to bring their creative visions to life on the web.

## Why choose three.js?
During my research, I've identified three primary reasons why three.js resonated with me:

- Simplicity: three.js takes care of the nitty-gritty details of WebGL, making it easy to create stunning 3D graphics without getting bogged down by complex code.
- Documentation and Community: As someone new to the field, I've found its extensive documentation and supportive community to be immensely helpful.
- Versatility and Features: three.js supports an impressive array of features and allows me to create a variety of 3D objects and scenes. Its versatility truly feeds the imagination!

## Core Concepts in three.js
My journey with three.js has brought me face-to-face with several fundamental concepts that I'd like to share:

- Scene: Consider this as the universe where all your 3D objects exist. It's your canvas!
- Camera: This is your eye into the scene. By changing the camera position, you can view the scene from different perspectives.
- Renderer: The unsung hero that takes the scene and the camera and paints the final image onto your web page.
- Geometry: These are the building blocks of your 3D objects, as simple as a cube or as intricate as a custom-made model.
- Materials: These give your objects their appearance, color, and texture.
- Light: This mimics real-world light behavior, helping create more realistic and visually appealing scenes.
- Animation: With three.js, I found that I could breathe life into these static objects by animating them.

## Example Code in three.js
During my experiments with three.js, I created a spinning cube with dynamic lighting. Here's how I did it:

```js
var scene = new THREE.Scene();
var camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight, 0.1, 1000);

var renderer = new THREE.WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);

var geometry = new THREE.BoxGeometry(1, 1, 1);
var material = new THREE.MeshPhongMaterial({color: 0x00ff00});
var cube = new THREE.Mesh(geometry, material);
scene.add(cube);

var light = new THREE.PointLight(0xFFFFFF, 1, 1000);
light.position.set(10, 10, 10);
scene.add(light);

camera.position.z = 5;

var animate = function () {
    requestAnimationFrame(animate);

    cube.rotation.x += 0.01;
    cube.rotation.y += 0.01;

    renderer.render(scene, camera);
};

animate();
```

In this example, I added a PointLight to the scene, which gave the cube an illusion of depth and shape.

## Conclusion
My research has shown me that three.js is a potent ally for anyone wishing to venture into the realm of 3D web graphics. There may be a steep hill to climb at first, but with patience and a grasp of the core concepts, the peak is certainly reachable! For anyone wishing to embark on this journey, I highly recommend the three.js documentation and the three.js fundamentals website as invaluable guides.

## Sources
1. "Three.js - Javascript 3D Library." Three.js. https://threejs.org/
2. "Three.js Fundamentals." Three.js Fundamentals. https://threejsfundamentals.org/
3. "WebGL - OpenGL ES for the Web." Khronos Group. https://www.khronos.org/webgl/

# Artikel 2, My Research Journey into Crafting Accessible Websites

## Introduction
During my exploration of web design, I learned the importance of creating websites that aren't just visually appealing but are accessible to everyone. I discovered that in the digital world, inclusivity is just as important as aesthetics, functionality, or search engine optimization. I was inspired to write this article because of a talk I had attended which was given by Cyd Stumpel, a Front-end developer.

## Unraveling the Concept of Accessibility
Accessibility, in the context of the web, means building websites that everyone, including people with disabilities, can use effectively. This includes people with auditory, cognitive, neurological, physical, speech, and visual impairments.

I found the concept beautifully summarized by the Web Content Accessibility Guidelines (WCAG), produced by the World Wide Web Consortium (W3C). They laid out four key principles that should guide the construction of an accessible website:

- Perceivable: Can all users perceive the information? This principle entails providing alternatives for non-text content and ensuring that users can consume the content in various ways, such as visually or audibly.
- Operable: Can all users use the interface and navigate the website? Websites must be fully functional using only a keyboard, and users must be given ample time to consume the content.
- Understandable: Is the operation of the interface and the information easily understood by users? Here, the focus is on making text readable, avoiding jargon, and ensuring web pages operate predictably.
- Robust: Can a variety of technologies interpret the content reliably? This principle encourages forward-thinking design compatible with current and future user tools, including assistive technologies.

## Creating Accessible Websites: Key Insights from My Research
Through my research, I've found that creating accessible websites involves several critical factors:

- Consistent Navigation: Navigation should remain consistent throughout the website. This includes the placement of navigation bars, search bars, buttons, and links.
- Readable Text: The text should be easy to read. This involves selecting high-contrast color combinations, readable fonts, and an appropriate text size.
- Alternative Text for Images: All images should include alternative text (alt text) to describe the image for those who cannot see it.
- Accessible Forms: Forms should be designed with accessibility in mind, including appropriately labeled fields and error messages that help users correct mistakes.
- Captions and Transcripts: Videos should have captions or transcripts available. This not only aids deaf and hard of hearing users, but also those who cannot play sound due to their current environment.
- Keyboard Accessibility: All website functionality should be available using a keyboard. This helps people who cannot use a mouse or have difficulty with fine motor skills.
- Avoidance of Flashing Content: Flashing content can trigger seizures in people with conditions like photosensitive epilepsy and should be avoided.
- Testing: Finally, I learned that you should regularly test your website for accessibility. Tools like the WAVE Web Accessibility Evaluation Tool can help identify areas for improvement.
