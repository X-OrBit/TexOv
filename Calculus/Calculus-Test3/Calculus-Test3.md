![[template]]
_Благодарность выражается:
[@Another\_option](https://t,me/Another\_option) - за дополнительный материал в конспекте
[@adeliagaraeva](https://t.me/adeliagaraeva) - за найденный баг в решении 7+.4а
[@mishasvintus](https://t.me/mishasvintus) - за найденный баг в решении 7.4а
Колесниченко Елене Юрьевне за прекрасные семинары_

# Материал к к/р в 3 модуле. Матанализ

## Табличные производные
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

(a^x)^\prime = a^x \ln a \newline \text{частный случай } (e^x)^\prime = e^x &
(\tg x)^\prime = \cfrac{1}{\cos^2 x} &
(\arctg x)^\prime = \cfrac{1}{1 + x^2} &
\left(\cfrac{U}{V}\right)^\prime = \cfrac{U^\prime \cdot V - U \cdot V^\prime}{V^2}
\\\hline

(\log_a x)^\prime = \cfrac{1}{x}\log_a e \newline \text{частный случай } (\ln x)^\prime = \cfrac{1}{x} &
(\ctg x)^\prime = -\cfrac{1}{\sin^2 x} &
(\arcctg x)^\prime = -\cfrac{1}{1 + x^2} &
(f(g(x)))^\prime = f^\prime(g) \cdot g^\prime(x)

\\\hline
\end{array}$$

$$
\begin{array}{ccc}
\cfrac{dt}{dx} = t^\prime &
dx = \cfrac{dt}{t^\prime} &
dt = t^\prime dx
\end{array}
$$

#### Правило Лопиталя
Если: $f(x),g(x)$ — действительнозначные функции, дифференцируемые в проколотой окрестности $U$ точки $a$, где $a$ — действительное число или один из символов $+\infty,-\infty,\infty$, причём
1. $\Lim{x}{a} f(x) = \Lim{x}{a} g(x) = 0$ или $\infty$;
2. $g^\prime(x) \ne 0$ в $U$;
3. существует $\Lim{x}{a} \cfrac{f^\prime(x)}{g^\prime(x)}$
Тогда $\Lim{x}{a} \cfrac{f(x)}{g(x)} = \Lim{x}{a} \cfrac{f^\prime(x)}{g^\prime(x)}$
_Пределы также могут быть односторонними_

##### Пример
$$
\Lim{x}{0} \cfrac{\sin x}{x} = \Lim{x}{0} \cfrac{(\sin x)^\prime}{x^\prime} = \Lim{x}{0} \cfrac{\cos x}{1} = \Lim{x}{0} \cos x = \cos 0 = 1
$$
%%PDF break%% <div style="page-break-after: always;"></div>

## Табличные интегралы
$$\begin{array}{|c|c|c|}
\hline

\bint x^a dx = \cfrac{x^{a + 1}}{a + 1} + c, a \ne -1 &
\bint \cfrac{dx}{x} = \ln |x| + c &
\bint e^x dx = e^x + c
\\\hline

\bint \sin x dx = -\cos x + c &
\bint \cos x dx = \sin x + c &
\bint \cfrac{dx}{\cos^2 x} = \tg x + c
\\\hline

\bint \cfrac{dx}{\sin^2 x} = -\ctg x + c &
\bint \cfrac{dx}{1 + x^2} = \arctg x + c &
\bint \cfrac{dx}{\sqrt{1 - x^2}} = \arcsin x + c
\\\hline

\bint \cfrac{dx}{\sqrt{1 + x^2}} = \ln (x + \sqrt{1 + x^2}) + c
\\\hline
\end{array}$$

$$
\displaylines{
\int f(x) dx = F(x) + c \cr
\int f(ax) dx = \cfrac{1}{a} F(ax) + c \cr
\int f(ax + b) dx = \cfrac{1}{a} F(ax + b) + c
}
$$

## Неопределенный интеграл

### Техники интегрирования
#### Замена переменной
$$\int f(\phi(t)) \cdot \phi^\prime(t) dt = \int f(x) dx, \quad x = \phi (t)$$

##### Универсальная тригонометрическая замена
$$
\displaylines{
	\int \cfrac{\text{многочлен}(\sin x, \cos x)}{\text{многочлен}(\sin x, \cos x)} dx \\
	\text{Замена} \quad \begin{array}{|c|}
		\hline \tg \cfrac{x}{2} = t
		\\\hline
	\end{array}\\
	\sin x = \cfrac{2t}{1 + t^2} \quad 
	\cos x = \cfrac{1 - t^2}{1 + t^2} \quad 
	dx = \cfrac{2dt}{1 + t^2}
}
$$

##### Другие тригонометрические замены
Если подынтегральная функция обладает одним из свойств:
1) $R(-\sin x; \cos x) = -R(\sin x; \cos x);$
2) $R(\sin x; -\cos x) = -R(\sin x; \cos x);$
3) $R(-\sin x; -\cos x) = R(\sin x; \cos x);$

то для вычисления интеграла удобнее использовать соответственно подстановки:
1) $t = \cos x, \quad x \in (-\pi/2; \pi/2)$;
2) $t = \sin x, \quad x \in (0; \pi)$;
3)  $t = \tg x, \quad x \in (-\pi/2; \pi/2)$;

#### Интегрирование по частям
$$
\displaylines{
	\int u v^\prime dx = uv - \int u^\prime v dx \\
	\int u dv = uv - \int v du \\	
}
$$

### Интегрирование рациональных функций
Если нам нужно найти интеграл от рациональной функции вида $\cfrac{P(x)}{Q(x)}$, действует по следующей схеме:
1. $\deg P \ge \deg Q \RR$ выделить целую часть
2. $Q(x)$ раскладывается на множители
	1. $\cfrac{P(x)}{(x - a_1) \cdots (x - a_n)}$  все корни различны и действительны 
		$= \cfrac{A_1}{x - a_1} + \dotsc + \cfrac{A_n}{x - a_n}$, находим $A_1, \dotsc, A_n$
	2. Все корни действительны, но есть кратные
		$\cfrac{P(x)}{(x - a_1)^{\alpha_1} \cdots (x - a_n)^{\alpha_n}} = \cfrac{A_{11}}{x - a_1} + \dotsc + \cfrac{A_{1 \alpha_1}}{(x - a_1)^{\alpha_1}} + \dotsc + \cfrac{A_{n1}}{x - a_n} + \dotsc + \cfrac{A_{n \alpha_1}}{(x - a_n)^{\alpha_n}}$
	3. Есть комплексные корни, не кратные
		$\cfrac{P(x)}{(x^2 + px + q)(x^2 + ax + b)}, \quad (D^\star < 0) \quad = \cfrac{Ax + B}{x^2 + px + q} + \cfrac{Cx + D}{x^2 + ax + b} + \dotsc$
	4. Есть комплексные корни, кратные
		$\cfrac{P}{Q} = \cfrac{P}{(x^2 + px + q)^n \cdot \dotsc} = \cfrac{A_1x + B_1}{x^2 + px + q} + \cfrac{A_2x + B_2}{(x^2 + px + q)^2} + \dotsc + \cfrac{A_nx + B_n}{(x^2 + px + q)^n} + \dotsc$
$\star - \text{тут имеется в виду дискриминант от многочлена}$

#### Метод Остоградского
Пусть $\deg P < \deg Q$. Тогда:
$$\int \cfrac{P(x)}{Q(x)} dx =\cfrac{P_1(x)}{Q_1(x)} + \int \cfrac{P_2(x)}{Q_2(x)} dx$$
где $Q_2(x)$ имеет те же корни, что и многочлен $Q(x)$, но однократно,
$Q_1(x)= Q(x)/Q_2(x)$, а $P_1(x)$ и $P_2(x)$ находятся методом неопределенных коэффициентов после дифференцирования формулы, с учетом $\deg P_1 < \deg Q_1(x), ~\deg P_2(x) < \deg Q_2(x)$.

_Метод Остоградского удобно использовать, если знаменатель $Q(x)$ имеет кратные корни._

%%PDF break%% <div style="page-break-after: always;"></div>

### Рекурентные интегралы
$$
\displaylines{
	I_n = \int \sin^n x dx = \cfrac{n - 1}{n}I_{n - 2} - \cfrac{1}{n} \cos x (\sin x)^{n - 1} \\
	I_0 = x + c, \quad I_1 = -\cos x + c
}
$$

#### Рекурентный определенный интеграл
$$
\displaylines{
	I_n = \inti{0}{\pi/2} \sin^n x dx = \cfrac{n - 1}{n} \cdot I_{n - 2} \\
	I_0 = \cfrac{\pi}{2}, \quad I_1 = 1 \\
	n \equiv_2 0 : I_n = \cfrac{n - 1}{n} \cdot \cfrac{n - 3}{n - 2} \cdot \dotsc \cdot \cfrac{1}{2} \cdot I_0 = \cfrac{(n - 1)!!}{n!!} \cdot \cfrac{\pi}{2} \\
	
	n \equiv_2 1 : I_n = \cfrac{n - 1}{n} \cdot \cfrac{n - 3}{n - 2} \cdot \dotsc \cdot \cfrac{2}{3} \cdot I_1 = \cfrac{(n - 1)!!}{n!!}
}
$$

### Определенный интеграл
$$
\displaylines{
\int_a^b f(x) dx = \lim_{\lambda(T) \to 0} \sum_{k = 1}^n f(\xi_k) \cdot |\Delta_k|\\
\xi_k \in \Delta_k, \quad \Delta_k = [x_{k - 1}, x_k], \quad a = x_0 < x_1 < \dotsc < x_n = b, \quad \lambda(T) = \max_{k} |\Delta_k|
}
$$
##### Пример
$$
\displaylines{
	\lim_{n \to \infty} \left( \cfrac{1}{n + 1} + \cfrac{1}{n + 2} + \dotsc + \cfrac{1}{3n} \right) = \lim_{n \to \infty} \sum_{k = 1}^{2n} \cfrac{1}{n + k} = \lim_{n \to \infty} \sum_{k = 1}^{2n} \cfrac{1}{1 + \frac{k}{n}} \cdot \underbrace{\cfrac{1}{n}}_{\Delta_k} \fbox{=}\\
	
	f(x) = \cfrac{1}{1 + x}, \quad \xi_k = \cfrac{k}{n}, \quad x \in [0, 2]\\
	
	\fbox{=} \int_0^2 \cfrac{1}{1 + x} dx = \fint{\ln|1 + x|}{0}{2} = \ln|1 + 2| - \ln|1 + 0| = \ln 3
}
$$
_P.s. Использовалась теорема, что непрерывная функция интегрируема_

#### Формула Ньютона - Лейбница
$$
\displaylines{
\int_a^b f(x) dx = F(b) - F(a) = \fint{F(x)}{a}{b}\\
F - \text{любая первообразная для $f$}
}
$$

%%PDF break%% <div style="page-break-after: always;"></div>

#### Интегрирование по частям
$$\inti{a}{b} f(x)g^\prime(x)dx = \fint{f(x)g(x)}{a}{b} - \inti{a}{b}f^\prime(x)g(x) dx$$

## Несобственный интеграл

$$
\displaylines{
	\inti{a}{+\infty}f(x)dx = \lim_{A \to +\infty} \inti{a}{A} f(x) dx\\
	\text{Проблема в $b$ } - \inti{a}{b}f(x)dx = \lim_{A \to b-} \inti{a}{A} f(x) dx\\
}
$$

#### Выделение проблемных точек
$$
\displaylines{
	\inti{a}{b} f(x) dx = \inti{a}{c_1} + \inti{c_1}{\alpha} + \inti{\alpha}{c_2} + \inti{c_2}{b} \\
	c_1, c_2, \dotsc, c_n - \text{проблемные точки} \\
	\text{В интеграле проблема должна быть одна и с краю!}
}
$$

### Производная от интеграла
$$
\displaylines{
	\cfrac{d}{dx} \inti{0}{\phi(x)} f(t) dt = f(\phi(x)) \cdot \phi^\prime(x) \\
	\cfrac{d}{dx} \inti{a(x)}{b(x)} f(t) dt = f(b(x)) b^\prime(x) - f(a(x)) a^\prime(x)
}
$$

##### Пример 1
$$
\displaylines{
	\lim_{x \to +\infty} \cfrac{\inti{0}{x} (\arctg u)^2 du}{\sqrt{x^2 + 1}} =_\star \left[ \cfrac{\infty}{\infty} \right] \fbox{=} \\
	
	=_\star \inti{0}{x} (\arctg u)^2 du \ge \inti{\pi/4}{x} (\arctg u)^2 du \ge \inti{\pi/4}{x} 1 du = x - \cfrac{\pi}{4} \to +\infty \\
	\text{По Лопиталю:} \quad 
	\fbox{=} \lim_{x \to +\infty} \cfrac{(\arctg x)^2}{\frac{1}{2\sqrt{x^2 + 1}} \cdot 2x} = \lim_{x \to +\infty} \cfrac{(\arctg x)^2}{\frac{x}{\sqrt{x^2 + 1}}} = \cfrac{(\pi/2)^2}{1} = \cfrac{\pi^2}{4} 
}
$$

%%PDF break%% <div style="page-break-after: always;"></div>

##### Пример 2
$$
\cfrac{d}{dx} \inti{0}{x^2} \sqrt{1 + t^2} dt = \underbrace{\sqrt{1 + (x^2)^2}}_{f(x^2)} \cdot \underbrace{2x}_{(x^2)^\prime} = 2x\sqrt{1 + x^4}
$$

### Сходимость несобственных интегралов
- Интеграл $\inti{1}{\infty} \cfrac{dx}{x^\alpha}$ сходится при $\alpha > 1$ и расходится при $\alpha \le 1$
- Интеграл $\inti{0}{1} \cfrac{dx}{x^\alpha}$ сходится при $\alpha < 1$ и расходится при $\alpha \ge 1$

### Признаки сравнения
1. Пусть $f(x) \ge g(x) \ge 0$, тогда справедливо следующее
	1. $\inti{a}{+\infty} f(x) dx$ сходится $\RR \inti{a}{+\infty} g(x)dx$ сходится
	2. $\inti{a}{+\infty} g(x) dx$ расходится $\RR \inti{a}{+\infty} f(x)dx$ расходится
2. $f \sim g \quad (f \ge 0)$ 
	$\inti{a}{+\infty} f(x) dx \LR \inti{a}{+\infty} g(x) dx$ оба сходятся/расходятся

### Критерий Коши (для сходимости и расходимости)
$$\inti{0}{\infty} f(x) dx \text{ сходится } \LR \forall \eps > 0 \quad \exists A \quad \forall A_1, A_2 > A \quad \underbrace{\left| \inti{A_1}{A_2} f(x) dx \right|}_{\text{кусок хвоста интеграла}} < \eps$$
$$\inti{0}{\infty} f(x) dx \text{ расходится } \LR \exists \eps > 0 \quad \forall A \quad \exists A_1, A_2 > A \quad \underbrace{\left| \inti{A_1}{A_2} f(x) dx \right|}_{\text{кусок хвоста интеграла}} \ge  \eps$$

%%PDF break%% <div style="page-break-after: always;"></div>

### Признак Дирихле (для сходимости)
1. $\l| \inti{a}{A} f(x) dx \r| \le M$ - не зависит от $A$
2. $g$ - монотонная 
3. $x \to +\infty \RR g \to 0$
Тогда $\inti{a}{\infty} f(x) g(x) dx$ сходится

##### Пример
$$
\displaylines{
	\inti{1}{+\infty} \cfrac{\cos x}{x} dx \\
	f = \cos x - \text{ограничена}, \quad g = \cfrac{1}{x} \to 0,~ x \to \infty, \quad g - \text{монотонна} \\
	\l| \inti{1}{A} \cos x dx \r| = \bigg|\fint{\sin x}{1}{A}\bigg| \le 2 \RR \text{пр. Дирихле, интеграл сходится}
}
$$

### Признак Абеля (для сходимости)
1. $\inti{a}{+\infty} f(x) dx$ сходится
2. $g$ - монотонная 
3. $|g| \le M$ не зависит от $x$
Тогда $\inti{a}{\infty} f(x) g(x) dx$ сходится

### Условная и абсолютная сходимость
$$
\displaylines{
	\inti{a}{+\infty} f(x) dx \text{ сходится абсолютно, если } \inti{a}{\infty} |f| dx \text{ сходится} \\
	\inti{a}{+\infty} f(x) dx \text{ сходится условно, если } \inti{a}{\infty} f dx \text{ сходится и} \inti{a}{\infty} |f| dx \text{ расходится}
}
$$
%%PDF break%% <div style="page-break-after: always;"></div>

## Площадь, длина, объём

##### Площадь фигуры
1. Рисуется примерный график
2. Находятся границы фигуры
3. Считается определенный интеграл с найденными границами

##### Длина кривой
1. На входе имеются формулы для каждой координаты ($x = f_x(t),~ y = f_y(t),~ z = f_z(t)$)
2. Находятся границы кривой относительно $t$ ($t_1, t_2$)
3. Длина считается по формуле:
$$
t \in [t_1, t_2]; \quad l = \inti{t_1}{t_2} \sqrt{(x^\prime)^2 + (y^\prime)^2 + (z^\prime)^2)} dt
$$

##### Объём тела, образованного при вращении вокруг оси $Ox$
1. Рисуется примерный график
2. Находятся границы фигуры
3. Объём считается по формуле:
$$V = \inti{a}{b} \pi f^2(x) dx$$

##### Площадь поверхности, образованной при вращении вокруг оси $Ox$
1. Рисуется примерный график
2. Находятся границы фигуры
3. Площадь поверхности считается по формуле:
$$
	S = 2\pi \inti{a}{b} |y| \cdot \sqrt{1 + (y^\prime)^2} dx
$$

## Формула Стирлинга
$$
n! = \sqrt{2\pi n} \l( \cfrac{n}{e} \r)^n \exp \cfrac{\Theta_n}{12n}, \quad \exp x = e^x, \quad \Theta_n \in (0, 1), \quad n > 0
$$

%%PDF break%% <div style="page-break-after: always;"></div>

## Ряды Тейлора ($x \to 0$)
$$
\displaylines{
	e^x = 1 + x + \cfrac{x^2}{2!} + \cfrac{x^3}{3!} + o(x^3)\\
	\sin x = x - \cfrac{x^3}{3!} + \cfrac{x^5}{5!} + o(x^5) \\
	\cos x = 1 - \cfrac{x^2}{2!} + \cfrac{x^4}{4!} - \cfrac{x^6}{6!} + o(x^6) \\
	\ln(1 + x) = x - \cfrac{x^2}{2} + \cfrac{x^3}{3} - \cfrac{x^4}{4} + o(x^4) \\
	(1 + x)^\alpha = 1 + \alpha x + \cfrac{\alpha(\alpha - 1)}{2}x^2 + \cfrac{\alpha(\alpha - 1)(\alpha - 2)}{3!} x^3 + o(x^3)
}
$$

##### Пример применения
$$
\Lim{x}{0} \cfrac{\sin x}{x} = \Lim{x}{0} \cfrac{\cancel{x}^1 + o(\cancel{x}^1)}{\cancel{x}} = \Lim{x}{0} (1 + o(1)) = 1 + 0 = 1
$$
### Замечательные пределы
$$
\lim_{x \to 0 } \cfrac{\sin x}{x} = 1 \quad \lim_{x \to \infty} \l( 1 + \cfrac{1}{x} \r)^x = e
$$

### Не менее замечательные замены
$$
\displaylines{
	(1 + t^2) = \tg^2 x + 1 = \cfrac{\sin^2 x + cos^2 x}{\cos^2 x} = \cfrac{1}{\cos^2 x} \\
	\sqrt{1 - t^2} = \sqrt{1 - \sin^2 x} = \sqrt{\cos^2 x} \\
	\sqrt{1 - t^2} = \sqrt{1 - \cos^2 x} = \sqrt{\sin^2 x}
}
$$

### Тригонометрия
$$
	\sin^2 x + \cos^2 x = 1 \quad
	\sin 2x = 2 \sin x \cos x \quad
	\cos 2x = \cos^2 x - \sin^2 x
$$

%%PDF break%% <div style="page-break-after: always;"></div>


## Почти табличные интегралы
$$\displaylines{
\int x^\alpha dx = \cfrac{x^{\alpha + 1}}{\alpha + 1} + c, \quad \alpha \ne -1
\qquad 

\int \cfrac{dx}{x + a} = \ln|x + a| + c
\\

\int a^x dx = \cfrac{a^x}{\ln a} + c, \quad a > 0, \quad a \ne 1
\qquad 

\int e^x dx = e^x + c
\\

\int \sin x dx = -\cos x + c
\qquad 

\int \cos x dx = \sin x + c
\\

\int \cfrac{dx}{\cos^2x} = \tg x + c
\qquad 

\int \cfrac{dx}{\sin^2x} = -\ctg x + c
\\

\int \sh x dx = \ch x + c
\qquad 

\int \ch x dx = \sh x + c
\\

\int \cfrac{dx}{\ch^2 x} = \th x + c
\qquad 

\int \cfrac{dx}{\sh^2 x} = -\cth x + c
\\

\int \cfrac{dx}{x^2 + a^2} = \cfrac{1}{a} \arctg \cfrac{x}{a} + c = -\cfrac{1}{a} \arcctg \cfrac{x}{a} + c
\\

\int \cfrac{dx}{x^2 - a^2} = \cfrac{1}{2a}\ln \left| \cfrac{x - a}{x + a} \right| + c
\\

\int \cfrac{dx}{\sqrt{a^2 - x^2}} = \arcsin \cfrac{x}{a} + c = -\arccos \cfrac{x}{a} + c, \quad |x| < a, \quad a \ne 0
\\

\int \cfrac{dx}{\sqrt{x^2 + a^2}} = \ln |x + \sqrt{x^2 + a^2}| + c, \quad 
a \ne 0
\\

\int \cfrac{dx}{\sqrt{x^2 - a^2}} = \ln|x + \sqrt{x^2 - a^2}| + c, \quad a \ne 0 \quad (|x| > |a|)
\\

\int \sqrt{x^2 + a^2} dx = \cfrac{1}{2} (x\sqrt{x^2 + a^2} + a^2 \ln(x + \sqrt{x^2 + a^2})) + c
\\

\int \sqrt{x^2 - a^2} dx = \cfrac{1}{2} (x\sqrt{x^2 - a^2} - a^2 \ln (x + \sqrt{x^2 - a^2})) + c
\\

\int \sqrt{a^2 - x^2} dx = \cfrac{1}{2} \l(x\sqrt{a^2 - x^2} + a^2 \arcsin \l( \cfrac{x}{a} \r)\r) + c
\\

\int \sin^2 x dx = \cfrac{1}{2}\l(x - \cfrac{1}{2}\sin(2x)\r) + c
\\

\int \cos^2 x dx = \cfrac{1}{2}\l(x + \cfrac{1}{2}\sin(2x)\r) + c 
\\
}$$

%%PDF break%% <div style="page-break-after: always;"></div>


# Разбор листка №7

### Задание 1
#### Пункт а)
$$
\displaylines{
	\int \cfrac{dx}{(x^2 - 1)^3} = \int \cfrac{dx}{(x - 1)^3(x + 1)^3} = \cfrac{\dots}{(x - 1)^2(x + 1)^2} + \int \cfrac{\dots}{(x - 1)(x + 1)} dx =\\
	=\cfrac{Cx^3 + Dx^2 + Ex + F}{(x^2 + 1)^2} + \int \cfrac{A}{x - 1} + \cfrac{B}{x + 1} dx \fbox{=} \\

	\cfrac{1}{(x^2 - 1)^3} = \cfrac{(3Cx^2 + 2Dx + E)(x^2 - 1)^{\cancel{2}} - (Cx^3 + Dx^2 + Ex + F) \cdot 2\cancel{(x^2 - 1)} \cdot 2x}{(x^2 - 1)^{\cancel{4} 3}} + \cfrac{A}{x - 1} + \cfrac{B}{x + 1} \\

	1 = (3Cx^2 + 2Dx + E)(x^2 - 1) - 4x(Cx^3 + Dx^2 + Ex + F) + A(x - 1)^2(x + 1)^3 + B(x + 1)^2(x - 1)^3 \\\\

	\begin{array}{llll}
		x = 1 : & 1 = -4(C + D + E + F) & \text{при }x^5 : & 0 = A + B \\
		x = -1 : & 1 = 4(-C + D - E + F) & \text{при }x^4 : &0 = 3C - 4C + 3A - 2A - 3B + 2B \\
		x = 0 : & 1 = -E + A - B & \text{при }x : & 0 = -2D -4F -2A + 3A - 2B + 3B
	\end{array} \\
	
	\l(\begin{array}{cccccc|c}
		0 &  0 & -4 & -4 & -4 & -4 & 1 \\
		0 &  0 & -4 &  4 & -4 &  4 & 1 \\
		1 & -1 &  0 &  0 & -1 &  0 & 1 \\
		1 &  1 &  0 &  0 &  0 &  0 & 0 \\
		1 & -1 & -1 &  0 &  0 &  0 & 0 \\
		1 &  1 &  0 & -2 &  0 & -4 & 0 \\
	\end{array}\r)
	\underset{\Longrightarrow}{\text{УСВ}}
	\l(\begin{array}{cccccc|c}
		1 & 0 & 0 & 0 & 0 & 0 & \frac{3}{16} \\  
		0 & 1 & 0 & 0 & 0 & 0 & -\frac{3}{16} \\  
		0 & 0 & 1 & 0 & 0 & 0 & \frac{3}{8} \\  
		0 & 0 & 0 & 1 & 0 & 0 & 0 \\  
		0 & 0 & 0 & 0 & 1 & 0 & -\frac{5}{8} \\  
		0 & 0 & 0 & 0 & 0 & 1 & 0 \\
	\end{array}\r) \\\\

	\fbox{=} \cfrac{\frac{3}{8}x^3 - \frac{5}{8}x}{(x^2 - 1)^2} + \int \cfrac{3/16}{x - 1} - \cfrac{3/16}{x + 1} dx = \cfrac{1}{16} \l(\cfrac{6x^3 - 10x}{(x^2 - 1)^2} + 3\ln|x - 1| - 3\ln|x + 1|\r) + c
}
$$

#### Пункт б)
$$
\displaylines{
	\int \cfrac{dx}{2 + \sin x - 2\cos x} = \begin{bmatrix}
		t = \tg \cfrac{x}{2}
	\end{bmatrix} = \int \cfrac{\frac{\cancel{2}dt}{1 + t^2}}{\cancel{2}^1 + \frac{\cancel{2}t}{1 + t^2} - \cancel{2} \cdot \frac{1 - t^2}{1 + t^2}} = \int \cfrac{dt}{1 + t^2 + t - 1 + t^2} = \int \cfrac{dt}{t(2t + 1)} =\\
	= \int \cfrac{1}{t} - \cfrac{2}{2t + 1} dt = \int \cfrac{1}{t} - \cfrac{1}{t + \frac{1}{2}} dt = \ln |t| - \ln\l|t + \frac{1}{2}\r| + c = \ln \l| \tg \frac{x}{2} \r| - \ln \l| \tg \frac{x}{2} + \frac{1}{2} \r| + c
}
$$

%%PDF break%% <div style="page-break-after: always;"></div>

### Задание 2
#### Пункт а)
$$
\displaylines{
	\lim_{n \to \infty} \cfrac{\sqrt{n^2 - 1^2} + \sqrt{n^2 - 2^2} + \dotsc + \sqrt{n^2 - n^2}}{n^2} =\\
	= \lim_{n \to \infty} \cfrac{n}{n^2} \l( \sqrt{1 - \frac{1^2}{n^2}} + \sqrt{1 - \frac{2^2}{n^2}} + \dotsc + \sqrt{1 - \frac{n^2}{n^2}} \r) = \lim_{n \to \infty} \sum_{k = 1}^n \sqrt{1 - \l( \frac{k}{n} \r)^2} \cdot \frac{1}{n} \fbox{=} \\

	f(x) = \sqrt{1 - x^2}, \quad \xi_k = \cfrac{k}{n}, \quad x \in [0, 1]\\

	\fbox{=} \inti{0}{1} \sqrt{1 - x^2} dx = \begin{bmatrix}
		x = \sin t \\
		dt = \cfrac{dx}{x^\prime} \RR dx = x^\prime dt = \cos t dt \\
		x \in [0, 1] \RR t \in [0, \pi/2]
	\end{bmatrix} = \inti{0}{\pi/2} \sqrt{1 - \sin^2 t} \cdot \cos t ~ dt = \inti{0}{\pi/2} |\cos t| \cdot \cos t ~ dt =_* \\
	=_* \inti{0}{\pi/2} \cos^2 t ~dt = \inti{0}{\pi/2} \cfrac{\cos 2t + 1}{2} dt = \frac{1}{2} \inti{0}{\pi/2} \cos 2t + 1 dt = \frac{1}{2} \l( \fint{\frac{1}{2} \sin 2t + t}{0}{\pi/2} \r) = \frac{1}{2} \l(0 + \frac{\pi}{2} - (0 + 0)\r) = \frac{\pi}{4}\\

	* - \text{при } t \in [0, \pi/2] \quad \cos t \text{ неотрицателен, поэтому модуль можно снять}
}
$$

#### Пункт б)
$$
\displaylines{
	\lim_{x \to 0} \cfrac{\inti{-\sin x}{\sin x} \l( e^{t^2} - 1 \r)}{x^3} = \lim_{x \to 0} \cfrac{\l( 2 \cdot \inti{0}{\sin x} \l( e^{t^2} - 1 \r) \r)^\prime}{(x^3)^\prime} = \lim_{x \to 0} \cfrac{2 \cdot \l( e^{\sin^2 x} - 1 \r) \cdot \cos x}{3x^2} = \cfrac{2}{3} \Lim{x}{0} \cfrac{e^{\sin^2 x} - 1}{x^2} \cdot \cos x =\\
	= \cfrac{2}{3} \Lim{x}{0} \cfrac{1 + \sin^2 x + o(\sin^2 x) - 1}{x^2} \cdot \cos x = \cfrac{2}{3} \Lim{x}{0} \cfrac{(x + o(x)))^2 + o(x^2)}{x^2} \cdot \cos x = \cfrac{2}{3} \Lim{x}{0} \cfrac{\cancel{x^2}^1 + o(\cancel{x^2}^1)}{\cancel{x^2}^1} \cdot \cos x =\\
	= \cfrac{2}{3} \Lim{x}{0} \cos x = \cfrac{2}{3} \cdot 1 = \cfrac{2}{3}
}
$$

### Задание 3
#### Пункт а)
$$
\displaylines{
	\inti{0}{+\infty} 5^{-\sqrt{x}} dx = \begin{bmatrix}
		t = \sqrt{x} \\
		dx = \cfrac{dt}{t^\prime} = \cfrac{dt}{\frac{1}{2\sqrt{x}}} = 2t dt
	\end{bmatrix} = 2 \inti{0}{+\infty} 5^{-t}t~dt = 2 \l( \ffint{-\cfrac{5^{-t} t}{\ln 5}}{0}{+\infty} - \inti{0}{+\infty} -\cfrac{5^{-t}}{\ln 5} ~dt\r) =\\
	= 2 \l( 0 + \frac{1}{\ln 5}\inti{0}{+\infty} 5^{-t} ~dt\r) = \frac{2}{\ln 5} \cdot \ffint{\l(-\cfrac{5^{-t}}{\ln 5}\r)}{0}{+\infty} = \frac{2}{\ln 5} \cdot \l(0 + \frac{1}{\ln 5}\r) = \frac{2}{\ln^2 5}
}
$$
%%PDF break%% <div style="page-break-after: always;"></div>

#### Пункт б)
$$
\displaylines{
	I = \inti{0}{+\infty} 3^{-x}\cos(6x) ~dx = \ffint{-\frac{3^{-x} \cos(6x)}{\ln 3}}{0}{+\infty} - \inti{0}{+\infty} -\frac{3^{-x}}{\ln 3} \cdot (-\sin (6x) \cdot 6) ~ dx = \frac{1}{\ln 3} - \frac{6}{\ln 3} \inti{0}{+\infty} 3^{-x} \sin(6x) ~dx =\\
	= \frac{1}{\ln 3} - \frac{6}{\ln 3} \l( \ffint{-\cfrac{3^{-x} \sin(6x)}{\ln 3}}{0}{+\infty} - \inti{0}{+\infty} -\frac{3^{-x}}{\ln 3} \cdot (\cos(6x) \cdot 6) \r) = \frac{1}{\ln 3} - \frac{6}{\ln 3} \l( 0 + \frac{6}{\ln 3}\inti{0}{+\infty} 3^{-x}\cos(6x) \r) =\\
	= \frac{1}{\ln 3} - \frac{36}{\ln^2 3} \inti{0}{+\infty} 3^{-x}\cos(6x) = \frac{1}{\ln 3} - \frac{36}{\ln^2 3} \cdot I \\

	I = \frac{1}{\ln 3} - \frac{36}{\ln^2 3} \cdot I \\
	I \l(1 + \frac{36}{\ln^2 3} \r)= \frac{1}{\ln 3} \\
	I = \frac{\ln^2 3}{\ln 3 \cdot (\ln^2 3 + 36)} = \frac{\ln 3}{\ln^2 3 + 36}\\
}
$$

### Задание 4
#### Пункт а)
$$
\displaylines{
	\inti{0}{+\infty} \frac{x^{5/2}}{(1 + x^2)^2} dx = \inti{0}{1} \frac{x^{5/2}}{(1 + x^2)^2} dx_{(1)} + \inti{1}{+\infty} \frac{x^{5/2}}{(1 + x^2)^2} dx_{(2)} \\

	(1) \inti{1}{+\infty} \frac{x^{2.5}}{1 + 2x^2 + x^4} dx \le \inti{0}{+\infty} \frac{x^{2.5}}{x^4} dx = \inti{1}{+\infty} \frac{1}{x^{1.5}} - \text{сходится, т.к. 1.5 > 1} \\

	(2) - \text{сходится, проблемных точек нет}\\

	\text{Сумма сходящихся интегралов сходится} \RR \text{исходный интеграл сходится}
}
$$

#### Пункт б)
$$
\displaylines{
	\inti{0}{+\infty} \frac{\arctg ax \arctg bx}{x^2} dx = \inti{0}{1} \frac{\arctg ax \arctg bx}{x^2} dx + \inti{1}{+\infty} \frac{\arctg ax \arctg bx}{x^2} dx \\

	\inti{1}{+\infty} \frac{\arctg ax \arctg bx}{x^2} dx, \quad g(x)  = \arctg ax \arctg bx, \quad f(x) = \frac{1}{x^2} \\
	\inti{1}{+\infty} f(x) dx - \text{сходится}, \quad g(x) - \text{монотонна}, \quad g(x) \le \frac{\pi^2}{4} \\
	\RR \text{по пр. Абеля интеграл сходится}
}
$$
$$
\displaylines{
	ab \ge 0 \quad \inti{0}{1} \frac{\arctg ax \arctg bx}{x^2} dx \qquad \frac{\arctg ax \arctg bx}{x^2} \underset{x \to 0}{\sim} \frac{ax \cdot bx}{x^2} = ab - \text{сходится} \\

	ab \le 0 \quad \inti{0}{1} \frac{\arctg ax \arctg bx}{x^2} dx = -\inti{0}{1} \frac{-\arctg ax \arctg bx}{x^2} dx ~~\text{ сводится к случаю, когда }~~ ab \ge 0 
}
$$
Так как слагаемые сходятся, то и сумма интегралов сходится

### Задание 5
Рисуем примерный график
![[task5.png|300]]
Площадь зеленой + синей области - площадь прямоугольника со сторонами $2$ и $8$ - $16$
Найдем место пересечения $y = 2$ и $y = x^3 + x$ - $x = 1$ и $y = 10, ~ y = x^3 + x$ - $x = 2$
Площадь красной области - площадь прямоугольника со сторонами $1$ и $2$ - $2$
Площадь красной + синей области, это определенный интеграл:
$$
	\displaylines{
		\inti{1}{2} x^3 + x ~ dx = \ffint{\l(\frac{x^4}{4} +\frac{x^2}{2} \r)}{1}{2} = (4 + 2) - (1/4 + 1/2) = 6 - 3/4 = \frac{21}{4}
}
$$
Итого ответ: $16 - \l(\cfrac{21}{4} - 2\r) = \cfrac{51}{4}$

%%PDF break%% <div style="page-break-after: always;"></div>

### Задание 6
#### Пункт а)
1. Рисуем примерный график
![[Calculus/Calculus-Test3/images/list7/task6-a.png|396]]
2. Так как нижняя половина симметрична верхней, будем искать определенный интеграл от $y = \sqrt{x^3 - x^4}$. Для этого, надо найти точку пересечения функции и $Ox$: $x = 0, x = 1$
3. Считаем определенный интгеграл:
$$
\displaylines{
	\inti{0}{1} \sqrt{x^3 - x^4} ~dx = \inti{0}{1} x^2\sqrt{\frac{1}{x} - 1} ~dx = \inti{0}{1} x^2\sqrt{\frac{1 - x}{x}} ~dx = \begin{bmatrix}
		t = \sqrt{\cfrac{1 - x}{x}} \\
		x = \cfrac{1}{1 + t^2}\\
		dx = x^\prime dt = -\cfrac{2t}{(1 + t^2)^2} dt \\
		x \in [0, 1] \RR t \in (+\infty, 0]
	\end{bmatrix} =\\
	= \inti{+\infty}{0} \frac{1}{(1 + t^2)^2} \cdot t \cdot \frac{-2t}{(1 + t^2)^2} dt = 2\inti{0}{+\infty} \frac{t^2}{(1 + t^2)^4} dt =_* 2 \l( \ffint{\frac{At^5 + Bt^3 + Ct}{(1 + t^2)^3}}{0}{+\infty} - \inti{0}{+\infty} \frac{D}{1 + t^2} dt \r) \fbox{=} \\

	\frac{t^2}{(1 + t^2)^4} = \l( \frac{At^5 + Bt^3 + Ct}{(1 + t^2)^3} \r)^\prime - \frac{D}{1 + t^2} = \frac{-A(t^2 - 5)t^4 - 3B(t^2 - 1)t^2 - C(5t^2 - 1) - D(1 + t^2)^3}{(1 + t^2)^4} \\
	\begin{array}{llll}
		t = 0: & 0 = C - D & \text{при } t^2: & 1 = 3B - 5C - 3D\\
		t = 1: & 1 = 4A - 4C - 8D & \text{при } t^4: & 0 = 5A - 3B - 3D\\
	\end{array} \\
	\l(\begin{array}{cccc|c}
		0 &  0 &  1 & -1 & 0 \\
		4 &  0 & -4 & -8 & 1 \\
		0 &  3 & -5 & -3 & 1 \\
		5 & -3 &  0 & -3 & 0 \\
	\end{array}\r)
	\underset{\Longrightarrow}{\text{УСВ}}
	\l(\begin{array}{cccc|c}
		1 & 0 & 0 & 0 & \frac{1}{16} \\  
		0 & 1 & 0 & 0 & \frac{1}{6} \\  
		0 & 0 & 1 & 0 & -\frac{1}{16} \\  
		0 & 0 & 0 & 1 & -\frac{1}{16} \\
	\end{array}\r)
}
$$
$$
\displaylines{
	\fbox{=} ~ 2 \l(0 + \frac{1}{16} \inti{0}{+\infty} \frac{1}{1 + t^2} dt \r) = \frac{1}{8} \fint{\arctg t}{0}{\infty+} = \frac{\pi}{16}
}
$$
Итого, получаем ответ: $2 \cdot \cfrac{\pi}{16} = \cfrac{\pi}{8}$

_* - если функция четная, то в методе Остоградского вне интеграла коэффициенты при четных степенях равны нулю, внутри интеграла коэффициенты при нечетных степенях равны нулю_

#### Пункт б) 
1. Рисуем примерный график
![[Calculus/Calculus-Test3/images/list7/task6-b.png|400]]
2. Находим точки пересечения:
	$$2\ln x = \ln(x + 20) \RR e^{2\ln x} = e^{\ln(x + 20)} \RR x^2 = x + 20 \RR x^2 - x - 20 = 0 \RR (x - 5)(x + 4) \RR x_{12} = -4, 5$$
	Графики пересекаются при $x = 5$
3. Осталось посчитать определенный интеграл для промежутка $[0, 1]$ и $[1, 5]$:
$$
\displaylines{
	S = \inti{0}{1} \ln(x + 20) dx + \inti{1}{5} \ln(x + 20) - 2\ln x ~dx =\\
	= \fint{(\ln(x + 20)(x + 20) - (x + 2))}{0}{1} + \fint{(\ln(x + 20)(x + 20) - (x + 20))}{1}{5} - \fint{(2x\ln x - 2x)}{1}{5} =\\
	= \fint{(\ln(x + 20)(x + 20) - (x + 20))}{0}{5} - 10\ln 5 + 10 + 2\ln 1 - 2 = 25\ln 25 - 25 - 20\ln 20 + 20 + - 10\ln 5 + 8 =\\
	= 25\ln 25 - 20\ln 20 - 10\ln 5 + 3
}
$$
%%PDF break%% <div style="page-break-after: always;"></div>

### Задание 7
#### Пункт а)
$$
\displaylines{
	\Lim{n}{\infty} \frac{\ln((2n)!)}{\ln n!} = \Lim{n}{\infty} \frac{\ln\l( \sqrt{4\pi n} \l( \cfrac{2n}{e} \r)^{2n} \exp \cfrac{\Theta_{2n}}{24n} \r)}{\ln \l( \sqrt{2\pi n} \l( \cfrac{n}{e} \r)^n \exp \cfrac{\Theta_n}{12n} \r)} = \Lim{n}{\infty} \frac{\ln \sqrt{4\pi n} + \ln e^{-2n} + \ln 2n^{2n} + \ln \l(\exp \cfrac{\Theta_{2n}}{24n}\r)}{\ln \sqrt{2\pi n} + \ln e^{-n} + \ln n^n + \ln \l(\exp \cfrac{\Theta_{n}}{12n}\r)} =\\
	= \Lim{n}{\infty} \frac{\ln \sqrt{4\pi n} - 2n + 2n\ln 2n + \cfrac{\Theta_{2n}}{24n}}{\ln \sqrt{2\pi n} - n + n\ln n + \cfrac{\Theta_{n}}{12n}} = \Lim{n}{\infty} \frac{\ln \sqrt{4\pi n} - 2n + 2n\ln n + 2n\ln2}{\ln \sqrt{2\pi n} - n + n\ln n} =\\
	= \Lim{n}{\infty} \frac{\frac{\ln \sqrt{4\pi n}}{n\ln n} - \frac{2}{\ln n} + 2 + \frac{2\ln2}{\ln n}}{\frac{\ln \sqrt{2\pi n}}{n\ln n} - \frac{1}{\ln n} + 1} = \Lim{n}{\infty} \frac{0 - 0 + 2 + 0}{0 - 0 + 1} = 2
}
$$

#### Пункт б)
$$
\displaylines{
	\Lim{n}{\infty} \l( 1 + \cfrac{\sqrt{2\pi n}}{n!} \r)^{\l( \cfrac{n}{e} \r)^n} = \Lim{n}{\infty} e^{\l( \cfrac{n}{e} \r)^n \ln\l( 1 + \cfrac{\sqrt{2\pi n}}{n!} \r)} \fbox{=}

	\\ \Lim{n}{\infty} \l( \cfrac{n}{e} \r)^n \ln\l( 1 + \cfrac{\sqrt{2\pi n}}{n!} \r) = \Lim{n}{\infty} \l( \cfrac{n}{e} \r)^n \cfrac{\sqrt{2\pi n}}{n!}(1 + o(1)) =\\
	= \Lim{n}{\infty} \cancel{\l( \cfrac{n}{e} \r)^n} \cfrac{\cancel{\sqrt{2\pi n}}}{\cancel{\sqrt{2\pi n}} \cdot \cancel{\l( \cfrac{n}{e} \r)^n} \cdot \exp \cfrac{\Theta_n}{12n}}(1 + o(1))\\
	= \Lim{n}{\infty} \cfrac{1 + o(1)}{1 + o(1)} = 1\\

	\fbox{=} ~ e^1 = e
}
$$

### Задание 8
$$
\displaylines{
	C_n^k = \cfrac{n!}{k!(n - k)!} = \cfrac{\sqrt{2\pi n} \l( \cfrac{n}{e} \r)^n \exp \cfrac{\Theta_n}{12n}}{k! \l( \sqrt{2\pi (n - k)} \l( \cfrac{n - k}{e} \r)^{n - k} \exp \cfrac{\Theta_{n - k}}{12(n -k )} \r)} \sim \cfrac{\sqrt{n} \cdot n^n}{k! \sqrt{(n - k)} (n - k)^{n - k}e^k} \sim \\
	\sim \cfrac{n^n}{k!~(n - k)^{n - k}} = \cfrac{e^{n\ln n}}{k!~e^{(n - k)\ln(n - k)}} = \cfrac{e^{n\ln n - (n - k)\ln(n - k)}}{k!} \sim \cfrac{e^{k\ln n}}{k!} = \cfrac{n^k}{k!}
}$$

%%PDF break%% <div style="page-break-after: always;"></div>

# Разбор листка №7+
## Задание 1
### Пункт а)
Решим самым простым способом:
$$
(\cos x + \sin x )' = -\sin x + \cos x = \cos x - \sin x
$$
применим это знание:
$$
\displaylines{
\int \frac{\cos x - \sin x}{\cos x + \sin x} dx = \int \frac{(\cos x + \sin x)'}{\cos x + \sin x} dx = [t = \cos x + \sin x] = \\ \int \frac{1}{t} dt = \ln |t| + c = \ln |\cos x + \sin x| + c
}
$$
Альтернативно можно воспользоваться упрощенной тригометрической заменой, а именно видим, что $R(\sin x, \cos x) = R(-\sin x, -\cos x)$, действительно:
$$
\frac{(-\cos x) - (-\sin x )}{(-\cos x) + (-\sin x)} = \frac{- \cos x + \sin x }{- \cos x - \sin x} = \frac{\cos x - \sin x}{\cos x + \sin x}
$$
поэтому воспользуемся заменой $t = \tg x$:
$$
\displaylines{
	\int \frac{\cos x - \sin x}{\cos x + \sin x} = \int \frac{1 - \tg x}{1 + \tg x} = \begin{bmatrix}
		t = \tg x \\
		x = \arctg t \\
		dx = \frac{dt}{1 + t^2}
	\end{bmatrix} = \\
	= \int \frac{1 - t}{1 + t} \cdot \frac{dt}{1 + t^2} = \int \frac{A}{1 + t} + \frac{Bt + C}{1 + t^2} dt 
} 
$$
решим систему:
$$
	\displaylines{
	\frac{1 - t}{(1 + t)(1 + t^2)} = \frac{A}{1 + t} + \frac{Bt + C}{1 + t^2} \RR A(1 + t^2) + (Bt + C)(1 + t) = 1 - t \\ 
	при\ \begin{cases}
	t^0 : A + C = 1 \\
	t^1 : B + C = -1\\
	t^2: A + B = 0 \\
	\end{cases} \RR \begin{cases} A = 1 \\ B = -1 \\ C = 0\end{cases}
}
$$
продолжим
$$
\displaylines{
= \int \frac{1}{1 + t} + \frac{-t}{1 + t^2} dt = \int \frac{dt}{1 + t} - \int \frac{t}{1 + t^2} dt = \ln |1 + t| - \frac{1}{2}\ln|1 + t^2| + c \\
\ln |1 + \tg x| - \frac{1}{2} \ln |1 + \tg^2 x| + c = \ln \l|\frac{\cos x + \sin x }{\cos x}\r| - \ln \sqrt{\frac{\sin^2x + \cos^2x}{\cos^2x}} + c =  \\
= \ln |\cos x + \sin x| + c
}

$$
%%PDF break%% <div style="page-break-after: always;"></div>

### Пункт б)
$$
\displaylines{
\int \frac{dx}{4\cos^2 x - 2\sin 2x + \sin^2 x} = \int \frac{dx}{4\cos^2 x - 4 \sin x \cos x + \sin^2 x} = \\ 

= [R(\cos x, \sin x) = R(-\cos x, -\sin x)]= \int \frac{\frac{dx}{\cos^2 x}}{4 - 4\tg x + \tg^2 x} = [t = \tg x] = \int \frac{dt}{4 - 4t + t^2} =\\
=\int \frac{1}{(t - 2)^2} dt = -\frac{1}{t - 2} + c = \frac{1}{2 - \tg x }+ c

}
$$

## Задание 2
### Пункт а)
$$
\displaylines{
\lim_{n \to \infty} \l (\frac{1}{n + 1} + \frac{1}{n + 2} + \dots + \frac{1}{2n}\r) = \lim_{n \to \infty} \sum_{k = 1}^{n} \frac{1}{n + k} = \lim_{n \to \infty} \frac{1}{n}\sum_{k = 1}^{n} \frac{1}{1 + \frac{k}{n}} = \inti{0}{1} \frac{dx}{1 + x} = \\

= \ln |x + 1| \Big |_{0}^{1} = \ln 2 - \ln 1 = \ln 2

}
$$


### Пункт б)
$$
\displaylines{

\lim_{n \to \infty} n \l(\frac{1}{n^2 + 1^2} + \frac{1}{n^2 + 2^2} + \dots + \frac{1}{n^2 + n^2}\r) = \lim_{n \to \infty} n\sum_{k = 1}^{n} \frac{1}{n^2 + k^2} = \lim_{n \to \infty} \frac{1}{n} \sum_{k = 1}^{n} \frac{1}{1 + (\frac{n}{k})^2} =\\
= \int_{0}^{1} \frac{dx}{1 + x^2} = \arctg(x) \Big |_{0}^{1} = \frac{\pi}{4} - 0 = \frac{\pi}{4}

}
$$



## Задание 3
### Пункт а)
$$
\inti{0}{\infty} \frac{1}{(1 + x)\sqrt{x}}
$$
Посмотрим на проблемые точки нашего интеграла, это точки $x = \{0, -1\}$, в задаче нас интересует только $0$, поэтому разобьем наш интеграл на $2$ по аддитивности и изучим по отдельности:
$$
\inti{0}{\infty} \frac{1}{(1 + x)\sqrt{x}} = \inti{0}{1} \frac{1}{(1 + x)\sqrt{x}} + \int_{1}^{\infty} \frac{1}{(1 + x)\sqrt{x}}
$$
Второй очевидно сходится, поэтому посмотрим на $1$:
$$
\displaylines{
\inti{0}{1} \frac{1}{(1 + x)\sqrt{x}} = \inti{0}{1} \frac{1}{\sqrt{x} + x\sqrt{x}} \le \inti{0}{1} \frac{1}{\sqrt{x}} - \text{сходится} 


}
$$
Тогда давайте вычислим определенный интеграл:
$$
\displaylines{
\inti{0}{\infty} \frac{1}{(1 + x)\sqrt{x}} = \begin{bmatrix}
	t = \sqrt{x} \\
	x = t^2 \\
	dx = 2t\cdot dt
\end{bmatrix} = \inti{0}{\infty} \frac{2t}{t(1 + t^2)} dt = 2\arctg(\sqrt{x}) \Big |_{0}^{\infty} = \pi
}
$$
Можно было сразу найти определенный интеграл без проверки на сходимость, я показал сходимость для тех, кому это могло было не совсем очевидно.

### Пункт б)
$$
\inti{1}{\infty} \frac{\arctg x}{x^2} dx 
$$
Этот интеграл тоже очевидно сходится
1) $\arctg x$ в числители ограничивается константой на бесконечности
2) $\frac{1}{x^2}$ сходится
Более формально:
$$
\inti{1}{\infty} \frac{\arctg x}{x^2} dx \le \inti{1}{\infty} \frac{\frac{\pi}{2}}{x^2} - \text{сходится}
$$
Тогда вычислим определенный интеграл:
$$
\displaylines{
\inti{1}{\infty} \frac{\arctg x}{x^2} dx = -\inti{1}{\infty} \arctg x \cdot \l(\frac{1}{x}\r)' dx = \ffint{-\frac{\arctg x}{x}}{1}{\infty} + \inti{1}{\infty} \frac{1}{1 + x^2} \cdot \frac{1}{x} dx = \\
= \frac{\pi}{4} + \inti{1}{\infty} \frac{A}{x} + \frac{Bx + C}{1 + x^2} dx = \frac{\pi}{4} + \inti{1}{\infty} \frac{1}{x} + \frac{-x}{1 + x^2} dx = \frac{\pi}{4} + \ffint{\l(\ln x - \frac{1}{2}\ln (1 + x^2)\r)}{1}{\infty} = \\
=\frac{\pi}{4} + \ffint{\l(\ln \frac{x}{\sqrt{1 + x^2}}\r)}{1}{\infty} = \frac{\pi}{4} + \ln 1 - \ln \l(\frac{1}{\sqrt{1 + 1}}\r) = \frac{\pi}{4} + \ln \sqrt{2}
}
$$

## Задание 4
### Пункт а)
$$
\displaylines{
	\inti{2}{\infty} \l (\cos \frac{2}{x} - 1\r)dx = \begin{bmatrix}
		t = \frac{1}{x} \\
		x = \frac{1}{t} \\
		dx = -\frac{1}{t^2} \\
		x \in [2; +\infty) \RR t \in [1/2, 0]
	\end{bmatrix} = \inti{1/2}{0} \frac{1 - \cos(2t)}{t^2} dt =\\
	= -\inti{0}{1/2} \frac{1 - \cos(2t)}{t^2} dt, \text{ смотрим что происходит при } t \to 0:
\frac{1 - \cos(2t)}{t^2} = \frac{1 - \l(1 - \frac{(2t)^2}{2} + o(t^2)\r)}{t^2} =\\
= \frac{\frac{(2t)^2}{2} + o(t^2)}{t^2} = 2 + o(1) \to 2 \RR \text{ исходный интеграл сходится}
}
$$

### Пункт б)
$$
\inti{1}{\infty} \frac{\ln x}{x\sqrt{x^2 - 1}}dx 
$$
Мы знаем, что логарифм слабее любой степени, поэтому $\exists x_1 > 2, \forall x > x_2 :\ln (x) < x^{\frac{1}{2}}$, и $\exists x_2 > 2, \forall x > x_2 : x^\frac{2}{3} < \sqrt{x^2 - 1}$ возьмем $x_0 = max(x_1, x_2)$:

$$
\displaylines{
	\int_{2}^{\infty} \frac{\ln x}{x\sqrt{x^2 - 1}} dx = \int_{2}^{x_0} \frac{\ln x}{x\sqrt{x^2 - 1}} dx + \inti{x_0}{\infty} \frac{\ln x}{x\sqrt{x^2 - 1}} \le \int_{2}^{x_0} \frac{\ln x}{x\sqrt{x^2 - 1}} dx + \inti{x_0}{\infty} \frac{x^{1/2}}{x\sqrt{x^2 - 1}} \le \\
	\le \int_{2}^{x_0} \frac{\ln x}{x\sqrt{x^2 - 1}} dx + \inti{x_0}{\infty} \frac{dx}{x^{\frac{1}{2} + \frac{2}{3}}}
}
$$
оба сходятся. 

Теперь посмотрим на проблемную точку, а именно $x \to 1$. Здесь удобно будет делать замены по эквивалентности, поэтому сделаем замену:
$$
\displaylines{
\inti{1}{2} \frac{\ln x}{x\sqrt{x^2 - 1}}dx = [t = x - 1, x = t + 1] = \inti{0}{1} \frac{\ln (t + 1)}{(t + 1)\sqrt{t(t + 2)}}dt = [t \to 0] = \\
\inti{0}{1} \frac{t}{(t + 1)\sqrt{t(t + 2)}} \le \inti{0}{1} \frac{t}{(1)\sqrt{t} \cdot \sqrt{2}} = \frac{1}{\sqrt{2}} \int_{0}^{1} \frac{1}{\sqrt{t}}
}
$$
так как $\sqrt{t} = t^{\frac{1}{2}}, \frac{1}{2} < 1$ - предел сходится, а раз сходится больший, то сходится и наш.

## Задание 5
![[task5-1.png|120]]

Вот функция $f(x) = 2^x + 3^x$, что такое $g(y)?$

$g(y)$ такая функция, что если мы возьмем какой-то $x_0$, применим к нему функцию, получим $y_0 = f(x_0)$, а затем применим уже $g(y_0) = x_0$ получим снова тот же $x_0$. По сути это тоже самое, что поменять $x$ и $y$ местами, поэтому нам нужно найти черную площадь:

![[task5-2.png|100]]

Как уже видно на рисунке, мы ее можем найти так: взять какой-то прямоугольник в котором она лежит, взять его площадь, вычесть лишнее. 

Самый удобный прямоугольник будет в точке пересечения с нашими границами, то есть прямоугольник $(0, 0), (g(13), 13)$. Можно руками перебрать, что $g(13) = 2$. Площадь такого прямоугольника равна $2 \cdot 13 = 26$. 

Далее, вычтем лишнее, самое легкое это оранжевый квадрат, в точках $(0, 0), (2, 2)$.
Его площадь $4$. 

Осталось самое сложное: красная фигура, но такое мы умеем находить, это просто
$$
\inti{0}{2} f(x) - 2 dx = \inti{0}{2} 2^x + 3^x - 2 dx = \ffint{\l( \frac{2^x}{\ln 2} + \frac{3^x}{\ln 3} - 2x \r)}{0}{2} = \frac{3}{\ln 2} + \frac{8}{\ln 3} - 4
$$

Ответ: $26 - 4 - \cfrac{3}{\ln 2} - \cfrac{8}{\ln 3} + 4 = 26 - \cfrac{3}{\ln 2} - \cfrac{8}{\ln 3}$ 

P.S. Можно было не выпендриваться и просто найти $\inti{0}{2} f(x)$, тогда мы бы посчитали красную и оранжевую площадь сразу

%%PDF break%% <div style="page-break-after: always;"></div>

## Задание 6
### Пункт а)
Схематично зарисуем график:
![[Calculus/Calculus-Test3/images/list7+/task6-a.png|300]]
Черное это уравнение $\sqrt{x} + \sqrt{y} = 2$, красный соотвественно $x = y^2$. 

Так как нас интересует только первая плоскость, то можно преобразовать функции в $y = (2 - \sqrt x)^2$ и $y = \sqrt{x}$ соотвественно.  

Что нам нужно сделать. Видим, что функции строго монотонны в разные стороны, откуда одна точка пересечения. Найдем ее:

$(2 - \sqrt{x})^2 = \sqrt{x}$, не тяжело заметить, что это $x = 1$. 

Теперь нам нужно найти площадь фигуры, соотвественно это просто, площадь под красным графиком до $x = 1$ и площадь под черным после:
$$
\displaylines{
\inti{0}{1} \sqrt{x} dx + \inti{1}{2} (2 - \sqrt{x})^2 dx = \ffint{\frac{2x^{\frac{3}{2}}}{3}}{0}{1} + 4x \Big |_{1}^{4} - \ffint{\frac{8x^{\frac{3}{2}}}{3}}{1}{4} + \ffint{\frac{x^2}{2}}{1}{4} = \\ = \frac{2}{3} + 12 - \frac{64}{3} + \frac{8}{3} + 8 - \frac{1}{2} = \frac{2 + 36 - 64 + 8 + 24}{3} - \frac{1}{2} =  \frac{6}{3} - \frac{1}{2} = \frac{3}{2}
}
$$

### Пункт б)
$$
y^2 = \sin^2 x \cos x, -\frac{\pi}{2} \le x \le \frac{\pi}{2}
$$
![[Calculus/Calculus-Test3/images/list7+/task6-b.png|300]]

Вот схематичный рисунок (в реале он в сто раз красивее). Поделим функцию на две: $y = \sqrt{\sin^2 x \cos x}, y = -\sqrt{\sin^2 x \cos x}$. 
В первой четверти и $\sin x > 0$ и $\cos x > 0$, так что вся функция выше $Ox$. В остальных аналогичные рассуждения со своими $x$. 

Важно лишь то, что у нас нет смены знака (и неопределенности), поэтому мы можем брать интеграл полностью на отрезках. Можно заметить что площадь снизу равна площади сверху и слева, так как $\sin^2 (-x) \cos (-x) = (-\sin x)^2 \cos x = \sin^2 x \cos x$, нам осталось только посчитать:
$$
\displaylines{
	\inti{0}{\frac{\pi}{2}} \sqrt{\sin^2 x \cos x} dx = \begin{bmatrix}
		t = \cos x \\
		x = \arccos t \\
		dx = -\frac{1}{\sqrt{1 - t^2}}
	\end{bmatrix} = -\int_{1}^{0} \sqrt{t - t^3} \cdot \frac{dt}{\sqrt{1 - t^2}} = \inti{0}{1} \sqrt{t} dt = \\
	 = \ffint{\frac{2x^{\frac{3}{2}}}{3}}{0}{1} = \frac{2}{3}
}
$$
Ответ: $\cfrac{8}{3}$

## Задание 7
$$
\displaylines{
\lim_{n \to \infty} \frac{(2n)!\sqrt{n}}{2^{2n} (n!)^2} = [\text{Стирлинг}] = \lim_{n \to \infty} \frac{\sqrt{4\pi n} \cdot \l(\frac{2n}{e}\r)^{2n} \cdot \exp\l(\frac{\Theta_1}{24n}\r)}{2\pi n \cdot \l(\frac{n}{e}\r)^{2n} \cdot \exp\l(\frac{2\Theta_2}{12n}\r)} \cdot \frac{\sqrt{n}}{2^{2n}} = \\
 = \lim_{n \to \infty} \frac{\sqrt{4\pi n} \cdot \sqrt{n}}{2\pi n} \cdot \frac{\l(\frac{2n}{e}\r)^{2n}}{\l(\frac{n}{e}\r)^{2n} \cdot 2^{2n}} \cdot \exp\l(\frac{\Theta_1- 4\Theta_2}{24n}\r) = \lim_{n \to \infty} \frac{1}{\sqrt{\pi}} \cdot 1 \cdot 1 = \frac{1}{\sqrt{\pi}}
}
$$