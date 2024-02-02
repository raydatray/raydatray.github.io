<script>
    import "../app.css"
    import {IconExternalLink} from '@tabler/icons-svelte'

    export let projectName;
    export let shortHeader;
    export let description;
    export let date;
    export let link;
    export let imageURL;
</script>

<div class = 'grid grid-cols-1 mb-4 xl:grid-cols-4 xl:gap-4'>
    <div class = 'col-span-2'>
        <div class = "flex justify-between gap-2 place-items-center">
            <h3>{projectName}</h3>
            <p class = 'text-base text-sky-300'>{date}</p>
        </div>

        <h4>{shortHeader}</h4>

        <a href = {link}>
            <div class = 'ml-2 my-2 grid grid-flow-col auto-cols-max gap-2 justify-start place-items-start'>
                <IconExternalLink/>
                <p>View the project on Github</p>
            </div>
        </a>

        <p>{description}</p>
    </div>

    <div class = 'col-span-2 w-full scroll-pt-4 scorll-pb-4 flex items-center justify-center'>
        <img class = 'rounded-md p-0.5 shadow-md p-1' src = {imageURL} alt = 'project exmaple'/>
    </div>
</div>
