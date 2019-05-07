# intro

`SceneSetup.intro();`

# intro-play-button

[<div class="mini-icon" pic="play1"></div> ИГРАТЬ! <div class="mini-icon" pic="play2"></div>](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

# intro-start

(...500)

`clearText()`

n3: гы

`publish("show_options_bottom")`

# intro-start-2

`clearText()`

(...1000)

`publish("intro-to-game-2")`

n2: ЭТО ЧЕЛОВЕК

(...600)

`clearText()`

(...300)

`publish("intro-to-game-3")`

# act1

`SceneSetup.act1();`

(...300)

n: А ЭТО ТРЕВОГА ЧЕЛОВЕКА

n: _ВЫ_ И ЕСТЬ ТРЕВОГА

[Ешь обед один! Опять!](#act1a_alone)

[Ты не продуктивен, пока ешь!](#act1a_productive)

[Тебе вреден этот белый хлеб!](#act1a_bread)

# act1a_alone

`bb({mouth:"small", eyes:"narrow"})`

b: Ты разве не знаешь, что одиночество настолько же опасно преждевременной смертью, как и выкуривание 15 сигарет в день?-

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad et al, 2010, PLoS Medicine)

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: Эм, спасибо, что приводишь источники, но…

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: Это значит, что если ты ни с кем не затусишь *прямо сейчас*, то ты-

`bb({body:"panic"})`

b: УМРЁЁЁЁЁЁЁЁЁЁЁШШШШШШЬ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("20p", "alone");
publish("hp_show");
```

(...2500)
