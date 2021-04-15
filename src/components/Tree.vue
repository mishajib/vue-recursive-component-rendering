<template>
    <div class="tree">
        <NodeTree :node="treeData"></NodeTree>
    </div>
</template>

<script>
import NodeTree from './NodeTree.vue';

export default {
    name: "Tree",
    props: {
        treeData: Object,
    },
    components: {
        NodeTree,
    },
}
</script>

<style>
.tree-list ul {
  padding-left: 16px;
  margin: 6px 0;
}
</style>