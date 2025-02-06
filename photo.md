---
layout: default
permalink: /photo/
---
<div class='container-fluid inter-regular'>
    <div class='row'>
        <div class='col-12'>
            <a class='avatar' href='{{site.url}}'>
                <div class='avatar-image'><img src='{{site.url}}/img/avatar.png' alt='Ivan Kovylyaev'></div>
                <div class='avatar-text'>
                    <span class='inter-regular'>Иван Ковыляев</span>
                    <p class='inter-regular'>UX/UI и продуктовый дизайнер</p>
                </div>
            </a>
            <div class='links'>
                <a class='pill-link' href='https://t.me/ikovylyaev'>Telegram</a>
                <a class='pill-link' href='mailto:hi@ikovylyaev.com'>hi@ikovylyaev.com</a>
                <a class='pill-link' href='https://behance.net/{{site.behance}}'>Behance</a>
                <a class='pill-link' href='https://dprofile.ru/{{site.dprofile}}'>DProfile</a>
                <a class='pill-link active' href='https://ikovylyaev.com/photo'>Photo</a>
            </div>
        </div>
    </div>
    <div class='row'>
        {% for counter in (1..87) %}
            <div class='col-md-4 col-sm-6 col-12 photo' style='background: url({{site.url}}/img/photo/{{ counter }}.webp);background-size: cover; background-position: center;'></div>
        {% endfor %}
        <a href="https://media.ikovylyaev.com" target="_blank" class='col-md-4 col-sm-6 col-12 photo' style='background: var(--orange);'>
            <h4>Больше фотографий на&nbsp;media.ikovylyaev.com</h4>
        </a>
    </div>
    <footer class='row'>
        <div class='col text-start'>2019 - {{ 'now' | date: "%Y" }}</div>
        <div class='col text-center'><a class='link' target='_blank' href='mailto:{{ site.email }}'>{{ site.email}}</a></div>
        <div class='col text-center'><a class='link' target='_blank' href='https://t.me/{{ site.telegram }}'>Телеграм</a></div>
        <div class='col text-center'><a class='link' target='_blank' href='https://behance.net/{{ site.behance }}'>Беханс</a></div>
        <div class='col text-center'><a class='link' target='_blank' href='https://dprofile.ru/{{ site.dprofile }}'>ДПрофайл</a></div>
        <div class='col text-end'><a class='link' target='_blank' href='https://figma.com/@{{ site.figma }}'>Фигма</a></div>
    </footer>
    <footer class='row text-center'>
        <div class='col'><a class='link secondary-link' href='{{ site.url }}/policy'>Политика конфиденциальности</a></div>
    </footer>
</div>

<style>
  .photo{
    aspect-ratio: 1/1;
    border: 8px solid #FFFFFF;
    position: relative;
  }
  .photo h4{
    position: absolute;
    width: calc(100% - 32px);
    text-align:center;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    color: #ffffff;
  }
</style>