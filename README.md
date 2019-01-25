# GameJamUnityTips
## Tips for students coming to Global Game Jam 2019

-	Use unity teams/collaborate for Unity project version control and sharing (max 3 ppl)
o	If you have more than 3 ppl using Unity and have team members skilled with GIT, use it!
-	For assets, use G Drive / Dropbox etc.
o	Make sure to organize everything so that every team member knows where to find things
-	Check out lists of free assets
o	https://globalgamejam.org/jammer-resources
o	https://assetstore.unity.com/lists/global-game-jam-2019-free-assets-63987
o	https://github.com/kobitoko/Game-Jam-Tools-Resources
o	Opengameart.org
o	https://sonniss.com/gameaudiogdc18/
o	https://sonniss.com/gameaudiogdc2017/
-	Unity tips:
o	Decide first on if your game is 2D or 3D
	Unity is a 3D game engine, 2D means:
•	Setting camera projection mode to orthographic
•	Using Physics2D
o	Rigidbody2D
o	Collider2D
•	3D and 2D physics don’t mix! They have no interaction!
•	Set scene window to 2D (button in top of the window) if you’re using 2D
	If you go 3D
•	Choose between perspective and orthographic projection
o	On scene window, click the icon top-right corner XYZ indicator to switch between prespective and ortho in scene window
o	Figure out your player controller based on physics simulation needs
	What does the player collide with?
	Choose appropriate rigidbody type and input method
•	AddForce
•	Set rigidbody.velocity
•	Or use rigidbody.moveposition
	For 2d movement, Input.getaxis works great with built-in input dampening
o	Use existing playerController solutions for non-physics based movement
	Remember that only dynamic rigidbody movement is stopped by colliders!
	All rigidbodies w. colliders register OnCollision and OnTrigger events
o	For easy setup of follow camera(s), use Cinemachine!
o	Basic functions:
	Distance between 2 GameObjects:
•	(gameObject1.position – gameObject2.position).magnitude
	Physics(2D).Raycasts for checking line of sight between 2 points
•	Rigidbody.cast to check if the attached colliders hit anything while moving to a designated point
•	Boxcast/spherecast/circlecast
•	Don’t use too many (>100) per update or your fps may dip!
	
o	For importing 3D models, remember to check basic unit conversion
	Unity units are meters, while Blender units are cm’s!
o	For 3D games, remember to bake your lights!
	Lots of realtime lights? Switch to deferred rendering
	Switch off automatic bake when tweaking lights (or use progressive with low settings)
o	
