<template>
    <div class="product-card" :class="{ 'featured-border': isFeatures }">
        <span v-if="isFeatures" class="badge">⭐ 推薦商品</span>

        <h3 class="product-title">{{ title }}</h3>

        <p class="product-price">NT$ {{ price }}</p>
    </div>
</template>

<script setup>
// 【任務一：使用 defineProps 定義接收的資料】
// 請根據以下規格宣告 props：
// 1. title: 字串 (String), 必填 (required: true)
// 2. price: 數字 (Number), 必填 (required: true)
// 3. isFeatures: 布林值 (Boolean), 非必填, 預設值為 false (default: false)
</script>

<style scoped>
.product-card {
    border: 1px solid #e0e0e0;
    border-radius: 8px;
    padding: 16px;
    background-color: #fff;
    position: relative;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}
.featured-border {
    border: 2px solid #42b883; /* 推薦商品會有綠色邊框 */
}
.badge {
    position: absolute;
    top: -10px;
    left: 10px;
    background-color: #42b883;
    color: white;
    font-size: 12px;
    padding: 2px 8px;
    border-radius: 4px;
}
.product-title {
    margin: 10px 0 5px 0;
    font-size: 18px;
}
.product-price {
    color: #e67e22;
    font-weight: bold;
    margin: 0;
}
</style>
