# MeshDistortMaterial
#### The MeshDistortMaterial is a custom shader material provided by Drei.js, which can be used to create a variety of interesting 3D effects in Three.js. The material applies a distortion effect to the geometry of the mesh, which can create effects such as ripples, waves, or bulges.

#### The MeshDistortMaterial works by taking a texture as input, which is used to define the distortion effect. The texture can be any image or data that can be loaded as a texture in Three.js, such as a PNG, JPG, or data URL. The texture is then used to displace the vertices of the mesh in a customizable way, creating the desired distortion effect.

#### The MeshDistortMaterial also provides a number of customizable parameters that can be used to fine-tune the effect, such as the intensity and frequency of the distortion, the speed of the animation, and the overall color of the material.

#### To use the MeshDistortMaterial, you need to first create a mesh object in Three.js and apply the material to it. You can then use the texture and the customizable parameters to create the desired distortion effect. Here is an example of how to create a mesh with the MeshDistortMaterial in Three.js:

```js
    import { MeshDistortMaterial } from 'drei';

    // create a mesh object with some geometry
    const geometry = new THREE.BoxGeometry(1, 1, 1);
    const mesh = new THREE.Mesh(geometry);

    // create a MeshDistortMaterial and set its parameters
    const material = new MeshDistortMaterial({
    color: 0xff0000, // set the color of the material
    distort: 0.4, // set the intensity of the distortion effect
    speed: 2, // set the speed of the animation
    displacementScale: 1, // set the scale of the displacement effect
    displacementBias: 0.5, // set the bias of the displacement effect
    map: myTexture, // set the texture to use for the distortion effect
    });

    // apply the material to the mesh
    mesh.material = material;
```

### Overall, the MeshDistortMaterial is a powerful tool for creating unique and dynamic 3D effects in Three.js, and it can be used to create a wide range of visual styles and animations.

#### [MeshDistortMaterial Drei.js](https://drei.pmnd.rs/?path=/story/shaders-meshdistortmaterial--mesh-distort-material-st)

______________________________________________________________________________________________________________

## Properties

* **dispose**

    is a method that is used to clean up the material when it is no longer needed. When you create a **MeshDistortMaterial**, it allocates GPU memory and other resources that need to be properly freed when the material is no longer in use. The **dispose** method is responsible for releasing these resources.

    To use the **dispose** method, you simply need to call it on the **MeshDistortMaterial** object that you want to dispose of. For example:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial(/* options */);

        // use the material

        material.dispose(); // dispose of the material when no longer needed
    ```

    The **dispose** method will free up any resources allocated by the **MeshDistortMaterial** and ensure that they are available for other parts of your application. It is good practice to always dispose of materials when they are no longer needed to avoid memory leaks and other performance issues.

    In addition to **MeshDistortMaterial**, most materials in Three.js have a **dispose** method, and it is generally a good practice to dispose of any materials or other resources that you no longer need in your application.

* **addEventListener**

    is a material class that is used to define the appearance of a 3D mesh in Three.js.

    However, the **addEventListener** method is commonly used in JavaScript to attach event listeners to DOM elements, such as HTML elements on a webpage. It is not directly related to the **MeshDistortMaterial** class or Three.js.

    In Three.js, you can attach event listeners to various objects, such as **Scene**, **Camera**, **Mesh**, etc. by using the **addEventListener** method provided by the **EventDispatcher** class. This allows you to handle various events, such as mouse clicks, keyboard inputs, or object interactions, and respond to them in your application.

    Here is an example of how you can use the **addEventListener** method in Three.js to handle a mouse click event on a mesh:

    ```js
        import { Mesh, EventDispatcher } from 'three';

        const mesh = new Mesh(/* geometry, material */);
        mesh.name = 'MyMesh';

        // create an event dispatcher and attach it to the mesh
        const dispatcher = new EventDispatcher();
        mesh.userData.dispatcher = dispatcher;

        // add a click event listener to the mesh
        mesh.addEventListener('click', (event) => {
        console.log(`Clicked on mesh "${event.target.name}"`);
        });

        // trigger the click event programmatically
        mesh.userData.dispatcher.dispatchEvent({ type: 'click', target: mesh });
    ```

    In this example, we create a **Mesh** object and attach an **EventDispatcher** object to it using the **userData** property. We then add a click event listener to the mesh and log a message when the event is triggered. Finally, we programmatically trigger the click event using the **dispatchEvent** method of the event dispatcher.

    Note that while the **addEventListener** method is not directly related to the **MeshDistortMaterial** class in Drei.js, it can be used to create interactive 3D applications using Three.js.

* **hasEventListener**

    is a material class that is used to define the appearance of a 3D mesh in Three.js.

    However, the **hasEventListener** method is commonly used in Three.js to check if a particular object has a certain type of event listener attached to it. It is used in conjunction with the **addEventListener** method, which is used to attach event listeners to objects.

    Here is an example of how you can use the **hasEventListener** method in Three.js to check if a mesh has a click event listener attached to it:

    ```js
        import { Mesh, EventDispatcher } from 'three';

        const mesh = new Mesh(/* geometry, material */);

        // create an event dispatcher and attach it to the mesh
        const dispatcher = new EventDispatcher();
        mesh.userData.dispatcher = dispatcher;

        // add a click event listener to the mesh
        mesh.addEventListener('click', (event) => {
        console.log(`Clicked on mesh`);
        });

        // check if the mesh has a click event listener
        const hasClickListener = mesh.userData.dispatcher.hasEventListener('click');
        console.log(`Mesh has click event listener: ${hasClickListener}`); // should print "true"
    ```

    In this example, we create a **Mesh** object and attach an **EventDispatcher** object to it using the **userData** property. We then add a click event listener to the mesh and log a message when the event is triggered. Finally, we use the **hasEventListener** method to check if the mesh has a click event listener attached to it.

    Note that while the **hasEventListener** method is not directly related to the **MeshDistortMaterial** class in Drei.js, it can be used to check if certain types of events are attached to any object in Three.js, including meshes that are using the **MeshDistortMaterial**.