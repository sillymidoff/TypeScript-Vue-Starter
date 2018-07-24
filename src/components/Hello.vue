<template>
    <div>
        <div class="whats-new-container">
            <div class="value">Application Name: Pivot</div>
            <div class="value">Application Name: ORCA</div>
            <div class="value">Application Name: COMET</div>
        </div>
    </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
    props: ['name', 'initialEnthusiasm'],
    data() {
        return {
            enthusiasm: this.initialEnthusiasm,
        }
    },
    methods: {
        increment() { this.enthusiasm++; },
        decrement() {
            if (this.enthusiasm > 1) {
                this.enthusiasm--;
            }
        },
    },
    computed: {
        exclamationMarks(): string {
            return Array(this.enthusiasm + 1).join('!');
        }
    }
});
</script>

<style>
.whats-new-container {
  display: flex;
  justify-content: space-between;
}

.value {
  background: #D3D3D3;
  border: 2px solid black;
  padding: 50px;
}

</style>
