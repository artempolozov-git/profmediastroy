<template>
  <div class="home">
    <home-news></home-news>
    <home-first-screen></home-first-screen>
    <home-services></home-services>
    <home-portfolio></home-portfolio>
    <home-about-company></home-about-company>
    <home-advantages></home-advantages>
    <home-offers></home-offers>
    <home-contacts></home-contacts>
  </div>
</template>

<script>
    import HomeNews from "@/components/HomeNews";
    import HomeFirstScreen from "@/components/HomeFirstScreen";
    import HomeServices from "@/components/HomeServices";
    import HomePortfolio from "@/components/HomePortfolio";
    import HomeAboutCompany from "@/components/HomeAboutCompany";
    import HomeAdvantages from "@/components/HomeAdvantages";
    import HomeOffers from "@/components/HomeOffers";
    import HomeContacts from "@/components/HomeContacts";
    export default {
        name: "Home",
        components: {
            HomeContacts,
            HomeOffers,
            HomeAdvantages, HomeAboutCompany,  HomeServices, HomePortfolio, HomeFirstScreen, HomeNews}
    }
</script>

<style scoped>

</style>