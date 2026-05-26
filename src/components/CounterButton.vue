<template>
    <div class="counter-actions">
        <button class="btn btn-danger">- 1 件</button>
        <button class="btn btn-success">+ 1 件</button>
    </div>
</template>

<script setup>
// 【任務二：使用 defineEmits 定義要傳給父組件的自訂事件】
// 請定義一個名為 'change-volume' (或你自己喜歡的事件名稱) 的 emit
</script>

<style scoped>
.counter-actions {
    display: flex;
    gap: 10px;
    margin-top: 10px;
}
.btn {
    padding: 10px 20px;
    font-size: 16px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.2s;
}
.btn-success {
    background-color: #42b883;
    color: white;
}
.btn-success:hover {
    background-color: #339966;
}
.btn-danger {
    background-color: #e74c3c;
    color: white;
}
.btn-danger:hover {
    background-color: #c0392b;
}
</style>
