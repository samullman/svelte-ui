<script context="module" lang="ts">
	export const prerender = true;

	import Section from '../components/section.svelte';
	import Heading from '../components/heading.svelte';

	const colors = [
		'red',
		'green',
		'blue',
		'yellow',
		'purple',
		'pink',
		'orange',
		'teal',
		'lime'
	];

	function copyColor(e) {
		let color = getComputedStyle(document.documentElement).getPropertyValue(
			'--' + e.currentTarget.dataset.color
		);
		navigator.clipboard
			.writeText(color)
			.then((e) => {
				console.log(e);
			})
			.catch((err) => {
				console.log(err);
			});
	}
	// let mapComponent, someLat, someLng, someZoom;

	// import { Map, Geocoder, Marker, controls } from '@beyonk/svelte-mapbox'
	// import Earthquakes from './Earthquakes.svelte' // custom component

	// const { GeolocateControl, NavigationControl, ScaleControl } = controls

	// // Usage of methods like setCenter and flyto
	// mapComponent.setCenter([lng,lat],zoom) // zoom is optional
	// mapComponent.flyTo({center:[lng,lat]}) // documentation (https://docs.mapbox.com/mapbox-gl-js/example/flyto)

	// // Define this to handle `eventname` events - see [GeoLocate Events](https://docs.mapbox.com/mapbox-gl-js/api/markers/#geolocatecontrol-events)
	// function eventHandler (e) {
	//   const data = e.detail
	//   // do something with `data`, it's the result returned from the mapbox event
	// }
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<Section>
	<br />
	<Heading size="h1">Svelte UI</Heading>

	<p>Build transitional apps with ease.</p>

	<Heading size="h3">Colors</Heading>

	<div class="colors-grid">
		{#each colors as color}
			<div class="clickable" data-color={color} on:click={copyColor}>
				<div class={'color-box ' + color} />
				{color}
			</div>
		{/each}
	</div>

	<br />
</Section>

<!-- <Map
  accessToken="pk.eyJ1Ijoic2FtdWVsbG1hbiIsImEiOiJjaW1pbWxpZzgwMGRidmlrdXNuajExdmZvIn0.XuI3jM49UrUl8NBhrc2CmQ"
  bind:this={mapComponent} 
  on:recentre={e => console.log(e.detail.center.lat, e.detail.center.lng) } 
  options={{ scrollZoom: false }}
>
  <Earthquakes /> 
  <Marker lat={someLat} lng={someLng} color="rgb(255,255,255)" label="some marker label" popupClassName="class-name" /> 
  <NavigationControl />
  <GeolocateControl options={{ some: 'control-option' }} on:eventname={eventHandler} />
  <ScaleControl />
</Map> -->
<style lang="scss">
	:global(.mapboxgl-map) {
		height: 200px;
	}

	.color-box {
		height: 4em;
		width: 4em;
		margin-bottom: 0.1rem;
		border-radius: 0.2em;

		&.red {
			background-color: var(--red);
		}

		&.green {
			background-color: var(--green);
		}

		&.blue {
			background-color: var(--blue);
		}

		&.yellow {
			background-color: var(--yellow);
		}

		&.purple {
			background-color: var(--purple);
		}

		&.pink {
			background-color: var(--pink);
		}

		&.orange {
			background-color: var(--orange);
		}

		&.teal {
			background-color: var(--teal);
		}

		&.lime {
			background-color: var(--lime);
		}
	}

	.colors-grid {
		display: flex;
		gap: 1.5em;
		flex-wrap: wrap;
		// grid-template-columns: repeat(auto-fill, minmax(2em, 1fr));
		// grid-gap: 1em;
	}
</style>
