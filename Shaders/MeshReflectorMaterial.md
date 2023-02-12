# MeshReflectorMaterial
#### The MeshReflectorMaterial is a component of the drei library that provides a material for creating reflections on 3D objects in a WebXR application.

#### A material in a 3D graphics application is used to define the appearance of an object, including its color, texture, and how it responds to light. The MeshReflectorMaterial is a specialized material that is designed to create reflections on the surface of an object, which can help to make the object appear more realistic and add depth to the scene.

#### The MeshReflectorMaterial component takes advantage of the capabilities of WebXR to create reflections by rendering a reflection map of the scene and applying it to the surface of the object. The reflection map is updated in real-time as the camera moves, allowing the reflections to respond to the changing environment in a natural way.

#### The MeshReflectorMaterial component can be used in combination with other components from the drei library, such as lights, cameras, and 3D objects, to create complex and interactive 3D scenes in a web application.

______________________________________________________________________________________________________________

## Properties
&nbsp;
* **dispose**

    is a method that is used to dispose of the resources associated with the material.

    In a 3D graphics application, materials can consume significant amounts of memory and computational resources, especially when they involve reflections and other complex effects. The "dispose" property provides a way to clean up these resources when they are no longer needed.

    When you call the "dispose" method on a MeshReflectorMaterial, it will release any memory and other resources that are associated with the material, freeing up resources for other parts of the application to use. This is particularly important when working with complex 3D scenes that may contain many materials, objects, and other resources.

    In general, you should call the "dispose" method on a MeshReflectorMaterial when you are finished using it, or when you want to replace it with another material. This will help to ensure that the resources associated with the material are cleaned up in a timely and efficient manner, and will prevent potential performance issues in your 3D application.
&nbsp;
* **addEventListener**

    is a method that is used in JavaScript to attach event listeners to an element.

    In JavaScript, events are notifications that are sent to your script when certain things happen in the web page, such as a user clicking a button, a page finishing loading, or an element being updated. Event listeners are functions that are called when an event occurs, allowing you to respond to the event and take some action.

    The "addEventListener" method is used to attach an event listener to an element. You can specify the type of event you want to listen for (such as "click", "load", or "mousemove"), and the function you want to be called when the event occurs. For example:

    ```js
        document.querySelector("button").addEventListener("click", function() {
            console.log("Button was clicked");
        });
    ```

    In this example, an event listener is attached to a button element, and it will log a message to the console whenever the button is clicked.

    The "addEventListener" method is a powerful tool for working with events in JavaScript, and is used in many different types of web applications, including games, interactive user interfaces, and more.


* **normalScale**

    is used to specify how to scale the normals of a reflected object in a WebXR application.

    The normal scale property controls the appearance of the reflections on the surface of an object that is using the MeshReflectorMaterial. The normals of the reflected object are used to calculate the angle at which light should be reflected, and the normal scale property allows you to adjust this calculation. By changing the normal scale property, you can control the intensity and quality of the reflections on the surface of the object.

    For example, a value of 1 will result in reflections that match the normals of the reflected object exactly, while a value of 0 will result in no reflections. The normal scale property can also be negative, which will result in inverted reflections.
