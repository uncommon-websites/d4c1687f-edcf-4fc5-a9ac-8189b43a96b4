<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
    title="Hospitality, automated for scale"
    subtitle="Lapel is a customer operations platform that unifies data and automates support to deliver personal, human service—without the manual work"
    imageSrc="/mockups/airport-screen-1748608004061.png"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Lapel started with a frustration shared by many operators: customer conversations scattered across tools, missing context, and teams stuck copying info from one system to another. It felt inefficient, robotic—and worst of all, impersonal. We believed something better was possible. At companies we admired, great service didn’t just solve problems; it built loyalty. Hospitality, we realized, is still the greatest moat on the internet—and most teams are stuck without the tools to deliver it.",
		"So we’re building Lapel: a customer operations platform that unifies your systems and automates routine tasks, so humans can stay focused on what matters—real conversations, handled with clarity and care. One shared view brings together billing, product usage, support data, and more. Automations take care of the busywork, letting your team run lean without losing the personal touch.",
		"We’re a small team in San Francisco, working closely with early customers to get it right. While our current product is in early access, it’s already helping teams respond faster, stay in sync, and scale their customer support without compromising on quality. If you're building a company and want to serve customers like they matter at every step—let’s talk."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our team."
  subtitle="A small, focused group based in San Francisco."
  stakeholders={[
    {
      name: "Founder",
      position: "Founder",
      bio: "Building Lapel to put hospitality first on the internet. Based in San Francisco, working with early customers.",
      image: "/generated/image-a-professional-headshot-of-a-founder-cap.webp"
    }
  ]}
/>

<!-- No investors to display -->

<!-- CTA Section -->
<CallToAction
  title="Help set a new standard for service online"
  subtitle="Join our small high-trust team in San Francisco"
  description="We're obsessed with making hospitality a competitive advantage for the modern internet. If you want to build with customers, sweat the details, and work alongside humble high-ownership teammates, let’s talk. Reach out to join, request early access, or partner with us."
  imageSrc="/generated/image-a-friendly-and-diverse-san-francisco-sta.webp"
  callsToAction={[
    { href: "/early-access", label: "Request early access", variant: "primary" },
    { href: "mailto:hello@lapel.com", label: "Join the team", variant: "secondary" }
  ]}
/>
