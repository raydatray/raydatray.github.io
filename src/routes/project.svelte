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


<div>
    <div class = 'col-span-2'>
        <div class = 'flex justify-start gap-3 items-center'>
            <h3>{projectName}</h3>
            <p class = 'flex flex-col justify-end'>{date}</p>
        </div>
    
        <h4>{shortHeader}</h4>

        <a href = {link}>
            <div class = 'grid grid-flow-col auto-cols-max gap-3 justify-start items-end'>
                <IconExternalLink/>
                <p>See the project on Github</p>
            </div>
        </a>

        <p>{description}</p>

        <img class = 'rounded' src = {imageURL} alt = 'Project'>



    </div>
</div>

