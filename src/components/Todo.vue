<template>
    <div class='ui centered card'   v-bind:key="todo">
        <div class="content">
            <div class="header">
                {{ todo.title}}
            </div>
            <div class="meta">
                {{ todo.project}}

            </div>
            <div class="extra content">
                <span class='right floated edit icon'>
                    <i class='edit icon'></i>
                </span>
            </div>
        </div>
        <div class="ui bottom attached green basic button">
            Completed
        </div>
        <div class="ui bottom attached red basic button" >
            Complete
        </div>
    </div>
</template>

<script>
export default {
    props: ['todo'],
}
</script>