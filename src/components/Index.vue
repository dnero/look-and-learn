<template>
<q-layout>

<!-- Header -->
<div slot="header" class="toolbar">
<!-- opens left-side drawer using its ref -->
	<button class="hide-on-drawer-visible" @click="$refs.leftDrawer.open()">
		<i>menu</i><!-- makes a hamburger menu icon -->
	</button>

	<q-toolbar-title :padding="1">
		{{ appTitle }}
	</q-toolbar-title>
</div>

<!-- Navigation Tabs -->
<q-tabs slot="navigation">
    <q-tab icon="font_download" route="/letters" exact>Letters</q-tab>
    <q-tab icon="filter_1" route="/numbers" exact>Numbers</q-tab>
</q-tabs>


<!-- main view -->
<router-view class="layout-view"></router-view>

<!-- Left slide menu -->
<q-drawer ref="leftDrawer">
	<div class="toolbar">
    	<q-toolbar-title>
            Menu
		</q-toolbar-title>
	</div>
    <div class="list no-border platform-delimiter">
    	<q-drawer-link icon="font_download" to="letters">
        	Letters
    	</q-drawer-link>
        <q-drawer-link icon="filter_1" to="numbers">
        	Numbers
    	</q-drawer-link>
    </div>
</q-drawer>

</q-layout>
</template>

<script>

export default {
	data () {
		return {
			appTitle: 'Look & Learn'
		}
	},
	computed: {
		position () {
		//   let transform = `rotateX(${this.rotateX}deg) rotateY(${this.rotateY}deg)`
		//   return {
		//     top: this.moveY + 'px',
		//     left: this.moveX + 'px',
		//     '-webkit-transform': transform,
		//     '-ms-transform': transform,
		//     transform
		//   }
		}
	},
	methods: {
    	move (event) {
    	}
	},
	mounted () {
    // this.$nextTick(() => {
    //   document.addEventListener('mousemove', this.move)
    //   document.addEventListener('touchmove', this.move)
    // })
	},
	beforeDestroy () {
    // document.removeEventListener('mousemove', this.move)
    // document.removeEventListener('touchmove', this.move)
	}
}
</script>

<style>

</style>
