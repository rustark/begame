---
title: 'Помоги проекту'
menu: Связь
form:
    action: /
    classes: 'uk-grid-small uk-grid'
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

#Помоги проекту

**Begame 0.9.9** версия проекта по социальной динамике. При обнаружении ошибки, или если у вас есть предложения по расширению функционала - напишите об этом в сообщество [Begame](https://vk.com/topic-40016074_39188341). На данный момент полностью перенесено первое пособие по рутинам от **Love Systems**.

Вы можете помочь проекту, отправив свой гамбит для публикации в сообществе [Begame](https://vk.com/topic-40016074_39184993), в нашей закрытой группе [Vkontakte Lair](https://vk.com/vklair), или заполнив форму: