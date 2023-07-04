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
- "Three.js - Javascript 3D Library." Three.js. https://threejs.org/
- "Three.js Fundamentals." Three.js Fundamentals. https://threejsfundamentals.org/
- "WebGL - OpenGL ES for the Web." Khronos Group. https://www.khronos.org/webgl/

# Artikel 2, My Research Journey into Crafting Accessible Websites

## Introduction
During my exploration of web design, I learned the importance of creating websites that aren't just visually appealing but are accessible to everyone. I discovered that in the digital world, inclusivity is just as important as aesthetics, functionality, or search engine optimization. I was inspired to write this article because of a talk I had attended which was given by Cyd Stumpel, a Front-end developer.

## Unraveling the Concept of Accessibility
The cornerstone of my research revolved around understanding what web accessibility means. The term refers to designing and creating websites that are inclusive, ensuring individuals with disabilities can perceive, understand, navigate, and interact with the web. It also means they can contribute to the web, a right enshrined in the Convention on the Rights of Persons with Disabilities (CRPD).

Accessibility encompasses a wide range of disabilities, including blindness and low vision, deafness and hearing loss, learning disabilities, cognitive limitations, limited movement, speech disabilities, and photosensitivity.
I realized the importance of the Web Content Accessibility Guidelines (WCAG), a central element of web accessibility. Created by the World Wide Web Consortium (W3C), WCAG is organized around four principles known as POUR: Perceivable, Operable, Understandable, and Robust.

- Perceivable: This principle highlights that users must be able to perceive the information being presented. It can't be invisible to all of their senses. This involves providing text alternatives for non-text content, creating adaptable content, and making it distinguishable.
- Operable: This suggests that users must be able to operate the interface and navigation. The interface cannot require interaction that a user cannot perform. This includes making all functionalities available from a keyboard, providing users enough time, not designing content in a way that is known to cause seizures, and providing navigational aids.
- Understandable: The principle explains that users must be able to understand the information as well as the operation of the interface. The web page should not appear or operate in an unpredictable way. This involves making text readable and understandable, making web pages appear and operate in predictable ways, and helping users avoid and correct mistakes.
- Robust: This states that users must be able to access the content as technologies advance. It ensures compatibility with current and future user tools, including assistive technologies. This involves maximizing compatibility with current and future user agents, including assistive technologies.

## Creating Accessible Websites: Key Insights from My Research
Drawing from the WCAG guidelines, along with other resources, I've identified key steps and best practices to create accessible websites:

- Consistent Navigation: Keeping navigation consistent throughout the website is critical. This means maintaining the placement of elements like navigation bars, buttons, and links in the same place across different pages. It helps users learn the layout of your site and find what they need more quickly.
- Readable Text: The text should be easy to read for everyone, including people with visual impairments or learning disabilities. This involves selecting high-contrast color combinations, sans serif fonts for body text, and a minimum text size of 16 pixels.
- Alt Text for Images: Every image should have alternative text, often known as "alt text". This text describes the content of the image and is especially useful for those who use screen readers or have slow internet connections.
- Accessible Forms: Forms should be clearly labeled and provide clear instructions. This includes appropriately labeled fields, error identification that provides suggestions to the user to correct their input, and forms that are easily navigable using a keyboard.
- Media Alternatives: Provide alternatives for audio and video content. Videos should include captions and transcripts, while podcasts should provide a written transcript. These considerations are helpful for those who are hard of hearing or prefer to read rather than listen.
Keyboard Accessibility: All website functionality should be accessible using only a keyboard. This includes access to all pages, links, content, and even form inputs.
- Avoidance of Flashing Content: Flashing content, especially those that flash more than three times per second, should be avoided as they can trigger seizures in people with photosensitive epilepsy.
- Testing and Validation: One of the most critical steps is to test the website's accessibility. Tools like the WAVE Web Accessibility Evaluation Tool can help identify areas of improvement. Additionally, getting feedback from users with disabilities can provide real-world insights into your website's accessibility.

## Conclusion
The journey of creating an accessible website, while challenging, is deeply rewarding. It has broadened my understanding of web design from mere aesthetics to a more inclusive and holistic approach. Although making a site accessible might require additional effort, it ensures that everyone can benefit from the information and services provided, which, in my eyes, is a mark of true success in the digital landscape.

## Sources
- "Web Content Accessibility Guidelines (WCAG) Overview." W3C. https://www.w3.org/WAI/standards-guidelines/wcag/
- "Introduction to Web Accessibility." Web Accessibility Initiative. https://www.w3.org/WAI/fundamentals/accessibility-intro/
- "WAVE Web Accessibility Evaluation Tool." WebAIM. https://wave.webaim.org/

# Artikel 3,

## Introduction 
