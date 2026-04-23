# Rozwiązania zadań z zestawu 1

## Zadanie 1
**Pytanie teoretyczne:** Omówić działania w zbiorze liczb zespolonych w postaci algebraicznej: dodawanie, odejmowanie, mnożenie, dzielenie i wyznaczanie pierwiastka kwadratowego.

### Odpowiedź teoretyczna
Dla \(z_1=a+bi\), \(z_2=c+di\):
- \(z_1+z_2=(a+c)+(b+d)i\),
- \(z_1-z_2=(a-c)+(b-d)i\),
- \(z_1z_2=(ac-bd)+(ad+bc)i\),
- \(\dfrac{z_1}{z_2}=\dfrac{(a+bi)(c-di)}{c^2+d^2}\), \(z_2\neq 0\).

Pierwiastek kwadratowy z \(w=u+vi\) szukamy jako \(\sqrt{w}=p+qi\), wtedy:
\[
\begin{cases}
p^2-q^2=u,\\
2pq=v.
\end{cases}
\]
Dla niezerowego \(w\) są dwa pierwiastki przeciwne.

### Przykład do rozwiązania
\[
(2-i)z^2+(7+4i)z+(1+7i)=0.
\]

### Rozwiązanie krok po kroku
Równanie kwadratowe ma postać \(az^2+bz+c=0\), gdzie:
\[
a=2-i,\quad b=7+4i,\quad c=1+7i.
\]
Liczymy wyróżnik:
\[
\Delta=b^2-4ac.
\]
1. \(b^2=(7+4i)^2=33+56i\).
2. \(ac=(2-i)(1+7i)=9+13i\), więc \(4ac=36+52i\).
3. \(\Delta=(33+56i)-(36+52i)=-3+4i\).

Szukamy \(\sqrt{\Delta}\):
\[
(1+2i)^2=1+4i-4=-3+4i,
\]
zatem
\[
\sqrt{\Delta}=\pm(1+2i).
\]

Wzór na pierwiastki:
\[
z=\frac{-b\pm\sqrt{\Delta}}{2a}.
\]
Czyli
\[
z_1=\frac{-(7+4i)+(1+2i)}{4-2i}=\frac{-6-2i}{4-2i}=-1-i,
\]
\[
z_2=\frac{-(7+4i)-(1+2i)}{4-2i}=\frac{-8-6i}{4-2i}=-1-2i.
\]

**Odpowiedź:**
\[
\boxed{z_1=-1-i,\quad z_2=-1-2i.}
\]

### Sprawdzenie jednego rozwiązania (dla \(z=-1-i\))
\[
z^2=(-1-i)^2=2i,
\]
\[
(2-i)z^2=(2-i)\cdot 2i=2+4i,
\]
\[
(7+4i)z=(7+4i)(-1-i)=-3-11i.
\]
Suma:
\[
(2+4i)+(-3-11i)+(1+7i)=0.
\]
Rozwiązanie poprawne.

---

## Zadanie 2
**Pytanie teoretyczne:** Omówić metodę Gaussa rozwiązywania układów równań liniowych.

### Odpowiedź teoretyczna
Metoda Gaussa polega na sprowadzeniu macierzy rozszerzonej układu do postaci schodkowej operacjami elementarnymi na wierszach (zamiana wierszy, mnożenie przez \(\neq 0\), dodanie wielokrotności innego wiersza), a następnie odczytaniu rozwiązań.

### Przykład do rozwiązania
\[
\begin{cases}
-7t-3x+5y+2z=-6,\\
5t+x-3y-2z=6,\\
2t-y=2,\\
-2t-2x+2y+z=-1,\\
6t+2x-4y-2z=6.
\end{cases}
\]

### Rozwiązanie krok po kroku
Z trzeciego równania:
\[
2t-y=2\Rightarrow y=2t-2.
\]
Podstawiamy do drugiego:
\[
5t+x-3(2t-2)-2z=6\Rightarrow x-t-2z=0\Rightarrow x=t+2z.
\]
Podstawiamy do czwartego:
\[
-2t-2x+2y+z=-1.
\]
Po wstawieniu \(x=t+2z\), \(y=2t-2\):
\[
-2t-2(t+2z)+2(2t-2)+z=-1
\Rightarrow -3z-4=-1
\Rightarrow z=-1.
\]
Stąd:
\[
x=t+2(-1)=t-2,
\]
\[
y=2t-2.
\]
Pierwsze i piąte równanie są wtedy spełnione tożsamościowo, więc mamy 1 parametr swobodny.

Przyjmijmy parametr \(\lambda=y\). Wtedy:
\[
t=1+\frac{\lambda}{2},\quad x=-1+\frac{\lambda}{2},\quad y=\lambda,\quad z=-1.
\]

**Zbiór rozwiązań:**
\[
\boxed{(t,x,y,z)=\left(1+\frac{\lambda}{2},-1+\frac{\lambda}{2},\lambda,-1\right),\ \lambda\in\mathbb{R}.}
\]

### Trzy przykładowe rozwiązania
- dla \(\lambda=0\): \((1,-1,0,-1)\),
- dla \(\lambda=2\): \((2,0,2,-1)\),
- dla \(\lambda=4\): \((3,1,4,-1)\).

### Sprawdzenie jednego rozwiązania (dla \((2,0,2,-1)\))
Podstawiamy:
- \(-7\cdot2-3\cdot0+5\cdot2+2\cdot(-1)=-14+10-2=-6\),
- \(5\cdot2+0-3\cdot2-2\cdot(-1)=10-6+2=6\),
- \(2\cdot2-2=2\),
- \(-2\cdot2-2\cdot0+2\cdot2+(-1)=-1\),
- \(6\cdot2+2\cdot0-4\cdot2-2\cdot(-1)=12-8+2=6\).
Wszystkie równania spełnione.

---

## Zadanie 3
**Pytanie teoretyczne:** Zdefiniować macierz odwrotną oraz sposób jej wyznaczania. Podać warunek konieczny istnienia.

### Odpowiedź teoretyczna
Macierz odwrotna \(A^{-1}\) do \(A\) spełnia
\[
AA^{-1}=A^{-1}A=I.
\]
Istnieje wtedy i tylko wtedy, gdy \(\det A\neq 0\).
Wyznaczamy np. metodą Gaussa-Jordana: \([A|I]\to[I|A^{-1}]\).

### Przykład 1: kiedy macierz ma odwrotność?
\[
A=\begin{bmatrix}
2x-4&x+4&-1\\
2&x+3&-2\\
0&3&-1
\end{bmatrix}.
\]
Liczymy wyznacznik:
\[
\det A=-2(x-5)(x-1).
\]
Warunek odwracalności:
\[
\det A\neq 0\iff x\neq 1\ \text{i}\ x\neq 5.
\]

### Przykład 2: wyznaczyć \(A^{-1}\) dla \(x=-1\)
Po podstawieniu:
\[
A=\begin{bmatrix}
-6&3&-1\\
2&2&-2\\
0&3&-1
\end{bmatrix}.
\]
Otrzymujemy:
\[
A^{-1}=\begin{bmatrix}
-\frac16&0&\frac16\\[2mm]
-\frac1{12}&-\frac14&\frac7{12}\\[2mm]
-\frac14&-\frac34&\frac34
\end{bmatrix}.
\]

### Sprawdzenie
\[
A\cdot A^{-1}=I_3.
\]
Po przemnożeniu otrzymujemy macierz jednostkową, więc wynik jest poprawny.

---

## Zadanie 4
**Pytanie teoretyczne:** Omówić równanie prostej i płaszczyzny w przestrzeni 3D.

### Odpowiedź teoretyczna
- Prosta: \(\mathbf{r}=\mathbf{r}_0+t\mathbf{v}\) (postać wektorowa),
  albo postać symetryczna \(\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}\).
- Płaszczyzna: \(Ax+By+Cz+D=0\), normalna \(\mathbf{n}=(A,B,C)\).

### Przykład do rozwiązania
Wyznaczyć punkt symetryczny do
\[
P=(4,-1,4)
\]
względem płaszczyzny
\[
\pi:\ -x+y-z+3=0.
\]

### Rozwiązanie krok po kroku
Normalna płaszczyzny: \(\mathbf{n}=(-1,1,-1)\), \(d=3\).
Dla odbicia punktu względem płaszczyzny używamy wzoru:
\[
P'=P-2\frac{ax_0+by_0+cz_0+d}{a^2+b^2+c^2}(a,b,c).
\]
Liczymy:
\[
ax_0+by_0+cz_0+d=(-1)\cdot4+1\cdot(-1)+(-1)\cdot4+3=-6,
\]
\[
a^2+b^2+c^2=1+1+1=3.
\]
Zatem:
\[
P'=P-2\cdot\frac{-6}{3}(-1,1,-1)=P+4(-1,1,-1).
\]
\[
P'=(4,-1,4)+(-4,4,-4)=(0,3,0).
\]

**Odpowiedź:**
\[
\boxed{P'=(0,3,0).}
\]

### Sprawdzenie
Środek odcinka \(PP'\):
\[
S=\left(\frac{4+0}{2},\frac{-1+3}{2},\frac{4+0}{2}\right)=(2,1,2).
\]
Sprawdzamy \(S\in\pi\):
\[
-2+1-2+3=0.
\]
Wektor \(\overrightarrow{PP'}=(-4,4,-4)=4(-1,1,-1)\) jest równoległy do normalnej płaszczyzny.
Warunki symetrii spełnione.

---

## Zadanie 5
**Pytanie teoretyczne:** Omówić wzajemne położenie prostych skośnych w przestrzeni 3D.

### Odpowiedź teoretyczna
Proste skośne to takie, które się nie przecinają i nie są równoległe. Najkrótszy odcinek między nimi jest prostopadły do obu prostych.

### Przykład do rozwiązania
\[
l_1:\frac{x+3}{-3}=\frac{y-3}{-2}=\frac{z-2}{-2},
\qquad
l_2:\frac{x-2}{4}=\frac{y-3}{2}=\frac{z-3}{4}.
\]

### Rozwiązanie krok po kroku
Zapis parametryczny:
\[
l_1:\ (x,y,z)=(-3,3,2)+s(-3,-2,-2),
\]
\[
l_2:\ (x,y,z)=(2,3,3)+u(4,2,4).
\]
Wektory kierunkowe:
\[
\mathbf{v}_1=(-3,-2,-2),\quad \mathbf{v}_2=(4,2,4).
\]
Nie są proporcjonalne, więc proste nie są równoległe.

Iloczyn wektorowy:
\[
\mathbf{v}_1\times\mathbf{v}_2=(-4,4,2),\quad |\mathbf{v}_1\times\mathbf{v}_2|=6.
\]
Weźmy punkty \(P_1=(-3,3,2)\in l_1\), \(P_2=(2,3,3)\in l_2\),
\[
P_2-P_1=(5,0,1).
\]
Odległość prostych skośnych:
\[
d=\frac{|(P_2-P_1)\cdot(\mathbf{v}_1\times\mathbf{v}_2)|}{|\mathbf{v}_1\times\mathbf{v}_2|}
=\frac{|(5,0,1)\cdot(-4,4,2)|}{6}
=\frac{|-18|}{6}=3.
\]

**Odpowiedź (odległość):**
\[
\boxed{d(l_1,l_2)=3.}
\]

### Punkty realizujące minimalną odległość
Po minimalizacji odległości między punktami prostych otrzymujemy parametry:
\[
s=-1,\quad u=0.
\]
Stąd:
\[
A=P_1+(-1)\mathbf{v}_1=(0,5,4),
\]
\[
B=P_2+0\cdot\mathbf{v}_2=(2,3,3).
\]

Wektor
\[
\overrightarrow{AB}=(2,-2,-1)
\]
jest prostopadły do obu kierunków:
\[
\overrightarrow{AB}\cdot\mathbf{v}_1=0,\qquad \overrightarrow{AB}\cdot\mathbf{v}_2=0.
\]
Długość:
\[
|AB|=\sqrt{2^2+(-2)^2+(-1)^2}=3.
\]

**Punkty minimalnej odległości:**
\[
\boxed{A=(0,5,4),\quad B=(2,3,3).}
\]
