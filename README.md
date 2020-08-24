# Intersection Simulator [Concurrency patterns]
 an intersection simulator application
Create multiple Car threads, each with a random ID (random integer), that wants to cross the intersection
- Crossing the intersection works as follows:
  - The car drives up to the intersection, which takes 3 seconds (Thread.sleep())
  - If there are no cars in the intersection AND the light is green, it enters it, and exits 1 seconds later
  - If there are cars in the intersection OR the light is red, it waits for exactly as long as it becomes empty
AND the light turns green
  - Drives for a further 3 seconds after exiting the intersection, and the thread exits
- Log everything, e.g.:
  - „Car 173974 is approaching the intersection”
  - „Car 372800 arrived at the intersection”
  - „Car 507218 exited the intersection”
- You should have an Intersection object through which cars make sure that no two cars are in the intersection at the
same time
- The Intersection should also have its own thread, switching between red and green every 2.5 seconds
- Do not use sleep or busy waiting when waiting for the Intersection to become empty
- Create a test program that sends cars to the intersection
