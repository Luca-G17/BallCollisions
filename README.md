# Ball Collisions
My simulation of collisions between circles combining static and dynamic collisions. The update loop first checks for balls that are colliding, it will then compute the offset for static collisions (1/2 * (distanceBetweenCentres - radius1 - radius2), using this value it will scale the normalised vector connecting their centres in order to offset both balls away from eachother. Next for each colliding ball it will also calculate the normal vector between the two balls along with the tangent vector. Next the program will project velocity of each ball onto the tangent vector, this provides a scalar for the tangent velocity of the balls after the collision. Using the formula for 1D velocity after [elastic collisions](https://en.wikipedia.org/wiki/Elastic_collision) the program calculates a scalar for the normal vector for both balls. The scaled normal and tangent vectors are then summed to calculate the velocity after a collision

![image](https://user-images.githubusercontent.com/63655147/155713889-3ef625ad-9dad-41e7-98fa-4fffc0fea5b4.png)
