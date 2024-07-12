<template lang="pug">
.container
        tt
        ul.story-list
            li
                span.story-title Ai Bảo Hắn Tu Tiên
                span.chapter Chương 1
            li
                span.story-title Khai Cục Nữ Ma Đ...
                span.chapter Chương 1
            li
                span.story-title Túc Mệnh Chi Hoàn
                span.chapter Chương 1
            li
                span.story-title Đạo Gia Muốn Phi...
                span.chapter Chương 1

</template>
<script>
import tt from "../Title.vue";
export default {
    name: 'listdoc',
    components: { tt },
    data(){}
}
</script>

<style lang="stylus" scoped>
.container {
    width: 100%;
    margin: 0 auto;
    background-color: #fff;
    border: 1px solid #ddd;
    padding: 20px;
    border-radius: 5px;
}

h2 {
    text-align: center;
    font-size: 22px;
    margin-bottom: 20px;
    font-weight: bold;
}

.story-list {
    list-style-type: none;
    padding: 0;
    margin: 0;
}

.story-list li {
    display: flex;
    justify-content: space-between;
    padding: 8px 0;
    border-bottom: 1px solid #ddd;
}

.story-list li:last-child {
    border-bottom: none;
}

.story-title {
    flex: 1;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.chapter {
    flex-shrink: 0;
    margin-left: 10px;
    color: #888;
}
</style>