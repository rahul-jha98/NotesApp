<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="card panel panel-default">
            <div class="panel-body note">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Note"
    }
</script>

<style scoped>
    .panel {
        margin: 5px
    }
    .panel-body {
        padding: 20px;
        font-size: 20px;
        color: #6e6e6e;
    }
    .note {
        cursor: pointer;
    }
    .note:hover {
        background-color: #ffe2e2;
    }
</style>