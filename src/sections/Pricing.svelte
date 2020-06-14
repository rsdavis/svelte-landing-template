
<script>
    import Section from '../components/Section.svelte'
    import SectionHeader from '../components/SectionHeader.svelte'
</script>

<Section bgColor='#101D2D'>
    <SectionHeader>
        <h2 class='title' slot='title'>Simple, transparent pricing</h2>
        <p class='text' slot='text'>Vitae aliquet nec ullamcorper sit amet risus nullam eget felis semper quis lectus nulla at volutpat diam ut venenatis tellus in ornare.</p>
    </SectionHeader>
</Section>

<style>

    .title {
        color: white;
    }

    .text {
        color: var(--gray-light);
    }
</style>