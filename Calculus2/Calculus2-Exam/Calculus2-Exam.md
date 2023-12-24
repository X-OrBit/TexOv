# Тушканчик-матанчик
![[template_latex]]
![[template_dsalakhov]]
# Подготовительный лист к экзамену
## Задача №1
Вычислить сумму, применяя почленное дифферецирование:
$$
	\Sum{n=0}{\infty} \frac{x^{2n + 1}}{2n + 1}, \qquad |x| < 0.5
$$

### Решение
$$
\displaylines{
	\l( \Sum{n=0}{\infty} \frac{x^{2n + 1}}{2n + 1} \r)' = \Sum{n=0}{\infty} \l( \frac{x^{2n + 1}}{2n + 1} \r)' = \Sum{n=0}{\infty} x^{2n} = \frac{1}{1 - x^2} \quad (\text{производящая функция}) \\
	\l( \Sum{n=0}{\infty} \frac{x^{2n + 1}}{2n + 1} \r)' = \frac{1}{1 - x^2} \\
	\Sum{n=0}{\infty} \frac{x^{2n + 1}}{2n + 1} = \intg \frac{1}{1 - x^2} dx = \intg \frac{1/2}{1 - x} + \frac{1/2}{1 + x} dx = \frac{1}{2} \l( \log|1 + x| - \log|1 - x| \r) + c \\
	\text{Подставим } x = 0 \RR \Sum{n=0}{\infty} \frac{x^{2n + 1}}{2n + 1} = 0 \RR c = 0 \\
	\text{Т.к. } |x| < 0.5 \RR
		\Sum{n=0}{\infty} \frac{x^{2n + 1}}{2n + 1} = \frac{1}{2} \l( \log(1 + x) - \log(1 - x) \r) = \log\l( \sqrt{\frac{1 + x}{1 - x}} \r)
}
$$

## Задача №2
Вычислите интеграл:
$$
	\inti{0}{1} dx \inti{1 - \sqrt{1 - x^2}}{1 + \sqrt{1 - x^2}} \sqrt{y} dy
$$
%%PDF break%% <div style="page-break-after: always;"></div>
### Решение 1
$$
\displaylines{
	\text{Посмотрим на область интегрирования:}\\
	0 \le x \le 1, \quad 1 - \sqrt{1 - x^2} \le y \le 1 + \sqrt{1 - x^2} \\
	0 \le x \le 1, \quad -\sqrt{1 - x^2} \le y - 1 \le \sqrt{1 - x^2} \\
	0 \le x \le 1, \quad 0 \le y \le 2 \quad (y - 1)^2 \le 1 - x^2 \\
	0 \le x \le 1, \quad 0 \le y \le 2 \quad x^2 + (y - 1)^2 \le 1 \\
}
$$
Область интегрирования:
![[task2.png|center|300]]
$$
\displaylines{
	\text{Сделаем полярную замену: } \begin{cases}
		x = r\cos\phi \\
		y = r\sin\phi
	\end{cases} \\
	\text{Тогда область интегрирования: } \begin{cases}
		\phi \in [0, \pi/2] \\
		r \in [0, 2\sin\phi]^\star
	\end{cases} \\
	
	\inti{0}{1} dx \inti{1 - \sqrt{1 - x^2}}{1 + \sqrt{1 - x^2}} \sqrt{y} dy = \inti{0}{\pi/2} d\phi \inti{0}{2\sin\phi}\sqrt{r}\sqrt{\sin\phi} \cdot \underbrace{r}_{||J||} dr = \inti{0}{\pi/2} \sqrt{\sin\phi} d\phi \inti{0}{2\sin\phi} r^{3/2} dr = \inti{0}{\pi/2} \sqrt{\sin\phi} \ffint{\l[ \frac{r^{5/2}}{5/2} \r]}{0}{2\sin\phi} d\phi =\\
	
	= \frac{2}{5} \inti{0}{\pi/2} \sqrt{\sin\phi} (2\sin\phi)^{5/2} d\phi = \frac{8\sqrt{2}}{5} \inti{0}{\pi/2} \sin^3\phi d\phi = -\frac{8\sqrt{2}}{5} \inti{0}{\pi/2} (1 - \cos^2\phi) d\cos\phi = -\frac{8\sqrt{2}}{5} \ffint{\l[ \cos\phi - \frac{\cos^3\phi}{3} \r]}{0}{\pi/2} =\\
	
	-\frac{8\sqrt{2}}{5} \ffint{\l[ \cos\phi - \frac{\cos^3\phi}{3} \r]}{0}{\pi/2} = \frac{8\sqrt{2}}{5} \cdot \l( 1 - \frac{1}{3} \r) = \frac{16\sqrt{2}}{15} \\
	
	\star - \cos\alpha = \frac{r}{2} \RR r = 2\cos\alpha = 2\cos(90^\circ - \phi) = 2\sin\phi
}
$$
%%PDF break%% <div style="page-break-after: always;"></div>
### Решение 2
$$
\displaylines{
	0 \le x \le 1, \quad 1 - \sqrt{1 - x^2} \le y \le 1 + \sqrt{1 - x^2} \\
	0 \le x \le 1, \quad -\sqrt{1 - x^2} \le y - 1 \le \sqrt{1 - x^2} \\
	0 \le x \le 1, \quad 0 \le y \le 2 \quad (y - 1)^2 \le 1 - x^2 \\
	\quad 0 \le y \le 2 \quad 0 \le x \le \sqrt{2y - y^2} \\

	\inti{0}{1} dx \inti{1 - \sqrt{1 - x^2}}{1 + \sqrt{1 - x^2}} \sqrt{y} dy = \inti{0}{2} \sqrt{y} dy \inti{0}{\sqrt{2y - y^2}} dx = \inti{0}{2} y\sqrt{2 - y} dy = \begin{bmatrix}
		t = 2 - y \\
		dy = -dt \\
		y \in [0, 2] \RR t \in[2, 0]
	\end{bmatrix} = \inti{2}{0}(t - 2)\sqrt{t}dt =\\
	
	= \inti{2}{0}t^{3/2} - 2t^{1/2}dt = \ffint{\l[ \frac{t^{5/2}}{5/2} - \frac{2t^{3/2}}{3/2} \r]}{2}{0} = -\frac{8\sqrt{2}}{5} + \frac{8\sqrt{2}}{3} = \frac{16\sqrt{2}}{5}
}
$$

## Задача №3
Вычислите интеграл:
$$
	\tripleint{\underset{0 \le z \le y}{x^2 + y^2 \le 2x}} z\sqrt{x^2 + y^2} dxdydz
$$
### Решение
$$
x^2 + y^2 \le 2x \RR x^2 - 2x + 1 + y^2 - 1 \le 0 \RR (x - 1)^2 + y^2 \le 1
$$
Область интегрирования по $x,y$:
![[task3.png|center|300]]
$$
\displaylines{
	\text{Цилиндрическая замена:} \\
	\begin{cases}
		x = r\cos\phi \\
		y = r\sin\phi \\
		z = z
	\end{cases} \RR ||J|| = r \\
	\text{Тогда ограничения следующие:} \\
	\begin{cases}
		0 \le \phi \le \pi/2 \\
		0 \le r \le 2\cos\phi \\
		0 \le z \le r\sin\phi
	\end{cases} \\
	\text{Считаем:} \\
	\tripleint{\underset{0 \le z \le y}{x^2 + y^2 \le 2x}} z\sqrt{x^2 + y^2} dxdydz = \inti{0}{\pi/2} d\phi \inti{0}{2\cos\phi} dr \inti{0}{r\sin\phi} z \sqrt{r^2} \underbrace{r}_{||J||} dz = \inti{0}{\pi/2} d\phi \inti{0}{2\cos\phi} r^2 \ffint{\l[ \frac{z^2}{2} \r]}{0}{r\sin\phi} dr =\\
	
	= \inti{0}{\pi/2} d\phi \inti{0}{2\cos\phi} \frac{r^4}{2} \sin^2\phi dr = \frac{1}{2} \inti{0}{\pi/2} \sin^2\phi d\phi \inti{0}{2\cos\phi} r^4 dr = \frac{1}{2} \inti{0}{\pi/2} \sin^2\phi \ffint{\l[ \frac{r^5}{5} \r]}{0}{2\cos\phi} d\phi = \frac{1}{2} \inti{0}{\pi/2} \sin^2\phi \frac{32\cos^5\phi}{5} d\phi =\\

	= \frac{16}{5} \inti{0}{\pi/2} \sin^2\phi \cos^5\phi d\phi = \frac{16}{5} \inti{0}{\pi/2} \sin^2\phi (1 - \sin^2\phi)^2 d\sin\phi = \frac{16}{5} \inti{0}{\pi/2} \sin^2\phi - 2\sin^4\phi + \sin^6\phi d\sin\phi =\\
	
	= \frac{16}{5} \ffint{\l[ \frac{\sin^3\phi}{3} - \frac{2\sin^5\phi}{5} + \frac{\sin^7\phi}{7} \r]}{0}{\pi/2} = \frac{16}{5} \l( \frac{1}{3} - \frac{2}{5} + \frac{1}{7} \r) = \frac{16}{5} \cdot \frac{8}{105} =  \frac{128}{525}
}
$$

## Задача №4
Найти объем множества:
$$
	x^2 + y^2 \le 1, \quad x^2 + z^2 \le 1
$$
### Решение
$$
\displaylines{
	\begin{cases}
		x^2 + y^2 \le 1 \\
		x^2 + z^2 \le 1
	\end{cases} \RR \begin{cases}
		-1 \le x \le 1 \\
		-\sqrt{1 - x^2} \le y \le \sqrt{1 - x^2} \\
		-\sqrt{1 - x^2} \le z \le \sqrt{1 - x^2}
	\end{cases} \\
	\text{Объем вычисляется так:} \\
	\tripleint{D} 1 dxdydz = \inti{-1}{1} dx \inti{-\sqrt{1 - x^2}}{\sqrt{1 - x^2}} dy \inti{-\sqrt{1 - x^2}}{\sqrt{1 - x^2}} dz =_\star 8\inti{0}{1} dx \inti{0}{\sqrt{1 - x^2}} dy \inti{0}{\sqrt{1 - x^2}} = 8\inti{0}{1} dx \inti{0}{\sqrt{1 - x^2}} \sqrt{1 - x^2} dy =\\
	
	= 8\inti{0}{1} 1 - x^2 dx = 8\ffint{\l[ x - \frac{x^3}{3} \r]}{0}{1} = 8 \l( 1 - \frac{1}{3} \r) = \frac{16}{3} \\
	
	\star - \text{симм. по 3 коорд.}
}
$$

%%PDF break%% <div style="page-break-after: always;"></div>
# Cheat Sheet

## Замены координат
### Полярная замена координат
$$
\begin{cases}
	x = r\cos\phi \\
	y = r\sin\phi \\
\end{cases} \RR \det J = \begin{vmatrix}
	x'_r & x'_\phi \\
	y'_r & y'_\phi
\end{vmatrix} = \begin{vmatrix}
	\cos\phi & -r\sin\phi \\
	\sin\phi & r\cos\phi
\end{vmatrix} = r(\cos^2\phi + \sin^2\phi) = r
$$
### Цилидрическая замена координат
$$
\begin{cases}
	x = r\cos\phi \\
	y = r\sin\phi \\
	z = z
\end{cases} \RR \det J = \begin{vmatrix}
	x'_r & x'_\phi & x'_z \\
	y'_r & y'_\phi & y'_z \\
	z'_r & z'_\phi & z'_z \\
\end{vmatrix} = \begin{vmatrix}
	\cos\phi & -r\sin\phi & 0 \\
	\sin\phi & r\cos\phi & 0 \\
	0 & 0 & 1
\end{vmatrix} = r
$$
### Сферическая замена координат 1
$$
\displaylines{
	\begin{cases}
		x = r\cos\psi\cos\phi \\
		y = r\cos\psi\sin\phi \\
		z = r\sin\psi
	\end{cases} \RR \det J = \begin{vmatrix}
		x'_r & x'_\phi & x'_\psi \\
		y'_r & y'_\phi & y'_\psi \\
		z'_r & z'_\phi & z'_\psi \\
	\end{vmatrix} = \begin{vmatrix}
		\cos\psi\cos\phi & -r\cos\psi\sin\phi & -r\sin\psi\cos\phi \\
		\cos\psi\sin\phi & r\cos\psi\cos\phi & -r\sin\psi\sin\phi \\
		\sin \psi & 0 & r\cos\psi
	\end{vmatrix} =\\
	
	= r^2 \l( \sin\psi \begin{vmatrix}
		-\cos\psi\sin\phi & -\sin\psi\cos\phi \\
		\cos\psi\cos\phi & -\sin\psi\sin\phi \\
	\end{vmatrix} + \cos\psi \begin{vmatrix}
		\cos\psi\cos\phi & -\cos\psi\sin\phi \\
		\cos\psi\sin\phi & \cos\psi\cos\phi \\
	\end{vmatrix} \r) =\\

	= r^2 \l( \sin^2\psi\cos\psi + \cos^3\psi \r) = r^2 \cos\psi \l( \sin^2\psi + \cos^2\psi \r) = r^2\cos\psi
}
$$
### Сферическая замена координат 2
$$
\displaylines{
	\begin{cases}
		x = r\sin\psi\cos\phi \\
		y = r\sin\psi\sin\phi \\
		z = r\cos\psi
	\end{cases} \RR \det J = \begin{vmatrix}
		x'_r & x'_\phi & x'_\psi \\
		y'_r & y'_\phi & y'_\psi \\
		z'_r & z'_\phi & z'_\psi \\
	\end{vmatrix} = \begin{vmatrix}
		\sin\psi\cos\phi & -r\sin\psi\sin\phi & r\cos\psi\cos\phi \\
		\sin\psi\sin\phi & r\sin\psi\cos\phi & r\cos\psi\sin\phi \\
		\cos\psi & 0 & -r\sin\psi
	\end{vmatrix} =\\
	
	= r^2 \l( -\sin\psi \begin{vmatrix}
		\sin\psi\cos\phi & -\sin\psi\sin\phi \\
		\sin\psi\sin\phi & \sin\psi\cos\phi \\
	\end{vmatrix} + \cos\psi \begin{vmatrix}
		-\sin\psi\sin\phi & \cos\psi\cos\phi \\
		\sin\psi\cos\phi & \cos\psi\sin\phi \\
	\end{vmatrix} \r) =\\

	= r^2 \l( -\sin^3\psi - \cos^2\psi\sin\psi \r) = -r^2 \sin\psi \l( \sin^2\psi + \cos^2\psi \r) = -r^2\sin\psi \RR ||J|| = r^2\sin\psi
}
$$

%%PDF break%% <div style="page-break-after: always;"></div>
## Производящие ряды

$$
\begin{array}{|c|c|c|}
	\hline\\
	\Sum{n=0}{\infty}x^n = \frac{1}{1 - x} & \Sum{n=0}{\infty} x^{nk}= \frac{1}{1 - x^k} & \Sum{n=0}{\infty} (-1)^n x^n  =\frac{1}{1 + x} & \Sum{n=0}{\infty} 2^nx^n = \frac{1}{1 - 2x}
	\\\hline
	\Sum{n=0}{\infty} r^nx^n = \frac{1}{1 - rx} & \Sum{n=0}{\infty} (n + 1)x^n = \frac{1}{(1 - x)^2} & \Sum{n=0}{\infty} \frac{(n + 1)(n + 2)}{2} x^n = \frac{1}{(1 - x)^3}
	\\\hline
	\Sum{n=\bf{\underline{1}}}{\infty} \frac{(-1)^{n+1}}{n} x^n = \ln(1 + x) & \Sum{n=0}{\infty} \frac{1}{n!}x^n = e^x & \Sum{n=0}{\infty} \frac{1}{(2n)!} x^{2n} = \cos x & \Sum{n=0}{\infty} \frac{1}{(2n + 1)!} x^{2n + 1} = \sin x
	\\\hline
\end{array}
$$
### Выведение производящих рядов
$$
\displaylines{
	\Sum{n=0}{\infty} r^nx^{kn} = 1 + rx^k + r^2x^{2k} + \dotsc = I\\
	\RR 1 = 1 + rx^k + r^2x^{2k} + \dotsc - rx^k \cdot(1 + rx^k + r^2x^{2k} + \dotsc) = I - rx^k \cdot I \RR I = \frac{1}{1 - rx^k} \\
	\RR \begin{cases}
		\Sum{n=0}{\infty} x^n \frac{1}{1 - x} \\
		\Sum{n=0}{\infty} (-1)^nx^n \frac{1}{1 + x} \\
		\Sum{n=0}{\infty} x^{nk} = \frac{1}{1 - x^k} \\
		\Sum{n=0}{\infty} 2^nx^n = \frac{1}{1 - 2x}
	\end{cases} \\

	\Sum{n=0}{\infty} (n+1)x^n = \Sum{n=1}{\infty} nx^{n-1} = \l( \Sum{n=1}{\infty} x^n \r)' = \l( \Sum{n=0}{\infty} x^n \r)' = \l( \frac{1}{1 - x} \r)' = \frac{1}{(1 - x)^2} \\
	
	\Sum{n=0}{\infty} \frac{(n+1)(n+2)}{2}x^n = \Sum{n=2}{\infty} \frac{n(n - 1)}{2}x^{n - 2} = \frac{1}{2} \l( \Sum{n=1}{\infty} n x^{n-1} \r)' = \frac{1}{2} \l( \frac{1}{(1 - x^2)} \r)' = \frac{1}{(1 - x)^3} \\
	
	\cos x, \sin x, \ln(1 + x), e^x - \text{ряды тейлора}
}
$$

## Табличные производные
![[template_derivatives]]

## Табличные интегралы
![[template_integrals]]