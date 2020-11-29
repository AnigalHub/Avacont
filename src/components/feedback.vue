<template>
    <div id="feedback">
        <div class="background">
            <b-container>
               <h2 class="h2_light">Обратная связь</h2>
                <form name="sentMessage" id="Form">
                    <b-row>
                        <b-col cols="5" class="text_light">
                            <label for="name">Ваше имя:</label>
                            <input type="text" class="form-control" placeholder="ФИО" id="name" name="name" required="" data-validation-required-message="Пожалуйста, введите Ваше имя">
                            <label for="phone">Ваше телефон:</label>
                            <input type="tel" class="form-control" placeholder="+7(xxx)xxx-xx-xx" pattern="+7\([0-9]{3}\)[0-9]{3}-[0-9]{2}-[0-9]{2}" id="phone" name="phone" required="" data-validation-required-message="Пожалуйста, введите Номер телефона">
                            <label for="mail">Ваш E-mail:</label>
                            <input type="email" class="form-control" placeholder="Электронная почта" id="mail" name="mail" required="" data-validation-required-message="Пожалуйста, введите Ваш электронный адрес">
                        </b-col>
                        <b-col class="text_light">
                            <label for="message">Ваше сообщение:</label>
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
        background: url("../../public/images/background/background_5.jpg") 100% 100% no-repeat;
        background-size:100% 100%;
    }
    input{
        padding: 25px 10px;
        min-height: 32px;
        margin-bottom: 1%;
    }
    input:hover, textarea:hover{
        box-shadow: 7px 7px 7px #161616;
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
        margin-bottom: 1%;
        font-weight: 600;
        font-family: "Tenor Sans", sans-serif;
        font-size: 1.1rem;
        border-width: 2px 0;
        border-style: solid none;
        border-color: #838383 #838383 #838383;
        border-radius: 6px;
        background: linear-gradient(rgba(188, 153, 122, 0.58), rgba(233, 223, 201, 0.76)) #eee4ce;
        transition: 0.2s;
    }
    button:hover { background: linear-gradient(#eee0d7, #eee0d7) #d6c8bf; }
    button:active { background: linear-gradient(#b6a89f, #eee0d7) #d6c8bf; }
    @media screen and (max-width: 500px) {
        #feedback{
            background-size:cover;
        }
        input{
            padding: 2.5px 2.5px;
            min-height: 18px;
            height: 25px;
            background: rgba(255, 255, 255, 0.88);
        }
        .col-5 {
            flex: 0 0 100% !important;
            max-width: 100% !important;
        }
        .col-5,.col{
            padding: 0 2px !important;
        }
        button{
            margin-top: 3%;
            font-size: 1rem;
            margin-bottom: 4%;
        }
        .row{
            flex-direction: column
        }
        textarea{
            height: 120px !important;
            background: rgba(255, 255, 255, 0.88);
        }
        form{
            padding: 0;
        }
        label {
            margin-bottom: 0.25rem !important;
        }
    }
    @media screen and (min-width: 500px)and (max-width: 768px) {
        input{
            padding: 10px 5px;
        }
        .col-5 {
            flex: 0 0 100% !important;
            max-width: 100% !important;
        }
        .col-5,.col{
            padding: 0 5px !important;
        }
        textarea{
            height: 120px !important;
        }
        button{
            margin-top: 2%;
        }
        form{
            padding: 0 10%;
        }
        label {
            margin-bottom: 0.25rem !important;
        }
    }
    @media screen and (min-width: 768px)and (max-width: 992px) {
        input{
            padding: 20px 10px;
        }
    }
</style>