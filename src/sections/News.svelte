
<script>
    import Section from '../components/Section.svelte'
    import SectionHeader from '../components/SectionHeader.svelte'
    import NewsCard from '../components/NewsCard.svelte'
</script>

<Section bgColor='#F3F5F8'>

    <SectionHeader>
        <h2 class='title' slot='title'>Product news and updates</h2>
        <p class='text' slot='text'>Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum consequat.</p>
    </SectionHeader>

    <div class='feed'>

        <NewsCard
            title='How to build anything'
            text='Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex.'
            imgSrc='images/undraw_5.png'
            className='feed-item'
        />

        <NewsCard
            title='Facebook ads work'
            text='Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum consequat.'
            imgSrc='images/undraw_6.png'
            className='feed-item'
        />

        <NewsCard
            title='Logo tricks'
            text='Amet dolores laudantium tempore animi debitis sequi quos sit minima natus veritatis.'
            imgSrc='images/undraw_7.png'
            className='feed-item'
        />

    </div>

</Section>

<style>

    .title {
        color: var(--gray-dark);
    }

    .text {
        color: var(--gray-light);
    }

    .feed {
        display: flex;
        flex-flow: row wrap;
        justify-content: center;
        align-items: stretch;
    }

    .feed > :global(.feed-item) {
        max-width: 100%;
    }

    @media (min-width: 640px) {
        .feed > :global(.feed-item) {
            flex-basis: 30%;
            min-width: 300px;
        }
    }

</style>