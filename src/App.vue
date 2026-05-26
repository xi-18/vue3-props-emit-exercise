<template>
    <div class="app-container">
        <header>
            <h1>🛒 前端商城控制台</h1>
            <div class="cart-badge">
                購物車商品總數: <span>{{ totalCartCount }}</span> 件
            </div>
        </header>

        <main>
            <h2>商品上架預覽</h2>
            <div class="product-list">
                <ProductCard v-for="product in products" :key="product.id" />
            </div>

            <hr class="divider" />

            <h2>購物車數量快速調整</h2>
            <div class="control-panel">
                <p>不分類型，快速為購物車商品總數進行加減：</p>
            </div>
        </main>
    </div>
</template>

<script setup>
import { ref } from "vue";
// 💡 請記得在這裡 import 你的子組件：ProductCard 與 CounterButton

// 模擬從後端取得的商品資料
const products = ref([
    { id: 1, title: "💻 27吋 4K 專業螢幕", price: 12900, isFeatures: true },
    { id: 2, title: "⌨️ 機械式人體工學鍵盤", price: 3490, isFeatures: false },
    { id: 3, title: "🖱️ 無線垂直靜音滑鼠", price: 1890, isFeatures: true },
]);

// 購物車總數的響應式資料
const totalCartCount = ref(0);

// 【任務二：Emit 處理函式】
const updateCartCount = (amount) => {
    // 實作邏輯：根據子組件傳回的數字（正數或負數）來更新 totalCartCount.value
    // 💡 進階思考：購物車數量可以變成負數嗎？如果小於 0 該怎麼處理？
};
</script>

<style scoped>
.app-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    font-family: Arial, sans-serif;
}
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-bottom: 20px;
    border-bottom: 2px solid #35495e;
}
.cart-badge {
    background-color: #42b883;
    color: white;
    padding: 10px 20px;
    border-radius: 20px;
    font-weight: bold;
}
.product-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-top: 20px;
}
.divider {
    margin: 40px 0;
    border: 0;
    border-top: 1px solid #ddd;
}
.control-panel {
    background-color: #f9f9f9;
    padding: 20px;
    border-radius: 8px;
    border: 1px solid #eee;
}
</style>
