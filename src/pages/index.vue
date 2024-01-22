<template>
  <div>
    <TheHeader />
    <main>
      <HeroSection />
      <FeatureSection />
      <DesignSection />
      <ShowNow />
      <section class="bg-secondary-100 py-12 text-gray-800" data-pg-collapsed>
        <div class="container mx-auto px-4 relative">
          <BenefitSection />
          <SubscribeToDeals client:visible />
          <BookAnAppointment client:visible />
        </div>
      </section>
    </main>
    <FooterSection />
  </div>
</template>
