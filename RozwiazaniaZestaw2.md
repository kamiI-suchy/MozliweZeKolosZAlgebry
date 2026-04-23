# Rozwiązania zadań z zestawu 2

## Zadanie 1
**Pytanie teoretyczne:** Omówić diagonalizację macierzy.

### Odpowiedź teoretyczna
Macierz $A\in M_n$ jest diagonalizowalna, gdy istnieje macierz odwracalna $P$ taka, że
$$
P^{-1}AP=D,
$$
gdzie $D$ jest diagonalna. Kolumny $P$ to liniowo niezależne wektory własne, a na przekątnej $D$ stoją odpowiadające im wartości własne.

### Przykład do rozwiązania
$$
A=\begin{bmatrix}2&2\\3&3\end{bmatrix}.
$$
### Rozwiązanie krok po kroku
Wielomian charakterystyczny:
$$
\det(A-\lambda I)=\begin{vmatrix}2-\lambda&2\\3&3-\lambda\end{vmatrix}
=(2-\lambda)(3-\lambda)-6
=\lambda(\lambda-5).
$$
Wartości własne: $\lambda_1=5$, $\lambda_2=0$.

1. Dla $\lambda=5$:
$$
(A-5I)v=0\Rightarrow
\begin{bmatrix}-3&2\\3&-2\end{bmatrix}
\begin{bmatrix}x\\y\end{bmatrix}=0
\Rightarrow y=\frac{3}{2}x.
$$
Bierzemy $v_1=(2,3)^T$.

2. Dla $\lambda=0$:
$$
Av=0\Rightarrow
\begin{bmatrix}2&2\\3&3\end{bmatrix}
\begin{bmatrix}x\\y\end{bmatrix}=0
\Rightarrow x=-y.
$$
Bierzemy $v_2=(-1,1)^T$.

Tworzymy:
$$
P=\begin{bmatrix}2&-1\\3&1\end{bmatrix},
\qquad
D=\begin{bmatrix}5&0\\0&0\end{bmatrix}.
$$
$\det P=5\neq 0$, więc $P$ jest odwracalna.

**Wynik diagonalizacji:**
$$
\boxed{P^{-1}AP=D.}
$$
### Sprawdzenie
$$
P^{-1}=\begin{bmatrix}\frac15&\frac15\\-\frac35&\frac25\end{bmatrix},
$$
po obliczeniu:
$$
P^{-1}AP=\begin{bmatrix}5&0\\0&0\end{bmatrix}=D.
$$
---

## Zadanie 2
*(To samo co Zadanie 1 z zestawu 1.)*

**Pytanie teoretyczne:** Omówić działania w zbiorze liczb zespolonych w postaci algebraicznej: dodawanie, odejmowanie, mnożenie, dzielenie i wyznaczanie pierwiastka kwadratowego.

### Odpowiedź teoretyczna
Dla $z_1=a+bi$, $z_2=c+di$:
- $z_1+z_2=(a+c)+(b+d)i$,
- $z_1-z_2=(a-c)+(b-d)i$,
- $z_1z_2=(ac-bd)+(ad+bc)i$,
- $\dfrac{z_1}{z_2}=\dfrac{(a+bi)(c-di)}{c^2+d^2}$, $z_2\neq 0$.

Pierwiastek $\sqrt{u+vi}=p+qi$ spełnia:
$$
\begin{cases}
p^2-q^2=u,\\
2pq=v.
\end{cases}
$$
### Przykład do rozwiązania
$$
(2-i)z^2+(7+4i)z+(1+7i)=0.
$$
### Rozwiązanie krok po kroku
$$
a=2-i,\quad b=7+4i,\quad c=1+7i.
$$
$$
\Delta=b^2-4ac.
$$
$$
(7+4i)^2=33+56i,
$$
$$
(2-i)(1+7i)=9+13i\Rightarrow 4ac=36+52i,
$$
$$
\Delta=-3+4i.
$$
$$
\sqrt{\Delta}=\pm(1+2i),\ \text{bo}\ (1+2i)^2=-3+4i.
$$
$$
z=\frac{-b\pm\sqrt{\Delta}}{2a}.
$$
$$
z_1=\frac{-6-2i}{4-2i}=-1-i,
\qquad
z_2=\frac{-8-6i}{4-2i}=-1-2i.
$$
**Odpowiedź:**
$$
\boxed{z_1=-1-i,\quad z_2=-1-2i.}
$$
### Sprawdzenie jednego rozwiązania ($z=-1-i$)
$$
z^2=2i,
$$
$$
(2-i)z^2=2+4i,
$$
$$
(7+4i)z=-3-11i,
$$
$$
(2+4i)+(-3-11i)+(1+7i)=0.
$$
---

## Zadanie 3
*(To samo co Zadanie 2 z zestawu 1.)*

**Pytanie teoretyczne:** Omówić metodę Gaussa rozwiązywania układów równań liniowych.

### Odpowiedź teoretyczna
Metoda Gaussa: macierz rozszerzoną układu sprowadzamy operacjami elementarnymi do postaci schodkowej i wyznaczamy zmienne główne oraz swobodne.

### Przykład do rozwiązania
$$
\begin{cases}
-7t-3x+5y+2z=-6,\\
5t+x-3y-2z=6,\\
2t-y=2,\\
-2t-2x+2y+z=-1,\\
6t+2x-4y-2z=6.
\end{cases}
$$
### Rozwiązanie krok po kroku
Z równania $2t-y=2$:
$$
y=2t-2.
$$
Z równania $5t+x-3y-2z=6$:
$$
x=t+2z.
$$
Wstawiamy do $-2t-2x+2y+z=-1$:
$$
-2t-2(t+2z)+2(2t-2)+z=-1
\Rightarrow -3z=3
\Rightarrow z=-1.
$$
Stąd:
$$
x=t-2,\qquad y=2t-2.
$$
Parametryzacja przez $\lambda=y$:
$$
t=1+\frac{\lambda}{2},\quad x=-1+\frac{\lambda}{2},\quad y=\lambda,\quad z=-1.
$$
**Zbiór rozwiązań:**
$$
\boxed{(t,x,y,z)=\left(1+\frac{\lambda}{2},-1+\frac{\lambda}{2},\lambda,-1\right),\ \lambda\in\mathbb{R}.}
$$
### Trzy przykładowe rozwiązania
- $(1,-1,0,-1)$,
- $(2,0,2,-1)$,
- $(3,1,4,-1)$.

### Sprawdzenie jednego rozwiązania
Dla $(2,0,2,-1)$ po podstawieniu wszystkie równania dają odpowiednio: $-6,6,2,-1,6$, więc układ jest spełniony.

---

## Zadanie 4
*(To samo co Zadanie 3 z zestawu 1.)*

**Pytanie teoretyczne:** Zdefiniować macierz odwrotną oraz podać sposób jej wyznaczania. Podać warunek konieczny istnienia.

### Odpowiedź teoretyczna
$A^{-1}$ spełnia $AA^{-1}=I$. Macierz odwrotna istnieje wtedy i tylko wtedy, gdy $\det A\neq 0$.

### Przykład 1: warunek odwracalności
$$
A=\begin{bmatrix}
2x-4&x+4&-1\\
2&x+3&-2\\
0&3&-1
\end{bmatrix}.
$$
$$
\det A=-2(x-5)(x-1).
$$
Stąd:
$$
\boxed{x\neq 1\ \text{i}\ x\neq 5.}
$$
### Przykład 2: macierz odwrotna dla $x=-1$
$$
A=\begin{bmatrix}
-6&3&-1\\
2&2&-2\\
0&3&-1
\end{bmatrix},
\quad
A^{-1}=\begin{bmatrix}
-\frac16&0&\frac16\\
-\frac1{12}&-\frac14&\frac7{12}\\
-\frac14&-\frac34&\frac34
\end{bmatrix}.
$$
### Sprawdzenie
$$
A\cdot A^{-1}=I_3.
$$
---

## Zadanie 5
*(To samo co Zadanie 4 z zestawu 1.)*

**Pytanie teoretyczne:** Omówić równanie prostej i płaszczyzny w przestrzeni 3-wymiarowej.

### Odpowiedź teoretyczna
- Prosta: $\mathbf{r}=\mathbf{r}_0+t\mathbf{v}$.
- Płaszczyzna: $Ax+By+Cz+D=0$, normalna $(A,B,C)$.

### Przykład do rozwiązania
Wyznaczyć punkt symetryczny do
$$
P=(4,-1,4)
$$
względem płaszczyzny
$$
\pi:\ -x+y-z+3=0.
$$
### Rozwiązanie krok po kroku
$$
\mathbf{n}=(-1,1,-1),\quad d=3.
$$
$$
ax_0+by_0+cz_0+d=-6,
\qquad
a^2+b^2+c^2=3.
$$
$$
P'=P-2\frac{-6}{3}(-1,1,-1)=P+4(-1,1,-1)=(0,3,0).
$$
**Odpowiedź:**
$$
\boxed{P'=(0,3,0).}
$$
### Sprawdzenie
Środek $S=(2,1,2)$ leży na płaszczyźnie:
$$
-2+1-2+3=0,
$$
a $\overrightarrow{PP'}=(-4,4,-4)$ jest równoległy do normalnej $(-1,1,-1)$.
