![[template_latex]]
![[template_channel_info]]
**!!! Attention, могут быть ошибки**

# CheatSheet по Теорверу
## Матожидание&Дисперсия&Ковариация&Момент
### Матожидание
$$
\displaylines{
	\E \xi = \Sum{a 
	\in A = \xi(\Omega)}{} aP(\xi = a) \\
	\E \xi = \inti{-\infty}{\infty} xp_\xi(x) dx \\
	\E f(\xi_1, \dotsc, \xi_n) = \multint{\R^n} f(x_1, \dotsc, x_n) p_{\xi_1, \dotsc, x_n}(x_1, \dotsc, x_n) dx_1, \dotsc dx_n
}
$$
### Свойства матожидания
#### Для дискретной с.в.
$$
\displaylines{
	\E(a\xi + b \eta) = a\E\xi + b \E \eta \\
	\forall w \quad \xi(w) \le \eta(w) \RR \E \xi \le \E \eta \\
	|\E \xi| \le \E |\xi| \\
	\E f(\xi) = \Sum{a \in A = \xi(\Omega)}{} f(a) P(\xi = a) \\
	\xi, \eta - \text{независимые с.в} \RR \E (\xi\eta) = \E \xi \E \eta
}$$
#### В общем случае
$$
\displaylines{
	\E(a\xi + b \eta) = a\E\xi + b \E \eta \\
	\xi \le \eta \RR \E \xi \le \E \eta \\
	|\E \xi| \le \E |\xi| \\
	\xi, \eta - \text{независимые/некоррел. с.в} \RR \E (\xi\eta) = \E \xi \E \eta \\
	f(x) - \text{борелл. функция} \RR \E f(\xi) = \inti{-\infty}{\infty} f(x) p_\xi(x) dx \\
	|\E \xi \eta| \le \sqrt{\E \xi^2 \E \eta^2}, \qquad |\E \xi \eta| = \sqrt{\E \xi^2 \E \eta^2} \LR \xi \text{ и } \eta \text{ лин. завис. п.н. между собой}
}
$$
### Дисперсия&Ковариация
Определение:
$$
\displaylines{
	\D\xi = \E[(\xi - \E\xi)^2] \\
	\cov{\xi}{\eta} = \E[(\xi - \E\xi)(\eta - \E\eta)] \\
	\text{коеф. корр.: }~~ \rho(\xi, \eta) = \frac{\cov{\xi}{\eta})}{\sqrt{\D \xi} \sqrt{\D \eta}}, \quad 0 < \D \xi, \D \eta < \infty \\
}
$$
Удобные формулы:
$$
\displaylines{
	\D \xi = \E\xi^2 - (\E \xi)^2 \\
	\cov{\xi}{\eta} = \E(\xi\eta) - \E\xi\E\eta
}
$$
### Свойства Дисперсии&Ковариации
$$
\displaylines{
	\cov{a_1\xi + b_1\eta}{a_2\zeta + b_2\chi} = a_1a_2\cov{\xi}{\zeta} + a_1b_2\cov{\xi}{\chi} + b_1a_2\cov{\eta}{\zeta} + b_1b_2\cov{\eta}{\chi} \\
	\D \xi \ge 0 \\
	\D \xi = \cov{\xi}{\xi} \\
	\D (c \cdot \xi) = c^2 \cdot \D \xi \quad c \in \R\\
	\D (c + \xi) = \D \xi \quad c \in \R\\
	\D (\xi + \eta) = \D\xi + \D\eta + 2\cov{\xi}{\eta} \\
	|\rho(\xi, \eta)| \le 1 \qquad |\rho(\xi, \eta)| = 1 \LR (\xi - \E \xi) \text{ и } (\eta - \E \eta) \text{ лин. завис. п.н. между собой}\\
	\xi_1, \dotsc, \xi_n - \text{ попарно некоррелированные с.в.} \RR \D(\xi_1 + \dotsc + \xi_n) = \D\xi_1 + \dotsc + \D\xi_n \\
	\text{С.в. } \xi_1, \dotsc, \xi_n  \text{ независимы в совокупности} \RR \D(\xi_1 + \dotsc + \xi_n) = \D\xi_1 + \dotsc + \D\xi_n \\
}
$$
### Момент с.в
$$
\displaylines{
		\nu_k = \E \xi^k - \text{$k$-ый начальный момент с.в. $\xi$, в случае, если } \E \xi^k \text{ определено} \\
		\mu_k = \E[(\xi - \E\xi)^k] - \text{$k$-ый центральный момент с.в $\xi$}
}
$$


## Независимость&Некоррелируемость
### Определения
- Дискретные с.в. называются независимы, если $P(\{\xi = a\} \cap \{ \eta = b \}) = P(\{ \xi = a \}) \cdot P(\{ \eta = b \})$.
- С.в $\xi_1, \dotsc, \xi_n$ независимы в совокупности, если $\forall x_1, \dotsc, x_n \in R \quad P(\xi_1 < x_1, \dotsc, \xi_n < x_n) = P(\xi_1 < x_1) \cdot \dotsc \cdot P(\xi_n < x_n) \LR$
- $\LR F_\xi(x_1, \dotsc, x_n) = F_{\xi_1}(x_1) \cdot \dotsc \cdot F_{\xi_n}(x_n) \LR$
- $\LR p_\xi(x_1, \dotsc, x_n) = p_{\xi_1}(x_1) \cdot \dotsc \cdot p_{\xi_n}(x_n)$
- Если $\cov{\xi}{\eta} = 0$, то $\xi$ и $\eta$ некоррелируемые
### Свойства
$$
\displaylines{
	\xi, \eta - \text{независимые с.в.} \RR \xi, \eta \text{ некореллируемые} \\\\
	
	\xi_1, \dotsc, \xi_n - \text{независимые в сов. с.в}, \quad f_1, \dotsc, f_n - \text{бор. функции из $\R$ в $\R$} \RR\\
	\RR f_1(\xi_1) \dotsc, f_n(\xi_n) \text{ независимы в совокупности}\\\\

	
}
$$

## Распределения
### Функция распределения
$$
	F_\xi(x) = P[\xi \le x], \quad  F_\xi(x) = \inti{-\infty}{x} p_\xi(t) dt, \quad p_\xi(x) = F'_\xi(x)
$$
### Биномиальное распределение
$$
\displaylines{
	\xi \sim Bin(p, n) \\
	P(\xi = k) = \binom{n}{k} p^k (1 - p)^{n - k} \\
	\E \xi = np, \qquad \D \xi = np(1 - p) \\
	\phi_\xi(t) = (1 - p + pe^{it})^n
}
$$
### Геометрическое распределение
$$
\displaylines{
	\xi \sim Geom(p), \qquad q = p - 1 \\
	P(\xi = k) = q^{k - 1} \cdot p \\
	\E \xi = \frac{1}{p}, \qquad \D \xi = \frac{q}{p^2} \\
	\phi_\xi(t) = \frac{pe^{it}}{1 - qe^{it}}
}
$$
### Пуассоновское распределение
$$
\displaylines{
	\xi \sim Pois(\lambda) \\
	P(\xi = k) = \frac{e^{-\lambda}\lambda^k}{k!} \\
	\E \xi = \lambda, \qquad \D \xi = \lambda \\
	\phi_\xi(t) = e^{\lambda(e^{it} - 1)}
}
$$
### Непрерывное равномерное распределение
$$
\displaylines{
	\xi \sim U(a, b), \qquad a \le b \\
	F_\xi(x) = \begin{cases}
		0, & x < a \\
		\frac{x - a}{b - a}, & x \in [a, b) \\
		1, & x \ge b \\
	\end{cases} \\
	p_\xi(x) = \begin{cases}
		\frac{1}{b - a}, & x \in [a, b] \\
		0 & \text{иначе}
	\end{cases} \\
	\E \xi = \frac{a + b}{2}, \qquad \D \xi = \frac{(b - a)^2}{12} \\
	\phi(t) = \frac{e^{itb} - e^{ita}}{it(b - a)}
}
$$
### Нормальное распределение
$$
\displaylines{
	\xi \sim N(\mu, \sigma^2) \sim \mu + \sigma N(0, 1) \\
	p_\xi(x) = \frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x - \mu)^2}{2\sigma^2}} \\
	\E = \mu, \qquad \D = \sigma^2 \\
	\phi_\xi(t) = e^{\mu i t - \frac{\sigma^2t^2}{2}}
}
$$
### Стандартное нормальное распределение
$$
\displaylines{
	\xi \sim N(0, 1) \\
	p_\xi(x) = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}} \\
	\E \xi = 0, \qquad \D \xi = 1 \qquad \E \xi^2 = \D \xi + (\E \xi)^2 = 1 + 0 =1\\
	\phi_\xi(t) = e^{-\frac{t^2}{2}} \\
	\text{Для сверки: } \mu_{2k} = \E\xi^{2k} = (2k - 1)!!, \quad \mu_{2k + 1} = \E\xi^{2k + 1} = 0
}
$$

### Экспоненциальное распределение
$$
\displaylines{
	\xi = Exp(\alpha) \\
	F_\xi(x) = \begin{cases}
		0, & x < 0 \\
		1 - e^{-\alpha x}, & x \ge 0
	\end{cases} \\
	p_\xi(x) = \begin{cases}
		0, & x < 0 \\
		\alpha e^{-\alpha x}, & x \ge 0
	\end{cases} \\
	\E \xi = \frac{1}{\alpha}, \qquad \D \xi = \frac{1}{\alpha^2} \\
	\phi_\xi(t) = \frac{1}{1 - \frac{it}{\alpha}}
}
$$



## Случайный вектор
### Определение
$$
	\xi = (\xi_1, \dotsc, \xi_n) : \Omega \to \R^n, \quad \forall i ~~ \xi_i - \text{с.в}, \RR \xi - \text{случайный вектор}
$$
### Свойства
$$
\displaylines{
	\xi - \text{случайный вектор}, \quad f - \text{бор. ф.} \RR f(\xi) - \text{случайный вектор} \\
	
}
$$
### Распределение случайного вектора
$$
\displaylines{
	\xi = (\xi_1, \dotsc, \xi_n) - \text{случ. вектор} \\
	\text{Совместная функция распределения с.в. ($\xi_1, \dotsc, \xi_n$): } ~~ F_\xi(x_1, \dotsc, x_n) = P(\xi_1 \le x_1, \dotsc, \xi_n \le x_n)
}
$$
### Матожидание случайного вектора
$$
	\xi = (\xi_1, \dotsc, \xi_n) - \text{случайный вектор} \RR \E \xi = (\E \xi_1, \dotsc, \E \xi_n)
$$
### Дисперсия (матрица ковариации) случайного вектора
$$
	\xi = (\xi_1, \dotsc, \xi_n) - \text{случайный вектор} \RR \D \xi = (\cov{\xi_i}{\xi_j} : i, j \in \set{1, \dotsc, n}) \qquad (\text{матрица ков. симм.})
$$

## Характеристические функции случайной величины
### Определение
$$
	\phi_\xi(t) = \E e^{it\xi} = \E \cos(t\xi) + i\E \sin(t\xi)
$$
### Свойства хар. функций
$$
\displaylines{
	\forall t \in \R \quad |\phi_\xi(t)| \le \phi_\xi(0) = 1 \\
	\eta = a\xi + b \RR \phi_\eta(t) = e^{itb}\phi_\xi(at) \\
	\phi_\xi(t) \text{ равн. непрерывна на } \R\\
	\overline{\phi_\xi(t)} = \phi_\xi(-t) = \phi_{-\xi}(t) \\
	\forall t ~~\phi_\xi(t) \in \R \LR \xi \overset{d}{=} -\xi \\
	\xi, \eta - \text{независимые с.в} \RR \phi_{\xi + \eta}(t) = \phi_\xi(t) \cdot \phi_\eta(t) \\
}
$$
### Следствия из свойств хар. функций
$$
\displaylines{
	Pois(\lambda_1) + Pois(\lambda_2) = Pois(\lambda_1 + \lambda_2) \\
	\xi_1, \xi_2 - \text{нез. с.в} \quad \xi_1 \sim N(a_1, \sigma_1^2), \quad \xi_2 \sim N(a_2, \sigma_2^2) \RR \xi_1 + \xi_2 \sim N(a_1 + a_2, \sigma_1^2 + \sigma_2^2)
}
$$
### Производная хар функции
$$
\displaylines{
	\xi - \text{с.в} \quad \forall r \in \set{1, \dotsc, n} E[|\xi|^r] < \infty \RR\\
	\RR \forall r \in \set{1, \dotsc, n} \quad  \phi_\xi^{(r)}(t) = E[(i\xi)^re^{it\xi}], \qquad \phi_\xi^{(r)}(0) = i^r E [\xi^r]
}
$$
### Единственность с.в.
$$
	\xi, \eta - \text{с.в., тогда } \xi \overset{d}{=} \eta \LR \phi_\xi(t) = \phi_\eta(t) \quad \forall t \in \R
$$


## Характеристические функции случайного вектора
### Определение
$$
	\xi \in \R^n - \text{случ. вектор} \RR \phi_\xi(t) = E \l[ e^{i \scalar{\xi, t}} \r], \quad t \in \R^n, \quad \scalar{\xi, t} = \Sum{k=1}{n} t_k \xi_k - \text{скалярное произв.}
$$
### Критерий независимости
$$
	\xi_1, \dotsc, \xi_n \text{ независимы в совокупности}\LR \phi_\xi(t) = \phi_{\xi_1}(t) \cdot \dotsc \cdot \phi_{\xi_n}(t), \quad \xi = (\xi_1, \dotsc, \xi_n)
$$



## Нормальные (Гауссовские) векторы
### Определения
$$
	\xi - \text{ гауссовский вектор} \LR \phi_\xi(t) = e^{-\frac{1}{2}\scalar{Rt, t} + i\scalar{a, t}}, \qquad R - \text{симм. неотр. опр. матрица}
$$

Теорема об эквивалентных определениях:
1. $\xi - \text{гаусс. вектор}$
2. $\xi = A\eta + b, \quad \eta_i \sim N(0, 1), \quad \eta_i$ (компоненты) независимы, $A = \Mat_{n \times m}(\R), b \in \R^n$
3. $\forall x \quad \scalar{x, \eta}$ - нормальная с.в.
### Лемма о независимости компонент
$$
		\xi = (\xi_1, \dotsc, x_n), \text{ компоненты $\xi$ независимы } \LR \xi_1, \dotsc, \xi_n \text{ некорр.}
$$
### Плотность гауссовских векторов
$$
\displaylines{
	\xi \sim N(a, R) - \text{$n$-мерный гауссовский вектор} \\
	\text{Тогда } R \text{ положит. опр. } \LR \exists ~p_\xi(t)  \text{ и } p_\xi(t) = \frac{1}{(2\pi)^{n/2} \sqrt{\det R}} \cdot \exp \l( -\frac{1}{2} \scalar{R(t - a), t - a} \r) \quad \forall t \in \R^n
}
$$
### Приведения гаусс. вектора к стандартному нормальному
$$
\displaylines{
	\xi \sim N(a, R) \text{ - $n$-мерный гауссовский вектор} \quad D = \sqrt{R} \\
	\eta = D^{-1}(\xi - a) \RR \eta \sim N(0, D^{-1}R(D^{-1})^T) \sim N(0, E_n)
}
$$
### Свойства
$$
\displaylines{
	\xi \sim N(\mu, \Sigma) \\
	A\xi \sim N(A\mu, A\Sigma A^T) \\
	\phi_{A\xi + b}(t) = e^{i\scalar{t, b}}\phi_\xi(A^Tt)
}
$$
 ,
### Ортогонализация Грамма-Шмидта
Пусть нам дан вектор $\xi = (\xi_1, \dotsc, \xi_n) \sim N(0, R)$. Хотим найти такие $A \in Mat_{n\times n}(\R)$ и $\eta = (\eta_1, \dotsc, \eta_n)$, что $\eta_i \sim N(0, 1)$ и $\xi = A\eta$
Для этого сначала находим ортогональный базис (1). Далее нормируем его (2) 
1. $\eta'_1 = \xi_1, \quad \eta'_2 = \xi_2 - \frac{\cov{\xi_2}{\eta'_1}}{\sqrt{\D \eta'_1}}\eta'_1, \quad \dotsc, \quad \eta'_n = \xi_n - \Sum{k = 1}{n - 1} \frac{\cov{\xi_n}{\eta'_k}}{\sqrt{\D \eta'_k}} * \f$
2. $\forall i \in \set{1, \dotsc, n} \quad \eta_i = \frac{\eta'_i}{\sqrt{\D \eta'_i}}$
3. Мы выразили $\eta_i$ через $\xi$. Тогда запишем в строки матрицы $A^{-1}$ линейную комбинацию $\eta_i$ и найдем обратную матрицу к $A^{-1}$. ($\xi = A\eta \RR \eta = A^{-1}\xi$)
В случае, если $\xi \sim N(a, R), a \ne 0$. Тогда, рассматриваем $\xi' = \xi - a \sim N(0, R)$
## Сходимости 
### Сходимость по вероятности
$$
	\xi_n \toP \xi \LR \forall \eps > 0 : P(|\xi_n - \xi| \ge \eps) \to 0, n \to \infty
$$
### Сходимость почти наверное
$$
	\xi_n \almostsurely \xi \LR P\l(\set{\omega : \Lim{n}{\infty} \xi_n(\omega) = \xi(\omega)}\r) = 1 \qquad \text{поточечная сходимость}
$$
#### Критерий сходимости п.н
$$
	\xi_n \almostsurely \xi \LR \forall \eps > 0 \quad P(\sup_{m \ge n}|\xi_m - \xi| > \eps) \to 0, n \to \infty
$$
#### Признак сходимости п.н
$$
	\xi_n \almostsurely \xi \LL \forall \eps > 0 ~~ \Sum{n=1}{\infty} P(|\xi_n - \xi| \ge \eps) \text{ сходится}
$$
### Сходимость в среднем порядка p
$$
	p > 0 \quad \xi_n \overset{Lp}{\to} \xi \LR \E |\xi_n - \xi|^p \to 0, n \to \infty
$$
### Сходимость по распределению
$$
	\xi_n \toD \xi \LR \forall x \quad F_{\xi_n}(x) \to F_\xi(x), n \to \infty
$$
### Следствия сходимостей
1. $\xi_n \almostsurely \xi \RR \xi_n \toP \xi$ (в случае дискретных величин: $\xi_n \almostsurely \xi \LR \xi_n \toP \xi$)
2. $\xi_n \overset{Lp}{\to} \xi \RR \xi_n \toP \xi$
3. $\xi_n \toP \xi \RR \xi_n \toD \xi$

### Теорема Пуассона
$$
S_n \sim Bin(n, p), \quad np(n) \to \lambda \quad \lambda > 0 \RR \forall k \in \Z+ \quad  P(S_n = k) \to \frac{\lambda^k}{k!} e^{-\lambda}, n\to \infty
$$
### Теорема Муавра-Лапласа
$$
\displaylines{
	p = const \in (0, 1) \RR \forall a, b \in \R, a < b, P_n(a, b) = P\l( a < \frac{S_n - np}{\sqrt{np(1 - p)}} < b \r) \\
	\sup_{a < b} \l| P_n(a, b) - \inti{a}{b} \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}} dx \r| \underset{n\to\infty}{\to} 0
}
$$
### ЗБЧ
#### Закон больших чисел в форме Чебышева
$$
\displaylines{
	\set{\xi_n, n \in \N} - \text{попарно некорр. с.в} \quad \exists c~~ \forall n ~~\D\xi_n \le c \quad S_n = \xi_1 + \dotsc + \xi_n, ~~n \in \N \RR\\
	\RR \forall \eps > 0 \quad P\l( \l| \frac{S_n - \E S_n}{n} \r| \ge \eps \r) \to 0, n \to \infty
}
$$
#### Усиленный закон больших чисел в форме Колмогорова
$$
	\set{\xi_n, n \in \N} - \text{посл. нез. и одинаково распр. с.в. }~\E \xi_1 < \infty \RR \frac{S_n}{n} \almostsurely \E\xi_1
$$

### ЦПТ
$\xi_1, \dotsc, \xi_n$ - нез. одинак. распр., $\E \xi_1 = a, \D \xi = \omega^2$. Тогда:
$$
	\frac{S_n - n a}{\sqrt{n\sigma^2}} \toD N(0, 1), \qquad \sqrt{n} \l( \frac{S_n}{n} - a \r) \toD N(0, \sigma^2)
$$
### Многомерная ЦПТ
$$
\displaylines{
	\set{\xi_n, n \in N} - \text{послед. независ. одинаково распр. с.в. из $R^m$} \\
	a = \E\xi_1, \quad R = \D\xi_1\quad  \text{конечные} \\
	S_n = \xi_1 + \dotsc + x_n \\
	\text{Тогда } \sqrt{n}\l( \frac{S_n}{n} - a \r) \toD N(0, R)
}
$$

Для размера $2$:
$$
	\sqrt{n} \l( \begin{pmatrix}
		Y \\ Z
	\end{pmatrix} - \begin{pmatrix}
		\E Y \\
		\E Z
	\end{pmatrix}\r) \toD \N(0, \Sigma), \text{ где } \Sigma = \begin{pmatrix}
		\D Y & \cov{Y}{Z} \\
		\cov{Y}{Z} & \D Z \\
	\end{pmatrix}
$$
### Наследование сходимости:
$$
	\xi_n \overset{\text{п.н.}/p/d}{\to} \xi, \quad f - \text{непрер. относ. } \xi \RR f(\xi_n) \overset{\text{п.н.}/p/d}{\to} f(\xi)
$$
### Лемма Слуцкого:
$$
	\xi_n \toD \xi, \quad \eta_n \toD C \text{ - константа} \RR \xi_n(+/\cdot) \eta_n \toD \xi (+/\cdot) C
$$




## Неравенства
### Неравенство Маркова
$$
	\xi \ge 0, a > 0 \RR P[\xi \ge a] \le \frac{\E \xi}{a}
$$
### Неравенство Чебышева
$$
	\D \xi < \infty \RR P[|\xi - \E \xi| \ge a] \le \frac{\D \xi}{a^2}
$$


## Свертки
Если $\xi$ и $\eta$ независимые случайные величины, тогда:
$$
\displaylines{
	p_{\xi+\eta}(x) = \inti{-\infty}{\infty} p_\xi(y)p_\eta(x - y) dy \\
	p_{\xi-\eta}(x) = \inti{-\infty}{\infty} p_\xi(y)p_\eta(x + y) dy \\
	p_{\xi\cdot\eta}(x) = \inti{-\infty}{\infty} p_\xi(y)p_\eta(x/y) \frac{1}{|y|} dy \\
	p_{\xi/\eta}(x) = \inti{-\infty}{\infty} p_\xi(y)p_\eta(xy) |y| dy \\
}
$$
### Выведение формулы свертки
Можно пользоваться только сверткой для суммы, остальные нужно дополнительно выводить. Покажем, как вывести свертку для умножения:
$$
\displaylines{
	P(\xi \cdot \eta \le z) = \doubleint{x \cdot y \le z} p_{\xi \cdot \eta}(x, y) dxdy =_\star \doubleint{x \cdot y \le z} p_\xi(x)p_\eta(y) dxdy \\
	\text{замена: } \begin{cases}
		u = x \\
		v = x \cdot y
	\end{cases} \LR \begin{cases}
		x = u \\
		y = \frac{v}{u} 
	\end{cases} \\
	\det J = \begin{pmatrix}
		x'_u & x'_v \\
		y'_u & y'_v \\
	\end{pmatrix} = \begin{pmatrix}
		1 & 0 \\
		\frac{v}{u^2} & \frac{1}{u}
	\end{pmatrix} = \frac{1}{u} \RR |\det J| = \frac{1}{|u|} \\
	\doubleint{x \cdot y \le z} p_\xi(x)p_\eta(y) dxdy = \doubleint{v \le z} p_\xi(u) p_\eta\l(\frac{v}{u}\r) \underbrace{\frac{1}{|u|}}_{|\det J|} dudv =_\sstar \inti{-\infty}{z} dv \inti{-\infty}{\infty} p_\xi\l( \frac{v}{u} \r) p_\eta(u) \frac{1}{|u|} du \RR\\
	\RR p_{\xi \cdot \eta} (x) = \inti{-\infty}{\infty} p_\xi(x/y) p_\eta(y) \frac{1}{|y|} dy \\
	\star \text{ - пользуемся независимостью} \\
	\sstar \text{ - легендарная теорема Фубини}
}
$$

### Формула Байеса
$$
\displaylines{
	P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(B|A) P(A)}{P(B)} \\
	P(B_i|A) = \frac{P(A|B_i) P(B_i)}{\Sum{k=1}{n} P(A|B_k) P(B_k)}
}
$$



## Допы
## Интегралы
### Интегрирование по частям
$$
\displaylines{
	\intg uv' dx = uv - \intg u'v dx \\
	\intg udv = uv - \intg vdu \\
	\inti{a}{b} uv' dx = \fint{uv}{a}{b} - \inti{a}{b} u'v dx \\
	\inti{a}{b} udv = \fint{uv}{a}{b} - \inti{a}{b} v du
}
$$
### Для сверки
$$
\begin{array}{|c|c|}
	\hline
	\inti{a}{+\infty} e^{-xc} dx = \frac{e^{-ac}}{c}, c > 0 &
	\inti{a}{+\infty} x^{-xc} dx = \frac{(ac + 1)e^{-ac}}{c^2}, c > 0 \\
	\\\hline
	\inti{a}{+\infty} x^2 e^{-xc} dx = \frac{((ac)^2 + eac + 2)e^{-ac}}{c^3}, c > 0 &
	\inti{0}{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
	\\\hline
	\inti{a}{+\infty} xe^{-x^2} dx = \frac{e^{-a^2}}{a} &
	\inti{0}{+\infty} x^2e^{-x^2} dx = \frac{\sqrt{\pi}}{4}
	\\\hline
	\inti{-\infty}{+\infty} e^{ax - bx^2} dx = \frac{\sqrt{\pi}e^{\frac{a^2}{4b}}}{\sqrt{b}}, b > 0
	\\\hline
\end{array}
$$
### Табличные интегралы
$$
\begin{array}{|c|c|c|}
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
\end{array}
$$

### Интегралы, которые не смогли
$$
\displaylines{
	\intg e^{-x^2} dx \qquad \intg \frac{\sin{x}}{x} dx \qquad \intg \frac{\cos{x}}{x} dx \qquad \intg \frac{1}{\ln x} dx
}
$$
