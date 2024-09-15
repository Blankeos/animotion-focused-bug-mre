<script lang="ts">
	import { Presentation, Slide, Code, Transition, Action } from '@animotion/core'
	import { tween } from '@animotion/motion'

	let text: HTMLParagraphElement
	let code: Code
	let circle = tween({ x: 0, y: 80, r: 80, fill: '#00ffff' })
	let items = $state([1, 2, 3, 4])
	let layout = $state('flex gap-4')
</script>

<Presentation options={{ history: true, transition: 'slide', controls: false, progress: true }}>
	<Slide class="h-full place-content-center place-items-center">
		<Action
			do={() => {
				console.log('do 1')
			}}
			focused={() => {
				console.log('focused 1')
			}}
		/>
		<Action
			do={() => {
				console.log('do 2')
			}}
			focused={() => {
				console.log('focused 2')
			}}
		/>
	</Slide>
</Presentation>
