# act1

`SceneSetup.act1();`

(...300)

n: А ЭТО — ТРЕВОГА ЧЕЛОВЕКА

n: _ВЫ_ И ЕСТЬ ТРЕВОГА

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: Как здорово, я *и не* надеялся нормально поесть сегодня.

`hong({eyes:"0_neutral"})`

n: ВАША ЗАДАЧА — УБЕРЕЧЬ ЧЕЛОВЕКА ОТ *ОПАСНОСТИ*

`bb({eyes:"look", mouth:"small_lock"})`

n: ЭТОТ СЕНДВИЧ ПРЕДСТАВЛЯЕТ ДЛЯ НЕГО *ОПАСНОСТЬ* ПРЯМО СЕЙЧАС

n: БЫСТРЕЕ, ПРЕДУПРЕДИТЕ ЧЕЛОВЕКА!

`bb({eyes:"normal", mouth:"normal"})`

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (ПУСТЬ _ВАША_ ТРЕВОГА ИГРАЕТ! ВЫБИРАЙТЕ, ЧТО МОГ БЫ ВАМ СКАЗАТЬ _ВАШ_ СТРАХ)

[Ешь обед один! Опять!](#act1a_alone)

[Ты не продуктивен, пока ешь!](#act1a_productive)

[Тебе вреден этот белый хлеб!](#act1a_bread)

# act1a_alone

`bb({mouth:"small", eyes:"narrow"})`

b: Ты разве не знаешь, что одиночество настолько же опасно преждевременной смертью, как и выкуривание 15 сигарет в день?

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad et al, 2010, PLoS Medicine)

`hong({eyes:"0_annoyed"})`

h: Эм, спасибо, что приводишь источники, но…-

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: Это значит, что если ты ни с кем не затусишь *прямо сейчас*, то ты…

`bb({body:"panic"})`

b: УМРЁЁЁЁЁЁЁЁЁЁЁШШШШШШЬ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("20p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: ВЫ ИСПОЛЬЗОВАЛИ *СТРАХ ОДИНОЧЕСТВА*

(#act1b)

# act1a_productive

b: Доставай лаптоп и давай работай сейчас же!

`hong({eyes:"0_annoyed"})`

h: Эм, я боюсь, крошки попадут в клавиа…

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Если ты не продуктивен, то ты станешь нищебродом, а твои родители скажут:

`bb({mouth:"small", eyes:"narrow"})`

b: «Ты обесчестил нашу семью, теперь мы все должны сделать сеппуку»

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: а потом ты…

`bb({body:"panic"})`

b: УМРЁЁЁЁЁЁЁЁЁЁЁШШШШШШЬ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("20p", "bad");
publish("hp_show");
```

(...2500)

`_.seppuku = true`

n: ВЫ ИСПОЛЬЗОВАЛИ *СТРАХ БЫТЬ ПЛОХИМ*

(#act1b)

# act1a_bread

`hong({eyes:"0_annoyed"})`

h: Разве эти исследования были подтвержде…

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: От очищенной пшеницы у тебя в крови резко повысится уровень глюкозы, тебе придется ампутировать все конечности, а потом ты…

`bb({body:"panic"})`

b: УМРЁЁЁЁЁЁЁЁЁЁЁШШШШШШЬ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("20p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: ВЫ ИСПОЛЬЗОВАЛИ *СТРАХ УГРОЗЫ ЗДОРОВЬЮ*

(#act1b)

# act1b

n: СУПЕРЭФФЕКТИВНО

`bb({mouth:"smile", eyes:"smile"});`

b: Я лучший уберегатель!

n: НО ВАШЕГО ЧЕЛОВЕКА ЕЩЕ СПАСАТЬ И СПАСАТЬ

n: ПРИВЕДИТЕ УРОВЕНЬ ЕГО ЭНЕРГИИ К НУЛЮ

n: ЧТОБЫ УБЕРЕЧЬ ФИЗИЧЕСКИЕ + СОЦИАЛЬНЫЕ + МОРАЛЬНЫЕ НУЖДЫ ЧЕЛОВЕКА, МОЖНО ИСПОЛЬЗОВАТЬ:

n: СТРАХ *УГРОЗЫ ЗДОРОВЬЮ* #harm#

n: СТРАХ *ОДИНОЧЕСТВА* #alone#

n: И СТРАХ *БЫТЬ ПЛОХИМ* #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (PRO-TIP: ВЫБИРАЙТЕ, ЧТО ЗАДЕВАЕТ ЛИЧНО ВАШИ САМЫЕ ГЛУБОКИЕ И ТЕМНЫЕ СТРАХИ)

h: ...

```
hong({body:"putaway"});
sfx("rustle");
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: Ладно, пора проверить телефон.

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: УБЕРЕГИТЕ СВОЕГО ЧЕЛОВЕКА

n: ОТ МИРА. ОТ ДРУГИХ ЛЮДЕЙ. ОТ НЕГО САМОГО.

n: УДАЧИ

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: ROUND ONE: *FIGHT!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: Хм. В ленте Фейсбука пишут, что на выходных будет вечеринка.

`bb({eyes:"uncertain"});`

b: Разве этот чудак не устраивает вечеринки *каждые* выходные?

`bb({eyes:"uncertain_right"});`

b: Похоже на какой‐то невроз.

`hong({eyes:"surprise"});`

h: О, меня пригласили?

`bb({eyes:"narrow", mouth:"normal"});`

b: Так!

[Скажи да, или ты умрешь от одиночества](#act1c_loner)

[Скажи нет, там походу куча смертельной наркоты](#act1c_drugs)

[Игнорь, ты и так портишь вечеринки](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: Пятнадцать сигарет в день, человек. Пятнадцать.
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: Никто не придет на твои похороны, твой прах развеют над океаном и ты превратишься в КИТОВЫЕ КАКАШКИ.
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: Так что да, тебе обязательно надо идти на вечеринку.
{{/if}}

{{if _.seppuku}}
b: Только лаптоп захвати, чтоб работу делать.
{{/if}}

{{if _.whitebread}}
b: Главное, чтоб там не подавали БЕЛЫЙ ХЛЕБ
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: Господи! Лишь бы ты заткнулся, окей.

h: Я скажу да.

{{if _.whalepoop}}
b: Китовые какашки, человек. Китовые какашки.
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: или хуже... БЕЛЫЙ ХЛЕБ
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: У тебя случится передозировка от метамфетаминов и белого хлеба, твой жирный труп не смогут засунуть в крематорий!
{{/if}}

{{if !_.whitebread}}
b: У тебя случится передозировка от такого дикого количества наркоты, что гробовщик удивится, почему твое тело *уже заранее* забальзамировано!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "harm");
```

(...2500)

{{if _.seppuku}}
b: Да и вообще, нельзя расслабляться: тебе надо работать, а то родители сделают сеппуку.
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: Господи! Лишь бы ты заткнулся, окей.

h: Я скажу нет.

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: Всё, что ты делаешь, это плачешься в жилетку о том, как одиночество по смертности равносильно 15 сигаретам в день.
{{/if}}

{{if _.seppuku}}
b: Всё, что ты делаешь на вечеринках, это печешься о том, что тебе нужно вместо вечеринки работать.
{{/if}}

{{if _.whitebread}}
b: Всё, что ты делаешь, это печешься о том, что вокруг сплошь нездоровая пища и она тебя убьет.
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: Мда, интересно почему.

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: Если ты пойдешь, то испортишь им настроение, но если ты откажешься — тоже испортишь им настроение!

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: ТЫ ТОЛЬКО И ДЕЛАЕШЬ, ЧТО ПОРТИШЬ ЛЮДЯМ НАСТРОЕНИЕ, ТЫ ПЛОХОЙ

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: Уф. Лишь бы ты заткнулся, окей.

h: Я проигнорю приглашение.

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: Ладно. Хватит с меня Фейсбука. Нужно что-то поспокойнее, менее тревожное.

`hong({eyes:"neutral"});`

h: Что там в Твиттере?

`bb({eyes:"look"});`

[О нет, посмотри на эту ужасную новость!](#act1d_news)

[О нет, кажется этот твит на самом деле о *тебе?*](#act1d_subtweet)

[О, гифка кота, пьющего молоко](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: Боже, такое ощущение, что мир катится в тартарары, да?

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: Как будто всё скоро погибнет, мы все обречены и ничего не можем сделать.

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: Давай ретвитнем эту новость!

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"uncertain"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Хорошо, я ее ретвитну, только помолчи, пожалуйста!

`hong({mouth:"neutral", eyes:"annoyed"});`

h: Пошло оно, позырим, что в Снапчате.

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: Это сабтвит! Подлый, подлый сабтвит!

`hong({eyes:"annoyed"});`

h: А может нет?

`bb({eyes:"narrow", mouth:"small"});`

b: Что если все уже болтают всякое за твоей спиной

h: Никто не...

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: ПРЯМО ПЕРЕД ТВОЕЙ СПИНОЙ

`hong({eyes:"sad", mouth:"sad"});`

h: Я не...

`bb({eyes:"narrow", mouth:"small"});`

b: но *что если*

h: С...

`bb({eyes:"narrow_eyebrow"});`

b: *что если*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"uncertain"});
```

h: ЛАДЫ, посмотрю Снэпчат.

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: Ха, очень мило, только что ретвитнул, я дума...

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream_anger"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: КОШКИ НЕ ПЕРЕВАРИВАЮТ МОЛОКО, ТЫ УЖАСНЫЙ ЧЕЛОВЕК, РАЗ НАСЛАЖДАЕШЬСЯ ЖЕСТОКИМ ОБРАЩЕНИЕМ С ЖИВОТНЫМИ

```
bb({body:"normal", mouth:"normal", eyes:"narrow"});
attack("10p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"uncertain"});
```

h: ЛАДЫ, посмотрю Снэпчат.

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: Хм, фотографии со вчерашнего вечера. Так *вот как* выглядят эти еженедельные вечеринки.

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: Ох, слишком людно для моей тревожности.

h: Может, мне не надо было отвечать да на приглашение?

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[Меняешь ответ? Ты ненадежная сволочь!](#act1e_yes_dontchange)

[Меняй ответ! Слишком людно!](#act1e_yes_changetono)

{{if _.subtweet}}
[да, они точно писали о тебе подлые сабтвиты](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[постой, ты ретвитнул историю и даже не проверил факты](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Ты знаешь, что у тебя очень кривая осанка?](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Они рассчитывали, что ты придешь, а теперь ты подрываешь их доверие? Ты хочешь помереть в одиночестве?

{{if _.fifteencigs}}
b: ПЯТНАДЦАТЬ. СИГАРЕТ.
{{/if}}

{{if _.whalepoop}}
b: КИТОВЫЕ. КАКАШКИ.
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я оставлю ответ да!

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Ты разве не знаешь о давках?

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: В 2003 году в ночном клубе в штате Род-Айленд случился пожар, люди в панике устроили давку на выходе, из-за чего 100 людей сгорело заживо.

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: ТЫ ХОЧЕШЬ, ЧТОБЫ ТО ЖЕ САМОЕ СЛУЧИЛОСЬ С ТОБОЙ?

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: ОТВЕЧАЙ НЕТ ОТВЕЧАЙ НЕТ ОТВЕЧАЙ НЕТ ОТВЕЧАЙ НЕТ ОТВЕЧАЙ НЕТ ОТВЕЧАЙ НЕТ ОТВЕЧАЙ Н...


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("10p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я поменяю ответ на нет! Боже!

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: Хм... выглядит весело.

h: Может, мне не следовало отвечать нет на приглашение?

`bb({mouth:"normal", eyes:"normal"});`

[Меняешь ответ? Ты ненадежная сволочь!](#act1e_no_dontchange)

[Меняй ответ! Не помирай в одиночестве!](#act1e_no_changetoyes)

{{if _.subtweet}}
[да, они точно писали о тебе подлые сабтвиты](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[wait you retweeted that story without fact-checking](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Ты знаешь, что у тебя очень кривая осанка?](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: Все на тебя рассчитывали! ...что ты не придешь и все нормально повеселятся без тебя, ты ужасное мерзкое {{if _.whitebread}}пожирающее белый хлеб{{/if}} чудови...


```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я оставлю ответ нет!

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Хроническое одиночество увеличивает уровень кортизола, а также риск кардиоваскулярных заболеваний и инсульта!

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: ПЯТНАДЦАТЬ. СИГАРЕТ.
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я поменяю ответ на да! Боже!

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Все твои проблемные твиты тебе аукнулись!

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: Хоть *раз* скажешь что-то нето и все так называемые друзья польют тебя грязью за интернет-очки!

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Почему ты такая?!

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Ты распространяешь дезинформацию!

```
bb({body:"scream_anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Из-за таких как ты фашизм снова поднимет свою уродливую голову из руин демократии!

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("10p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Почему ты такая?!

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: У тебя вместо позвоночника будет крендель! Прекращай горбиться над экраном!

```
bb({body:"meta"});
```

b: И ты тоже.

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("10p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Почему ты такая?!

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: Хм... выглядит весело.

h: Может, мне не надо было игнорить приглашение?

`bb({mouth:"normal", eyes:"normal"});`

[Игнорь, ты все вечеринки портишь](#act1e_ignore_continue)

[Знаешь, скажи да.](#act1e_ignore_changetoyes)

[Знаешь, скажи нет.](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: Но ведь игнорить невежливо?

`bb({eyes:"normal_right"});`

b: Ну, остальные же игнорят *тебя*, так что...

```
hong({mouth:"shock", eyes:"shock"});
attack("10p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: так что квиты.

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: Ты... даешь мне пойти потусить?

b: Ну, просто, одиночество *реально* может убить.

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: Слишком людно. Толпы опасны.

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: Whatever. New Tinder notification.

`bb({eyes:"uncertain"})`

b: What, that hookup app?

`hong({eyes:"annoyed"})`

h: It's not a hookup app, it's just a way to meet new peopl--

`bb({eyes:"narrow"})`

b: It's a hookup app.

`hong({eyes:"surprise", mouth:"smile"})`

h: Oh, I got a match! They look cute!

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: Please don't ruin this for m--

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: DANGER DANGER DANGER DANGER DANGER DANGER

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[You're being *used* by other people.](#act1f_used_by_others)

[You're just *using* other people.](#act1f_using_others)

[YOUR MATCH IS A SERIAL KILLER](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: Random hookups may be able to fill the hole down there

b: but they can never fill the hole

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: in *here*.

(...3000)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Point is you're gonna die alone

```
hong({mouth:"shock", eyes:"shock"});
attack("30p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: You think other people's genitals are Pokémon for you to collect?

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (pokemon theme song)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ I wanna be, the slutti-est-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ Like no one ever was-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ Thighs n' ass, voluptuous breast-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ with sweaty dick and balls!-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ PERVY-MON! GOTTA CA-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Point is you're a manipulative creep

```
hong({mouth:"shock", eyes:"shock"});
attack("30p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: They'll trap you in a well and force-feed you white bread to fatten you up so they can wear your skin like a suit!
{{/if}}

{{if _.seppuku}}
b: They'll bludgeon you with a pomodoro timer and slice your belly open and say "this is what slackers get, SEPUKKU'D"
{{/if}}

{{if !_.whitebread && !_.seppuku}}
b: They'll tear your flesh to gory confetti, turn your entrails into streamers, and mix your blood into a punch bowl!
{{/if}}

{{if !_.whitebread && !_.seppuku}}
b: How's THAT for a party invite?!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("30p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: i'm so sick of this game.

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"loneliness will kill you"... {{/if}}
{{if _.seppuku}}"be productive or you'll be dishonored"... {{/if}}
{{if _.whitebread}}"don't eat that, it'll kill you"... {{/if}}
{{if _.subtweet}}"they're talking behind your back"... {{/if}}
{{if _.badnews}}"the world is burning"... {{/if}}
{{if _.hookuphole}}"you'll die alone"... {{/if}}
{{if _.serialkiller}}"they're a serial killer"... {{/if}}
{{if _.catmilk}}"cats can't digest milk"... {{/if}}
{{if _.pokemon}}a crappy parody song... {{/if}}

h: i just want to live my life.

h: i just want to be free from all this... pain.

`bb({eyes:"look_sad"});`

b: Hey... human...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: It'll be okay.

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: As your loyal protector, I'll always keep an eye out for danger, and do my best to keep you safe.

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: I promise.

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: Last app. Instagram. What you got?

`hong({eyes:"sad"});`

h: It's... more party pictures.

`hong({mouth:"sad"});`

h: Everyone looks so happy. Free from worry. Free from anxiety.

`hong({mouth:"anger"});`

h: God, why can't I be like them? Why can't I just be *normal?*

`bb({eyes:"normal_right"});`

b: Speaking of parties, about this weekend's invite. Here's my FINAL decision:

`bb({eyes:"normal"});`

[You should go.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[You should not go.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: You sh--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *FUCK.*

`hong({body:"2_you"});`

h: YOU.

(...500)

b: w

(...1500)

`bb({eyes:"wat_2"});`

b: wha?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: I'm going to say YES to that party

{{if _.act1g=="go"}}
h: NOT because you want me to, but because *I* want to.
{{/if}}

{{if _.act1g=="dont"}}
h: Precisely BECAUSE you don't want me to.
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: You're NOT in control of me.

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: Now excuse me while I eat this delicious sandwich in goddamn peace.

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[AHHHHH WE'RE GONNA DIE](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHHH EVERYONE HATES US](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHHH WE'RE HORRIBLE PEOPLE](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHHH WE'RE GONNA DIE AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHHH EVERYONE HATES US AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHHH WE'RE HORRIBLE PEOPLE AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: CONGRATULATIONS

(...500)

n: YOU'VE SUCCESSFULLY PROTECTED YOUR HUMAN'S NEEDS FOR SAFETY, LOVE, AND GOODNESS

n: WHY, LOOK HOW GRATEFUL THEY ARE!

(...500)

n: NOW THAT THEIR ENERGY IS ZERO, YOU CAN DIRECTLY CONTROL THEIR ACTIONS

`bb({mouth:"smile", eyes:"normal"});`

n: PICK YOUR ENDING MOVE

`bb({mouth:"normal", eyes:"narrow"});`

n: *FINISH THEM*

[{FIGHT: Punish your stressful phone!}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{FLIGHT: Curl up in a ball and cry!}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({eyes:"anger", mouth:"normal"})`

b: Your phone was giving you a panic attack!

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Punish it! Destroy your phone! Kill it!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL I--

(#act1j)

# act1i_cry

`bb({eyes:"fear"})`

b: The whole world is filled with danger!

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Do like the armadillo! Curl up into a ball for self-defense!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CR-- 

(#act1j)

# act1j

`SceneSetup.act1_outro()`