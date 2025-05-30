<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [] }: { values: Value[] } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-white dark:bg-gray-950">
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader title="Our culture" subtitle="Small team. Big trust. Shared mission. These are the values we live every day." />

		<div
			class="grid gap-(--gap)"
			style:grid-template-columns="repeat(auto-fit, minmax(280px, 1fr))"
		>
			{#each [
				{ title: 'Customers first, always', description: 'We do the unscalable things—talking directly with users, texting when something breaks, shipping what actually helps them. Building alongside customers is our default.' },
				{ title: 'Hospitality is our moat', description: 'We believe the last true competitive advantage online is genuine, human hospitality. We bring care, effort, and craft to every interaction.' },
				{ title: 'Small teams, high trust', description: 'We stay lean, sweat the details, and take ownership over outcomes. Collaboration, humility, and deep trust are required here.' },
				{ title: 'Bias for momentum', description: 'We move fast, learn directly from the market, and never hide behind process. Progress over optics, always.' },
				{ title: 'No egos, just clear thinkers', description: 'We care more about humility, curiosity, and customer obsession than credentials or bravado. The best ideas win.' }
			] as value, i}
				<div
					bind:this={cards[i]}
					class="relative border-t border-gray-200 pt-4 dark:border-gray-900"
				>
					<!-- Content -->
					<div class="text-caption z-10">
						<div>
							<div class="text-headline mb-[1em]">{value.title}</div>
							<div class="text-body text-gray-500 dark:text-gray-400">{value.description}</div>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
