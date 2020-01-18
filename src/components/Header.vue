<template>
    <div>
        <h3>Notes Added to Notebook</h3>
        <div class="progress">
            <div class="progress-bar" role="progressbar" aria-valuenow="60"
            aria-valuemin="0"
            aria-valuemax="100"
            :style="{width: (noteCount/maxNotes) * 100 +'%'}">
                {{noteCount}} / {{maxNotes}}
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props:['noteCount', 'maxNotes']
    }
</script>

<style scoped>

</style>