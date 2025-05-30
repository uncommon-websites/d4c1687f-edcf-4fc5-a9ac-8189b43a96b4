<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing 
  title="Make every customer interaction feel personal. Automatically."
  subtitle="Choose the plan that matches your scale and how you serve customers."
  tierNames={["Starter", "Growth", "Enterprise"]}
  features={[
    { name: "Seats", tiers: { Starter: "Up to 3", Growth: "Unlimited", Enterprise: "Unlimited" } },
    { name: "Unified customer timeline", tiers: { Starter: true, Growth: true, Enterprise: true } },
    { name: "Inbox monitoring", tiers: { Starter: true, Growth: true, Enterprise: true } },
    { name: "Automated personalized messaging", tiers: { Starter: "Basic", Growth: "Advanced", Enterprise: "Advanced + Custom" } },
    { name: "Custom workflows", tiers: { Starter: false, Growth: true, Enterprise: "Custom" } },
    { name: "Integrations (CRM/support/ticketing)", tiers: { Starter: false, Growth: "Standard", Enterprise: "Premium & Tailored" } },
    { name: "Analytics & reporting", tiers: { Starter: "Basic", Growth: "Advanced", Enterprise: "Custom" } },
    { name: "Support response time", tiers: { Starter: "24 hours", Growth: "6 hours", Enterprise: "2 hours, priority" } },
    { name: "Onboarding & success", tiers: { Starter: "Self-serve", Growth: "Guided", Enterprise: "Custom Implementation" } },
    { name: "Security & SSO", tiers: { Starter: false, Growth: false, Enterprise: true } },
    { name: "Uptime SLA", tiers: { Starter: false, Growth: false, Enterprise: "99.9%" } }
  ]}
  tiers={[
    {
      name: "Starter",
      monthlyPrice: 49,
      yearlyPrice: 39,
      description: "For small teams automating basic customer workflows.",
      features: [
        "Up to 3 seats",
        "Live timeline sync",
        "Inbox monitoring",
        "Basic message automation"
      ],
      cta: {
        label: "Start for free",
        href: "/signup?plan=starter"
      }
    },
    {
      name: "Growth",
      monthlyPrice: 199,
      yearlyPrice: 159,
      description: "For fast-moving teams scaling customer interaction volume.",
      features: [
        "Unlimited seats",
        "Advanced automations",
        "Custom workflows",
        "CRM and ticketing integrations",
        "Performance analytics"
      ],
      cta: {
        label: "Try Growth Plan",
        href: "/signup?plan=growth"
      },
      highlight: true
    },
    {
      name: "Enterprise",
      monthlyPrice: null,
      yearlyPrice: null,
      description: "For large ops teams running advanced customer operations.",
      features: [
        "Unlimited scale",
        "Premium/Custom integrations",
        "Security review & SSO",
        "Custom implementation & onboarding",
        "Premium support",
        "99.9% uptime SLA"
      ],
      cta: {
        label: "Contact sales",
        href: "/contact"
      }
    }
  ]}
/>

<Testimonials
  testimonials={[
    {
      name: "Erica Li",
      position: "Head of Customer Experience",
      company: "Bramble",
      quote: "Lapel helped us cut response times by 60%. Our users are happier—and so is our team.",
      image: "/generated/image-a-professional-asian-woman-smiling-in-a-.webp"
    },
    {
      name: "Sean Fossett",
      position: "COO",
      company: "Beamloop",
      quote: "Finally, we have visibility into what's actually happening across customer channels in real time. The ROI was obvious within the first month.",
      image: "/generated/image-a-confident-black-man-wearing-a-blazer-i.webp"
    },
    {
      name: "Nadine Choi",
      position: "Director of Operations",
      company: "VenuePays",
      quote: "Our support used to feel reactive. With Lapel, we're one step ahead every time—and the team picked it up instantly.",
      image: "/generated/image-a-professional-middle-eastern-woman-in-b.webp"
    }
  ]}
/>

<CallToAction
  title="Turn customer service into your advantage"
  subtitle="Centralized, automated, and built for modern teams."
  description="Lapel helps fast-moving teams deliver fast, personal support—without adding headcount. Centralized profiles, smart automations, and instant workflows mean less busywork and more moments that matter. Claim your spot—build a smarter support team. Early access is limited. Join our first wave of partners improving support without growing costs."
  imageSrc="/generated/image-a-happy-customer-sitting-in-a-modern-off.webp"
  callsToAction={[
    {
      href: '/get-started',
      label: 'Claim your spot',
      variant: 'primary'
    },
    {
      href: '/contact',
      label: 'Talk to our team',
      variant: 'secondary'
    }
  ]}
/>
