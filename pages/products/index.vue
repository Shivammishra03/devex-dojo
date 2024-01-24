<script setup>
    const {data:products} = await useFetch('https://fakestoreapi.com/products/')
    useHead({
        title: 'Devx Dojo | Product'
    })
</script>
<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in products">
                <ProductCard :product="p"></ProductCard>
            </div>
        </div>
    </div>
</template>