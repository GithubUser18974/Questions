# Interview_Questions
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

