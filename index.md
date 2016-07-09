---

layout: default

---

# Яндекс

## **{{ site.presentation.title }}** {#cover}

<div class="s">
    <div class="service">{{ site.presentation.service }}</div>
</div>

{% if site.presentation.nda %}
<div class="nda"></div>
{% endif %}

<div class="info">
	<p class="author">{{ site.author.name }}, <br/> {{ site.author.position }}</p>
</div>

## **![](pictures/no-docs.gif)**

## **Документация — это хорошо**

## **Автогенерируемая документация — лучше!**

## **Что есть**

## Что было
* Сайт внутренней библиотеки Яндекса
* ...[bem.info](https://ru.bem.info/libs/bem-components/v2.4.0/showcase/)
* ...[bem-site-engine](https://github.com/bem/bem-site-engine/)

## Что еще было
* [bem-site](https://github.com/bem-site)
* ...bem-data-source
* ...provider
* ...bse-admin
* ...mds-wrapper
* ...builder-libraries
* ...snapshot-master

## Что еще было
* builder-sitemap-xml
* ...dependency-updater
* ...snapshot-cleaner
* ...bem-md-renderer
* ...и так далее...

## **![](pictures/vegas.jpg)**

## **Что появилось**

## **[bem-lib-site](https://github.com/bem-site/bem-lib-site)**

## **Как устроено**

## Как устроено
* bem-lib-site
    * ...bem-lib-site-data
    * ...bem-lib-site-view

## bem-lib-site-data
* Ставит зависимости
* ...Собирает интроспекцию о всех БЭМ-сущностях
    * ...Пути к исходным файлам блоков со всех уровней
    * ...Пути к кастомным файлам примеров

## bem-lib-site-data
* Ставит зависимости
* Собирает интроспекцию о всех БЭМ-сущностях
* Собирает документацию
    * ...block.{lang}.md (с учетом инлайновых примеров)
    * ...JSDoc


## bem-lib-site-data
* Ставит зависимости
* Собирает интроспекцию о всех БЭМ-сущностях
* Собирает документацию
* Собирает примеры
    * ...Живые, в iframe
    * ...HTML
    * ...BEMJSON
    * ...deps

## bem-lib-site-data
* Ставит зависимости
* Собирает интроспекцию о всех БЭМ-сущностях
* Собирает документацию
* Собирает примеры
* Общие readme, migration, changelog
* ...На выходе JSON и файлы примеров

## Структура данных
~~~
library
    version
        gh: '',
        readme: '',
        changelog: ''
        migration: ''
        sets
            desktop
                button
                    docs: ''
                    jsdoc: ''
                    examples: ''
                    sources: ''
~~~

## bem-lib-site-view
* Типичный БЭМ-проект
* ...Можно использовать как уровень переопределения
* ...Можно запилить свой
* ...На вход результат работы bem-lib-site-data
* ...На выходе статичный сайт

## **![](pictures/howto.gif)**

## **Как использовать**

## Как использовать
~~~
npm i bem-lib-site
~~~

## Как использовать
~~~
npm i bem-lib-site
bem-lib-site path/to/my/lib
~~~

## **![](pictures/engino.png)**

## Как использовать
~~~
blocks/
    button/
        button.js
        button.bemhtml.js
    input/
    ...
~~~

## Как использовать
~~~
blocks/
    button/
        button.md
        button.js
        button.bemhtml.js
    input/
    ...
~~~

## **[button.md](https://github.com/bem/bem-components/blob/v3/common.blocks/button/button.ru.md)**

## **[bem.info](https://ru.bem.info/libs/bem-components/v2.4.0/showcase/)**

## Конфигурация
~~~
'bem-lib-site-data': {
    tempFolder: 'tmp',
    outputFolder: 'output',
    platforms: { desktop: ['common', 'deskpad', 'desktop'] },
    libs: {
        'bem-components': {
            langs: ['ru', 'en'],
            github: {
                url: 'github.com', user: 'bem', repo: 'bem-components', defaultBranch: 'v3'
            }
        }
    }
}
~~~

## Планы на будущее
* Внедрить в bem.info
* ...Поддержать инкрементальную сборку
* ...Написать тестов, наконец!

## **Ваши вопросы!**

## **![](pictures/horse.gif)**

## **Контакты** {#contacts}

<div class="info">
<p class="author">{{ site.author.name }}</p>
<p class="position">{{ site.author.position }}</p>

    <div class="contacts">
        <p class="contacts-left contacts-top">bem.info</p>
        <p class="contacts-left mail">info@bem.info</p>
        <p class="contacts-right twitter">bem_ru #b_</p>
        <!-- <p class="contacts-right contacts-bottom vk">vk</p> -->
        <!-- <p class="contacts-right facebook">facebook</p> -->
    </div>
</div>
