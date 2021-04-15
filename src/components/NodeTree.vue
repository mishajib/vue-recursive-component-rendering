<template>
    <div class="accordion" :id="'accordion' + node.id">
        <div class="card">
            <div class="card-header" :id="'heading' + node.id">
                <h2 class="mb-0">
                    <button class="btn btn-link btn-block text-left" type="button" data-toggle="collapse" :data-target="'#collapse' + node.id" aria-expanded="true" :aria-controls="'collapse' + node.id">
                        {{ node.title }}
                    </button>
                </h2>
            </div>

            <div :id="'collapse' + node.id" class="collapse show" :aria-labelledby="'heading' + node.id" :data-parent="'#accordion' + node.id">
                <div class="card-body">
                    <p class="description" v-if="node.type === 'file'">
                        {{ node.description }}
                    </p>
                    <NodeTree v-for="(child, index) in node.children" :node="child" :key="index" v-else></NodeTree>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NodeTree',
    props: {
        node: Object,
    },
}
</script>