# Earth-Graphic


The code starts by creating a new scene. The background color is set to black and the fog color is set to a dark brown. Next, a camera object is created with the following parameters: perspectiveCamera, window width / height, near clipping plane distance, far clipping plane distance, field of view angle in degrees (55), aspect ratio (1/1000), and near and far clip planes distances. The code then creates an instance of THREE.Scene called scene which has been initialized with the background color being black and the fog being dark brown.

The code starts by declaring variables for the camera, planet, moon, sphereBg and terrainGeometry. The container is a reference to an element on the canvas that will be used later in this code. The next line of code declares a variable called frame which starts at 0 and counts up from there. This variable is used to keep track of how many frames have been rendered so far. Next it declares two variables: cameraDx and count which are both set to 0 initially but will be incremented every time a new frame is drawn with the help of three different functions: cameraDx = Math.random() * 2 - 1; // Randomly choose between x axis values (0-1) count = count + 1; // Increment counter value by one frame++; // Increase current frame number by one These lines are all part of what's known as "looping" because they repeat themselves over and over again until some condition changes or something else happens that interrupts them like when you press enter or click outside the window where this code runs in order to stop it from looping endlessly without any input from you. 

## three.js installation
[three.js](https://threejs.org/docs/index.html#manual/en/introduction/Installation)

### Getting started
```
// Option 1: Import the entire three.js core library.
import * as THREE from 'three';

const scene = new THREE.Scene();


// Option 2: Import just the parts you need.
import { Scene } from 'three';

const scene = new Scene();
```

### When creating 3D models
```
const loader = new GLTFLoader();

loader.load( 'path/to/model.glb', function ( gltf ) {

	scene.add( gltf.scene );

}, undefined, function ( error ) {

	console.error( error );

} );
```

#### When drawing line
```
const renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );
document.body.appendChild( renderer.domElement );

const camera = new THREE.PerspectiveCamera( 45, window.innerWidth / window.innerHeight, 1, 500 );
camera.position.set( 0, 0, 100 );
camera.lookAt( 0, 0, 0 );

const points = [];
points.push( new THREE.Vector3( - 10, 0, 0 ) );
points.push( new THREE.Vector3( 0, 10, 0 ) );
points.push( new THREE.Vector3( 10, 0, 0 ) );

const geometry = new THREE.BufferGeometry().setFromPoints( points );
```

### Libraries and Plugins can be found [here](https://threejs.org/docs/index.html#manual/en/introduction/Libraries-and-Plugins)
