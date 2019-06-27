---
title: 'Процесс'
menu: Процесс
process:
    -
        author: 'Love Systems'
        title: 'Routines Manual Vol.1'
        img: michael-discenza-199756-unsplash.jpg
        percent: 100
    -
        author: 'Brad P'
        title: 'Black Book'
        img: michael-dam-258165-unsplash.jpg
        percent: 75
    -
        author: 'Mystery'
        title: 'Hey Guys'
        img: alexander-popov-342444-unsplash.jpg
        percent: 100
    -
        author: 'Love Systems'
        title: 'Routines Manual Vol.2'
        img: alexander-popov-566913-unsplash.jpg
        percent: 4
    -
        author: 'Mystery'
        title: 'Book of Negs'
        img: marcela-laskoski-118684-unsplash.jpg
        percent: 10
form:
    action: /
    classes: 'uk-grid uk-hidden'
    fields:
        author:
            classes: uk-input
            label: Автор
            labelclasses: 'uk-form-label uk-margin-top uk-margin-small-bottom'
            outerclasses: uk-width-1-3@s
            placeholder: 'Имя автора'
            type: text
            validate:
                required: true
        title:
            classes: uk-input
            label: Название
            labelclasses: 'uk-form-label uk-margin-top uk-margin-small-bottom'
            outerclasses: uk-width-1-3@s
            placeholder: 'Название гамбита'
            type: text
            validate:
                required: true
        stage:
            classes: uk-select
            default: a
            label: Этап
            labelclasses: 'uk-form-label uk-margin-top uk-margin-small-bottom'
            outerclasses: uk-width-1-3@s
            size: long
            type: select
            options:
                a: Привлечение
                c: Комфорт
                s: Влечение
                r: Отношения
        message:
            classes: uk-textarea
            label: Гамбит
            labelclasses: 'uk-form-label uk-margin-top uk-margin-small-bottom'
            outerclasses: uk-width-1-1
            placeholder: Содержание
            type: textarea
        recaptcha:
            dataclasses: 'uk-margin-top uk-width-responsive'
            outerclasses: uk-hidden
            label: Капча
            labelclasses: 'uk-hidden'
            recaptcha_not_validated: 'Не сработало!'
            type: captcha
            validate:
                required: true
    buttons:
        submit:
            type: submit
            value: Отправить
            classes: 'uk-button uk-margin-top uk-button-default uk-button-large uk-width-1-1'
    process:
        captcha:
        email:
            from: '{{ config.plugins.email.from }}'
            to: '{{ config.plugins.email.to }}'
            subject: '[Begame] {{ form.value.name|e }}'
            body: '{% include ''forms/data.html.twig'' %}'
        save:
            fileprefix: order-
            dateformat: dmY-Hi
            extension: txt
            body: '{% include ''forms/data.txt.twig'' %}'
        message: '<b>Спасибо!</b><br/>Мы постараемся опубликовать ваш материал в ближайшее время!'
---

#Процесс

<span uk-icon="icon: begame"></span> <sup>beta</sup> здесь ты узнашь что такое пикап, социальная динамика и игра без регистрации и СМС.
<!--
Более 10 лет [я](/players/dmitry-yakushev "Dmitry Yakushev") практикую **Mystery Method**. Все это время я был, есть и буду глубоко убежден в том, что абсолютно все знания по пикапу / социальной динамике / игре должны быть бесплатными и доступными каждому мужчине на планете. Более 10 лет я совершенно бесплатно делюсь знаниями и соблюдаю все правила игры (в т.ч. строгая конфиденциальность, но ты мог знать меня под несколькими псевдонимами в разное время).

С годами энтузиазм как на ведение тренингов (единственное, за что брал деньги - потраченое мной время на тренингах) так и на беготню по полям растерялся. Время уходить из игры все ближе и этот сайт «последний рубеж».  
Здесь я совершенно бесплатно <abbr title="Раздел статей в доработке">пишу об игре</abbr> по принципу от общего к частному и собираю каталог гамбитов от лучших игроков на планете. И ты можешь внести свой вклад!
-->
[Поддержи проект](https://money.yandex.ru/to/41001425190789 "Поддержать материально")

[Vkontakte](https://vk.com/begame "Помоги с переводом, либо просто подпишись"){.uk-button .uk-button-text .uk-margin-right} [GitHub](https://github.com/rustark/begame "Гамбиты в .md для свободного использования"){.uk-button .uk-button-text .uk-margin-right} [Telegram](https://t.me/begame_gambits "RSS лента в телеграм"){.uk-button .uk-button-text .uk-margin-right}

Процесс перевода гамбитов: