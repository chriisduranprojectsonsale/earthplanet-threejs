# Three.js Earth Planet

<div align="center">

[<img src="https://i.ibb.co/mS8RCYs/cover.png">](https://chriisduran.github.io/chriisdurantechnologies/)

</div>

- - -

###### If you would like to implement a planet earth 3d in your website this project is for you!

* Easy to define the "from" and "to" locations.
* Works with the latest versions of Node.js.
* Flexible design customization options.

<div align="center">

[<img src="https://i.ibb.co/MpJWwKG/nodejs-Vue-TR.png" width="455px">](https://vimeo.com/1016815356?share=copy#t=0)

</div>

- - -
#### Documentation

##### Run it!

```console
chriisduran@cmd:~$ /
npm install 
npm run build
npm run dev 
```
- Go to http://localhost:3000/

#### Interesting parameters
1. Threejs Config: [Basic.ts](/src/ts/world/Basic.ts)

	```typescript
	setControls() {
		this.controls = new OrbitControls(this.camera, this.renderer.domElement);
		this.controls.autoRotateSpeed = 3;
		this.controls.enableDamping = true;
		this.controls.dampingFactor = 0.05;
		this.controls.enableZoom = true;
		this.controls.minDistance = 100;
		this.controls.maxDistance = 300;
		this.controls.enablePan = false;
	}
	```

2. Defining locations: [Data.ts](/src/ts/world/Data.ts)

	```typescript

	export default [
	{
		startArray: {
			name: 'Nicaragua',
			N: 12.865416, // init coords 
			E: -85.207229,
		},
		endArray: [
			{
			name: 'España',
			N: 40.416775, // coords destinity 1 
			E: -3.703790,
			},
			{
			name: 'Reino Unido',
			N: 51.507351, // coords destiny 2 
			E: -0.127758,
			}
		],
	},
	];


	```

3. Easy earth customization design: [Earth.ts](/src/ts/world/Earth.ts)

	```typescript

	async init(): Promise<void> {
    	return new Promise(async (resolve) => {
			this.createEarth(); // comment any line to disable features
			this.createStars(); 
			this.createEarthGlow()
			this.createEarthAperture() 
			await this.createMarkupPoint()
			await this.createSpriteLabel()
			this.createAnimateCircle() 
			this.createFlyLine()
			this.show()
			resolve()
    })
  }
 

### Setting port

You can do it editing [webpack.config.js](/webpack.config.js) and more options to custom the project are available!

- - -
##### Software and technologies used

<p align="center">

[<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Three.js_Icon.svg/1200px-Three.js_Icon.svg.png" width="55px">](https://threejs.org/)
[<img src="https://seeklogo.com/images/N/nodejs-logo-FBE122E377-seeklogo.com.png" width="55px">](https://nodejs.org/)
[<img src="https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png" width="55px">](https://www.javascript.com/)
[<img src="https://cdn-icons-png.flaticon.com/512/919/919832.png" width="55px">](https://www.typescriptlang.org/)
[<img src="https://cdn-icons-png.flaticon.com/512/136/136443.png" width="55px">](https://www.json.org/)

</p>

- - -
##### Developer

<div align="left">

[<img src="https://i.ibb.co/vX2mShm/chrisduran.png" width="55px">](https://www.instagram.com/chriis.duran)

</div>


[![Patreon](https://img.shields.io/badge/Patreon-F96854?style=for-the-badge&logo=patreon&logoColor=white)](https://www.patreon.com/posts/3d-earth-planet-113497637?utm_medium=clipboard_copy&utm_source=copyLink&utm_campaign=postshare_creator&utm_content=join_link)
[![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/post/3D-Earth-Planet-With-ThreeJS-U7U114ECWJ)
[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/chriisduran/3d-earth-planet-threejs)
[![Gumroad](https://img.shields.io/badge/GUMROAD-36a9ae?style=for-the-badge&logo=gumroad&logoColor=white)](https://chriisduran.gumroad.com/l/3dplanetwiththreejs)
