<script context="module" lang="ts">
	export const prerender = true;

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

	<div style="text-align:center;">
	<h1>
		Svelte UI
	</h1>

	<div>
		Very chill, svelte-based, cross-browser UI library with utilities.
	</div>

	<div>
	  400 bytes. 0.5b zipped. 
	</div>

</div>



<div>

	<h3>
		Sidebar
	</h3>
	<ul>
		<li>
			<a sveltekit:prefetch href="/components">
				All components
				</a>
		</li>

		<li>
			<a sveltekit:prefetch href="/components/breadcrumb">
				Breadcrumb
				</a>
		</li>


		<li>
			<a sveltekit:prefetch href="/components/button">
				Button
				</a>
		</li>

	


		<li>
			<a sveltekit:prefetch href="/components/accordion">
			Accordion
			</a>
		</li>
		
		<li>
			<a sveltekit:prefetch href="/components/tabs">
				Tabs
				</a>
		</li>

		<li>Container</li>

		<li>Tooltip

			<ul>
				<li>Light</li>
				<li>Dark</li>
			</ul>
		</li>
		<li>
				<a sveltekit:prefetch href="/components/input">
					Input
					</a>

			<ul>
				<li>Text</li>
				<li>Checkbox</li>
				<li>Radio</li>
				<li>Select</li>
				<li>Colorwheel</li>
			</ul>
		</li>
	</ul>
</div>

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


<style>
    :global(.mapboxgl-map) {
        height: 200px;
        
    }
</style>