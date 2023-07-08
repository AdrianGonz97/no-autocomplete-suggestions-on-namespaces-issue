<script lang="ts">
	import Card from "./Card.svelte";
	import C from "./children";
</script>

<!-- Notice how there are no autocomplete suggestions when starting from `<C.>` -->
<Card>
	<C.Title>Hello World</C.Title>
	<C.Description>
		Lorem Ipsum is simply dummy text of the printing and typesetting industry.
	</C.Description>
	<C.Button>Get started</C.Button>
</Card>

<!-- This uses <slot key={value}> to pass the namespace, -->
<!-- which still suffers from the same issue -->
<Card let:Ch>
	<Ch.Title>Hello World</Ch.Title>
	<Ch.Description>
		Lorem Ipsum is simply dummy text of the printing and typesetting industry.
	</Ch.Description>
	<Ch.Button>Get started</Ch.Button>
</Card>

<!-- NOTE: the closing `>` brace must be present as well to get any kind of autocomplete -->
