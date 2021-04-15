<template>
  <div id="app">
    <HelloWorld :msg="message"/>
    <Tree :tree-data="tree"></Tree>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Tree from './components/Tree.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Tree,
  },
  data() {
    return {
      message: "Recursive Component Rendering",
      tree: {
        id: 1,
        title: "A Root Folder",
        description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error exercitationem facilis reprehenderit nam explicabo ipsa quas corporis consectetur officiis asperiores.",
        type: 'folder',
        children: [
          {
            id: 2,
            title: "A Sub folder 1",
            description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error exercitationem facilis reprehenderit nam explicabo ipsa quas corporis consectetur officiis asperiores.",
            type: 'folder',
            children: [
              { 
                id: 3,
                title: 'A sub-sub-folder 1',
                description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error exercitationem facilis reprehenderit nam explicabo ipsa quas corporis consectetur officiis asperiores.",
                type: 'file',
              },
              { 
                id: 4,
                title: 'A sub-sub-folder 2',
                description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error exercitationem facilis reprehenderit nam explicabo ipsa quas corporis consectetur officiis asperiores.",
                type: 'file',
              },
            ],
          },
          { 
            id: 5,
            title: 'A sub folder 2',
            description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error exercitationem facilis reprehenderit nam explicabo ipsa quas corporis consectetur officiis asperiores.",
            type: 'file',
          },
        ],
      },
    };
  },
}
</script>