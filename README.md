# Artikel 1, 3D en three.js. 

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

In this code, I added a PointLight to the scene, which creates the illusion of depth and shape on the cube.

## Conclusion
three.js is a powerful tool for creating 3D graphics in web applications. The learning curve might seem steep initially, but understanding the core concepts such as scenes, cameras, renderers, geometries, materials, lights, and animation will pave the way towards creating visually stunning and interactive 3D web applications.

For more in-depth learning, the three.js documentation and the three.js fundamentals website are great resources.

## Sources
1. "Three.js - Javascript 3D Library." Three.js. https://threejs.org/
2. "Three.js Fundamentals." Three.js Fundamentals. https://threejsfundamentals.org/
3. "WebGL - OpenGL ES for the Web." Khronos Group. https://www.khronos.org/webgl/
