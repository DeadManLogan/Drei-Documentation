# MeshReflectorMaterial
#### The MeshReflectorMaterial is a component of the drei library that provides a material for creating reflections on 3D objects in a WebXR application.

#### A material in a 3D graphics application is used to define the appearance of an object, including its color, texture, and how it responds to light. The MeshReflectorMaterial is a specialized material that is designed to create reflections on the surface of an object, which can help to make the object appear more realistic and add depth to the scene.

#### The MeshReflectorMaterial component takes advantage of the capabilities of WebXR to create reflections by rendering a reflection map of the scene and applying it to the surface of the object. The reflection map is updated in real-time as the camera moves, allowing the reflections to respond to the changing environment in a natural way.

#### The MeshReflectorMaterial component can be used in combination with other components from the drei library, such as lights, cameras, and 3D objects, to create complex and interactive 3D scenes in a web application.

______________________________________________________________________________________________________________

## Properties
* **normalScale**
    is used to specify how to scale the normals of a reflected object in a WebXR application.

    The normal scale property controls the appearance of the reflections on the surface of an object that is using the MeshReflectorMaterial. The normals of the reflected object are used to calculate the angle at which light should be reflected, and the normal scale property allows you to adjust this calculation. By changing the normal scale property, you can control the intensity and quality of the reflections on the surface of the object.

    For example, a value of 1 will result in reflections that match the normals of the reflected object exactly, while a value of 0 will result in no reflections. The normal scale property can also be negative, which will result in inverted reflections.
