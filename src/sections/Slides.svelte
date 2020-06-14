<script>
    import Section from '../components/Section.svelte'
    import SectionHeader from '../components/SectionHeader.svelte'
    import Slider from '../components/Slider.svelte'
</script>


<Section borderTop={true}>

    <SectionHeader>
        <h2 class='title' slot='title'>Built exclusively for you</h2>
        <p class='text' slot='text'>Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum — semper quis lectus nulla at volutpat diam ut venenatis.</p>
    </SectionHeader>

    <Slider/>

</Section>


<style>
    .title {
        color: var(--blue-dark);
    }

    .text {
        color: var(--gray-dark);
    }
</style>