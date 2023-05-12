<template>
    <div>
        <component v-for="widget in pageContext.pageData.Widgets" :is="widgets[widget.Type]" :widget="widget">
        </component>
    </div>
</template>

<script setup lang="ts">
import TestWidget1 from '../components/TestWidget1.vue';
import TestWidget2 from '../components/TestWidget2.vue';
import TestWidget3 from '../components/TestWidget3.vue';
import { usePageContext } from '../renderer/usePageContext';
const pageContext = usePageContext();

enum WidgetType {
    Test1,
    Test2,
    Test3
}

const widgets: Record<number, {}> = {
    [WidgetType.Test1]: TestWidget1,
    [WidgetType.Test2]: TestWidget2,
    [WidgetType.Test3]: TestWidget3,
}
</script>