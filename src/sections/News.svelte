
<script>
    import Section from '../components/Section.svelte'
    import SectionHeader from '../components/SectionHeader.svelte'
</script>

<Section bgColor='#F3F5F8'>
    <SectionHeader>
        <h2 class='title' slot='title'>Product news and updates</h2>
        <p class='text' slot='text'>Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum consequat.</p>
    </SectionHeader>
</Section>

<style>

    .title {
        color: var(--gray-dark);
    }

    .text {
        color: var(--gray-light);
    }
</style>