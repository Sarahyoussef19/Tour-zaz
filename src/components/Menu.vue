<template>
    <div class="menu">
        <n-menu v-model:value="activeKey" mode="horizontal" :options="menuOptions" />

    </div>
</template>

<script>
import { defineComponent, h, ref } from "vue";
import { NIcon, NMenu } from "naive-ui";
import {

    MusicalNotes,
    MusicalNoteOutline,
    MusicalNote
} from "@vicons/ionicons5";

function renderIcon(icon) {
    return () => h(NIcon, null, { default: () => h(icon) });
}

const menuOptions = [
    {
        label: () => h("a", {
            href: "https://www.zazofficial.com/en",
            target: "_blank",
            rel: "noopenner noreferrer"
        }, "zaz-official"),
        key: "zaz-official",
        icon: renderIcon(MusicalNotes)
    },

    {
        href: "https://zaz.lnk.to/isaWW",
        label: "Tours",
        key: "Tours",
        icon: renderIcon(MusicalNoteOutline),
        children: [
            {
                href: "https://www.youtube.com/watch?v=f2uxifMlIcs",
                type: "group",
                label: "People",
                key: "people",
                children: [
                    {
                        label: "Europe",
                        key: "Europe",
                        icon: renderIcon(MusicalNote)
                    },
                    {
                        label: "Middle East",
                        key: "Middle-East",
                        icon: renderIcon(MusicalNote)
                    }
                ]
            },
        ]
    }
];

export default defineComponent({
    setup() {
        return {
            activeKey: ref(null),
            menuOptions
        };
    }, components: { NMenu }
});
</script>

<style>
.menu {
    background-color: rgba(107, 183, 218, 0.401);
    margin: 5px 0;
    padding: 10px;
    position: relative;
    top: 0;
    border-radius: 20px;
}
</style>