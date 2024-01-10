<script lang="ts">
import { defineComponent, createVNode } from 'vue'
export default defineComponent({
    render() {
        const vnode = createVNode('div', { class: 'test', style: { width: "20px", height: '1rem', backgroundColor: "red",position:'absolute',top:0} }, ['hello'])
        return vnode
    }
})
</script>
