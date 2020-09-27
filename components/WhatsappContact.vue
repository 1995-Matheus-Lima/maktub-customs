<template>
    <div class="contact-us">
      <div class="item">
        <Whats />
        <a :href="`https://wa.me/${phoneNum}?text=${message}`" target="_blank" class="link">Como podemos ajudar?</a>
        <p class="description">Seu carro está em nossos cuidados ou pediu um orçamento? Consulte o status do serviço aqui!</p>
      </div>
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
    width: 300px;
    height:250px;
    text-align:center;
    padding:20px;
    margin-top: 40px;
    border-top: 1px solid #bdbdbd57;
    border-left: 1px solid #bdbdbd57;
    box-shadow: 2px 2px 3px 0px #25252570;

    @media screen and (min-width: 768px) {
      
    }

  .link {
    display: block;
    padding: 20px;
    text-decoration: none;
    color: black;
    font-weight: 600;
    font-size: large;
    &:hover {
      cursor: pointer;
      color: #E49061;
    }
  }
 
}

</style>
     