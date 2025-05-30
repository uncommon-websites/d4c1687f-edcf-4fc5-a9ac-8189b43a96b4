<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
    centered={true}
    title="Customer ops made personal at scale"
    subtitle="Lapel unifies all your data and automates customer interactions, so every support experience feels tailored—no matter the volume."
    customers={[
        {
            name: "Maya Chen",
            position: "Head of support",
            imageSrc: "/generated/image-a-young-asian-woman-in-a-bright-office-w.webp"
        },
        {
            name: "Jake Morales",
            position: "Operations lead",
            imageSrc: "/generated/image-a-latino-man-in-a-modern-startup-workspa.webp"
        },
        {
            name: "Priya Nair",
            position: "Customer experience manager",
            imageSrc: "/generated/image-a-south-asian-woman-in-a-tech-office-env.webp"
        },
        {
            name: "Tom Becker",
            position: "Founder",
            imageSrc: "/generated/image-a-white-man-in-a-modern-internet-startup.webp"
        },
        {
            name: "Serena Wu",
            position: "Customer success lead",
            imageSrc: "/generated/image-an-east-asian-woman-customer-success-lea.webp"
        }
    ]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		'https://logo.clearbit.com/notion.so',
		'https://logo.clearbit.com/figma.com',
		'https://logo.clearbit.com/stripe.com',
		'https://logo.clearbit.com/zapier.com'
	]}
/>

<Summary
  title="What we do"
  text="Lapel unifies all your customer data and automates interactions, providing personal service at scale for modern internet businesses. Every customer feels known—no matter how fast you grow."
/>

<Testimonials
	testimonials={[
		{
			name: "Mateo Alvarez",
			position: "Ops Manager",
			company: "Shiplyne",
			quote: "We used to spend hours every day stitching together orders and responding to tickets. Lapel gives us that time back—and lets us scale without new hires.",
			image: "/generated/image-a-male-e-commerce-operations-manager-sta.webp"
		},
		{
			name: "Harper Lowe",
			position: "Customer Support Lead",
			company: "Beamlane",
			quote: "Lapel's proactive monitoring helps us spot and resolve issues before they hit our customers. It's taken so much risk—and stress—off the table.",
			image: "/generated/image-a-female-customer-support-lead-in-a-mode.webp"
		},
		{
			name: "Leon Mensah",
			position: "Founder",
			company: "LedgerLift",
			quote: "Our support costs shrank by nearly 40% in the first quarter alone. Lapel pays for itself, month after month.",
			image: "/generated/image-a-male-fintech-startup-founder-sitting-a.webp"
		}
	]}
/>

<Features
	title="Do more for every customer"
	subtitle="Three ways Lapel stands out for support teams"
	features={[
		{
			title: "Automation, the human way",
			description: "Automate answers, routes, and updates—without losing the personal touch that matters."
		},
		{
			title: "All your context at hand",
			description: "See every conversation, order, and data point in one place for faster, smarter support."
		},
		{
			title: "Ready for any scale",
			description: "Scale service instantly with templates, plug-and-play integrations, and zero need for engineering."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "Automate common support conversations",
			description: "Let Lapel instantly resolve routine requests—so your team can focus on what customers really need.",
			image: "/generated/image-a-customer-support-agent-with-a-warm-smi.webp",
			link: {
				href: "/use-cases/automated-support",
				label: "Learn more"
			}
		},
		{
			title: "Proactive, personal outreach",
			description: "Send targeted messages at just the right moment to turn questions into loyalty and reduce churn.",
			image: "/generated/image-a-collaborative-team-engaged-in-a-lively.webp",
			link: {
				href: "/use-cases/proactive-outreach",
				label: "Learn more"
			}
		},
		{
			title: "Insights at every agent's fingertips",
			description: "Unify conversations, orders, and context so agents give fast, informed answers—every time.",
			image: "/generated/image-a-business-team-in-a-modern-well-lit-off.webp",
			link: {
				href: "/use-cases/agent-insights",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="Free your team to deliver world-class service"
  subtitle="Lapel takes care of the busywork so your team can focus on what matters"
  description="Lapel unifies support data and automates interactions so your team spends less time stitching systems together and more time helping customers."
  imageSrc="/generated/image-a-cheerful-young-customer-support-lead-i.webp"
  callsToAction={[{ href: "/get-started", label: "Request early access", variant: "primary" }, { href: "/contact", label: "Chat with us", variant: "secondary" }]}
/>

