<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Пример страницы с кнопками</title>
    <style>
	body{
            background-color:rgb(32, 31, 31);
        }
        #content {
            background-color: rgb(255 255 255/.3) ;
            text-align: center;
            padding: 20px;
            border: 1px solid #ccc;
            margin: 20px;
        }

        .button {
            padding: 10px 20px;
            font-size: 14px;
            cursor: pointer;
            margin: 5px;
        }
        img{
            width: 250px;
        }
    </style>
</head>
<body>
    

<!-- Блок с картинкой и текстом -->
<div id="content">
    <img src="маф1.jpeg"> 
    <p>1 Вы пацан ходите в школу и пахан предлагает вам записаться на единоборства </p>
<button class="button" onclick="changeContent('page1')">Записаться в споривную секцию</button>
<button class="button" onclick="changeContent('page2')">Продолжать и дальше ничего не делать(я бы не советовал нажимать)</button>
<audio>
					<source src="Адхах Дзыбов.mp3" type="audio/mpeg">
				</audio>
</div>

                


<script>
    function changeContent(page) {
        var content = document.getElementById('content');

        // В зависимости от выбранной кнопки меняем контент блока
        if (page === 'page1') {
            content.innerHTML = `
            <p>2 Отлично ты начал заниматься спортом и пахан поарил тебе кожанку но на у лице к тебе подходит гопник и говорит отдавать ее ему</p>
        <button class="button" onclick="changeContent('page3')">Постоять за себя</button>
        <button class="button" onclick="changeContent('page4')">Отдать ему кожанку</button>
        
                `
        } else if (page === 'page2') {
            content.innerHTML = `
<p>3 Тебя начали обижать в классе </p>
<button class="button" onclick="changeContent('page6')">Все таки записаться в спортивную секцию</button>
<button class="button" onclick="changeContent('page7')">Продолжать ничего не делать</button>
        
        `;
        } else if (page === 'page6') {
            content.innerHTML = `
            <p>2 Отлично ты начал заниматься спортом и пахан подарил тебе кожанку но на у лице к тебе подходит гопник и говорит отдавать ее ему</p>
        <button class="button" onclick="changeContent('page3')">Постоять за себя</button>
        <button class="button" onclick="changeContent('page4')">Отдать ему кожанку</button>
        `;
        }else if (page === 'page7') {
            content.innerHTML = `
            <p>8 ты с кентом начали бизнесс</p>
        <button class="button" onclick="changeContent('page8')">Продолжить это 8 кнопка</button>
        `;
        } else if (page === 'page3') {
            content.innerHTML = `
<p>7 Отлично ты дал ему отпор и рассказал об этом своим кентам и один из них позвал тебя поехать с ним в москву за товарами</p>
<button class="button" onclick="changeContent('page9')">Поехали</button>
        
        `;
        } else if (page === 'page9') {
            content.innerHTML = `
<p>9 Бизнесс идет в гору ты покупаешь баточники сникерс за 3 рубля и продаешь за 15 но вдруг к тебе приходят 2 бандита и говорят что теперь ты  им должен отдавать 20%</p>
<button class="button" onclick="changeContent('page12')">Звонить ментам</button>
<button class="button" onclick="changeContent('page13')">Дать отпор лично</button>
<button class="button" onclick="changeContent('page14')">Отдать им деньги</button>
        
        `;
        }else if (page === 'page8') {
            content.innerHTML = `
<p>8 ты решил открыть свой бизнесс и у тебя все получилось слабая версия</p>
<button class="button" onclick="changeContent('page18')">Звонить ментам</button>
<button class="button" onclick="changeContent('page14')">Отдать им деньги</button>

        
        `;
        }else if (page === 'page4') {
            content.innerHTML = `
            <p>9 Бизнесс идет в гору ты покупаешь баточники сникерс за 3 рубля и продаешь за 15 но вдруг к тебе приходят 2 бандита и говорят что теперь ты  им должен отдавать 20%</p>
<button class="button" onclick="changeContent('page12')">Звонить ментам</button>
<button class="button" onclick="changeContent('page13')">Дать отпор лично</button>
<button class="button" onclick="changeContent('page14')">Отдать им деньги</button>
        
        `;
        } else if (page === 'page12') {
            content.innerHTML = `
<p>17 Менты не приехали</p>
<button class="button" onclick="changeContent('page13')">Дать отпор лично</button>
<button class="button" onclick="changeContent('page14')">Отдать им деньги</button>
        
        `;} else if (page === 'page14') {
            content.innerHTML = `
<p>14 Вы стали отдавать им деньги но к вам приехали еще и говорят что они из другой опг и теперь вы должны 15% им тоже</p>
<button class="button" onclick="changeContent('page15')">Звонить ментам</button>
<button class="button" onclick="changeContent('page13')">Взять все в свои руки и лично дать отпор</button>
<button class="button" onclick="changeContent('page16')">отдать деньги им тоже</button> 
<button class="button" onclick="changeContent('page17')">Позвонить главному авторитету</button>       
        `;
    } else if (page === 'page15') {
            content.innerHTML = `
<p>Они все равно не приехали</p>
<button class="button" onclick="changeContent('page16')">отдать деньги им тоже</button>
<button class="button" onclick="changeContent('page13')">Взять все в свои руки и лично дать отпор</button>     
        `;
    }else if (page === 'page16') {
            content.innerHTML = `
<h2>Вы проиграли</h2>
<p>Вы маленький бизнесмен который работает и отдает большую часть прибыли ОПГ и надеется что все закончится само собой</p>       
        `;
    }else if (page === 'page17') {
            content.innerHTML = `
<h2>Вы проиграли</h2>
<p>Вы маленький бизнесмен который не может дать отпор и отдает 30% самому сильному авторитету в замен за засщиту</p>       
        `;
    }else if (page === 'page18') {
            content.innerHTML = `
<p>17 Менты не приехали</p>   
<button class="button" onclick="changeContent('page16')">Отдать им деньги</button>
<button class="button" onclick="changeContent('page17')">Позвонить главному авторитету</button>
       `;
        } else if (page === 'page13') {
            content.innerHTML = `
<p>19 Вы дали им отпор и они но на следующий день к вам пришли 20 вооруженных бандитов оказалось это было ОПГ</p>
<button class="button" onclick="changeContent('page20')">Драться один против двадцати</button>
<button class="button" onclick="changeContent('page21')">Позвать кентов и тянуть время</button>     
<button class="button" onclick="changeContent('page17')">Позвонить главному авторитету</button>
`;
    } else if (page === 'page20') {
            content.innerHTML = `
    <h2>Вы проиграли</h2>
<p>Вас избили толпой и отжали бизнес повезло хотя бы выжили</p>       
       `;
    } else if (page === 'page21') {
            content.innerHTML = `
<p>Как только кенты узнали что вы стоите один в 20 они моментально приехали и вместе вы разбили их ОПГ</p>
<button class="button" onclick="changeContent('page22')">Дальше</button>   
        `;
    } else if (page === 'page22') {
            content.innerHTML = `
<p>О вашей победе узнали во всем городе и теперь они считают что вы ОПГ к вам обращаются за помощью и отдают 30% за защиту</p>
<button class="button" onclick="changeContent('page23')">Дальше</button>   
        `;
    } else if (page === 'page23') {
            content.innerHTML = `
<p>К вам стали приходить спортсмены и просить работать на вас ведь знают что вы авторитет также маленькие ОПГ захотели войти в ваш состав чтобы вообще не исчезнуть под гнетом более сильных</p>
<button class="button" onclick="changeContent('page24')">Дальше</button>   
        `;
    }else if (page === 'page24') {
            content.innerHTML = `
<p>Теперь вы управляете сотнями людей и зарабатываете миллионы каждый день что с ними делать</p>   
<button class="button" onclick="changeContent('page25')">Потратить все на наркотики и дома и тачки</button>
<button class="button" onclick="changeContent('page26')">Тратить все без разбора покупая ненужные вещи </button>
<button class="button" onclick="changeContent('page27')">Хранить деньги ведь их и так хватает</button>
       `;
    } else if (page === 'page25') {
            content.innerHTML = `
    <h2>Вы проиграли</h2>
    <img src="1617289629_d4767c5c047059130ffaaf6fed2bfead.jpg">
<p>Вы повторили судьбу Тони Монтаны. Вы начали думать только о себе и вас стали предовать свои же и когда вы схлестнулись с другим ОПГ вам никто не помог</p>       
       `;
    } else if (page === 'page26') {
            content.innerHTML = `
<p>Вашего лучшего друга похитили и требуют выкуп в миллиард за его голову у вас нет этих денег</p>
<button class="button" onclick="changeContent('page29')">Продать все что есть и брать в долг чтобы расплатится</button>
<button class="button" onclick="changeContent('page28')">Не отдавать деньги</button>
        `;
    } else if (page === 'page28') {
            content.innerHTML = `
    <h2>Игра окончена</h2>
<p>От вас отвернулись ваши самые близкие ведь они с вами не из-за страха а из уважения и на вас напали те ОПГ и победили игра окнчена</p>       
       `;
    } else if (page === 'page29') {
            content.innerHTML = `
    <h2>Игра окончена</h2>
<p>Вы спасли своего друга но у вас закрнчились деньги а то ОПГ которому вы их отдали наняли наемников и одолели вас это была их тактика завоевания теперь это их территория </p>       
       `;
    } else if (page === 'page27') {
            content.innerHTML = `
<p>Вашего лучшего друга похитили и требуют выкуп в миллиард за его голову у вас нет этих денег</p>
<button class="button" onclick="changeContent('page29')">Отдать все что у вас есть</button>
<button class="button" onclick="changeContent('page28')">Не отдавать деньги</button>
<button class="button" onclick="changeContent('page30')">Потратить все на ЧВК и забрать его силой</button>
        `;
    } else if (page === 'page30') {
            content.innerHTML = `
<p>На эти деньги вы наняли вооруженную, обученную армию и угродали уничтожить всех если вам не выдадут вашего человека целым и невредимым </p>
<button class="button" onclick="changeContent('page31')">Дальше</button>   
        `;
    } else if (page === 'page31') {
            content.innerHTML = `
<p>Они не ожидали такого не были готовы к войне вам моментально вернули вашего человека</p>
<button class="button" onclick="changeContent('page32')">Дальше</button>   
        `;
    } else if (page === 'page32') {
            content.innerHTML = `
    <h2>Поздравляю вы прошли игру</h2>
<p>Слава о вашем поступке дошла до всех уголков страны теперь вы самый главный авторитет и другие ОПГ вступают с вами в союз желая иметь такого союзника</p>       
       `;
        }
    }
</script>

</body>
</html>
