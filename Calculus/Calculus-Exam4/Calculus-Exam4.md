![[template_draft]]
![[template]]
# Материал к экзамену в 4 модуле. Матанализ

## Разбор Листка 13+

### Задача 1
#### Условие
Найдите производную функции $f$ в точке $M$ по направлению вектора $\vec{a}$:
1) $f = xy^2 z^3$, $M = (3, 2 ,1)$, $\vec{a} = (3, 4, 5)$ 
2) $f = \ln(x^2 + y^2 + z^2)$, $M = (3, 3, 1)$, $\vec{a} = (-1, 2, 2)$

#### Решение
##### Пункт а

В самом начале отнормируем направляющий вектор. $\vec{a} = (3, 4, 5) \leadsto \frac{1}{5\sqrt{2}}(3, 4, 5)$ 

Тогда
$$
\frac{\p f}{\p \vec{a}} = \frac{1}{5\sqrt{2}} \l ( 3 \cdot \frac{\p f }{\p x} + 4 \cdot \frac{\p f}{\p y} + 5 \cdot \frac{\p f}{\p z}\r)
$$
Найдем частные производные:
$$
\begin{cases}
	\frac{\p f}{\p x} = y^2 z^3 \\
	\frac{\p f}{\p y} = 2xyz^3 \\
	\frac{\p f}{\p z} = 3xy^2z^2
\end{cases}
$$
Подставляем в выражение:
$$
\frac{\p f }{\p \vec{a}} = \frac{1}{5 \sqrt{2}} \l(3y^2 z^3 + 8xyz^3 + 15 xy^2 z^2 \r)
$$
Осталось лишь найти значение в точке:
$$
\frac{\p f }{\p a} \atpoint{(3, 2 ,1)} = \frac{1}{5 \sqrt{2}} (3 \cdot 4 \cdot 1 + 8 \cdot 3 \cdot 2 \cdot 1 + 15 \cdot 3 \cdot 4 \cdot 1) = \frac{1}{5\sqrt{2}}(12 + 48 + 180) = 24\sqrt{2}
$$

##### Пункт б

Делаем тоже самое:

$$
\vec{a} = (-1, 2, 2) \leadsto \frac{1}{3}(-1, 2, 2)$$
$$
\frac{\p f}{\p \vec{a}} = \frac{1}{3} \l(-\frac{\p f}{\p x} + 2\cdot \frac{\p f}{\p y} + 2 \cdot \frac{\p f}{\p z}\r)
$$
$$
\begin{cases}
\frac{\p f}{\p x} = \frac{2x}{x^2 + y^2 + z^2}\\[3mm]
\frac{\p f}{\p y} = \frac{2y}{x^2 + y^2 + z^2} \\[3mm]
\frac{\p f}{\p z} = \frac{2z}{x^2 + y^2 + z^2}
\end{cases}
$$
$$
	\frac{\p f}{\p \vec{a}} = \frac{1}{3(x^2 + y^2 + z^2)} \cdot \l(-2x + 4y + 4z \r)
$$
$$
\frac{\p f}{\p \vec{a}} \atpoint{(3, 3, 1)} = \frac{10}{3\cdot 19} = \frac{10}{57}
$$

### Задача 2
#### Условие
Вычислите значение дифференциала функции
$$
	f(x, y) = x^3 y^6 + e^{x + y^2}
$$
в точке (1, 1) на векторе (1, 2)

#### Решение

В дифференциале уже не надо нормировать вектор.

воспользуемся равенством:
$$
	df = \frac{\p f}{\p x} dx + \frac{\p f}{\p y} dy
$$
Наш вектор $v$ и будет отвечать $(dx, dy)$, мы как бы приближаемся по нему. Посчитаем частные производные:
$$
\begin{cases}
\frac{\p f}{\p x} = 3x^2 y^6 + e^{x + y^2} \\[3mm]
\frac{\p f}{\p y} = 6x^3 y^5 + 2y \cdot e^{x + y^2}
\end{cases}
$$
$$
df \atpoint{(1, 1)} = (3 + e^2)dx + (6 + 2e^{2})dy
$$
тогда ответ:
$$
(3 + e^2) \cdot 1 + (6 + 2e^2) \cdot 2 = 5e^2 + 15
$$

### Задача 3
#### Условие
Найдите касательную плоскость
1) к графику функции $z = e^x xy + e^y xy$ в точке $(x_0, y_0, z_0) = (1, 1, 2e)$ 
2) к поверхности, заданной уравнением $z^2 = x^3 + y^2$ в точке $(x_0, y_0, z_0) = (2, 1, 3)$ 

#### Решение

![[task3.png]]
##### Пункт а

приведем к нужному виду:
$$
	F(x; y; z) = e^x xy + e^y xy - z= 0
$$
$$
\begin{cases}
	F'_{x}(x;y;z) = e^x y + e^x xy + e^y y \\[3mm]
	F'_{y}(x;y;z) = e^x x + e^y x + e^y xy \\[3mm]
	F'_{z}(x;y;z) = -1 
\end{cases}
$$
Подставим в точку
$$
\begin{cases}
F'_{x}(1; 1; 2e) = e + e + e = 3e\\[3mm]
F'_{y}(1;1;2e) = e + e + e = 3e \\[3mm]
F'_{z}(1;1;2e) = -1
\end{cases}
$$
**Ответ:**
$$
3e(x - 1) + 3e(y - 1) - (z - 2e) = 0 \RR 3ex + 3ey - z = 4e
$$

##### Пункт б
$$
	F(x;y;z) = x^3 + y^2 - z^2 = 0
$$
$$
\begin{cases}
F'_{x}(x;y;z) = 3x^2 \\[3mm]
F'_{y}(x;y;z) = 2y \\[3mm]
F'_{z}(x;y;z) = -2z
\end{cases}
$$
$$
\begin{cases}
F'_{x}(2;1;3) = 12 \\[3mm]
F'_{y}(2;1;3) = 2 \\[3mm]
F'_{z}(2;1;3) = -6
\end{cases}
$$
**Ответ:**
$$
	12(x - 2) + 2(y - 1) - 6(z - 3) = 0 \RR 6x + y - 3z = 4
$$

### Задача 4
#### Условие
Пусть $\phi$ - дважды непрерывно дифференцируемая, а $f$ — сложная функция, заданная следующим образом
$$
	f(x, y) = \phi(xy, x^3 + y^2)
$$
1) Выразите дифференциал 1-го порядка функции $f$ через частные производные функции $\phi$
2) Выразите дифференциал 2-ого порядка функции $f$ через частные производные функции $\phi$ 

#### Решение

Найти решение таких же задач с семинара можно [тут](https://disk.yandex.ru/d/hVWLMgTBxXHBUQ/%D0%9C%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B9%20%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7/%D0%A1%D0%B5%D0%BC%D0%B8%D0%BD%D0%B0%D1%80/%D0%91%D0%9F%D0%9C%D0%98227%20%D0%9A%D0%BE%D0%BB%D0%B5%D1%81%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%BA%D0%BE%202023-05-25T11-36-23Z.mp4) c примерно 24-ой минуты
$$
	u = xy, v = x^3 + y^2
$$
$$
\displaylines{
	\frac{\p f}{\p x} = \frac{\p \phi}{\p u} \cdot \frac{\p u}{\p x} + \frac{\p \phi}{\p v} \cdot \frac{\p v}{\p x} = 
	\phi'_{u} \cdot y + \phi'_{v} \cdot 3x^2 \\[3mm]

\frac{\p f}{\p y} = \frac{\p \phi}{\p u} \cdot \frac{\p u}{\p y} + \frac{\p \phi}{\p v} \cdot \frac{\p v}{\p y} = \phi'_{u} \cdot x + \phi'_{v} \cdot 2y
}
$$

Тогда
$$
df = \frac{\p f}{\p x} dx + \frac{\p f}{\p y} dy = (\phi'_u \cdot y + \phi'_v \cdot 3x^2)dx + (\phi'_{u} \cdot x + \phi'_v \cdot 2y) dy
$$

Первый дифференциал нашли, поищем вторые:
(так как $\phi$ дважды дифференцируема по Шварцу смешанные производные равны)
$$
\displaylines{
f''_{xx} = \frac{\p}{\p x} (f'_{x}) = \frac{\p }{\p x} (\phi'_{u} \cdot y + \phi'_{v} \cdot 3x^2)
 = y \cdot (\phi''_{u u} \cdot \frac{\p u}{\p x} + \phi''_{uv} \frac{\p v}{\p x}) + \\
+ 6x \cdot \phi'_{v} + 3x^2 \cdot (\phi''_{vu} \cdot \frac{\p u}{\p x} + \phi''_{vv} \cdot \frac{\p v}{\p x}) = \\
 = y^2 \phi''_{uu} + 6x \phi'_{v} + 6x^2y \phi''_{uv} + 9x^4 \phi''_{vv}
}
$$

$$
\displaylines{
	f''_{xy} = f''_{yx} = \frac{\p}{\p x} (f'_{y}) = \frac{\p}{\p x} (\phi'_{u} \cdot x + \phi'_{v} \cdot 2y) = \\
	= \phi'_{u} + x (\phi''_{uu} \cdot \frac{\p u}{\p x} + \phi''_{vu} \cdot \frac{\p v}{\p x}) + 2y (\phi''_{uv} \cdot \frac{\p u}{\p x} + \phi''_{vv} \cdot \frac{\p v}{\p x}) = \\
	\phi'_{u} + xy \phi''_{uu} + 3x^3 \phi''_{vu} + 2xy \phi''_{uv} + 6x^2 y \phi''_{vv} = \\\phi'_{u} + xy \phi''_{uu} + x \phi''_{vu}(3x^2 + 2y) + 6x^2 y \phi''_{vv}
}
$$

$$
\displaylines{
f''_{yy} = \frac{\p}{\p y} (f'_{y}) = \frac{\p}{\p y} (\phi'_u \cdot x + \phi'_v \cdot 2y) = x (\phi''_{uu} \cdot \frac{\p u}{\p y} + \phi''_{uv} \cdot \frac{\p v}{\p y}) + 2\phi'_{v} + 2y (\phi''_{vu} \cdot \frac{\p u}{\p y} + \phi''_{vv} \cdot \frac{\p v}{\p y}) =  \\
x^2 \phi''_{uu} + 2xy \phi''_{uv} + 2\phi'_{v} + 2xy \phi''_{vu} + 4y^2 \phi''_{vv} = \\
x^2 \phi''_{uu} + 4xy \phi''_{vu} + 4y^2\phi''_{vv} + 2\phi'_{v}
}
$$

Теперь просто подставим все, что мы нашли в равенство (автор не видит смысл делать это явно)
$$
d^2 f = f''_{xx} dx^2 + 2f''_{xy} dx dy + f''_{yy} dy^2$$

### Задача 5
#### Условие
Функция $z = z(x, y)$ задана неявно системой уравнений
$$
\begin{cases}
	x = v \sin u \\
	y = v \cos u \\
	z = uv^2
\end{cases}
$$
Найдите $dz$ и $\frac{\p^2 z}{\p x \p y}$ в точке $u = \frac{\pi}{4}$, $v = 1$ 

#### Решение

$$
dz = d(uv^2) = z'_{v} dv + z'_{u} du = 2vu \cdot dv + v^2 \cdot du
$$

теперь нам нужно выразить $(dv, du)$ через $(dx, dy)$, так как нас просят выразить $dz$ через $(x, y)$.

Мы это осуществим с помощью матрицы Якоби:
$$
\begin{pmatrix} dx \\ dy \end{pmatrix} = \begin{pmatrix}
	\sin u & v \cos u \\
	\cos u & -v \sin u
\end{pmatrix} \begin{pmatrix} dv \\ du \end{pmatrix}
$$
Мы нашли эти выражения с помощью первых двух равенств в системе.

Найдем:
$$
\begin{pmatrix}
	\sin u & v \cos u \\
	\cos u & -v \sin u
\end{pmatrix}^{-1} = \frac{1}{-v}\begin{pmatrix}
	-v \sin u & - v \cos u \\
	- \cos u & \sin u
\end{pmatrix} (*)
$$
Тогда:
$$
\begin{pmatrix} dv \\ du \end{pmatrix} = \frac{1}{-v}\begin{pmatrix}
	-v \sin u & - v \cos u \\
	- \cos u & \sin u
\end{pmatrix} \begin{pmatrix} dx \\ dy \end{pmatrix}
$$

Теперь уже можно выразить $dz$ через $(x, y)$:
$$
\displaylines{
dz = 2vu \cdot dv + v^2 \cdot du = 2vu (\sin u \cdot dx + \cos u\cdot  dy) - v (- \cos u \cdot dx + \sin u \cdot dy) = \\
(2vu \sin u + v \cos u)dx + (2vu \cos u - v \sin u)dy
}
$$
Найдем также значение в точке, для этого найдем саму точку:
$$
\begin{cases}
	x = v \sin u \\
	y = v \cos u \\
	z = uv^2 \\
	v = 1 \\
	u = \frac{\pi}{4}
\end{cases} \RR P = (\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}, \frac{\pi}{4}, 1, \frac{\pi}{4})
$$
Тогда:
$$
dz \atpoint{P} = (\frac{\pi}{2\sqrt{2}} + \frac{1}{\sqrt{2}})dx + (\frac{\pi}{2\sqrt{2}} - \frac{1}{\sqrt{2}})dy
$$

Второй дифференциал уже не инвариантен, поэтому найдем его стандартным способом. Для нахождением $z'_y$ воспользуемся равенством $dz = z'_x dx + z'_y dy$ 
$$
\displaylines{
\frac{\p }{\p x} (z'_{y}) = \frac{\p}{\p x} (2vu \cos u - v \sin u) = \\
 = 2 v'_{x} u \cos u + 2v u'_{x} \cos u - 2vu \sin u \cdot u'_x - v'_x \sin u - v \cos u \cdot u'_x = \\
 = v'_x (2 u \cos u - \sin u) + u'_x (2v \cos u - 2vu \sin u - v \cos u)
}
$$
чтобы не таскать с собой громоздкие выражения, сразу подставим точку:
$$
\displaylines{
\RR \atpoint{P} = v'_x (\frac{\pi}{2\sqrt{2}} - \frac{1}{\sqrt{2}}) + u'_x (\sqrt{2} - \frac{\pi}{2\sqrt{2}} - \frac{1}{\sqrt{2}}) = \\

= v'_x (\frac{\pi - 2}{2\sqrt{2}}) + u'_x (\frac{2 - \pi}{2\sqrt{2}}) = 
}
$$
тут воспользуемся обратной матрицей Якоби $(*)$ 
$$
= \sin u (\frac{\pi - 2}{2\sqrt{2}}) + \cos u (\frac{2 - \pi}{2\sqrt{2}}) = \frac{\pi - 2 + 2 - \pi}{4} = 0
$$


### Задача 6
#### Условие
Найдите все точки локального экстремума функции
$$
 f(x, y) = 2x^3 - 6xy - 3y^2 + 12y
$$

#### Решение

Найдем все стационарные точки, то есть точки, в которых дифференциал равен 0:
$$
 df = (6x^2 - 6y)dx + (-6x - 6y + 12)dy 
$$
$$
	df = 0 \iff \begin{cases} 
	f'_{x} = 0 \\
	f'_{y} = 0 
\end{cases} \RR \begin{cases}
	6x^2 - 6y = 0 \\
	6x + 6y - 12 = 0
\end{cases} \RR \begin{cases}
	6x^2 + 6x - 12 = 0 \\
	y = 2 - x
\end{cases} \RR P_1 = (1, 1), P_2 = (-2, 4)
$$

Нашли кандидатов, теперь посмотрим на второй дифференциал функции, выпишем сразу в матрицу, чтобы применить критерий Сильвестра:

$$
\begin{pmatrix}
	f''_{xx} & f''_{xy} \\
	f''_{yx} & f''_{yy} 
\end{pmatrix} = 
\begin{pmatrix}
	12x & -6 \\
	-6 & -6
\end{pmatrix} \RR [\text{применим хитрость с линала}] \RR \begin{cases}
	\sigma_{1} = -6 \\
	\sigma_{2} = -72x - 36
\end{cases}
$$
подставим обе точки:
$$
P_1 = (1, 1) \RR \begin{cases}
	\sigma_1 = -6 \\ \sigma_2 = -108
\end{cases} 
$$
нулевых миноров нет, по критерию она неопределенная
$$
	P_2 = (-2, 4) \RR \begin{cases}
		\sigma_1 = -6 \\
		\sigma_2 > 0
\end{cases} \RR \max
$$
**Ответ:**
точка $(-2, 4)$ - точка локального максимума 

### Задача 7
#### Условие
Найдите все точки условного локального экстремума функции
1) $f(x, y, z) = \sqrt{3} x + 3y + 2z$, если $x^2 + y^2 + z^2 = 1$
2) $f(x, y, z) = x^2 + y^2 + z^2$, если $xy = z^2 - 6z + 5$

#### Решение
##### Пункт а
Функция ограничитель: $\phi(x, y, z) = x^2 + y^2 + z^2 - 1$
Выпишем функцию Лагранжа:
$$
	L(x, y, z) = f + \lambda \phi
$$
Найдем стационарные точки:
$$
\begin{cases}
	L'_{x} = \sqrt{3} + 2x \lambda = 0 \\[3mm]
	L'_{y} = 3 + 2y \lambda = 0 \\[3mm]
	L'_{z} = 2 + 2z\lambda = 0 \\[3mm]
	L'_{\lambda} = x^2 + y^2 + z^2 - 1 = 0
\end{cases}
$$
Решим систему и получим:
$P_1 = (-\frac{\sqrt{3}}{4}, -\frac{3}{4}, -\frac{1}{2})$ с $\lambda = 2$
$P_2 = (\frac{\sqrt{3}}{4}, \frac{3}{4}, 1)$ с $\lambda = -2$ 

Как и в предущей задачи мы решим задачу критерием Сильвестра, составим матрицу:
$$
\begin{pmatrix}
	f''_{xx} & f''_{xy} & f''_{xz} \\
	f''_{yx} & f''_{yy} & f''_{yz} \\
	f''_{zx} & f''_{zy} & f''_{zz} 
\end{pmatrix} = \begin{pmatrix}
	2\lambda & 0 & 0 \\
	0 & 2 \lambda & 0 & \\
	0 & 0 & 2 \lambda
\end{pmatrix}
$$
видно, что невырожденная матрица либо положительно либо отрицательно определенная при любых условиях, поэтому даже не смотря на значение $d\phi$, можно сразу выписать ответ:

$P_1$ - точка локального условного минимума
$P_2$ - точка локального условного максимума

%%PDF break%% <div style="page-break-after: always;"></div>
##### Пункт б
$$
	\phi(x, y, z) = z^2 - 6z + 5 - xy
$$
$$
L = f + \lambda \phi
$$
$$
\begin{cases}
L'_{x} = 2x - y \lambda = 0 \\[3mm]
L'_{y} = 2y - x \lambda = 0 \\[3mm]
L'_{z} = 2z + 2z \lambda - 6\lambda = 0 \\[3mm]
L'_{\lambda} = z^2 - 6z + 5 - xy = 0
\end{cases}
$$
Решаем, получаем:
$P_1 = (0, 0, 1), \lambda = \frac{1}{2}$
$P_2 = (0, 0, 5), \lambda = -\frac{5}{2}$

составим матрицу:

тут уже не так очевидно, выпишем вторые дифференциалы:
$$
\begin{cases}
	d^2 L = 2 dx^2 - 2\lambda dx dy + 2 dy^2 + (2 + 2\lambda)dz^2 \\
	d \phi = -y dx - x dy + (2z - 6)dz = 0
\end{cases}
$$

**Подставим точки:**

$$
P_1 = (0, 0, 1) : \begin{cases}
	d^2 L = 2 dx^2 - 2\lambda dx dy + 2 dy^2 + (2 + 2\lambda)dz^2 \\
	d \phi = (2 - 6)dz = 0 \RR dz = 0
\end{cases} \RR 
	 d^2 L = 2dx^2 - 2\lambda dx dy + 2 dy^2
$$
выпишем матрицу:
$$
\begin{pmatrix}
2 & -\lambda \\
-\lambda & 2
\end{pmatrix} \RR \begin{cases}
\sigma_1 = 2 \\
\sigma_2 = 4 - \lambda^2 = 4 - \frac{1}{4} > 0
\end{cases} \RR \min
$$

$$
P_2=(0, 0, 5) : \begin{cases}
	d^2 L = 2 dx^2 - 2\lambda dx dy + 2 dy^2 + (2 + 2\lambda)dz^2 \\
	d \phi = (10 - 6)dz = 0 \RR dz = 0
\end{cases} \RR 
	 d^2 L = 2dx^2 - 2\lambda dx dy + 2 dy^2
$$
выпишем матрицу:
$$
\begin{pmatrix}
2 & -\lambda \\
-\lambda & 2
\end{pmatrix} \RR \begin{cases}
\sigma_1 = 2 \\
\sigma_2 = 4 - \lambda^2 = 4 - \frac{25}{4} < 0
\end{cases} \RR \max
$$
**Ответ:**
$P_1$ - локальный условный минимум, $P_2$ - локальный условный максимум