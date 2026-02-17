<h1>Physics-Based Character Controller Test Project</h1>

<h3>Summary</h3>
<p>&emsp;A small project I used as a sandbox to create a character controller based on ideas from a <a href=https://www.youtube.com/watch?v=qdskE8PJy6Q>video by Toyful Games</a>. I used this project to learn more about character controllers, the Unity 3D physics engine, C# events, polymorphism, component-based programming, and creating gameplay elements within a 3D environment. It was also going to eventually become the base for a game concept I was working on but the project fell to the side.</p>

<h3>Download Information</h3>
<p>&emsp;The download for this project is only available through this repository and only a Windows version of it is available for now. Clone the repo and unzip the "build.zip" folder. The project can be launched from the "3DCharacterTestBed.exe" file within the unzipped folder.</p>

<h3>Project Controls</h3>
<p>Please keep in mind that this is a test environment and not a game. All stations can be interacted with the interaction key and are functional. But I seem to have forgotten to add the interacton prompt too a few of them. And they can get thrown around too so they are prone to spawning things under the floor if they fall over the wrong way.</p>
<table align="center">
	<tr>
		<td>Movement</td>
        <td>WASD</td>
    </tr>
    <tr>
		<td>Jump</td>
        <td>Spacebar</td>
    </tr>
    <tr>
		<td>Interact/Pick up</td>
        <td>E</td>
    </tr>
    <tr>
		<td>Drop Held Object</td>
        <td>X</td>
    </tr>
    <tr>
    	<td>Summon a box from the box dimension<br/>traveling directly at your head</td>
        <td>B</td>
    </tr>
    <tr>
		<td>Explosion</td>
        <td>Keypad 1</td>
    </tr>
</table>

<h3>Development Notes</h3>
<p>&emsp;A few months after being laid off, a friend and I participated in a game jam that didn't very get far. We stepped into the unfamiliar territory of 3D physics and were unaware of just how unfamiliar we were. However, I thought the concept we had come up with was interesting and decided to keep pressing forward even after the jam had ended. The first thing that I knew I needed to do was learn how to work within a 3D environment. We had originally tried the game jam in Godot but I decided to use Unity since I was more familiar with it. I figured once I learned it there, I could translate the knowledge to Godot for future projects.</p>
<p>&emsp;The video that I linked above in the Summary section was one I had seen before. It seemed like a good place to start since it doesn't give all solutions to the idea of a physics based character controller I could use it as a springboard to experiment. Experiment I did until I got the wobbly, red, capsule character present in this build. I wanted to maintain the wobbliness and thought I might be able to use it in a future feature of the game.</p>
<p>&emsp;The different "Stations" around the test area were to test character interaction with environmental objects. The player can interact with them to obtain, convert, store, and delete objects that I referred to as "task objects". They are split into four categories according to which components they implement; producers, converters, consumers, and storage. Each component is represented by a base class and they each do what their names imply. Producers produce objects, converters take one object and then give a different one back, consumers take one object and remove it from the game, and storage takes one object at a time and holds them in a queue to obe retrieved again later. These components also allow for composite stations to be made, such as the Producer/Converter station which produces the rod-shaped task object and can convert them into the torus.</p>
