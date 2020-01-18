<template>
    <div class="container">
        <form class="adder">
            <div class="form-group">
                <label>New Note</label>
                <textarea class="form-control" rows="3" v-model="note"></textarea>
            </div>
            <div class="form-group">
                <button class="btn btn-primary" @click.prevent="addNewNote">Add Note</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                note: ''
            }
        },
        methods: {
            addNewNote() {
                console.log("Emitting");
                this.$emit('onNoteAdded', this.note);
                this.note = ''
            }
        }
    }
</script>

<style scoped>
.adder{
    max-width: 70%;
    margin: auto;
}
</style>