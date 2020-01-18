<template>
    <div class="row">
        <app-note v-for="(note, i) in notes"
            @click.native="deleteNote(i)">
            {{note}}
        </app-note>
    </div>
</template>

<script>
    import Note from "@/components/Note";

    export default {
        props: ['notes'],
        components: {
            appNote: Note
        },
        methods: {
            deleteNote(index) {
                this.$emit('onNoteDeleteRequested', index);
            }
        }
    }
</script>

<style scoped>

</style>