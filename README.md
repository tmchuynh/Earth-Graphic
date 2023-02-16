# Earth-Graphic

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
