<template>
    <div class="container">
        <br>
        <app-header :note-count="notes.length" :max-notes="maxNotes"/>
        <br>
        <br>
        <app-new-note @onNoteAdded="addNewNote"/>
        <br>
        <app-note-grid :notes="notes"
            @onNoteDeleteRequested="deleteNote"/>
        <br>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class = 'alert alert-info'>
                    Info: Click on a note to remove it!
                </div>
            </div>
        </div>
    </div>
</template>

<script>

    import NoteGrid from "@/components/NoteGrid";
    import NewNote from "@/components/NewNote";
    import Header from "@/components/Header";
    export default {
        data() {
            return {
                maxNotes: 10,
                notes: [
                    'This is a temporary note'
                ]
            }
        },
        methods: {
            addNewNote(note) {
                if(this.notes.length === this.maxNotes) {
                    return alert('Notebook full!! Delete notes to add more')
                }
                this.notes.push(note);
            },
            deleteNote(index) {
                console.log("Delete requested");
                this.notes.splice(index, 1);
            }
        },
        components: {
            appHeader: Header,
            appNoteGrid: NoteGrid,
            appNewNote: NewNote
        }
    }
</script>

<style>

</style>
