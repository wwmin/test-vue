<template>
    <div>
        <div>
            <el-button
                    plain
                    @click.native="open">
                可自动关闭
            </el-button>
            <el-button
                    plain
                    @click.native="open2">
                不会自动关闭
            </el-button>
        </div>

        <div>
            <el-button
                    plain
                    @click.native="open3">
                成功
            </el-button>
            <el-button
                    plain
                    @click.native="open4">
                警告
            </el-button>
            <el-button
                    plain
                    @click.native="open5">
                消息
            </el-button>
            <el-button
                    plain
                    @click.native="open6">
                错误
            </el-button>
        </div>
        <div class="co">
            应用样式
        </div>
    </div>

</template>

<script>
    export default {
        name: 'app',
        methods: {
            open(){
                this.$notify({
                    title: "标题名称",
                    message: '这是提示文案这是提示文案这是提示文案这是提示文案这是提示文案这是提示文案这是提示文案这是提示文案'
                })
            },
            open2(){
                this.$notify({
                    title: '提示',
                    message: '这是一条不会自动关闭的消息',
                    duration: 0
                })
            },
            open3() {
                this.$notify({
                    title: '成功',
                    message: '这是一条成功的提示消息',
                    type: 'success'
                });
            },

            open4() {
                this.$notify({
                    title: '警告',
                    message: '这是一条警告的提示消息',
                    type: 'warning'
                });
            },

            open5() {
                this.$notify({
                    title: '消息',
                    message: '这是一条消息的提示消息',
                    type: 'info'
                });
            },

            open6() {
                this.$notify({
                    title: '错误',
                    message: '这是一条错误的提示消息',
                    type: 'error'
                });
            }
        }
    };
</script>

<style>
    .co {
        padding: 20px;
        color: #2e90fe;
    }

</style>
