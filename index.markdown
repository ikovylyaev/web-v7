---
layout: default
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
            <div class='about'>
                <h4 class='second-color inter-regular'>Кратко</h4>
                <p class='main-color inter-regular'>Занимаюсь дизайном интерфейсов, веб-сайтов, созданием дизайн-систем, брендингом и&nbsp;шрифтовым дизайном более 5&nbsp;лет. Работаю в&nbsp;xi.effect. Это лучшее приложение для репетиторов и&nbsp;малого бизнеса. Также успел поработать в&nbsp;коде Екатеринбурга над транспортным порталом. Живу в&nbsp;Екатеринбурге, вдохновляюсь этим замечательным городом и&nbsp;природой вокруг. </p>
            </div>
            <div class='links'>
                <a class='pill-link' href='https://t.me/ikovylyaev'>Telegram</a>
                <a class='pill-link' href='mailto:hi@ikovylyaev.com'>hi@ikovylyaev.com</a>
                <a class='pill-link' href='https://behance.net/{{site.behance}}'>Behance</a>
                <a class='pill-link' href='https://dprofile.ru/{{site.dprofile}}'>DProfile</a>
            </div>
        </div>
    </div>
    {% for post in site.design %}
    <div class='row'>
        <div class='col-12'>
            <div class='image' style="background: url({{site.url}}/img/works/{{ post.image }}.webp); background-size: {{ post.imgsize }}; background-position: center; background-repeat: no-repeat; background-color: {{ post.bgcolor}};"></div>
        </div>
        {% if post.link != "" %}
            <a  href="{{ post.link }}" target="blank" class='col-12'>
        {% else%}
            <div class='col-12'>
        {% endif %}
            <p class='inter-regular'>
                <span class='main-color inter-regular'>{{ post.title}}.</span> 
                {{ post.description }}
            </p>
        {% if post.link != "" %}
            </a>
        {% else%}
            </div>
        {% endif %}
    </div>
    {% endfor %}
    <footer class='row'>
        <div class='col text-start'>2019-2023</div>
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
