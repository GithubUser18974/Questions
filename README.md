  #              Interview_Questions
# What is number of Unverified Transactions?
The total number of IAP transactions, whether or not they have been verified.
IAP transactions include Unity IAP purchases and purchases reported using the Analytics.Transaction() function.
# why Vectors Should Be Normalized When Used To Move An Object?
Normalization makes the vector unit length. It means, for instance, that if you want to move with speed 20.0, multiplying speed * vector will result in a precise 20.0 units per step. If the vector had a random length, the step would be different than 20.0 units.
# Explain why Time.deltaTime should be used to make things that depend on time operate correctly?
Real time applications, such as games, have a variable FPS. They sometimes run at 60FPS, or when suffering slowdowns, they will run on 40FPS or less.

If you want to change a value from A to B in 1.0 seconds you can’t simply increase A by B-A between two frames because frames can run fast or slow, so one frame can have different durations.

The way to correct this is to measure the time taken from frame X to X+1 and increment A, leveraging this change with the frame duration deltaTime by doing A += (B-A) * DeltaTime.

When the accumulated DeltaTime reaches 1.0 second, A will have assumed B value
# Can two GameObjects, each with only an SphereCollider, both set as trigger and raise OnTrigger events? Explain your answer.
No. Collision events between two objects can only be raised when one of them has a RigidBody attached to it. This is a common error when implementing applications that use “physics.”
# What is sessions per User?
The average number of sessions per person playing on a given day.
Also known as Average Number of Sessions per DAU.
# Explain what a vertex shader is, and what a pixel shader is ?
Vertex shader is a script that runs for each vertex of the mesh, allowing the developer to apply transformation matrixes, and other operations, in order to control where this vertex is in the 3D space, and how it will be projected on the screen.

Pixel shader is a script that runs for each fragment (pixel candidate to be rendered) after three vertexes are processed in a mesh’s triangle. The developer can use information like the UV / TextureCoords and sample textures in order to control the final color that will be rendered on scree
# Can threads be used to modify a Texture on runtime?
No. Texture and Meshes are examples of elements stored in GPU memory and Unity doesn’t allow other threads, besides the main one, to make modifications on these kinds of data.
# Can threads be used to move a GameObject on the scene?
No. Fetching the Transform reference isn’t thread safe in Unity.
# What is Coroutine,is it running on new thread ?
Coroutine methods can be executed piece by piece over time, but all processes are still done by a single main Thread. If a Coroutine attempts to execute time-consuming operation, the whole application freezes for the time being.

Threads are different. The execution of separate Threads is managed by the operating system (this actually depends on the .NET implementation). If you have more than one logical CPU, many threads are executed on different CPUs. Thanks to that, any expensive operation will not freeze your game, but it might slow it down a little.
# What is the differnce between Stack and Heap 
https://www.c-sharpcorner.com/article/stack-vs-heap-memory-c-sharp/
# Does C# support multiple inheritance ?
C# does not support multiple class inheritance. To overcome this problem we use interfaces to achieve multiple class inheritance.

# Difference between static class and singleton pattern?
 singleton allows a class for which there is just one, persistent instance across the lifetime of an application. That means, it created a single instance and that instance (reference to that instance) can be passed as a parameter to other methods, and treated as a normal object. While a static class allows only static methods and and you cannot pass static class as parameter.
A Singleton can implement interfaces, inherit from other classes and allow inheritance. While a static class cannot inherit their instance members. So Singleton is more flexible than static classes and can maintain state.
Singleton Objects stored on heap while static class stored in stack.
Singleton Objects can have constructor while Static Class cannot.
Singleton Objects can dispose but not static class.
Singleton Objects can clone but not with static cla
# What is abstract class in C# unity?
Abstract classes are a combination of both a normal class and an interface. A normal method cannot handle an abstract method and Interfaces are incapable of using constructors, encapsulation, member variables, and method definitions. But the abstract class is capable of doing what both of these classes cannot do.
# What is Serialization and De-Serialization
Serialization is a mechanism of converting the state of an object into a byte stream. Deserialization is the reverse process where the byte stream is used to recreate the actual Java object in memory. ... So, the object serialized on one platform can be deserialized on a different platform
