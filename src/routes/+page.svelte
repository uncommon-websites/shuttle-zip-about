<script>
  import Navbar from '$lib/components/Navbar.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import FeatureSection from '$lib/components/FeatureSection.svelte';
  import IntuitiveWindowContent from '$lib/components/IntuitiveWindowContent.svelte';
  import SmartWindowContent from '$lib/components/SmartWindowContent.svelte';
  import SafeWindowContent from '$lib/components/SafeWindowContent.svelte';
  import StorageLogos from '$lib/components/StorageLogos.svelte';
  import Footer from '$lib/components/Footer.svelte';
  import Cursor from '$lib/components/Cursor.svelte';
</script>

<Navbar />

<main class="overflow-hidden">
  <Hero />

  <FeatureSection 
    title="Intuitive" 
    description="No more lost files. With Shuttle, your files are exactly where you need them, all the time."
    cursorName="Jean"
    cursorColor="orange"
    cursorPosition="top-20 right-[15%] md:right-[20%]"
  >
    <IntuitiveWindowContent />
  </FeatureSection>

  <FeatureSection 
    title="Smart" 
    description="No more tool-hopping. Shuttle brings sharing and AI powered workflows into one smart workspace — so your files move faster, and you do too."
    cursorName="Giel"
    cursorColor="blue"
    cursorPosition="bottom-20 right-[10%] md:right-[15%]"
  >
    <div slot="extra-cursors">
      <Cursor name="Niels" color="red" className="top-20 left-[10%] md:left-[15%]" />
    </div>
    <SmartWindowContent />
  </FeatureSection>

  <FeatureSection 
    title="Safe" 
    description="Your files, your rules. Shuttle protects your IP by running AI inference in-house and giving you the option to host your files on your own server - so you stay in control, always."
  >
    <div slot="after-cta" class="mb-8">
      <StorageLogos />
    </div>
    <SafeWindowContent />
  </FeatureSection>

  <Footer />
</main>

