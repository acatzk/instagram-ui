<template>
	<div :class="story ? 'p-0.5 rounded-full bg-gradient-to-tr from-yellow-400 to-fuchsia-600' : undefined">
		<a class="block bg-white p-0.5 rounded-full" href="#">
			<img :class="`${className}`" :src="`${src}`" alt="avatar" />
		</a>
	</div>
</template>

<script>
	export default {
		props: {
			src: {
				type: String,
				required: false,
				default: 'https://instagram.fdvo1-1.fna.fbcdn.net/v/t51.2885-19/s150x150/41671377_475898572909086_6073809876599963648_n.jpg?_nc_ht=instagram.fdvo1-1.fna.fbcdn.net&_nc_ohc=5w6Oz_NosAMAX9R3tdQ&tp=1&oh=edc3b0706a0561c85f415c07e51bf5c0&oe=6033D860'
			},
			className: {
				type: String,
				required: true,
				default: 'w-14 h-14'
			},
			story: {
				type: Boolean,
				default: false
			}
		}
	}
</script>