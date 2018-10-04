<template>
    <div class="accordion" :class="accordionClasses">
        <div class="accordion-header" @click="toggleAccordion">
            {{ headerMsg }}
            <i class="material-icons right-pos-arrow">play_arrow</i>
        </div>
        <div class="accordion-body">
            <div class="accordion-content">
                {{ contentMsg }}
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Accordion',
    props: {
        headerMsg: String,
        contentMsg: String,
        isOpen: true
    },
    methods: {
        toggleAccordion: function() {
            this.isOpen = !this.isOpen;
        }
    },
    computed: {
        accordionClasses: function() {
            return {
                'is-closed': !this.isOpen,
                'is-primary': this.isOpen,
                'is-dark': !this.isOpen
            };
        }
    }
}
</script>
<style>
.accordion {
    background-color: white;
    width: 100%;
    margin-left: auto;
    margin-right: auto;
    outline: none;
}

.accordion-header {
    margin-top: 10px;
    color: #04464F;
    background-color: white;
    padding: 5px;
    border: 3px solid #04464F;
    cursor: pointer;
}

.accordion-body {
    background-color: white;
    color: #04464F;
    padding: 0;
    max-height: 10em;
    border: 3px solid #04464F;
    overflow: hidden;
    transition: 0.4s ease all;
}

.is-closed .accordion-body {
    max-height: 0;
}

.accordion-content {
    padding: 20px;
}

.right-pos-arrow {
    margin-left: 800px;
}
</style>