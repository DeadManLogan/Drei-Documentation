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

    is a method that is used to clean up the material when it is no longer needed. When you create a MeshDistortMaterial, it allocates GPU memory and other resources that need to be properly freed when the material is no longer in use. The dispose method is responsible for releasing these resources.

    To use the dispose method, you simply need to call it on the MeshDistortMaterial object that you want to dispose of. For example:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial(/* options */);

        // use the material

        material.dispose(); // dispose of the material when no longer needed
    ```

    The dispose method will free up any resources allocated by the MeshDistortMaterial and ensure that they are available for other parts of your application. It is good practice to always dispose of materials when they are no longer needed to avoid memory leaks and other performance issues.

    In addition to MeshDistortMaterial, most materials in Three.js have a dispose method, and it is generally a good practice to dispose of any materials or other resources that you no longer need in your application.