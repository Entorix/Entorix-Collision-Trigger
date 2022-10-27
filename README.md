Below are step-by-step instructions on how to set up this basic Collision trigger:


1. Drag "Collision Trigger" Prefab into scene Hierarchy

2. Move the "Collision Trigger" Gameobject to wherever you need it

3. Click on particle system "Trigger Particle" and in the inspector, go to the Contact Receiver component and change the parameter to whatever you wish to use (you may also change the custom collision tags, just make sure that the one on the sender matches the one on the receiver)

4. Set up your animator to use this Float parameter as a transition condition (it will be 1 by default, and 0 when the collision is detected)

--------------

This system works by using particle death and the "stop action" function of unity's particle systems that allows the death of the last active particle to disable the gameobject that the particle system component is on. This disables the contact sender and receiver, changing the float value associated with that receiver to 0, which can then be used to trigger a state transition inside your animator.
