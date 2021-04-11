<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

# Глава I

## Устойчивые паросочетания

### Алгоритм Гейла-Шепли

В начальном состоянии все $m \in M$ and $w \in W$ свободны \
Пока $\exists m \in M$ такой, что $m$ не успел сделать предложение каждой $w \in W$ \
&nbsp;&nbsp; Выбрать такого $m$ \
&nbsp;&nbsp; Выбрать $w \in W$ тукую, что её оценка в списке приоритетов $m$ максимальна среди тех $w \in W$, которым $m$ ещё не успел сделать предложение \
&nbsp;&nbsp; Сделать предложение выбранной $w$ \
&nbsp;&nbsp; Если $w$ свободна \
&nbsp;&nbsp;&nbsp;&nbsp; пара $(m, w)$ вступает в состояние помолвки \
&nbsp;&nbsp; Иначе $w$ в настоящее время помолвлена с $m'$ \
&nbsp;&nbsp;&nbsp;&nbsp; Если для $w$ $m'$ предпочтительнее $m$ \
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $m$ остаётся свободным \
&nbsp;&nbsp;&nbsp;&nbsp; Иначе \
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; пара $(m, w)$ вступает в состояние помолвки \
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; $m'$ становится свободным \
Вернуть множество $S$ помолвленных пар
