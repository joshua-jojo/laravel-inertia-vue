<template lang="">
    <teleport to="body">
        <input type="checkbox" :id="id" class="modal-toggle" />
        <div class="modal">
            <div class="modal-box">
                <h3 class="font-bold text-lg capitalize">
                    <slot name="title"></slot>
                </h3>
                <div class="py-4">
                    <slot name="content"></slot>
                </div>
                <div class="modal-action">
                    <slot name="action"></slot>
                    <label :for="id" class="btn">close</label>
                </div>
            </div>
        </div>
    </teleport>
</template>
<script>
export default {
    props: {
        id: String,
    },
};
</script>
<style lang=""></style>
