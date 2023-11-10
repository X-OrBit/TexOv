![[template_latex]]
![[template_dsalakhov]]
_Благодарность выражается:
[@nol_erk](https://t.me/nol_erk)- за прорешанный листок, с которым можно было сверится :)_

# Подготовительный лист к КР-1
## Задача #1
Исследовать ряд на сходимость

$$
\Sum{n = 1}{\infty} \frac{(n + 1)!}{\pi \cdot (\pi + 1) \cdot \dotsc \cdot (\pi + n - 1) \cdot n}
$$

### Решение

$$
\displaylines{
	\frac{(n + 1)!}{\pi \cdot (\pi + 1) \cdot \dotsc \cdot (\pi + n - 1) \cdot n)} < \frac{(n + 1)!}{3 \cdot 4 \cdot \dotsc \cdot (n + 2) \cdot n} = \frac{2(n + 1)!}{(n + 2)!n} = \frac{2}{n(n + 2)} \sim \frac{1}{n^2} \RR \text{сходится}
}
$$

## Задача #2
Исследовать ряд на сходимость:

$$
\Sum{n=1}{\infty} \sqrt[n]{n + \frac{1}{n}} \cos \frac{3 + 2n}{3 + 2n + n^2}
$$

### Решение
$$
\displaylines{
	\Lim{n}{\infty} \frac{3 + 2n}{3 + 2n + n^2} = 0 \RR \Lim{n}{\infty} \cos \frac{3 + 2n}{3 + 2n + n^2} = 1\\
	\Lim{n}{\infty} \sqrt[n]{n + \frac{1}{n}} \ge \Lim{n}{\infty} \sqrt[n]{n} \ge 1 \RR \Lim{n}{\infty} \sqrt[n]{n + \frac{1}{n}} \cos \frac{3 + 2n}{3 + 2n + n^2} \ne 0 \RR \text{расходится}
}	
$$

## Задача #3
Исследовать ряд на сходимость:

$$
\Sum{n=1}{\infty} \l( \frac{(0.5 + 1)(0.5 + 2) \cdot \dotsc \cdot (0.5 + n)}{(1.5 + 1)(1.5 + 2) \cdot \dotsc \cdot (1.5 + n)} \r)^\alpha, \quad \alpha > 0
$$

%%PDF break%% <div style="page-break-after: always;"></div>
### Решение
$$
a_n = \l( \frac{1.5 \cdot \cancel{2.5} \cdot \dotsc \cdot \cancel{(0.5 + n)}}{\cancel{2.5} \cdot \cancel{3.5} \cdot \dotsc \cdot (1.5 + n)} \r)^\alpha = \l( \frac{1.5}{1.5 + n} \r)^\alpha \sim \frac{1}{n^\alpha} \text{ сходится при } \alpha > 1, \text{иначе расходится} 
$$

## Задача #4
Исследовать ряд на сходимость:

$$
\Sum{n=1}{\infty} \frac{\ln^6 n}{\sqrt{n}} \cos \frac{\pi n}{6}
$$

### Решение
$$
\displaylines{
	a_n = \cos \frac{\pi n}{6}, \quad b_n = \frac{\ln^6 n}{\sqrt{n}} \\
	\Sum{n=1}{N}a_n \le \frac{1}{|\sin \frac{\pi}{6}|} \quad \text{// внизу можно посмотреть как это доказывается} \\
	\Lim{n}{\infty} b_n = 0 \quad \text{//лог слабее степени} \\
	\l( \frac{\ln^6 x}{\sqrt{x}} \r)' = \frac{6 \ln^ 5 x \cdot \frac{1}{x} \cdot \sqrt{x} - \ln^6 x \cdot \frac{1}{2\sqrt{x}}}{x} = \frac{12 \ln^ 5 x - \ln^6 x}{2x^{3/2}} = 0 \RR 12 - \ln x = 0 \RR\\
	\RR x = e^{12}. \quad \text{В овербольших числах производная } \le 0 \RR\\
	\RR \Sum{n=1}{\infty} \frac{\ln^6 n}{\sqrt{n}} \cos \frac{\pi n}{6} = \underbrace{\Sum{n=1}{\ceil{e^{12}} - 1} \frac{\ln^6 n}{\sqrt{n}} \cos \frac{\pi n}{6}}_{const} + \underbrace{\Sum{\ceil{e^{12}}}{\infty} \frac{\ln^6 n}{\sqrt{n}} \cos \frac{\pi n}{6}}_{\text{сходится по Дирихле}} - \text{сходится}
}
$$

## Задача #5
Исследовать условную/абсолютную сходимость:

$$
\Sum{n=1}{\infty} (-1)^n \ln \frac{n + 4}{n + 3}
$$

### Решение

$$
\displaylines{
	a_n = (-1)^n \ln\frac{n + 4}{n + 3}, \quad c_n = |a_n| \\
	C_n = \Sum{k=1}{n} c_k = \ln \frac{\cancel{5}}{4} \cdot \frac{\cancel{6}}{\cancel{5}} \cdot \dotsc \cdot \frac{n + 4}{\cancel{n + 3}} = \ln \frac{n + 4}{4} \RR \Lim{n}{\infty} B_n = +\infty \RR \text{ряд не сходится абсолютно} \\
	b_n = \ln\frac{n + 4}{n + 3}, ~~ \Lim{n}{\infty} b_n = 0, ~~ \set{b_n} \text{ убывает} \RR \text{по признаку Лейбница исходный ряд сходится условно} \\
}
$$

## Задача #6
Исследовать на равномерную сходимость:

$$
f_n(x) = \frac{1 + \ln(nx)}{nx}, \quad a) D_1 = (0; 1), \quad b) D_2 = (1; +\infty)
$$

### Решение
При фиксированно $x$, $f_n(x)$ сходится к $0$. Иначе говоря, последовательность поточечно сходится к нулю. Это означает, что если последовательность сходится равномерно, то оно должно сходится равномерно к $0$:

a)
$$
x = \frac{1}{n} \RR f_n(x) = \frac{1 + \ln(1)}{1} \ne 0 \RR \Lim{n}{\infty} \Sup{D_1} |f_n(x) - f(x)| \ne 0 \RR \text{посл. равномерно не сходится}
$$
b) 
$$
\displaylines{
	|f_n(x) - f(x)| < \eps \RR |f_n(x)| < \eps \overset{f_n(x) \ge 0, x \in D_2}{\RR} \frac{1 + \ln(nx)}{nx} < \eps \\
	f'_n(x) =  \frac{\frac{n}{nx} \cdot nx - (1 + \ln(nx)) \cdot n} {n^2x^2} = \frac{-\ln(nx)}{nx^2} < 0 \text{ при всех } x \in D_2 \RR\\
	\RR
	\Sup{D_2} |f_n(x) - f(x)| = \frac{1 + \ln n}{n} \RR\\
	\RR \Lim{n}{\infty} \Sup{D_2} |f_n(x) - f(x)| = \Lim{n}{\infty} \frac{1 + \ln n}{n} = 0 \RR \text{ сходится равномерно}
}
$$

## Задача #7
Исследовать на равномерную сходимость:

$$
\Sum{n=1}{\infty} \frac{\cos(nx) \cdot \sin \frac{1}{nx}}{4 + \ln^2(nx)}, \quad D = [2; +\infty)
$$

### Решение
$$
\displaylines{
	f_n(x) = \frac{\cos(nx) \cdot \sin \frac{1}{nx}}{4 + \ln^2(nx)}, \quad |f_n(x)| = \frac{|\cos(nx)| \cdot |\sin \frac{1}{nx}|}{4 + \ln^2(nx)} \le \frac{1 \cdot (\frac{1}{nx} + o(\frac{1}{nx}))}{\ln^2(nx)} = \frac{1 + o(1)}{nx\ln^2(nx)} \sim\\
	\sim \frac{1}{nx \ln^2 (nx)} <_\star \frac{1}{n\ln^2 n} \text{ сходится (ряд Бертрана)}\\
	\star \quad  n \ge 2
}
$$

%%PDF break%% <div style="page-break-after: always;"></div>

# Чем пользоваться?

### Необходимое условие сходимости ряда
Если ряд $\Sum{n=1}{\infty} a_n$ сходится, то $\Lim{n}{\infty} a_n = 0$. Иначе говоря:
Если, $\Lim{n}{\infty} a_n \ne 0$, то ряд $\Sum{n=1}{\infty} a_n$ не сходится. Однако, если $\Lim{n}{\infty} a_n = 0$, то ряд $\Sum{n=1}{\infty} a_n$ может расходится, например: $\Sum{n=1}{\infty} \frac{1}{n}$.

### Критерии сходимости ряда
#### Критерий Коши

Ряд $\Sum{n=1}{\infty} a_n$ сходится тогда и только тогда, когда
$$
\forall \eps > 0 \quad \exists N \in \N \quad \forall n, m : n > m > N \quad \l| \Sum{k=m + 1}{n} a_k \r| < \eps
$$
#### Обратный критерий Коши
Ряд $\Sum{n=1}{\infty} a_n$ сходится тогда и только тогда, когда
$$
\exists \eps > 0 \quad \forall N \in \N \quad \exists n, m : n > m > N \quad \l| \Sum{k=m + 1}{n} a_k \r| \ge \eps
$$

### Сходимость произведений
(Абсолютной/Условной) cходимость произведения $\Prod{n=1}{\infty} a_n$, эквивалентна (абсолютной/условной) сходимостью $\Sum{n=1}{\infty} \ln a_n$

### Признаки сходимости <u>знакопостоянного</u> ряда
#### Первый признак сравнения
Пусть $a_n \ge b_n \ge 0 \quad \forall n \in \N$. Тогда
1. если сходится $\Sum{n=1}{\infty} a_n$, то сходится и $\Sum{n=1}{\infty} b_n$,
2. если расходится $\Sum{n=1}{\infty} b_n$, то расходится и $\Sum{n=1}{\infty} a_n$
#### Второй признак сравнения
$a_n, b_n > 0$ и $\exists \Lim{n}{\infty} \frac{a_n}{b_n} = c \ne 0$. Тогда $\Sum{n=1}{\infty} a_n \sim \Sum{n=1}{\infty} b_n$ эквивалентны по сходимости, то есть (ра-)сходятся одновременно.
#### Признак Вейерштрасса
Если $|a_n| \le b_n$ и ряд $\Sum{n=1}{\infty} b_n$ сходится, то ряд $\Sum{n=1}{\infty} a_n$ сходится.
#### Признак Коши
Если $a_n \ge 0$ и $\set{a_n}$ - монотонно невозрастающая последовательность, то
$$\Sum{n=1}{\infty} a_n \sim \Sum{n=0}{\infty} 2^n a_{2^n}$$
#### Интегральный признак Коши
Если $f: [1, +\infty) \to \R, \quad f(x) \ge 0$ и $f(x)$ монотонно невозрастает, то
$$\Sum{n=1}{\infty} f(n) \sim \inti{0}{\infty} f(x) dx$$
#### Радикальный признак Коши
Если $a_n \ge 0, \UpLim{n}{\infty} \sqrt[n]{a_n} = q$, то
1. если $q < 1$, то ряд $\Sum{n=1}{\infty} a_n$ сходится
2. если $q > 1$, то ряд  $\Sum{n=1}{\infty} a_n$ расходится
3. если $q = 1$, то ряд $\Sum{n=1}{\infty} a_n$ как сходится $\l( \Sum{n=1}{\infty} \frac{1}{n^2} \r)$, так и расходится $\l(\Sum{n=1}{\infty} 1\r)$ 
#### Признак Даламбера
Если $a_n > 0, d = \LowLim{n}{\infty} \frac{a_{n + 1}}{a_n}, \quad D = \UpLim{n}{\infty} \frac{a_{n+1}}{a_n}$, то
1. если $d > 1$, то ряд $\Sum{n=1}{\infty} a_n$ расходится
2. если $D < 1$, то ряд $\Sum{n=1}{\infty} a_n$ сходится
#### Признак Гаусса
Если $a_n > 0$ и $\exists \alpha \in \R, \delta > 0 : \frac{a_{n + 1}}{a_n} = 1 - \frac{\alpha}{n} + O\l( \frac{1}{n^{1 + \delta}} \r)$, то
$$\Sum{n=1}{\infty} a_n \sim \Sum{n=1}{\infty} \frac{1}{n^\alpha}$$

### Признаки сходимости <u>знакопеременного</u> ряда
#### Признак Дирихле
$$
\l. \begin{matrix}
	\exists M > 0 : \quad \forall n \in \N \quad \l| \Sum{k=1}{n} a_k \r| \le M \\
	\set{b_n} \text{ (нестрого) монотонна} \\
	\Lim{n}{\infty} b_n = 0
\end{matrix}\r\} \RR \Sum{n=1}{\infty} a_nb_n \text{ сходится}
$$
#### Признак Абеля
$$
\l. \begin{matrix}
	\Sum{n=1}{\infty} a_n \text{ сходится} \\
	\set{b_n} \text{ (нестрого) монотонна} \\
	\exists M > 0 : \quad \forall n \in \N \quad |b_n| \le M	
\end{matrix}\r\} \RR \Sum{n=1}{\infty} a_nb_n \text{ сходится}
$$
#### Признак Лейбница
$$
\l. \begin{matrix}
	b_n \ge 0, \quad \Lim{n}{\infty} b_n = 0 \\
	\set{b_n} \text{ (нестрого) монотонно убывает}
\end{matrix}\r\} \RR \Sum{n=1}{\infty} (-1)^{n+1}b_n \text{ сходится}
$$
_Причем оценка на остаток:_ $|r_n| \le b_{n + 1}$


### Перестановки членов ряда
#### Сходимость перестановки
Если $a_n \ge 0$ и ряд $\Sum{n=1}{\infty} a_n$ сходится, то ряд полученной из какой-то перестановки членов исходного ряда сходится и равен изначальному ряду:
$$
\Sum{n=1}{\infty} a_{\sigma(n)} = \Sum{n=1}{\infty} a_n, \quad \sigma : \N \to \N
$$
%%PDF break%% <div style="page-break-after: always;"></div>
#### Абсолютная сходимость перестановки
Если ряд $\Sum{n=1}{\infty} a_n$ сходится абсолютно, то ряд полученной из какой-то перестановки членов исходного ряда сходится абсолютно и равен изначальному ряду:
$$
\Sum{n=1}{\infty} a_{\sigma(n)} = \Sum{n=1}{\infty} a_n, \quad \sigma : \N \to \N
$$

#### Условная сходимость перестановки (конструктив)
По теореме Римана, тогда существуют следующие перестановки:
1. $\forall A \in \R \quad \sigma : \N \to \N$ - биекция: $\Sum{n=1}{\infty} a_{f(n)} = A$
2. $\exists \sigma : \N \to \N$ - биекция: $\Sum{n=1}{\infty} a_{\sigma(n)} = \pm \infty$
3. $\exists \sigma \N \to \N$ - биекция: последовательность частичных сумм ряда $\Sum{n=1}{\infty}$ не имеет ни конечного, ни бесконечного предела

### Произведения рядов
#### Произведение абсолютно сходящихся рядов
$\Sum{n=1}{\infty} a_n = A, \quad \Sum{n=1}{\infty} b_n = B$ и оба сходятся абсолютно $\RR \l( \Sum{k=1}{\infty}a_k \r)\l( \Sum{m=1}{\infty}b_m \r) = \Sum{n=1}{\infty} c_n = A \cdot B$
#### Теорема Мертенса
$\Sum{n=1}{\infty} a_n = A, \quad \Sum{n=1}{\infty} b_n = B$, оба сходятся и хотя бы один из них сходится абсолютно $\RR \l( \Sum{k=1}{\infty}a_k \r)\l( \Sum{m=1}{\infty}b_m \r) = \Sum{n=1}{\infty} c_n = A \cdot B$, где $c_n = a_1 b_n + \dotsc + a_n b_1$
#### Теорема Абеля
$\Sum{n=1}{\infty} a_n = A, \quad \Sum{n=1}{\infty} b_n = B, \quad \Sum{n=1}{\infty} c_n = C$, где $c_n = a_1 b_n + \dotsc + a_n b_1$
Тогда $C = AB$

%%PDF break%% <div style="page-break-after: always;"></div>
### Функциональная последовательность
#### Поточечная сходимость
$f_n \overset{D}{\to} f$ - поточечная сходимость функциональная последовательности $f_n(x)$ к функции $f(x)$:
$$
\forall X \in D \quad \forall \eps > 0 \quad \exists N = N(x, \eps) \quad \forall n > N \quad |f_n(x) - f(x)| < \eps
$$

#### Равномерная сходимость
$f_n \overset{D}{\toto} f$ - равномерная сходимость функциональная последовательности $f_n(x)$ к функции $f(x)$:
$$
\forall \eps > 0 \quad \exists N = N(\eps) \quad \forall n > N, \forall x \in D \quad |f_n(x) - f(x)| < \eps
$$
Отличие равномерной сходимости от поточечной, что существует $N$ для всех $x$ при конкретном $\eps$.
**Замечание:** $f_n \overset{D}{\toto} f \RR f_n \overset{D}{\to} f$
### Критерии равномерной сходимости
#### lim-sup критерий
$$
f_n \overset{D}{\toto} f \LR \Lim{n}{\infty} \underset{D}{\sup} |f_n(x) - f(x)| = 0
$$
#### Критерий коши
Пусть $f_n, f : D \to \R$. Тогда:
$$
f_n \overset{D}{\toto} f \LR \forall \eps > 0 \quad \exists N \quad \forall n, m > N, \forall x \in D \quad |f_n(x) - f_m(x)| < \eps 
$$

### Полезные штучки
#### Как ограничивать сумму (ко-)синусов
Ограничим сумму синусов (для косинусов аналогично)

Есть два варианта: один для русов, другой для ящеров:
1. $\Sum{k=1}{n} \sin \alpha k = \Im \Sum{k=0}{n} (e^{\alpha i})^k \le \l|\Sum{k=1}{n} (e^{\alpha i})^k\r| =$ \[геом прогрессия\] $= \l|\frac{e^{\alpha i}(1 - e^{\alpha n i})}{1 - e^{\alpha i}}\r| \le \frac{2}{1 - e^{\alpha i}}$
2. Воспользуемся тем, что $2\cos\frac{\alpha}{2} \cdot \sin\alpha k = \sin\l( \alpha k + \frac{\alpha}{2} \r) - \sin\l( \alpha k - \frac{\alpha}{2} \r)$. Тогда домножим $\Sum{k=1}{n} \sin \alpha k$ на $2\cos\frac{\alpha}{2}$ и получим: $\sin\l( \alpha n + \frac{\alpha}{2} \r) - \sin\frac{\alpha}{2}$
	$\Sum{k=1}{n} \sin \alpha k = \frac{\sin\l( \alpha n + \frac{\alpha}{2} \r) - \sin\frac{\alpha}{2}}{2\cos \frac{\alpha}{2}} \le \l|\frac{\sin\l( \alpha n + \frac{\alpha}{2} \r) - \sin\frac{\alpha}{2}}{\cos \frac{\alpha}{2}}\r|$, дальше, наверное, как-то и можно сократить, но зачем, если есть первый способ
	 
#### Формула Эйлера
$$
\Sum{k = 1}{n} \frac{1}{k} = \ln n + \gamma + o(1)
$$
#### Формула Стирлинга
$$
n! = \sqrt{2\pi n} \l( \cfrac{n}{e} \r)^n \exp \cfrac{\Theta_n}{12n}, \quad \exp x = e^x, \quad \Theta_n \in (0, 1), \quad n > 0
$$

#### Ряд Бертрана
$$
\Sum{n=2}{\infty} \frac{1}{n^\alpha \ln^\beta n}
$$
1. При $\alpha > 1$ ряд сходится
2. При $\alpha = 1$, $\beta \ge 2$ ряд сходится 
3. При $\alpha = 1$, $\beta < 2$ ряд расходится
4. При $\alpha < 1$ ряд расходится

#### Ряды Тейлора (снова...)
$$
\displaylines{
	e^x = 1 + x + \cfrac{x^2}{2!} + \cfrac{x^3}{3!} + o(x^3)\\
	\sin x = x - \cfrac{x^3}{3!} + \cfrac{x^5}{5!} + o(x^5) \\
	\cos x = 1 - \cfrac{x^2}{2!} + \cfrac{x^4}{4!} - \cfrac{x^6}{6!} + o(x^6) \\
	\ln(1 + x) = x - \cfrac{x^2}{2} + \cfrac{x^3}{3} - \cfrac{x^4}{4} + o(x^4) \\
	(1 + x)^\alpha = 1 + \alpha x + \cfrac{\alpha(\alpha - 1)}{2}x^2 + \cfrac{\alpha(\alpha - 1)(\alpha - 2)}{3!} x^3 + o(x^3)
}
$$

%%PDF break%% <div style="page-break-after: always;"></div>
#### Табличные производные
$$\begin{array}{|c|c|c|c|}
\hline
(c)^\prime = 0 &
(\sin x)^\prime = \cos x &
(\arcsin x)^\prime = \cfrac{1}{\sqrt{1 - x^2}} &
(U \pm V)^\prime = U^\prime \pm V^\prime

\\\hline
(x^n)^\prime = n\cdot x^{n - 1} &
(\cos x)^\prime = -\sin x &
(\arccos x)^\prime = -\cfrac{1}{\sqrt{1 - x^2}} &
(U \cdot V)^\prime = U^\prime \cdot V + U \cdot V^\prime
\\\hline

(a^x)^\prime = a^x \ln a \newline (e^x)^\prime = e^x &
(\tg x)^\prime = \cfrac{1}{\cos^2 x} &
(\arctg x)^\prime = \cfrac{1}{1 + x^2} &
\left(\cfrac{U}{V}\right)^\prime = \cfrac{U^\prime \cdot V - U \cdot V^\prime}{V^2}
\\\hline

(\log_a x)^\prime = \cfrac{1}{x}\log_a e \newline (\ln x)^\prime = \cfrac{1}{x} &
(\ctg x)^\prime = -\cfrac{1}{\sin^2 x} &
(\arcctg x)^\prime = -\cfrac{1}{1 + x^2} &
(f(g(x)))^\prime = f^\prime(g) \cdot g^\prime(x)

\\\hline
\end{array}$$

