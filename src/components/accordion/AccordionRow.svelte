<script>
import {
  slide
} from "svelte/transition";
import MdChevronRight from 'svelte-icons/md/MdChevronRight.svelte';
let isOpen = false
const toggle = () => isOpen = !isOpen
export let title;
export let description;
</script>

<div class="item">
    <div on:click={toggle}  aria-expanded={isOpen} class="item-title" >
        { title }

        <div class="icon">
            <MdChevronRight />
        </div>
    </div>

    {#if isOpen}
    <div class="item-description"  aria-expanded={isOpen} transition:slide={{ duration: 300 }}>
        { description }
    </div>
    {/if}

</div>

<style>


.icon {
  transition: transform 0.2s ease-in;
}

[aria-expanded=true] .icon {
  transform: rotate(0.25turn);
}

[aria-expanded=true].item-description {
  border-top: 1px solid #2d2d2d;
	border-bottom: none;
}


.item-title {
  border: 1px solid #2d2d2d;
  border-bottom: none;
  padding: 4px;
	cursor: pointer;
}


.item-description {
  border-left: 1px solid #2d2d2d;
  border-right: 1px solid #2d2d2d;
	font-size: 14px;

}

.item-description:last-child {
  /* border-bottom: 1px solid #2d2d2d; */
}

.icon {
  display: inline-block;
  float: right;
  width: 18px;
  height: 18px;
}

.item .item-description {
  /* opacity: 0;
  height: 0;
  padding: 0px 4px;
  transition: height opacity 0.3s ease-in-out; */

	opacity: 1;
  padding: 4px 4px;
  height: auto;
	
}



</style>
