<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "Early builder impact",
    description: "Shape Lapel’s future and ship work that matters from day one.",
    icon: IconBriefcase
  },
  {
    title: "Real ownership",
    description: "High autonomy, high trust. Influence product, culture, and company trajectory.",
    icon: IconUsers
  },
  {
    title: "Grow fast",
    description: "Mentorship, personal development, and opportunities that scale with youyou won’t get lost in the shuffle.",
    icon: IconHeart
  }
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Isabella Torres",
    position: "Engineering Intern",
    company: "Engineering Team",
    quote:
      "As an intern, I felt immediately welcome and supported. My manager took a genuine interest in my growth and I always had someone ready to answer my questions. The culture here is warm, collaborative, and people are excited to help each other succeed.",
    image: "/generated/image-a-young-latina-woman-smiling-naturally-i.webp"
  },
  {
    name: "David Brown",
    position: "Product Manager",
    company: "Product Team",
    quote:
      "At Lapel, my ideas actually matter. Leadership listens, supports your development, and gives you real ownership of your work. I’ve grown more in the past year than I thought possible—all with a team that truly cares.",
    image: "/generated/image-a-black-man-in-his-30s-exuding-a-relaxed.webp"
  },
  {
    name: "Mei Lin",
    position: "VP of Marketing",
    company: "Marketing Team",
    quote:
      "Everyone here is deeply committed to raising the bar, but always with balance and kindness. We push each other, celebrate together, and innovate without ego. I’m proud to work in a place where collaboration isn’t just a buzzword—it’s how we win.",
    image: "/generated/image-an-asian-woman-vp-looking-stylish-and-co.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Say hello",
    description: "Send a short note and let us know what interests you about Lapel. No resume required, but share one if you’d like."
  },
  {
    step: 2,
    title: "Let’s talk",
    description: "We’ll have a casual call to learn more about each other, answer your questions, and talk through how you want to grow."
  },
  {
    step: 3,
    title: "Collaborate",
    description: "You’ll complete a brief, relevant working session—either with us live or as a short take-home challenge (paid if applicable)."
  },
  {
    step: 4,
    title: "Final decision, quickly",
    description: "We aim to go from first contact to a final answer in under two weeks. You’ll always know where you stand."
  }
];

	const values = [
  {
    icon: IconHeart,
    title: "Customers first, always",
    description: "We talk directly to users, respond quickly, and build what actually helps. Building alongside customers is our default."
  },
  {
    icon: IconUsers,
    title: "Hospitality is our moat",
    description: "We believe genuine, human hospitality online is the last real competitive advantage. We bring care and attention to every interaction."
  },
  {
    icon: IconGlobe,
    title: "Small team, high trust",
    description: "We stay lean, sweat the details, and take ownership over our work. Collaboration, humility, and deep trust aren’t just buzzwords—they’re required."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Build the future of service"
  subtitle="Small team. High trust. Early impact."
  imageSrc="/generated/image-a-modern-tech-startup-office-with-a-dive.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Work alongside founders, own big problems, and help shape the future of customer operations." />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<SectionHeader title="What our team is saying" subtitle="Hear from the people behind Lapel about why they love where they work." />
<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
