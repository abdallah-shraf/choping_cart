<template>
  <div class="Card">
    <h1>Your Carde  </h1>
    <CartItemCard
    v-for="product in products"
    :key="product.id"
    :product="product"/>
    <CartSummaryPaymentCard/>
  </div>
</template>


<script>
import CartItemCard from  '../components/cart/cartItem.vue'
import CartSummaryPaymentCard from '../components/cart/CartSummaryPaymentCard.vue'
export default {
  components: {
    CartItemCard, CartSummaryPaymentCard
  },
  computed: {
    products(){
      return this.$store.getters.cartItems
    }
  }
}
</script>
