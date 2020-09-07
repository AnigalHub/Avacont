<template>
    <div id="feedback">
        <div class="background">
            <b-container>
               <h2 class="h2_light">Обратная связь</h2>
                <form name="sentMessage" id="Form">
                    <b-row>
                        <b-col cols="5" class="text_light">
                            Ваше имя:
                            <input type="text" class="form-control" placeholder="ФИО" id="name" name="name" required="" data-validation-required-message="Пожалуйста, введите Ваше имя">
                            Ваше телефон:
                            <input type="tel" class="form-control" placeholder="+7(xxx)xxx-xx-xx" pattern="+7\([0-9]{3}\)[0-9]{3}-[0-9]{2}-[0-9]{2}" id="phone" name="phone" required="" data-validation-required-message="Пожалуйста, введите Номер телефона">
                            Ваш E-mail:
                            <input type="email" class="form-control" placeholder="Электронная почта" id="mail" name="mail" required="" data-validation-required-message="Пожалуйста, введите Ваш электронный адрес">
                        </b-col>
                        <b-col class="text_light">
                            Ваше сообщение:
                            <textarea class="form-control" placeholder="Опишите ваш запрос" id="message" name="message" required="" data-validation-required-message="Пожалуйста, введите сообщение"></textarea>
                        </b-col>
                    </b-row>
                    <button type="submit" class="draw justify-content-end">Отправить сообщение</button>
                </form>
            </b-container>
        </div>
    </div>
</template>

<script>
    export default {
        name: "feedback"
    }
</script>

<style scoped lang="scss">
    #feedback{
        background: url("../../src/assets/images/background_5.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
    }
    input{
        padding: 25px 10px;
        min-height: 32px;
        margin-bottom: 1%;
    }
    textarea{
        height: 87% !important;
    }
    .col,.col-5{
        padding-bottom: 0.5%;
    }
    button{
        display: block;
        margin-top: 0.5%;
        margin-left: auto;
        margin-right: auto;
        padding: 0.25% 2%;
        font-size: 1.2rem;
    }
    @media screen and (max-width: 500px) {
        #feedback{
            background-size:cover;
        }
        input{
            padding: 5px 5px;
            min-height: 28px;
            height: 28px;
        }
        .col-5 {
            flex: 0 0 100% !important;
            max-width: 100% !important;
        }
        .col-5,.col{
            padding: 0 5px !important;
        }
        button{
            margin-top: 2%;
            font-size: 1rem;
        }
        .row{
            flex-direction: column
        }
        textarea{
            height: 150px !important;
        }
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        input{
            padding: 15px 5px;
        }
        .col-5 {
            flex: 0 0 37% !important;
            max-width: 37% !important;
        }
        .col-5,.col{
            padding: 0 5px !important;
        }
        button{
            margin-top: 2%;
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        input{
            padding: 20px 10px;
        }
    }
</style>