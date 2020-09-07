<template>
    <div class="example">
        <b-container>
            <b-row class="important_row">
                <b-col class="important_col">
                    <h2>Информация о кассе</h2>
                    <form>
                        РНМ:<br>
                        <input type="text"><br>
                        Номер ФН:<br>
                        <input type="text"><br>
                        Заводской номер <br>
                        <input type="text"><br>
                        Название кассы <br>
                        <input type="text"><br>
                        Ресурс ФН <br>
                        <input type="text"><br><br>
                        <input class="change" type="submit" value="Изменить кассу">
                        <input class="cancel" type="submit" value="Отмена">
                    </form>

                </b-col>
                <b-col class="important_col">
                    Не используйте функцию "Изменить кассу" при замене фискального накопителя.
                    Она применяется только для изменения ошибочно зарегистрированных данных.
                    При замене ФН отключите кассу и добавьте ее с новым номером ФН.
                </b-col>
            </b-row>
        </b-container>


    </div>
</template>

<script>
    export default {
        name: "example"
    }
</script>

<style scoped lang="scss">
    input{
      width: 100%;
    }
    .change{
        width: 68% !important;
        margin: 1%;
    }
    .cancel{
        width: 28% !important;
        margin: 1%;
    }
    .important_col:first-child{
        max-width: 500px;
    }
    .important_col:last-child{
        max-width: 200px;
    }
    .important_col{
        background: white;
        margin: 2% 2% 1% 2%;
        padding: 2rem 1.5rem;
        border-radius: 2px;
        box-shadow: 0px 1px 3px 0px rgba(0,0,0,0.3);
        font-size:0.9rem ;
    }
    @media (min-width: 992px){
        .container, .container-lg, .container-md, .container-sm, .container-xl {
            max-width: 50% !important;
            max-height: 100%;
        }
    }
    @media (max-width: 992px){
        .container, .container-lg, .container-md, .container-sm, .container-xl {
            max-width: 60% !important;
            max-height: 100%;
        }
    }

    @media screen  and (max-width: 768px) {
        h2{
            font-size: 1.3rem !important;
        }
        .important_row{
             flex-direction: column;
            .important_col{
                max-width: 100%;
            }
         }
        .container, .container-lg, .container-md, .container-sm, .container-xl {
            max-width: 70% !important;
            max-height: 100%;
        }

    }
    @media screen and (min-width: 768px) and (max-width: 992px) {
        h2{
            font-size: 1.5rem !important;
        }

    }
</style>