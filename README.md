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

# Consider the following code snippet below:

# class Mover : MonoBehaviour
# {
#  Vector3 target;
#  float speed;
#
# void Update()
#  {
#  
#  }
# }
