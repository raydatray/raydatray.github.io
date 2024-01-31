<script>
    import "../app.css"

    export let projectName;
    export let description;
    export let date;
    export let link;
    export let imageURL;
</script>


<div class = 'grid grid-cols-2 -5 xl:grid-cols-4'>
    <div class = 'col-span-2'>
        <div class = 'flex justify-start gap-3 items-center'>
            <h3>{projectName}</h3>
            <p class = 'justify-left text-sm'>{date}</p>
        </div>

        <h6 class = "mb-.5 mt-.5">{description}</h6>


    </div>



</div>
