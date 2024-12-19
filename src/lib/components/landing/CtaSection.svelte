<script lang="ts">
	import { ChevronRight } from 'lucide-svelte';
	import Button from '../ui/button/button.svelte';

	// Updated content for the redesigned CTA Section
	let features = [
		{
			title: 'Simplify Your Workflow',
			icon: '💡',
			description: 'Save time and focus on what matters most with our intuitive design tools.'
		},
		{
			title: 'Collaborate Seamlessly',
			icon: '🤝',
			description: 'Work with your team in real-time to bring your ideas to life.'
		},
		{
			title: 'Stay Secure',
			icon: '🔒',
			description: 'Your data is protected with top-tier security standards.'
		}
	];
</script>

<section id="cta" class="bg-gradient-to-b from-blue-50 via-white to-blue-100 dark:from-gray-800 dark:to-gray-900 py-14">
	<div class="container mx-auto px-6 lg:px-16">
		<div class="text-center">
			<h1 class="text-4xl font-extrabold text-gray-900 dark:text-white mb-4">
				Design Smarter, Not Harder
			</h1>
			<p class="text-lg text-gray-600 dark:text-gray-300 mb-8">
				Transform your ideas into reality with tools designed for modern creators.
			</p>
			<Button size="lg" href="#" class="rounded-full px-8 py-3">
				Start Free Trial
				<ChevronRight class="ml-2 inline-block size-5" />
			</Button>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-12">
			{#each features as { title, icon, description }}
				<div class="flex flex-col items-center text-center p-6 bg-white dark:bg-gray-800 shadow-lg rounded-lg">
					<div class="text-4xl mb-4">{icon}</div>
					<h2 class="text-xl font-semibold text-gray-800 dark:text-white mb-2">{title}</h2>
					<p class="text-gray-600 dark:text-gray-400">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	.container {
		max-width: 1200px;
	}
</style>
