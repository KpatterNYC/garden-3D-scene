# CS 330: Computational Graphics and Visualization - Final Project

## Project Overview
This project is a 3D replication of a formal English garden, featuring a central spiral topiary, a circular trimmed hedge, a gravel pathway, and background conical trees. It was developed using C++ and OpenGL, implementing foundational graphics techniques including 3D mesh generation, texture mapping, camera navigation, and Phong lighting.

## Reflection


This project helped me craft exactly how to translate complex real-world objects into code using basic geometric primitives. I learned to look at a complex object (like a spiral topiary) and break it down into simple, stackable shapes (cones, cylinders, spheres) rather than trying to model an overly complex mesh from scratch.

My design process was highly modular and component-based. I started by identifying all the primitive shapes needed. Then, I mapped out the material and texture requirements for each surface (grass, bark, pavement). Finally, I designed the lighting environment to bring the scene together, working from the general (ambient and directional sunlight) to the specific (a colored spotlight highlighting the main object).


The tactic of breaking complex problems down into simple modular components applies to almost all software engineering. Instead of writing monolithic code, separating concerns—like having dedicated, reusable functions to apply transformations, set textures, and bind materials before drawing—makes code scalable and much easier to debug.

### How do I approach developing programs?
I relied heavily on writing custom, reusable helper functions. For example, instead of recalculating position, rotation, and translation matrices manually for every single object, I created function calls that bundled those transformations. This encapsulated the math and made the rendering loop fast to write and easy to read.

Iteration was the core of my development process in this project. I rarely got an object's scale, position, or lighting right on the first build. The development process involved placing an object, building the executable, reviewing the visual output, and tweaking the shader values or coordinate math. Iterative feedback was especially crucial when balancing the three-point lighting system so the scene felt like natural daylight without blowing out the textures.

**How has your approach to developing code evolved throughout the milestones, which led you to the project’s completion?**
Early in the course, my code was more procedural and hardcoded. As the milestones progressed to lighting and texturing, I shifted to a more declarative and organized state-machine approach. Before drawing a mesh, I set its state (texture, material, transformation) completely. This cleaner approach was the only way I could manage the complexity of rendering dozens of objects in the final milestone without severe bugs.

### How can computer science help me in reaching my goals?
Understanding the graphics pipeline provides a tangible, visual representation of complex mathematics like linear algebra and matrix transformations. This practical application bridges the gap between abstract math and real-world computing, creating a strong foundation for any advanced computer science courses involving system architecture, optimization, or physics simulations.

Building an OpenGL scene from scratch pulls back the curtain on how modern game engines, CAD software, and UI renderers actually work. Even if I do not become a dedicated graphics programmer, understanding how GPUs process vertices and fragments, how 3D math dictates object space, and how to optimize render loops are highly transferable problem-solving skills for any software engineering role that deals with performance, simulation, or data visualization.
