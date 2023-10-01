---
layout: default
---
<div class='container-fluid'>
    <div class='row'>
        <div class='col-md-10 col-12 offset-md-1'>
            <!---<p><span class='main-color'>Иван Ковыляев.</span>Дизайн-лид <a class='link' href="https://xieffect.ru" target="blank">Xieffect.ru</a> и веб-дизайнер в <a class='link' href="https://ekaterinburg.dev/" target="blank">Код Екатеринбурга</a>. Делаю удобные интерфейсы для людей.</p>-->
            <p><span class='main-color'>Иван Ковыляев.</span>Дизайнер дизайн-систем, интерфейсов, продуктов. Живу в Петербурге, работаю сразу в нескольких прекрасных командах.</p>
            <p><span class='main-color'><a class='link' href="https://xieffect.ru" target="blank">xieffect.ru</a></span> · Делаем лучшую образовательную платформу для репетиторов и малого бизнеса.</p>
            <p><span class='main-color'><a class='link' href="https://ekaterinburg.dev/" target="blank">Код Екатеринбурга</a></span> · Создаем цифровую экосистему города, отвечаю за транспорт.</p>
        </div>
    </div>
    <div class='row'>
        <div class='col-md-10 col-12 offset-md-1'>
            <p>Вы можете найти мои работы на <a class='link' href="https://behance.net/{{site.behance}}" target="blank">беханс</a>, <a class='link' href="https://dprofile.ru/{{site.dprofile}}" target="blank">дпрофайле</a> и <a class='link' href="https://figma.com/@{{site.figma}}" target="blank">фигме</a>.</p>
        </div>
    </div>
    <div class='row'>
        <div class='col-md-10 col-12 offset-md-1'>
            <p>Связаться со мной: <a class='link' href="mailto:{{site.email}}" target="blank">{{site.email}}</a> или <a class='link' href="https://t.me/{{site.telegram}}" target="blank">t.me/ikovylyaev</a>.</p>
        </div>
    </div>
    {% for post in site.design %}
    <div class='row'>
        <div class='col-12'>
            <div class='image' style="background: url({{site.url}}/img/works/{{ post.image }}.webp); background-size: {{ post.imgsize }}; background-position: center; background-repeat: no-repeat; background-color: {{ post.bgcolor}};"></div>
        </div>
        {% if post.link != "" %}
            <a  href="{{ post.link }}" target="blank" class='col-md-10 col-12 offset-md-1'>
        {% else%}
            <div class='col-md-10 col-12 offset-md-1'>
        {% endif %}
            <p>
                <span class='main-color'>{{ post.title}}</span> 
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
        <div class='row'>
            <div class='col'>2019-2023</div>
            <div class='col text-center'><a class='link' target='blank' href='mailto:{{ site.email }}'>{{ site.email}}</a></div>
            <div class='col text-center'><a class='link' target='blank' href='https://t.me/{{ site.telegram }}'>Телеграм</a></div>
            <div class='col text-center'><a class='link' target='blank' href='https://behance.net/{{ site.behance }}'>Беханс</a></div>
            <div class='col text-center'><a class='link' target='blank' href='https://dprofile.ru/{{ site.dprofile }}'>ДПрофайл</a></div>
            <div class='col text-end'><a class='link' target='blank' href='https://figma.com/@{{ site.figma }}'>Фигма</a></div>
        </div>
        <div class='row text-center'>
            <div class='col'><a class='link secondary-link' href='{{ site.url }}/policy'>Политика конфиденциальности</a></div>
        </div>
    </footer>
</div>
