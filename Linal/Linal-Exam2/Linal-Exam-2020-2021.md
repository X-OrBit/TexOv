![[template]]
# Линейная алгебра и геометрия

## Разбор экзамена 2020-2021
## Вариант 1

### Задача 1
#### Условие
Определите все значения, которые может принимать размерность пересечения ядра и образа линейного оператора $\phi : \R^{4} \to \R^{4}$ при условии, что в ядре содержится вектор $v = (1, 0, -1, 2)$

#### Решение [@azakarka]
Ключевой факт: $\dim \ker \phi + \dim \Im \phi = 4$ 
$\dim (\ker \phi \cap \Im \phi) \leq \min(\dim \ker \phi, \dim \Im \phi)$ 
Поэтому $0 \leq \dim (\ker \phi \cap \Im \phi) \leq 2$ 

Это была оценка, теперь примеры:

0) $\phi: \forall u \in \R^{4}, u\mapsto 0$ 
1) $(v, e_{1}, e_{2}, e_{3})$ - базис в $\R^4$, тогда $\phi : \begin{cases} v \mapsto 0 \\ e_{1} \mapsto v \\ e_{2}\mapsto e_{1} \\ e_{3} \mapsto e_{2}\end{cases}$
2) $(v, u, e_{1}, e_{2})$ - базис в $\R^{4}$, тогда $\phi : \begin{cases} v,u \mapsto 0 \\ e_{1} \mapsto v \\ e_{2} \mapsto u\end{cases}$ 
**Ответ:** $\{0, 1, 2\}$

### Задача 2
#### Условие
Определите нормальный вид квадратичной формы $Q(x, y, z) = x^{2} + ay^{2} + z^{2} + 4xy - 4xz - 8yz$ 

%%PDF break%% <div style="page-break-after: always;"></div>

#### Решение [@azakarka]
Сделаем замену координат: $\begin{cases} x' = x \\ y' = z  \\ z' = y\end{cases}$ 
Тогда матрица квадратичной формы $B(Q(x', y', z'))$ выглядит так:
$$
\begin{pmatrix} 
 1 & -2 & 2  \\ -2 & 1 & -4  \\  2 & -4 & a
\end{pmatrix}
$$
Решим задачу методом Якоби:
$$
\begin{cases}
\delta_{1} = 1 \\
\delta_{2} = 1 - 4 = -3 \\
\delta_{3} = a + 16 + 16 - 4 - 16 - 4a = -3a + 12
\end{cases}
$$
согласно методу после замены координат канонический вид выглядит так: $\delta_{1} (x'')^{2} + \frac{\delta_{2}}{\delta_{1}} (y'')^{2} + \frac{\delta_{3}}{\delta_{2}} (z'')^{2}$ 

то есть канонический (а значит и нормальный) вид зависит только от значения $-3a + 12$, переберем случаи:

1) $-3a + 16 > 0 \RR a < 4$, $(x'')^{2} - (y'')^{2} - (z'')^{2}$ 
2) $-3a + 16 = 0 \RR a = 4$, $(x'')^{2} - (y'')^{2}$ 
3) $-3a + 16 < 0 \RR a > 4$, $(x'')^{2} - (y'')^{2} + (z'')^{2}$ 


### Задача 3
#### Условие 
В четырёхмерном евклидовом пространстве $\E$ даны векторы $v_1, v_2, v_3$. Известно, что матрица Грама векторов $v_1, v_2$ равна $\begin{pmatrix}4&3\\3&5\end{pmatrix}$, вектор $v_3$ имеет длину $10$ и его ортогональная проекция $\hull{v_1, v_2}$ равна $2v_1 - v_2$. Найдите объём параллелепипеда, натянутого на векторы $v_1, v_2, v_3$.

#### Решение [@dsalakhov]
Сначала найдём матрицу Грама для всей системы векторов:
$$
\begin{multline*}
		(v_3, v_1) = (\pr v_3 + \ort v_3, v_1) = (\pr v_3, v_1) + \underbrace{(\ort v_3, v_1)}_{=0} =\\= (2v_1 - v_2, v_1) = 2(v_1, v_1) - (v_2, v_1) = 2 \cdot 4 - 3 = 5
	\end{multline*}
$$
$(v_3, v_2) = \dotsc = 2(v_1, v_2) - (v_2, v_2) = 2 \cdot 3 - 5 = 1$
$(v_3, v_3) = |v_3|^2 = 10^2 = 100$
Отсюда, матрица Грама:
$$
G = \begin{pmatrix}
	4 & 3 & 5 \\
	3 & 5 & 1 \\
	5 & 1 & 100 \\
\end{pmatrix}
$$
$\vol P(v_1, v_2, v_3)^2 = \det G \RR \vol P(v_1, v_2, v_3) = \sqrt{\det G}$
$$
\begin{multline*}
	\det G = \begin{vmatrix}
		4 & 3 & 5 \\
		3 & 5 & 1 \\
		5 & 1 & 100 \\
	\end{vmatrix} = 4 \cdot 5 \cdot 100 + 5 \cdot 3 \cdot 1 + 5 \cdot 3 \cdot 1 - 5^3 - 3^2 \cdot 100 - 4 \cdot 1^2 =\\
	= 2000 + 15 + 15 - 125 - 900 - 4 = 1001
	\end{multline*}
$$
**Ответ:** $\sqrt{1001}$


### Задача 4
#### Условие 
Приведите пример недиагонализуемого линейного оператора $\phi$ в $\R^2$, для которого оператор $\phi^2 - 3\phi$ диагонализуем.

#### Решение [@dsalakhov]
Оператор $\phi$ в $\R^2$ не диагонализуем, значит, в каноническом виде это жорданова клетка размера $2$ вида: $\begin{pmatrix}x&1\\0&x\end{pmatrix}$
Считаем $\phi^2 - 3\phi$:
$$
\phi^2 - 3\phi = \begin{pmatrix}
	x & 1 \\
	0 & x \\
\end{pmatrix}^2 - 3\begin{pmatrix}
	x & 1 \\
	0 & x \\
\end{pmatrix} = \begin{pmatrix}
	x^2 & 2x \\
	0 & x^2 \\
\end{pmatrix} - \begin{pmatrix}
	3x & 3 \\
	0 & 3x \\
\end{pmatrix} = \begin{pmatrix}
	x(x - 3) & 2x - 3 \\
	0 & x(x - 3) \\
\end{pmatrix}
$$
Тогда полученный оператор $\phi^2 - 3\phi$ диагонализуем, если $2x - 3 = 0 \RR x = \cfrac{3}{2}$
**Ответ:** $\begin{pmatrix}1.5 & 1\\0 & 1.5\end{pmatrix}$


### Задача 5
#### Условие
Про ортогональный линейный оператор $\phi : \R^{3} \to \R^{3}$ известно, что $\phi((1, -1, 1)) = (-1, 1, -1), \phi((2, 0, 1)) = (-2, 1, 0)$ и $\phi$ не самосопоряжен. Найдите ортонормированный базис, в котором матрица оператора $\phi$ имеет канонический вид, и выпишите эту матрицу.

#### Решение [@azakarka]
Так как $\phi$ - ортогональный, не самосопряженный оператор, то $\exists e$ - ОНБ, в котором:
$$
A(\phi, e) = \begin{pmatrix}
\cos \alpha & -\sin \alpha & 0 \\
\sin \alpha & \cos \alpha & 0 \\
0 & 0 & \pm 1
\end{pmatrix}
$$
Заметим, что $(1, -1, 1)$ - собственный вектор, с собственным значением $-1$, обозначим $e_{3} = \frac{1}{\sqrt{3}}(1, -1, 1)$

Теперь дальше по алгоритму, найдем $(e_{1}, e_{2})$ - базис в $\langle e_{3} \rangle^{\perp}$ 
$$
 (1, -1, 1) \RR ((1, 1, 0), (-1, 1, 2))
$$
$e_{1} = \frac{1}{\sqrt{2}}(1, 1, 0), e_{2} = \frac{1}{\sqrt{6}}(-1, 1,2)$ 

$$
\phi \begin{pmatrix} 2\\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} e_1 & e_2 & e_3 \end{pmatrix} A \begin{pmatrix} x_{1} \\ x_{2} \\ x_{3}\end{pmatrix}  = \begin{pmatrix} -2 \\ 1 \\ 0 \end{pmatrix}
$$

найдем координаты вектора в $e$, заметим, что $(2, 0, 1) = \sqrt{2}e_{1} + \sqrt{3} e_{3}$, откуда $(x_{1}, x_{2}, x_{3}) = (\sqrt{2}, 0, \sqrt{3})$. Теперь для $(-2, 1, 0) = ((-2, 1, 0), e_{1})e_{1} + ((-2, 1, 0), e_{2})e_{2} + ((-2, 1, 0), e_{3})e_{3}$, откуда можем вытащить координаты и получить систему

$$
\begin{cases}
\sqrt{2} \cos \alpha = ((-2, 1, 0), e_{1}) = -\frac{1}{\sqrt{2}} \\
\sqrt{2} \sin \alpha = ((-2, 1, 0), e_{2}) = \frac{\sqrt{3}}{\sqrt{2}} \\
-\sqrt{3} = ((-2, 1, 0), e_{3}) = -\sqrt{3}

\end{cases} \RR \begin{cases}
\cos \alpha = -\frac{1}{2} \\
\sin \alpha = \frac{\sqrt{3}}{2}
\end{cases}
$$

**Ответ:** в базисе $(e_{1}, e_{2}, e_{3})$ оператор $\phi$ имеет матрицу:
$$
\begin{pmatrix}
-\frac{1}{2} & -\frac{\sqrt{3}}{2} & 0 \\
\frac{\sqrt{3}}{2} & -\frac{1}{2} & 0 \\
0 & 0 & -1
\end{pmatrix}
$$


### Задача 6
#### Условие 
Существует ли матрица $A \in \Mat_{2\times3}(\R)$ ранга $2$ со следующими свойствами:
1) одно из сингулярных значений матрицы $A$ равно $\sqrt{50}$;
2) ближайшая к $A$ по норме Фробениуса матрица ранга $1$ есть $B = \begin{pmatrix}3&-6&3\\1&-2&1\end{pmatrix}$?
Если существует, то предъявите такую матрицу.

#### Решение [@dsalakhov]
Сингулярное разложение ранга $1$ имеет вид:
$v \cdot \Sigma \cdot u^T$, где $v \in \Mat_{2 \times 1}, u \in \Mat_{3 \times 1}$
Для $B$ легко находятся (пока не ортонормированные) $v = (3, 1)$ и $u = (1, -2, 1)$ и $\Sigma = (1)$
Чтобы получить корректное сингулярное разложение, $v$ и $u$ должны быть ортонормированы, поэтому $v \leadsto \frac{1}{\sqrt{10}}(3, 1), u \leadsto \frac{1}{\sqrt{6}}(1, -2, 1)$, тогда $\sigma_1 = \sqrt{60}$
При нахождении ближайших матриц по норме Фробениуса, нужно "отбрасывать" наименьшие сингулярные значения. Тогда $\sigma_1$ должен быть наибольшим сингулярным значением (т.к. при в ближайшей матрице ранга $1$ он остался), а значит остальные сингулярные значения меньше $\sqrt{60} \RR$ условие $1$ выполняется.
Ортогональный вектор к $v$: $\frac{1}{\sqrt{10}} (-1, 3)$, теперь нужен ортогональный вектор к $u$, что его длина до ортонормирования равна $\sqrt{5}$, например $(2, 1, 0) \leadsto \frac{1}{\sqrt{5}}(2, 1, 0)$
Получаем сингулярное разложение для $A$:
$$
A = \begin{pmatrix}
	\frac{3}{\sqrt{10}} & -\frac{1}{\sqrt{10}} \\
	\frac{1}{\sqrt{10}} & \frac{3}{\sqrt{10}} \\
\end{pmatrix}
\cdot
\begin{pmatrix}
	\sqrt{60} & 0 \\
	0 & \sqrt{50} \\
\end{pmatrix}
\cdot
\begin{pmatrix}
	\frac{1}{\sqrt{6}} & -\frac{2}{\sqrt{6}} & \frac{1}{\sqrt{6}} \\
	\frac{2}{\sqrt{5}} & \frac{1}{\sqrt{5}} & 0 \\
\end{pmatrix} = \begin{pmatrix}
	1 & -7 & 3 \\
	7 & 1 & 1
\end{pmatrix}
$$
**Ответ:** $\begin{pmatrix}1 & -7 & 3 \\7 & 1 & 1\end{pmatrix}$

### Задача 7
#### Условие 
Найдите все значения параметра $a$, при которых уравнение
$$2y^2 - 3z^2 + 4xz - 12y + a = 0$$
определяет однополостный гиперболоид в $\R^3$. Для каждого найденного значения $a$ укажите прямоугольную декартову систему координат в $\R^3$ (выражение старых координат через новые), в которых данное уравнение принимает канонический вид.

%%PDF break%% <div style="page-break-after: always;"></div>

#### Решение [@dsalakhov]
Сначала приведём квадратичную форму к главным осям:
$A = \begin{pmatrix}0 & 0 & 2 \\0 & 2 & 0 \\2 & 0 & -3 \end{pmatrix}$

$$\chi(t) = (-1)^3 \begin{vmatrix}
	-t & 0 & 2 \\
	0 & 2 - t & 0 \\
	2 & 0 & -3 - t \\
\end{vmatrix} = -((-t)(2 - t)(-3 - t) - 2^2(2 - t)) = (t - 2)(t + 4)(t - 1)
$$
$$\lambda = 2, \qquad A - \lambda E = \begin{pmatrix}
	-2 & 0 & 2 \\
	0 & 0 & 0 \\
	2 & 0 & -5 \\
\end{pmatrix} \rev \begin{pmatrix}
	1 & 0 & 0 \\
	0 & 0 & 1 \\
	0 & 0 & 0 \\
\end{pmatrix} \RR v_1 = (0, 1, 0)$$
$$\lambda = 1, \qquad A - \lambda E = \begin{pmatrix}
	-1 & 0 & 2 \\
	0 & 1 & 0 \\
	2 & 0 & -4 \\
\end{pmatrix} \rev \begin{pmatrix}
	1 & 0 & -2 \\
	0 & 1 & 0 \\
	0 & 0 & 0 \\
\end{pmatrix} \RR v_2 = (2, 0, 1) \leadsto \frac{1}{\sqrt{5}} (2, 0, 1)$$
$$\lambda = -4, \qquad A - \lambda E = \begin{pmatrix}
	4 & 0 & 2 \\
	0 & 6 & 0 \\
	2 & 0 & 1 \\
\end{pmatrix} \rev \begin{pmatrix}
	1 & 0 & 1/2 \\
	0 & 1 & 0 \\
	0 & 0 & 0 \\
\end{pmatrix} \RR v_3 = (-1, 0, 2) \leadsto \frac{1}{\sqrt{5}} (-1, 0, 2)$$
$$
C = \begin{pmatrix}
	0 & 2/\sqrt{5} & -1/\sqrt{5} \\
	1 & 0 & 0 \\
	0 & 1/\sqrt{5} & 2/\sqrt{5}\\
\end{pmatrix} \RR \begin{cases}
	x = \frac{2y^\prime}{\sqrt{5}} - \frac{z^\prime}{\sqrt{5}} \\
	y = x^\prime\\
	z = \frac{y^\prime}{\sqrt{5}} + \frac{2z^\prime}{\sqrt{5}}
\end{cases}
$$

Получаем: $2y^2 - 3z^2 + 4xz - 12y + a = 2(x^\prime)^2 + (y^\prime)^2 - 4(z^\prime)^2 - 12x^\prime + a = 0$

Теперь выделяем квадраты и приводим к каноническому виду:
$$
\begin{multline*}
	2(x^\prime)^2 + (y^\prime)^2 - 4(z^\prime)^2 - 12x^\prime + a = 2((x^\prime)^2 - 6x^\prime) + (y^\prime)^2 - 4(z^\prime)^2 + a =\\
	2\underbrace{(x^\prime - 3)^2}_{=(x^\pprime)^2} - 18 + (y^\prime)^2 - 4(z^\prime)^2 + a = 2(x^\pprime)^2 + (y^\pprime)^2 - 4(z^\pprime) + a - 18 = 0
\end{multline*}
$$
Уравнение однополостного гиперболоида имеет вид: $\cfrac{x^2}{a^2} + \cfrac{y^2}{b^2} - \cfrac{z^2}{c^2} = 1$
В нашем случае: $2(x^\pprime)^2 + (y^\pprime)^2 - 4(z^\pprime)^2 = 18 - a$
Получаем условие $18 - a > 0 \RR a < 18$
Выразим старые координаты через новые:
$$
\begin{cases}
	x = \frac{2y^\pprime}{\sqrt{5}} - \frac{z^\pprime}{\sqrt{5}} \\
	y = x^\pprime + 3 \\
	z = \frac{y^\pprime}{\sqrt{5}} + \frac{2z^\pprime}{\sqrt{5}}
\end{cases}
$$
**Ответ:** $a < 18$, замена выше

### Задача 8
#### Условие
Линейный оператор $\phi: \R^{4} \to \R^4$ имеет в стандартном базисе матрицу
$$
\begin{pmatrix}
4 & 0 & 0 &-2 \\
-5 & 3 & 2 & 6 \\
2 & 0 & 3 & 2 \\
1 & 0 & 0 & 1
\end{pmatrix}
$$
Найдите базис пространства $\R^4$, в котором матрица оператора $\phi$ имеет жорданову форму, и укажите эту жорданову форму. 

#### Решение [@azakarka]
$$
\displaylines{
\det \begin{pmatrix}
4-t & 0 & 0 &-2 \\
-5 & 3-t & 2 & 6 \\
2 & 0 & 3-t & 2 \\
1 & 0 & 0 & 1-t
\end{pmatrix} = (3 - t) \cdot 
\det \begin{pmatrix}
4-t & 0 &-2 \\
2 & 3-t & 2 \\
1 & 0 & 1-t
\end{pmatrix} = \\ =(3 - t)^{2} \cdot 
\det \begin{pmatrix}
4-t & -2 \\
1 & 1-t
\end{pmatrix} = (3 - t)^{2} (t^{2} - 5t + 4 + 2) = (t - 3)^{3}(t - 2)
}
$$
У нас два различных собственных значения, поэтому нам нужно найти базис в $V^{3}$ и ограничить на него наш оператор. Для этого введем 
$$
B = A - 3E = \begin{pmatrix}
1 & 0 & 0 &-2 \\
-5 & 0 & 2 & 6 \\
2 & 0 & 0 & 2 \\
1 & 0 & 0 & -2
\end{pmatrix}
$$
и найдем $\ker B^3$ что и будет нужным базисом:
$$
\displaylines{
B = \begin{pmatrix}
1 & 0 & 0 &-2 \\
-5 & 0 & 2 & 6 \\
2 & 0 & 0 & 2 \\
1 & 0 & 0 & -2
\end{pmatrix}, B^{2} = \begin{pmatrix}
-1 & 0 & 0 & 2 \\ 
5 & 0 & 0 & 2 \\
4 & 0 & 0 & -8 \\
-1 & 0 & 0 & 2
\end{pmatrix}, B^{3} = 
\begin{pmatrix}
1 & 0 & 0 & -2 \\
7 & 0 & 0 & -14 \\
-4 & 0 & 0 & 8 \\
1 & 0 & 0 & -2
\end{pmatrix} \RR \\\RR \ker B^{3}= \langle (0, 1, 0, 0),(0, 0, 1, 0),(2, 0, 0, 1)\rangle}
$$
заметим теперь, что rk$B = 1$, значит у нас ровно одна жорданова клетка с $\lambda = 3$, а значит нам просто нужно взять в найденном базисе вектор высоты 3, найдем:
$$
(0, 1, 0, 0) \overset{B}{\mapsto} 0 
$$
$$
(0, 0, 1, 0) \mapsto (0, 2, 0, 0) \mapsto (0, 0, 0, 0)
$$
$$
(2, 0, 0, 1) \mapsto (0, -4, 6, 0) \mapsto (0, 12, 0 ,0) \mapsto (0, 0, 0, 0)
$$

Теперь найдем собственный вектор для $\lambda = 2$:
$$
A - 2E = \begin{pmatrix}
2 & 0 & 0 &-2 \\
-5 & 1 & 2 & 6 \\
2 & 0 & 1 & 2 \\
1 & 0 & 0 & -1
\end{pmatrix} \to 
\begin{pmatrix}1&0&0&-1\\ 0&1&0&-7\\ 0&0&1&4\\ 0&0&0&0\end{pmatrix} \RR (1, 7, -4, 1)
$$

**Ответ:**
в базисе $(0, 12, 0, 0), (0, -4, 6, 0), (2, 0, 0, 1), (1, 7, -4, 1)$ оператор принимает вид
$$
\begin{pmatrix}
3 & 1 & 0 & 0 \\
0 & 3 & 1 & 0 \\
0 & 0 & 3 & 0 \\
0 & 0 & 0 & 2
\end{pmatrix}
$$