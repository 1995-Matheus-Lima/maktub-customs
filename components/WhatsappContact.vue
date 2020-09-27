<template>
    <div>
         <a :href="`https://wa.me/${phoneNum}?text=${message}`" target="_blank" class="contact-us">
          <Whats />
          Posso ajudar?
         </a>
    </div>
</template>

<script>
    import Whats from '@/components/Whats';
    export default {
        props: {
            phoneNum: {
                default: () => "5511972155208"
            },
            message: {
                default: () => "Gostaria de mais informações sobre os serviços Maktub."
            }
        },
        components: {
            Whats
        }
        
    }
</script>

<style lang="scss" scoped>
.contact-us {
    padding: 30px;
    background-color: green;
    text-decoration: none;
    color: white;
    width: 200px;
    height: 50px;
    svg {
      fill: #27cc44;
      width: 48px;
    }
}

</style>
     