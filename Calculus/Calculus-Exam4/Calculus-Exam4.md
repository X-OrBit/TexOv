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
b = \frac{1}{3}(-1, 2, 2)$$
$$
\frac{\p f}{\p b} = \frac{1}{3} \l(-\frac{\p f}{\p x} + 2\cdot \frac{\p f}{\p y} + 2 \cdot \frac{\p f}{\p z}\r)
$$
$$
\begin{cases}
\frac{\p f}{\p x} = \frac{2x}{x^2 + y^2 + z^2}\\[3mm]
\frac{\p f}{\p y} = \frac{2y}{x^2 + y^2 + z^2} \\[3mm]
\frac{\p f}{\p z} = \frac{2z}{x^2 + y^2 + z^2}
\end{cases}
$$
$$
	\frac{\p f}{\p b} = \frac{1}{3(x^2 + y^2 + z^2)} \cdot \l(-2x + 4y + 4z \r)
$$
$$
\frac{\p f}{\p b} \atpoint{(3, 3, 1)} = \frac{10}{3\cdot 19} = \frac{10}{57}
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
F'_{x}(1; 1; 2e) = e + e + e \\[3mm]
F'_{y}(1;1;2e) = e + e + e \\[3mm]
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
	12(x - 2) + 2(y - 1) - 6(z - 3) = 0 \RR 6x + y - 3z = 3
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
	\phi'_{u} \cdot y + \phi'_{v} \cdot 2x^2 \\[3mm]

\frac{\p f}{\p y} = \frac{\p \phi}{\p u} \cdot \frac{\p u}{\p y} + \frac{\p \phi}{\p v} \cdot \frac{\p v}{\p y} = \phi'_{u} \cdot x + \phi'_{v} \cdot 2y
}
$$

Тогда
$$
df = \frac{\p f}{\p x} dx + \frac{\p f}{\p y} dy = (\phi'_u \cdot y + \phi'_v \cdot 2x^2)dx + (\phi'_{u} \cdot x + \phi'_v \cdot 2y) dy
$$

Первый дифференциал нашли, поищем вторые:
(так как $\phi$ дважды дифференцируема по Шварцу смешанные производные равны)
$$
\displaylines{
f''_{xx} = \frac{\p}{\p x} (f'_{x}) = \frac{\p }{\p x} (\phi'_{u} \cdot y + \phi'_{v} \cdot 2x^2)
 = y \cdot (\phi''_{u u} \cdot \frac{\p u}{\p x} + \phi''_{uv} \frac{\p v}{\p x}) + \\
+ 4x \cdot \phi'_{v} + 2x^2 \cdot (\phi''_{vu} \cdot \frac{\p u}{\p x} + \phi''_{vv} \cdot \frac{\p v}{\p x}) = \\
 = xy \phi''_{uu} + 4x \phi'_{v} + 4x^2y \phi''_{uv} + 4x^4 \phi''_{vv}
}
$$

$$
\displaylines{
	\phi''_{xy} = \phi''_{yx} = \frac{\p}{\p x} (f'_{y}) = \frac{\p}{\p x} (\phi'_{u} \cdot x + \phi'_{v} \cdot 2y) = \\
	= \phi'_{u} + x (\phi''_{uu} \cdot \frac{\p u}{\p x} + \phi''_{vu} \cdot \frac{\p v}{\p x}) + 2y (\phi''_{uv} \cdot \frac{\p u}{\p x} + \phi''_{vv} \cdot \frac{\p v}{\p x}) = \\
	\phi'_{u} + xy \phi''_{uu} + 3x^3 \phi''_{vu} + 2xy \phi''_{uv} + 6x^2 y \phi''_{vv} = \\ f'_{u} + xy \phi''_{uu} + x \phi''_{vu}(3x^2 + 2y) + 6x^2 y \phi''_{vv}
}
$$

$$
\displaylines{
f''_{yy} = \frac{\p}{\p y} (\f'_{y}) = \frac{\p}{\p y} (\phi'_u \cdot x + \phi'_v \cdot 2y) = x (\phi''_{uu} \cdot \frac{\p u}{\p y} + \phi''_{uv} \cdot \frac{\p v}{\p y}) + 2\phi'_{v} + 2y (\phi''_{vu} \cdot \frac{\p u}{\p y} + \phi''_{vv} \cdot \frac{\p v}{\p y}) =  \\
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

<<<<<<< HEAD
> TODO
=======
Приведем все к стандартному виду:
$$
\begin{cases}
	F_1(x, y, v, u, z) = x - v \sin u = 0 \\
	F_2(x, y, v, u, z) = y - v \cos u = 0 \\
	F_3(x, y, v, u, z) = z - uv^2 = 0
\end{cases}
$$
Мы знаем только значения $v = 1, u = \frac{\pi}{4}$ найдем все остальные значения в точке.
$$
	x = \frac{\sqrt{2}}{2}, y = \frac{\sqrt{2}}{2}, z = \frac{\pi}{4}
$$
$$
	P = (\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}, 1, \frac{\pi}{4}, \frac{\pi}{4})
$$

Выпишем матрицу, которая используется в теореме о неявном отображении:
$$
\begin{pmatrix}
	\frac{\p F_1}{\p v}& \frac{\p F_2}{\p v} & \frac{\p F_3}{\p v} \\
	\frac{\p F_1}{\p u} & \frac{\p F_2}{\p u} & \frac{\p F_3}{\p u} \\
	\frac{\p F_1}{\p z} & \frac{\p F_3}{\p z} & \frac{\p F_3}{\p z} 
\end{pmatrix}\atpoint{P} = 
\begin{pmatrix}
	-\sin u & -\cos u & - 2uv \\
	- v \cos u & v \sin u & v^2 \\
	0 & 0 & 1
\end{pmatrix} \atpoint{P} = 
\begin{pmatrix}
	-\frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} & - \frac{\pi}{2} \\
	- \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} & 1 \\
	0 & 0 & 1
\end{pmatrix}
$$
не тяжело увидеть что определитель не нулевой, матрица обратима.

Тогда применим теорему о неявном отображении:
$$
\exists f_1, f_2, f_3: 
\begin{cases}
	v = f_1(x, y) \iff x = v \sin u\\
	u = f_2(x, y) \iff y = v \cos u\\
	z = f_3(x, y) \iff z = uv^2
\end{cases}
$$
$$
dz = d(uv^2) = (v^2 \cdot u'_x + 2uv \cdot v'_x)dx + (v^2 \cdot u'_y + 2uv \cdot v'_y)dy
$$
$$
\begin{cases}
	1 = \sin u \cdot v'_{x} + v \cos u \cdot u'_x\\
	0 = \cos u \cdot v'_{x} - v \sin u \cdot u'_x
\end{cases} \atpoint{P} = \begin{cases}
	1 = \frac{\sqrt{2}}{2} (v'_x + u'_x) \\
	0 = \frac{\sqrt{2}}{2} (v'_x - u'_x) 
\end{cases} \RR
\begin{cases}
v'_x = \frac{\sqrt{2}}{2} \\
u'_x = \frac{\sqrt{2}}{2}
\end{cases}
$$

подставим в дифференциал
$$
\displaylines{
dz \atpoint{P} = (u'_x + \sqrt{2} v'_x)dx + (u'_y + \sqrt{2} v'_y)dy =
\\
= (\frac{\sqrt{2}}{2} + 1)dx + (\frac{\sqrt{2}}{2} + 1)dy
}
$$
теперь найдем $\frac{\p^2 z}{\p x \p y}$ 

$$
\displaylines{
\frac{\p z}{\p x} (z'_{u} \cdot u'_{y} + z'_{v} \cdot v'_{y}) = \frac{\p z}{\p x} (v^2 \cdot u'_{y} + 2uv \cdot v'_y) = \\
2v \cdot v'_{x} \cdot u'_{y} + v^2 \cdot (u''_{yx}) + 2u \cdot u'_{x} \cdot v \cdot v'_{y} + 2u v \cdot v'_{x} \cdot v'_{y} + 2uv \cdot v''_{yx} 
}
$$
нужно теперь найти первые частные производные по $y$ и смешанные производные
$$
\begin{cases}
0 = \sin u \cdot v'_{y} + v \cos u \cdot u'_y \\
1 = \cos u \cdot v'_{y} - v \sin u \cdot  u'_y 
\end{cases} \RR 
\begin{cases}
0 = v'_y + u'_y \\
\sqrt{2} = v'_y - u'_y
\end{cases} \RR \begin{cases}
	v'_{y} = \frac{\sqrt{2}}{2} \\
	u'_{y} = -\frac{\sqrt{2}}{2}
\end{cases}
$$
$$
\RR \begin{cases}
0 = \cos u \cdot u'_{x} + \sin u \cdot v''_{yx} + v'_{x} \cdot \cos u \cdot u'_{y} - v \sin u \cdot u'_{x} \cdot u'_{y} + v \cos u \cdot u''_{yx} \\
1 = -\sin u \cdot u'_{x} v'_{y} + \cos u \cdot v''_{yx} - v'_{x} \sin u \cdot u'_{y} - v \cos u \cdot u'_{x} u'_{y} - v \sin u u''_{yx}
\end{cases} \RR
$$
$$
\begin{cases}
0 = \frac{\sqrt{2}}{2} + v''_{yx} - \frac{1}{2} + \frac{1}{2} + u''_{yx} \\
\sqrt{2} = - \frac{1}{2} + v''_{yx} + \frac{1}{2} + \frac{1}{2} - u''_{yx}
\end{cases} \RR \begin{cases}
-\frac{\sqrt{2}}{2} = v''_{yx} + u''_{yx} \\
\frac{2\sqrt{2} + 2}{2} = v''_{yx} - u''_{yx}
\end{cases} \RR
\begin{cases}
v''_{yx} = \frac{\sqrt{2} + 2}{4} \\
u''_{yx} = \frac{-3\sqrt{2} - 2}{4}
\end{cases}
$$

вернемся к нахождению:
$$
\frac{\p^2 z}{\p x \p y} \atpoint{P} = \frac{1}{2} (-\sqrt{2} + \frac{-3\sqrt{2} - 2}{4} + \sqrt{2} + \frac{\pi}{2} + \frac{\sqrt{2} + 2}{4}\pi)
$$

>>>>>>> a3296af (5th task and 4 improvments)

### Задача 6
#### Условие
Найдите все точки локального экстремума функции
$$
 f(x, y) = 2x^3 - 6xy - 3y^2 + 12y
$$

#### Решение

Найдем всех кандидатов, то есть точки, в которых дифференциал равен 0:
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
$$
	F = x^2 + y^2 + z^2 - 1
$$
$$
	L(x, y, z) = f(x, y, z) + \lambda F(x, y, z)
$$
найдем кандидатов на точку локального экстремума:
$$
\begin{cases}
	L'_{x} = \sqrt{3} + 2x \lambda = 0 \\[3mm]
	L'_{y} = 3 + 2y \lambda = 0 \\[3mm]
	L'_{z} = 2 - 2z\lambda = 0 \\[3mm]
	L'_{\lambda} = x^2 + y^2 + z^2 - 1 = 0
\end{cases}
$$
Решим систему и получим:

$P_1 = (-\frac{\sqrt{3}}{2}, \frac{-3}{2}, 1)$ с $\lambda = 1$
$P_2 = (\frac{\sqrt{3}}{2}, \frac{3}{2}, -1)$ с $\lambda = -1$ 

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
видно, что невырожденная матрица либо положительно либо отрицательно определенная при любых условиях, поэтому даже не смотря на значение $dF$, можно сразу выписать ответ:

$P_1$ - точка локального условного минимума
$P_2$ - точка локального условного максимума

##### Пункт б
$$
	F = z^2 - 6z + 5 - xy
$$
$$
L = f + \lambda F
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
$P_1 = (0, 0, 5), \lambda = \frac{1}{5}$
$P_2 = (0, 0, 1), \lambda = 5$

составим матрицу:

тут уже не так очевидно, выпишем вторые дифференциалы:
$$
\begin{cases}
	d^2 L = 2 dx^2 - 2\lambda dx dy + 2 dy^2 + (2 + 2\lambda)dz^2 \\
	d F = -y dx - x dy + (2z - 6)dz = 0
\end{cases}
$$

Подставим точки:
$$
P_1=(0, 0, 5) : \begin{cases}
	d^2 L = 2 dx^2 - 2\lambda dx dy + 2 dy^2 + (2 + 2\lambda)dz^2 \\
	d F = (10 - 6)dz = 0
\end{cases} \RR 
	 dx^2 - 2\lambda dx dy + 2 dy^2
$$
выпишем матрицу:
$$
\begin{pmatrix}
1 & -\lambda \\
-\lambda & 2
\end{pmatrix} \RR \begin{cases}
\sigma_1 = 1 \\
\sigma_2 = 2 - \lambda^2 = 2 - \frac{1}{25} > 0
\end{cases} \RR \min
$$

для точки $P_2$ будет тоже самое, кроме $\lambda$, получится уже неопределенная матрица

**Ответ:**
$P_1$ - точка локального условного минимума