<script>
    import { faFlag, faBullhorn, faAd, faLightbulb, faAtom, faPoll } from '@fortawesome/free-solid-svg-icons'
    import Section from '../components/Section.svelte'
    import FeatureCard from '../components/FeatureCard.svelte'

    // let faFlag = null

    let features = [
        {
            icon: faFlag,
            title: 'Robust workflow',
            text: 'Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat.'
        },
        {
            icon: faBullhorn,
            title: 'Top performance',
            text: 'Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.'
        },
        {
            icon: faAd,
            title: 'Killer SEO',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic velit eveniet quia enim. Eveniet odio dolor perferendis aut possimus explicabo fugit at obcaecati deleniti!'
        },
        {
            icon: faLightbulb,
            title: 'Awesome customers',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic velit eveniet quia enim. Amet dolores laudantium tempore animi debitis sequi quos sit minima natus veritatis.'
        },
        {
            icon: faAtom,
            title: 'Rockstar status',
            text: 'Molestiae amet deleniti rerum quod, quis blanditiis atque corrupti tenetur beatae, pariatur cupiditate odio. Amet dolores laudantium tempore animi debitis sequi quos sit minima natus veritatis.'
        },
        {
            icon: faPoll,
            title: 'Data driven',
            text: 'Amet dolores laudantium tempore animi debitis sequi quos sit minima natus veritatis.'
        }
    ]
</script>

<Section>

    <div class='grid'>
        { #each features as feature }
            <FeatureCard
                icon={feature.icon}
                title={feature.title}
                text={feature.text}
            />
        { /each }
    </div>

</Section>


<style>

    .grid {
        display: grid;
        grid-gap: 50px;
    }


    @media (min-width: 640px) {
        .grid {
            margin: 0;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            grid-gap: 50px;
            justify-items: center;
        }
    }
</style>
