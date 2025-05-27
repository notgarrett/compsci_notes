---
tags:
  - flashcards
---

>[!question]
>What is the primary purpose of hierarchical modeling in computer graphics?
>- To increase rendering complexity.
>- To organize and manipulate objects efficiently using a structured hierarchy.
>- To eliminate the need for transformations.
>- To replace rasterization with vector graphics.
>
?
>>[!answer]
>>To organize and manipulate objects efficiently using a structured hierarchy.

>[!question]
>In hierarchical modeling, transformations such as translation, rotation, and scaling are typically applied using:
>- Global coordinates only.
>- Local coordinate systems and parent-child relationships.
>- A single universal transformation matrix.
>- A direct pixel manipulation technique.
>
?
>>[!answer]
>>Local coordinate systems and parent-child relationships.
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which data structure is commonly used to represent hierarchical models in computer graphics?
>- Linked List  
>- Binary Tree  
>- Scene Graph  
>- Hash Table  
>
?
>>[!answer]
>>Scene Graph

>[!question]
>In a hierarchical model, if a parent node undergoes a transformation, how does it affect the child nodes?
>- Child nodes remain unchanged.  
>- Child nodes inherit the transformation of the parent.  
>- Child nodes only inherit scaling transformations.  
>- Child nodes apply transformations independently of the parent.  
>
?
>>[!answer]
>>Child nodes inherit the transformation of the parent.

>[!question]
>Which of the following is an example of hierarchical modeling in computer graphics?
>- Applying a single transformation to all objects in a scene independently.
>- Modeling a robotic arm where each joint's movement depends on the previous joint.
>- Using a single texture map for an entire 3D scene.
>- Rendering a 2D sprite with no dependencies.
>
?
>>[!answer]
>>Modeling a robotic arm where each joint's movement depends on the previous joint.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the advantage of using hierarchical modeling in animation?
>- It simplifies the rendering process by reducing computations.
>- It allows complex objects to be animated more efficiently by manipulating sub-parts.
>- It eliminates the need for keyframe animation.
>- It ensures all objects move in a synchronized manner without individual transformations.
>
?
>>[!answer]
>>It allows complex objects to be animated more efficiently by manipulating sub-parts.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the key benefit of hierarchical modeling in computer graphics?
>- It reduces memory usage.  
>- It organizes objects into a structured hierarchy for better transformations.  
>- It eliminates the need for rendering pipelines.
>- It removes the need for coordinate transformations.
>
?
>>[!answer]
>>It organizes objects into a structured hierarchy for better transformations.

>[!question]
>Which data structure is commonly used to represent hierarchical models?
>- Linked List  
>- Graph  
>- Scene Graph  
>- Stack  
>
?
>>[!answer]
>>Scene Graph

>[!question]
>How does hierarchical modeling improve object manipulation?
>- It forces objects to have the same transformations.
>- It allows transformations to be applied independently of the object structure.
>- It enables nested objects to inherit transformations from parent objects.
>- It does not affect transformations.
>
?
>>[!answer]
>>It enables nested objects to inherit transformations from parent objects.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the purpose of a matrix stack in computer graphics?
>- To store transformation matrices in a hierarchical manner.  
>- To perform pixel-based rendering.  
>- To create textures for objects.  
>- To optimize ray tracing computations.  
>
?
>>[!answer]
>>To store transformation matrices in a hierarchical manner.

>[!question]
>How does the matrix stack help in hierarchical transformations?
>- It speeds up rendering by avoiding transformations.  
>- It allows transformations to be pushed and popped for managing nested structures.  
>- It removes the need for coordinate systems.  
>- It prevents objects from being transformed.  
>
?
>>[!answer]
>>It allows transformations to be pushed and popped for managing nested structures.

>[!question]
>What happens when a transformation matrix is pushed onto the stack?
>- The previous transformations are erased.  
>- A copy of the current transformation matrix is stored for later use.  
>- The scene is reset to the default transformation.  
>- The rendering process restarts.  
>
?
>>[!answer]
>>A copy of the current transformation matrix is stored for later use.

>[!question]
>What does the "matrix stem" refer to in hierarchical modeling?
>- The root transformation matrix in a hierarchy.
>- A method to optimize rendering pipelines.
>- A technique to store multiple transformations in one matrix.
>- The use of identity matrices for transformations.
>
?
>>[!answer]
>>The root transformation matrix in a hierarchy.
<!--SR:!2025-04-14,1,230-->

>[!question]
>In hierarchical modeling, what role does the matrix stem play?
>- It acts as the origin of transformations that propagate through the hierarchy.
>- It replaces the need for local transformations.
>- It stores all transformation matrices in a single matrix.
>- It is used only in rasterization.
>
?
>>[!answer]
>>It acts as the origin of transformations that propagate through the hierarchy.
<!--SR:!2025-04-14,1,230-->

>[!question]
>How does transformation propagation work in hierarchical models?
>- Parent transformations are ignored when rendering child objects.  
>- Transformations applied to parent objects affect child objects.  
>- Transformations are applied in reverse order to child objects.  
>- Child objects cannot have their own transformations.  
>
?
>>[!answer]
>>Transformations applied to parent objects affect child objects.

>[!question]
>What is the correct order of transformations when propagating transformations in a hierarchy?
>- Scaling → Rotation → Translation  
>- Translation → Rotation → Scaling  
>- Rotation → Translation → Scaling  
>- The order depends on the scene graph.  
>
?
>>[!answer]
>>The order depends on the scene graph.

>[!question]
>Which of the following is an example of transformation propagation?
>- A character’s arm moving with the body in an animation.
>- A static 2D image being displayed.
>- A cube being rendered without any transformations.
>- A pixel shader applying color changes to a texture.
>
?
>>[!answer]
>>A character’s arm moving with the body in an animation.
<!--SR:!2025-04-14,1,230-->

>[!question]
>Why is transformation propagation important in hierarchical modeling?
>- It allows independent transformations without any relation between objects.  
>- It ensures consistency in movement and transformations across connected objects.  
>- It prevents transformations from being applied to objects.  
>- It eliminates the need for GPU processing.  
>
?
>>[!answer]
>>It ensures consistency in movement and transformations across connected objects.

>[!question]
>What is the primary purpose of rendering in 3D computer graphics?
>- To create wireframe models only.
>- To convert 3D models into 2D images using lighting, shading, and textures.
>- To increase the complexity of calculations.
>- To store object data without visualization.
>
?
>>[!answer]
>>To convert 3D models into 2D images using lighting, shading, and textures.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the main advantage of ray tracing in 3D rendering?
>- It is computationally inexpensive.  
>- It accurately simulates real-world lighting, reflections, and shadows.  
>- It eliminates the need for rasterization.  
>- It does not require GPU acceleration.  
>
?
>>[!answer]
>>It accurately simulates real-world lighting, reflections, and shadows.

>[!question]
>What type of lighting model considers ambient, diffuse, and specular components?
>- Flat shading  
>- Phong lighting model  
>- Wireframe rendering  
>- Ray marching  
>
?
>>[!answer]
>>Phong lighting model

>[!question]
>What is the purpose of shadow mapping in 3D rendering?
>- To improve texture resolution.  
>- To simulate how light interacts with objects and casts shadows.  
>- To enhance the polygon count of objects.  
>- To eliminate the need for ray tracing.  
>
?
>>[!answer]
>>To simulate how light interacts with objects and casts shadows.

>[!question]
>What is the purpose of projection in 3D graphics?
>- To convert a 3D scene into a 2D image for display.  
>- To increase the number of polygons in a scene.  
>- To eliminate depth information from the scene.  
>- To directly manipulate pixel colors.  
>
?
>>[!answer]
>>To convert a 3D scene into a 2D image for display.

>[!question]
>In perspective projection, objects appear:
>- The same size regardless of their distance.
>- Larger when farther from the camera.
>- Smaller when farther from the camera.
>- Unaffected by camera position.
>
?
>>[!answer]
>>Smaller when farther from the camera.
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which mathematical concept is commonly used to represent perspective projection?
>- Matrix transformations  
>- Simple arithmetic operations  
>- Boolean logic  
>- Differential equations  
>
?
>>[!answer]
>>Matrix transformations

>[!question]
>What is perspective convergence in 3D graphics?
>- The phenomenon where parallel lines appear to meet at a distance.
>- The process of increasing an object’s size based on distance.
>- The method of removing hidden surfaces.
>- The technique used in texture mapping.
>
?
>>[!answer]
>>The phenomenon where parallel lines appear to meet at a distance.
<!--SR:!2025-04-14,1,230-->

>[!question]
>In perspective projection, what is the vanishing point?
>- The point where objects disappear from view.
>- The point where parallel lines appear to converge.
>- The farthest point visible in an orthographic projection.
>- A fixed coordinate in object space.
>
?
>>[!answer]
>>The point where parallel lines appear to converge.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is a key characteristic of orthographic projection?
>- It preserves object proportions without perspective distortion.  
>- It makes objects appear smaller as they move farther away.  
>- It is only used for artistic drawings.  
>- It requires ray tracing for accurate rendering.  
>
?
>>[!answer]
>>It preserves object proportions without perspective distortion.

>[!question]
>What differentiates oblique projection from orthographic projection?
>- Oblique projection distorts depth, while orthographic projection does not.
>- Oblique projection removes all depth information.
>- Oblique projection eliminates parallel lines.
>- Oblique projection does not allow scaling transformations.
>
?
>>[!answer]
>>Oblique projection distorts depth, while orthographic projection does not.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the view volume in 3D rendering?
>- The region of space that is visible after projection.  
>- The entire 3D world space.  
>- The number of polygons rendered per frame.  
>- The resolution of the final image.  
>
?
>>[!answer]
>>The region of space that is visible after projection.

>[!question]
>Which of the following are common types of view volumes?
>- Cubic and Cylindrical  
>- Frustum and Orthographic  
>- Spherical and Elliptical  
>- Pyramid and Rectangular Grid  
>
?
>>[!answer]
>>Frustum and Orthographic

>[!question]
>What is the primary goal of rendering in 3D graphics?
>- Creating 3D models
>- Converting 3D scenes into 2D images
>- Animating objects
>- Simulating physics
>
?
>>[!answer]
>>Converting 3D scenes into 2D images
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which rendering technique simulates the way light interacts with objects by tracing rays from the camera?
>- Rasterization  
>- Ray casting  
>- Ray tracing  
>- Scanline rendering  
>
?
>>[!answer]
>>Ray casting

>[!question]
>In ray tracing, what is a "shadow ray" used for?
>- To determine the color of a pixel
>- To check if a point is in shadow
>- To calculate reflections
>- To generate ambient occlusion
>
?
>>[!answer]
>>To check if a point is in shadow
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which type of light source emits light uniformly in all directions?
>- Directional light
>- Point light
>- Spot light
>- Ambient light
>
?
>>[!answer]
>>Point light
<!--SR:!2025-04-14,1,230-->

>[!question]
>What type of shadow is softer and more realistic, created using area lights?
>- Hard shadow
>- Umbra shadow
>- Penumbra shadow
>- Diffuse shadow
>
?
>>[!answer]
>>Penumbra shadow
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which lighting model approximates how light reflects off diffuse surfaces?
>- Phong shading
>- Lambertian reflectance
>- Blinn-Phong
>- Fresnel effect
>
?
>>[!answer]
>>Lambertian reflectance
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which projection type gives a realistic view where distant objects appear smaller?
>- Orthographic  
>- Oblique  
>- Perspective  
>- Isometric  
>
?
>>[!answer]
>>Perspective

>[!question]
>In perspective projection, what is the "vanishing point"?
>- The point where parallel lines converge  
>- The center of the image  
>- The farthest point in the scene  
>- The position of the light source  
>
?
>>[!answer]
>>The point where parallel lines converge

>[!question]
>What is "perspective convergence"?
>- The bending of light rays  
>- The phenomenon where parallel lines appear to meet at a distance  
>- The blending of colors in a gradient  
>- The distortion of textures  
>
?
>>[!answer]
>>The phenomenon where parallel lines appear to meet at a distance

>[!question]
>Which matrix is used to transform 3D world coordinates to 2D screen coordinates in perspective projection?
>- Model matrix
>- View matrix
>- Projection matrix
>- Viewport matrix
>
?
>>[!answer]
>>Projection matrix
<!--SR:!2025-04-14,1,230-->

>[!question]
>In homogeneous coordinates, what does the perspective divide (dividing by the w-component) achieve?
>- Normalizes the vector
>- Applies scaling
>- Converts from clip space to NDC (Normalized Device Coordinates)
>- Removes lighting effects
>
?
>>[!answer]
>>Converts from clip space to NDC (Normalized Device Coordinates)
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which projection maintains parallel lines and does not exhibit foreshortening?
>- Perspective projection  
>- Orthographic projection  
>- Oblique projection  
>- Isometric projection  
>
?
>>[!answer]
>>Orthographic projection

>[!question]
>What is a key characteristic of oblique projection?
>- All axes are equally foreshortened
>- One face is parallel to the projection plane, and depth is at an angle
>- It uses a vanishing point
>- It mimics human vision
>
?
>>[!answer]
>>One face is parallel to the projection plane, and depth is at an angle
<!--SR:!2025-04-14,1,230-->

>[!question]
>What defines the boundaries of the visible 3D space in a rendered scene?
>- Clipping plane  
>- View volume  
>- Bounding box  
>- Frustum  
>
?
>>[!answer]
>>View volume

>[!question]
>In perspective projection, the view volume is a:
>- Cube  
>- Frustum (truncated pyramid)  
>- Sphere  
>- Cylinder  
>
?
>>[!answer]
>>Frustum (truncated pyramid)

>[!question]
>Which type of view volume is used in orthographic projection?
>- Frustum  
>- Rectangular prism  
>- Sphere  
>- Cone  
>
?
>>[!answer]
>>Rectangular prism

>[!question]
>Which of the following is NOT a type of light source in 3D graphics?
>- Directional  
>- Ambient  
>- Reflective  
>- Spot  
>
?
>>[!answer]
>>Reflective

>[!question]
>What is the primary difference between Phong and Gouraud shading?
>- Gouraud interpolates colors, Phong interpolates normals  
>- Phong is faster than Gouraud  
>- Gouraud is used only for ray tracing  
>- Phong does not handle specular highlights  
>
?
>>[!answer]
>>Gouraud interpolates colors, Phong interpolates normals

>[!question]
>Which technique helps reduce aliasing in rendered images?
>- Mipmapping  
>- Anti-aliasing  
>- Z-buffering  
>- Clipping  
>
?
>>[!answer]
>>Anti-aliasing

>[!question]
>What is the purpose of the "z-buffer" in rendering?
>- To store texture coordinates  
>- To determine visibility by depth testing  
>- To calculate reflections  
>- To apply shadows  
>
?
>>[!answer]
>>To determine visibility by depth testing

>[!question]
>In ray tracing, what does "recursive ray tracing" involve?
>- Tracing rays only once per pixel  
>- Tracing secondary rays for reflections and refractions  
>- Using only shadow rays  
>- Ignoring global illumination  
>
?
>>[!answer]
>>Tracing secondary rays for reflections and refractions

>[!question]
>Which of the following best describes "ambient occlusion"?
>- A technique to simulate soft shadows in crevices  
>- A type of directional light  
>- A method for texture filtering  
>- A form of orthographic projection  
>
?
>>[!answer]
>>A technique to simulate soft shadows in crevices

>[!question]
>What is the "focal length" in perspective projection?
>- The distance between the camera and the near clipping plane  
>- The angle of the camera’s field of view  
>- The distance between the camera and the projection plane  
>- The depth of the view volume  
>
?
>>[!answer]
>>The distance between the camera and the projection plane

>[!question]
>Which of the following is NOT a common type of camera projection in 3D graphics?
>- Perspective  
>- Orthographic  
>- Isometric  
>- Parabolic  
>
?
>>[!answer]
>>Parabolic

>[!question]
>What is the primary advantage of using a "view frustum" in rendering?
>- It simplifies lighting calculations  
>- It defines the visible area and improves culling efficiency  
>- It eliminates the need for a z-buffer  
>- It reduces texture memory usage  
>
?
>>[!answer]
>>It defines the visible area and improves culling efficiency

>[!question]
>In which projection do objects retain their true proportions regardless of distance?
>- Perspective  
>- Orthographic  
>- Oblique  
>- Fisheye  
>
?
>>[!answer]
>>Orthographic

>[!question]
>What happens to parallel lines in orthographic projection?
>- They converge at a vanishing point
>- They remain parallel
>- They curve
>- They disappear
>
?
>>[!answer]
>>They remain parallel
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which of the following is a common use of orthographic projection?
>- Video games  
>- Architectural blueprints  
>- Movie special effects  
>- Virtual reality  
>
?
>>[!answer]
>>Architectural blueprints

>[!question]
>What is the main disadvantage of ray tracing compared to rasterization?
>- It cannot handle shadows  
>- It is computationally expensive  
>- It does not work with textures  
>- It cannot render transparent objects  
>
?
>>[!answer]
>>It is computationally expensive

>[!question]
>Which of the following best describes "perspective distortion"?
>- The bending of light rays in a lens
>- The stretching or compression of objects due to camera angle
>- A type of texture filtering
>- An error in z-buffering
>
?
>>[!answer]
>>The stretching or compression of objects due to camera angle
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the primary purpose of perspective projection in 3D graphics?
>- To maintain parallel lines  
>- To simulate how objects appear smaller with distance  
>- To remove depth information  
>- To flatten all objects into 2D  
>
?
>>[!answer]
>>To simulate how objects appear smaller with distance

>[!question]
>Which of the following best defines the "field of view" (FOV) in perspective projection?
>- The distance to the far clipping plane
>- The angular extent of the visible scene
>- The aspect ratio of the viewport
>- The position of the vanishing point
>
?
>>[!answer]
>>The angular extent of the visible scene
<!--SR:!2025-04-14,1,230-->

>[!question]
>What happens to parallel lines in perspective projection?
>- They remain parallel
>- They converge at a vanishing point
>- They become curved
>- They disappear
>
?
>>[!answer]
>>They converge at a vanishing point
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which matrix is responsible for converting 3D eye-space coordinates to clip-space coordinates?
>- Model matrix  
>- View matrix  
>- Projection matrix  
>- Viewport matrix  
>
?
>>[!answer]
>>Projection matrix

>[!question]
>In a perspective projection matrix, what does the z coordinate become after the perspective divide?
>- It is discarded  
>- It becomes a depth value in Normalized Device Coordinates (NDC)  
>- It controls brightness  
>- It determines texture mapping  
>
?
>>[!answer]
>>It becomes a depth value in Normalized Device Coordinates (NDC)

>[!question]
>What is the role of the w component in homogeneous coordinates after applying a perspective matrix?
>- It stores color information  
>- It is used for the perspective divide (dividing x, y, z by w)  
>- It defines lighting intensity  
>- It determines anti-aliasing  
>
?
>>[!answer]
>>It is used for the perspective divide (dividing x, y, z by w)

>[!question]
>Which of the following is a correct form of a perspective projection matrix (OpenGL-style)?
>- \[1, 0, 0, 0; 0, 1, 0, 0; 0, 0, -1, 0; 0, 0, 0, 1]
>- \[f/aspect, 0, 0, 0; 0, f, 0, 0; 0, 0, (far+near)/(near-far), (2\*far\*near)/(near-far); 0, 0, -1, 0]
>- \[1, 0, 0, 0; 0, 1, 0, 0; 0, 0, 1, 0; 0, 0, 0, 0]
>- \[f, 0, 0, 0; 0, f, 0, 0; 0, 0, 1, 0; 0, 0, 0, 1]
>
?
>>[!answer]
>>\[f/aspect, 0, 0, 0; 0, f, 0, 0; 0, 0, (far+near)/(near-far), (2\*far\*near)/(near-far); 0, 0, -1, 0]
<!--SR:!2025-04-14,1,230-->

>[!question]
>How does increasing the field of view (FOV) affect the rendered scene?
>- Objects appear larger
>- More of the scene is visible, but objects appear smaller
>- Depth perception is lost
>- The aspect ratio changes
>
?
>>[!answer]
>>More of the scene is visible, but objects appear smaller
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which FOV angle gives a natural-looking perspective similar to human vision?
>- 30°  
>- 45°  
>- 60°  
>- 90°  
>
?
>>[!answer]
>>60°

>[!question]
>What happens if the vertical and horizontal FOVs are mismatched with the aspect ratio?
>- The image appears stretched or squashed  
>- Depth testing fails  
>- Lighting calculations break  
>- The view frustum becomes orthographic  
>
?
>>[!answer]
>>The image appears stretched or squashed

>[!question]
>What geometric shape defines the perspective view frustum?
>- A cube
>- A sphere
>- A truncated pyramid
>- A cylinder
>
?
>>[!answer]
>>A truncated pyramid
<!--SR:!2025-04-17,4,270-->

>[!question]
>Which planes define the boundaries of the view frustum?
>- Top, bottom, left, right, near, far  
>- Front, back, up, down  
>- X, Y, Z clipping planes  
>- Only near and far planes  
>
?
>>[!answer]
>>Top, bottom, left, right, near, far

# 74
>[!question]
>What is the purpose of the near clipping plane in the view frustum?
>- To define the minimum render distance  
>- To set the camera position  
>- To control FOV  
>- To remove distant objects  
>
?
>>[!answer]
>>**TBA**

>[!question]
>What happens to objects outside the view frustum?
>- They are rendered with lower quality  
>- They are clipped (not rendered)  
>- They appear distorted  
>- They are automatically scaled down  
>
?
>>[!answer]
>>They are clipped (not rendered)

>[!question]
>What is the primary purpose of the perspective projection matrix?
>- To position objects in the world
>- To convert 3D eye-space coordinates into clip-space
>- To apply lighting effects
>- To generate textures
>
?
>>[!answer]
>>To convert 3D eye-space coordinates into clip-space
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which parameter does NOT influence the perspective projection matrix?
>- Field of view (FOV)  
>- Aspect ratio  
>- Camera position  
>- Near and far clipping planes  
>
?
>>[!answer]
>>Camera position

# 78
>[!question]
>How is the aspect ratio used in the perspective matrix?
>- It scales the x-coordinate to prevent distortion
>- It controls the far clipping plane
>- It adjusts the FOV
>- It modifies the depth buffer
>
?
>>[!answer]
>>**TBA**
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the effect of setting the far clipping plane too far in perspective projection?
>- Improves performance  
>- Causes z-fighting (depth precision issues)  
>- Makes objects appear larger  
>- Disables perspective correction  
>
?
>>[!answer]
>>Causes z-fighting (depth precision issues)

>[!question]
>Which function in OpenGL/GLM creates a perspective projection matrix?
>- glOrtho()  
>- gluPerspective() / glm:\:perspective()  
>- glFrustum()  
>- glLookAt()  
>
?
>>[!answer]
>>gluPerspective() / glm:\:perspective()

>[!question]
>What is the correct order of transformations in the graphics pipeline?
>- Model → Projection → View
>- View → Model → Projection
>- Model → View → Projection
>- Projection → View → Model
>
?
>>[!answer]
>>Model → View → Projection
<!--SR:!2025-04-14,1,230-->

>[!question]
>What shape defines the perspective view frustum in 3D graphics?
>- Sphere  
>- Cube  
>- Truncated pyramid  
>- Cylinder  
>
?
>>[!answer]
>>Truncated pyramid

>[!question]
>Which planes define the boundaries of the view frustum?
>- Top, bottom, left, right, near, far  
>- Front, back, up, down  
>- X, Y, Z axes  
>- Only near and far planes  
>
?
>>[!answer]
>>Top, bottom, left, right, near, far

>[!question]
>What happens to objects outside the view frustum?
>- They are rendered with lower detail  
>- They are clipped (discarded)  
>- They appear stretched  
>- They are automatically scaled down  
>
?
>>[!answer]
>>They are clipped (discarded)

>[!question]
>What is the purpose of the near clipping plane?
>- To define the farthest visible distance
>- To set the minimum render distance
>- To control the field of view
>- To adjust the aspect ratio
>
?
>>[!answer]
>>To set the minimum render distance
<!--SR:!2025-04-14,1,230-->

>[!question]
>How does increasing the far clipping plane affect depth precision?
>- Improves it  
>- Causes z-fighting (depth artifacts)  
>- Has no effect  
>- Makes objects appear larger  
>
?
>>[!answer]
>>Causes z-fighting (depth artifacts)

>[!question]
>Which matrix is used to move an object in 3D space?
>- Rotation matrix  
>- Scaling matrix  
>- Translation matrix  
>- Projection matrix  
>
?
>>[!answer]
>>Translation matrix

>[!question]
>What is the correct order to apply transformations (scale, rotate, translate)?
>- Translate → Rotate → Scale  
>- Scale → Rotate → Translate  
>- Rotate → Translate → Scale  
>- Order does not matter  
>
?
>>[!answer]
>>Scale → Rotate → Translate

>[!question]
>Which transformation changes the size of an object?
>- Rotation  
>- Translation  
>- Scaling  
>- Shearing  
>
?
>>[!answer]
>>Scaling

>[!question]
>What does a 4x4 transformation matrix allow in homogeneous coordinates?
>- Only rotations
>- Only translations
>- Combined rotations, translations, and scaling
>- Only perspective corrections
>
?
>>[!answer]
>>Combined rotations, translations, and scaling
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which of the following is NOT a basic 3D transformation?
>- Translation  
>- Rotation  
>- Reflection  
>- Color grading  
>
?
>>[!answer]
>>Color grading

>[!question]
>How many degrees of freedom does a 3D rotation have?
>- 1  
>- 2  
>- 3 (roll, pitch and yaw)  
>- 4  
>
?
>>[!answer]
>>3 (roll, pitch and yaw)

>[!question]
>Which axis is typically used for "yaw" rotation?
>- X-axis
>- Y-axis
>- Z-axis
>- W-axis
>
?
>>[!answer]
>>Y-axis
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is quaternion rotation used for?
>- Faster interpolation than Euler angles
>- Only 2D rotations
>- Simplifying translations
>- Increasing polygon count
>
?
>>[!answer]
>>Faster interpolation than Euler angles
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which rotation method avoids gimbal lock?
>- Euler angles  
>- Axis-angle  
>- Quaternions  
>- Spherical coordinates  
>
?
>>[!answer]
>>Quaternions

>[!question]
>What are Euler angles?
>- A set of three angles (roll, pitch, yaw)  
>- A single rotation axis  
>- A 4x4 transformation matrix  
>- A type of scaling factor  
>
?
>>[!answer]
>>A set of three angles (roll, pitch, yaw)

>[!question]
>What is the main disadvantage of Euler angles?
>- They cannot represent rotations
>- They suffer from gimbal lock
>- They are too precise
>- They only work in 2D
>
?
>>[!answer]
>>They suffer from gimbal lock
<!--SR:!2025-04-14,1,230-->

>[!question]
>In which scenario does gimbal lock occur?
>- When two axes align, losing a degree of freedom
>- When all three axes are perpendicular
>- When using quaternions
>- When translating an object
>
?
>>[!answer]
>>When two axes align, losing a degree of freedom
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which rotation order is commonly used in aerospace (e.g., NASA)?
>- ZYX  
>- XYZ  
>- YXZ  
>- ZXZ  
>
?
>>[!answer]
>>ZYX

>[!question]
>How can gimbal lock be mitigated?
>- Using only 2D rotations
>- Avoiding rotations altogether
>- Using quaternions or axis-angle representations
>- Increasing the near clipping plane
>
?
>>[!answer]
>>Using quaternions or axis-angle representations
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is gimbal lock?
>- A hardware failure in 3D mice  
>- A loss of rotational degree of freedom due to aligned axes  
>- A type of projection error  
>- A texture rendering artifact  
>
?
>>[!answer]
>>A loss of rotational degree of freedom due to aligned axes

>[!question]
>Which Euler angle sequence is most prone to gimbal lock?
>- XYZ  
>- XZY  
>- ZYX  
>- All sequences can experience it  
>
?
>>[!answer]
>>All sequences can experience it

>[!question]
>In which real-world application is gimbal lock a critical problem?
>- 2D sprite animation  
>- Spacecraft attitude control  
>- Pixel shading  
>- Audio processing  
>
?
>>[!answer]
>>Spacecraft attitude control

>[!question]
>Which alternative to Euler angles avoids gimbal lock?
>- Cartesian coordinates  
>- Quaternions  
>- Affine transformations  
>- Orthographic projection  
>
?
>>[!answer]
>>Quaternions

>[!question]
>What visual artifact might gimbal lock cause in a 3D animation?
>- Sudden jumps in rotation
>- Objects disappearing
>- Incorrect shadows
>- Texture stretching
>
?
>>[!answer]
>>Sudden jumps in rotation
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the primary purpose of view frustum culling?
>- To sort objects by color  
>- To discard objects outside the camera’s visible volume  
>- To apply textures efficiently  
>- To calculate lighting  
>
?
>>[!answer]
>>To discard objects outside the camera’s visible volume

>[!question]
>Which technique checks if an object’s bounding volume intersects the view frustum?
>- Ray tracing
>- Z-buffering
>- Frustum culling
>- Painter’s algorithm
>
?
>>[!answer]
>>Frustum culling
<!--SR:!2025-04-14,1,230-->

>[!question]
>What happens to objects failing the view frustum test?
>- They are rendered with lower detail  
>- They are excluded from rendering  
>- They are moved closer to the camera  
>- Their textures are compressed  
>
?
>>[!answer]
>>They are excluded from rendering

>[!question]
>How does the Painter’s Algorithm determine visibility?
>- By depth testing each pixel  
>- By sorting objects from back to front and drawing them in order  
>- By using ray casting  
>- By comparing surface normals  
>
?
>>[!answer]
>>By sorting objects from back to front and drawing them in order

>[!question]
>What is a major drawback of the Painter’s Algorithm?
>- It requires excessive memory  
>- It cannot handle overlapping or cyclic occlusions  
>- It only works in orthographic projection  
>- It ignores lighting calculations  
>
?
>>[!answer]
>>It cannot handle overlapping or cyclic occlusions

>[!question]
>Which scenario breaks the Painter’s Algorithm?
>- A triangle fully behind another  
>- Three triangles overlapping in a cyclic manner (A over B, B over C, C over A)  
>- A triangle intersecting the view frustum  
>- A triangle with transparency  
>
?
>>[!answer]
>>Three triangles overlapping in a cyclic manner (A over B, B over C, C over A)

>[!question]
>Why is the Painter’s Algorithm rarely used in modern 3D graphics?
>- It is incompatible with GPUs  
>- Z-buffering is more efficient and accurate  
>- It only works for 2D sprites  
>- It requires ray tracing  
>
?
>>[!answer]
>>Z-buffering is more efficient and accurate

>[!question]
>What does the Z-buffer store for each pixel?
>- Color values  
>- Depth (distance from the camera)  
>- Texture coordinates  
>- Normal vectors  
>
?
>>[!answer]
>>Depth (distance from the camera)

# 114
>[!question]
>How does the Z-buffer resolve visibility between overlapping objects?
>- By blending their colors  
>- By keeping the object with the smallest Z-value (closest to the camera)  
>- By averaging their depths  
>- By discarding all overlapping pixels  
>
?
>>[!answer]
>>**TBA**

>[!question]
>What is the key advantage of Z-buffering over the Painter’s Algorithm?
>- It handles cyclic overlaps correctly
>- It requires no sorting
>- It works with transparency
>- Both a and b
>
?
>>[!answer]
>>Both a and b
<!--SR:!2025-04-14,1,230-->

>[!question]
>What causes Z-fighting?
>- Too many light sources
>- Insufficient Z-buffer precision for overlapping surfaces
>- Incorrect backface culling
>- Missing textures
>
?
>>[!answer]
>>Insufficient Z-buffer precision for overlapping surfaces
<!--SR:!2025-04-14,1,230-->

>[!question]
>How can Z-fighting be reduced?
>- Increasing the far clipping plane distance
>- Decreasing the near clipping plane distance
>- Using a higher precision depth buffer (e.g., 24-bit instead of 16-bit)
>- Disabling depth testing
>
?
>>[!answer]
>>Using a higher precision depth buffer (e.g., 24-bit instead of 16-bit)
<!--SR:!2025-04-14,1,230-->

>[!question]
>What visual artifact does Z-fighting produce?
>- Flickering or shimmering surfaces  
>- Black pixels  
>- Overly bright highlights  
>- Texture stretching  
>
?
>>[!answer]
>>Flickering or shimmering surfaces

>[!question]
>What is the purpose of backface culling?
>- To remove polygons facing away from the camera  
>- To sort transparent objects  
>- To calculate shadows  
>- To compress vertex data  
>
?
>>[!answer]
>>To remove polygons facing away from the camera

>[!question]
>How is backface culling typically determined?
>- By comparing the dot product of the view vector and face normal
>- By checking texture coordinates
>- By depth testing
>- By counting vertices
>
?
>>[!answer]
>>By comparing the dot product of the view vector and face normal
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the purpose of view volume testing in 3D rendering?
>- To eliminate objects that are outside the camera’s field of view.  
>- To increase the number of polygons rendered.  
>- To convert 2D objects into 3D objects.  
>- To apply textures to objects.  
>
?
>>[!answer]
>>To eliminate objects that are outside the camera’s field of view.

>[!question]
>What shape does the view volume take in perspective projection?
>- A cube
>- A frustum
>- A sphere
>- A cone
>
?
>>[!answer]
>>A frustum
<!--SR:!2025-04-14,1,230-->

>[!question]
>In view volume testing, what happens to objects that are entirely outside the view volume?
>- They are rendered but at a lower resolution.  
>- They are culled to improve performance.  
>- They are converted into wireframe models.  
>- They are stored for future rendering.  
>
?
>>[!answer]
>>They are culled to improve performance.

>[!question]
>What is a bounding volume in computer graphics?
>- A simplified geometric shape used to approximate an object's spatial extent.  
>- A detailed 3D model of an object.  
>- A texture applied to an object.  
>- A transformation matrix.  
>
?
>>[!answer]
>>A simplified geometric shape used to approximate an object's spatial extent.

>[!question]
>Why are bounding volumes used in collision detection and rendering?
>- To improve performance by reducing the number of detailed intersection tests.
>- To replace the need for rasterization.
>- To increase the polygon count of a scene.
>- To eliminate the need for GPU acceleration.
>
?
>>[!answer]
>>To improve performance by reducing the number of detailed intersection tests.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is a key advantage of using bounding spheres in collision detection?
>- They provide a perfect fit for all objects.  
>- Intersection tests are computationally inexpensive.  
>- They are always aligned with the object's geometry.  
>- They require complex mathematical computations.  
>
?
>>[!answer]
>>Intersection tests are computationally inexpensive.

>[!question]
>What is a disadvantage of bounding spheres?
>- They are difficult to implement.
>- They do not tightly fit objects with irregular shapes.
>- They require more memory than other bounding volumes.
>- They cannot be used in real-time applications.
>
?
>>[!answer]
>>They do not tightly fit objects with irregular shapes.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the primary purpose of Bounding Volume Hierarchies (BVH)?
>- To organize objects into a hierarchical structure for efficient spatial queries.  
>- To replace texture mapping in 3D rendering.  
>- To increase the number of polygons in a scene.  
>- To generate high-resolution shadows.  
>
?
>>[!answer]
>>To organize objects into a hierarchical structure for efficient spatial queries.

>[!question]
>How does BVH improve rendering performance?
>- By culling entire groups of objects at once instead of checking each object individually.
>- By increasing the resolution of rendered textures.
>- By removing the need for clipping.
>- By dynamically increasing the scene complexity.
>
?
>>[!answer]
>>By culling entire groups of objects at once instead of checking each object individually.
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the role of clip-space culling in 3D rendering?
>- To remove objects that are outside the view volume before rasterization.  
>- To increase the level of detail of objects.  
>- To apply textures to objects.  
>- To eliminate shadows from the scene.  
>
?
>>[!answer]
>>To remove objects that are outside the view volume before rasterization.

>[!question]
>What happens during clipping in rasterization?
>- Parts of primitives outside the view volume are removed or adjusted.  
>- The entire 3D scene is stored in the GPU.  
>- Only wireframe models are rendered.  
>- Every object in the scene is fully rendered, regardless of visibility.  
>
?
>>[!answer]
>>Parts of primitives outside the view volume are removed or adjusted.

>[!question]
>Why is clipping important in rasterization?
>- To ensure only visible portions of objects are processed for rendering.  
>- To increase the total number of rendered objects.  
>- To remove the need for transformations.  
>- To allow objects to be rendered in wireframe mode.  
>
?
>>[!answer]
>>To ensure only visible portions of objects are processed for rendering.

>[!question]
>What is the primary purpose of clipping in rasterization?
>- To apply textures  
>- To discard geometry outside the view frustum  
>- To calculate lighting  
>- To sort polygons by color  
>
?
>>[!answer]
>>To discard geometry outside the view frustum

>[!question]
>What happens to a triangle that intersects the near clipping plane?
>- It is discarded entirely  
>- It is split into smaller triangles  
>- Its colors are inverted  
>- It is rendered with transparency  
>
?
>>[!answer]
>>It is split into smaller triangles

>[!question]
>Which coordinate space is clipping typically performed in?
>- World space  
>- View (eye) space  
>- Clip space  
>- Screen space  
>
?
>>[!answer]
>>Clip space

>[!question]
>What is the role of the Sutherland-Hodgman algorithm?
>- To clip polygons against a plane
>- To interpolate vertex colors
>- To generate mipmaps
>- To compress textures
>
?
>>[!answer]
>>To clip polygons against a plane
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is the primary purpose of a scene graph?
>- To store textures  
>- To hierarchically organize and transform objects  
>- To calculate shadows  
>- To simulate physics  
>
?
>>[!answer]
>>To hierarchically organize and transform objects

>[!question]
>Which data structure is optimized for static scenes with axis-aligned geometry?
>- Linked list  
>- Binary Space Partitioning (BSP) tree  
>- Hash table  
>- Queue  
>
?
>>[!answer]
>>Binary Space Partitioning (BSP) tree

>[!question]
>What is a key disadvantage of BSP trees for dynamic scenes?
>- High memory usage
>- Expensive recomputation when objects move
>- Inability to handle translucent objects
>- Limited to 2D spaces
>
?
>>[!answer]
>>Expensive recomputation when objects move
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which structure partitions space into nested cubes for efficient spatial queries?
>- B-tree  
>- Octree  
>- KD-tree  
>- R-tree  
>
?
>>[!answer]
>>Octree

>[!question]
>What is the main advantage of a quad-tree over an octree?
>- Better for 3D scenes
>- Lower memory usage in 2D applications
>- Faster for dynamic objects
>- Supports curved surfaces
>
?
>>[!answer]
>>Lower memory usage in 2D applications
<!--SR:!2025-04-14,1,230-->

>[!question]
>How is a BSP tree constructed?
>- By recursively splitting space with hyperplanes  
>- By sorting polygons alphabetically  
>- By grouping textures  
>- By averaging vertex colors  
>
?
>>[!answer]
>>By recursively splitting space with hyperplanes

>[!question]
>In a BSP tree, what determines the splitting plane at each node?
>- A randomly chosen polygon
>- The polygon that best divides remaining geometry evenly
>- The largest polygon in the scene
>- The furthest polygon from the camera
>
?
>>[!answer]
>>The polygon that best divides remaining geometry evenly
<!--SR:!2025-04-14,1,230-->

>[!question]
>What is a key limitation of BSP trees?
>- Only works for 2D games  
>- Poor handling of dynamic objects  
>- Requires ray tracing  
>- Ignores lighting calculations  
>
?
>>[!answer]
>>Poor handling of dynamic objects

>[!question]
>Which industry uses 3D rendering for pre-visualizing surgical procedures?
>- Automotive  
>- Healthcare  
>- Agriculture  
>- Textile  
>
?
>>[!answer]
>>Healthcare

>[!question]
>What is a common use of 3D rendering in architecture?
>- Real-time weather simulation
>- Creating photorealistic building walkthroughs
>- Generating financial reports
>- Designing fonts
>
?
>>[!answer]
>>Creating photorealistic building walkthroughs
<!--SR:!2025-04-14,1,230-->

# 147
>[!question]
>Which technology relies heavily on 3D rendering for immersive experiences?
>- Spreadsheets  
>- Virtual Reality (VR)  
>- Email clients  
>- Word processors  
>
?
>>[!answer]
>>**TBA**

>[!question]
>Which algorithm is commonly used for real-time rasterization?
>- Path tracing  
>- Scanline rendering  
>- Photon mapping  
>- Metropolis light transport  
>
?
>>[!answer]
>>Scanline rendering

>[!question]
>What does ray tracing simulate more accurately than rasterization?
>- Polygon counts
>- Light reflections and refractions
>- Texture compression
>- Vertex shading
>
?
>>[!answer]
>>Light reflections and refractions
<!--SR:!2025-04-14,1,230-->

>[!question]
>Which hybrid rendering technique combines rasterization and ray tracing?
>- Z-buffering  
>- Deferred shading  
>- Hybrid ray marching  
>- NVIDIA’s RTX (DLSS + ray tracing)  
>
?
>>[!answer]
>>NVIDIA’s RTX (DLSS + ray tracing)

>[!question]
>What is the primary use of an octree in 3D rendering?
>- To store audio data  
>- To accelerate collision detection and visibility tests  
>- To compress video files  
>- To generate random numbers  
>
?
>>[!answer]
>>To accelerate collision detection and visibility tests

>[!question]
>How does a dynamic tree (e.g., loose octree) improve upon static trees?
>- By allowing runtime updates to moving objects
>- By using fixed-size nodes
>- By eliminating all memory usage
>- By rendering only 2D sprites
>
?
>>[!answer]
>>By allowing runtime updates to moving objects
<!--SR:!2025-04-17,4,270-->

>[!question]
>Which optimization is used for dynamic scenes in modern engines?
>- BSP trees  
>- Uniform grids  
>- BVH (Bounding Volume Hierarchy)  
>- Fixed arrays  
>
?
>>[!answer]
>>BVH (Bounding Volume Hierarchy)

>[!question]
>What is a drawback of quadtrees for 3D scenes?
>- They cannot represent heightmaps  
>- They ignore the Z-axis  
>- They are slower than linked lists  
>- They require ray tracing  
>
?
>>[!answer]
>>They ignore the Z-axis
