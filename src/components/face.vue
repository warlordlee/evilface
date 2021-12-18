<template>
    <div class="main pad">
        <div style="text-align: center;padding: 15px">Lee 草率的表情包制作</div>
        <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="证件" name="first">
                <certificate></certificate>
            </el-tab-pane>
            <el-tab-pane label="熊猫头" name="second">
                <panda></panda>
            </el-tab-pane>
            <el-tab-pane label="蘑菇人" name="third">
                <ms></ms>
            </el-tab-pane>
            <el-tab-pane label="摸鱼" name="forth">
                <fish></fish>
            </el-tab-pane>
        </el-tabs>
    </div>
</template>

<script>
    import certificate from "@/components/certificate";
    import fish from "@/components/fish";
    import panda from "@/components/panda";
    import ms from '@/components/ms'

    export default {
        name: "face",
        components: {
            certificate,
            fish,
            panda,
            ms
        },
        data() {
            return {
                activeName: 'first'
            }
        },
        methods: {
            handleClick() {

            }
        }
    }
</script>

<style scoped lang="less">
    .pad {
        padding: 30px 60px;
    }
</style>
