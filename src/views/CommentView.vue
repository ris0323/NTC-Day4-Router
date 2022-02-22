<template>
        product Id is {{$route.params.productId}}

        <router-link :to="`/product/${route.params.productId}/comments`">
</template>
