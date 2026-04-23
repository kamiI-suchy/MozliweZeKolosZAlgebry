# Rozwiązania zagadnień z `pytania.txt`

## 1. Definicja liczb zespolonych jako par liczb rzeczywistych
**Pytanie:** Zdefiniować liczby zespolone jako pary liczb rzeczywistych z odpowiednimi działaniami.

**Odpowiedź:**
Zbiór liczb zespolonych definiujemy jako
\[
\mathbb{C}=\mathbb{R}^2=\{(a,b):a,b\in\mathbb{R}\}
\]
z działaniami:
- dodawanie:
\[
(a,b)+(c,d)=(a+c,b+d),
\]
- mnożenie:
\[
(a,b)\cdot(c,d)=(ac-bd,ad+bc).
\]
Element neutralny dodawania: \((0,0)\), mnożenia: \((1,0)\).
Liczbę \((a,b)\) zapisujemy jako \(a+bi\).

---

## 2. Jednostka urojona
**Pytanie:** Zdefiniować jednostkę urojoną.

**Odpowiedź:**
Jednostka urojona to liczba
\[
i=(0,1),
\]
która spełnia
\[
i^2=-1.
\]
Dzięki temu każdą liczbę zespoloną zapisujemy jako \(z=a+bi\).

---

## 3. Postać algebraiczna i trygonometryczna liczby zespolonej
**Pytanie:** Omówić postać algebraiczną i trygonometryczną liczby zespolonej.

**Odpowiedź:**
- **Postać algebraiczna:** \(z=a+bi\), gdzie \(a=\Re z\), \(b=\Im z\).
- **Moduł:** \(|z|=\sqrt{a^2+b^2}=r\).
- **Argument:** \(\arg z=\varphi\), taki że
\[
\cos\varphi=\frac{a}{r},\quad \sin\varphi=\frac{b}{r}.
\]
- **Postać trygonometryczna:**
\[
z=r(\cos\varphi+i\sin\varphi),\quad r\ge 0.
\]

---

## 4. Działania na liczbach zespolonych w postaci algebraicznej i trygonometrycznej
**Pytanie:** Omówić działania mnożenia przez liczbę rzeczywistą, dodawania, odejmowania, mnożenia i dzielenia w obu postaciach.

**Odpowiedź:**
Dla \(z_1=a+bi\), \(z_2=c+di\):
- dodawanie: \(z_1+z_2=(a+c)+(b+d)i\),
- odejmowanie: \(z_1-z_2=(a-c)+(b-d)i\),
- mnożenie:
\[
(a+bi)(c+di)=(ac-bd)+(ad+bc)i,
\]
- dzielenie:
\[
\frac{a+bi}{c+di}=\frac{(a+bi)(c-di)}{c^2+d^2},\quad c+di\neq 0,
\]
- mnożenie przez \(\lambda\in\mathbb{R}\): \(\lambda(a+bi)=\lambda a+\lambda bi\).

W postaci trygonometrycznej \(z_k=r_k(\cos\varphi_k+i\sin\varphi_k)\):
- mnożenie:
\[
z_1z_2=r_1r_2\big(\cos(\varphi_1+\varphi_2)+i\sin(\varphi_1+\varphi_2)\big),
\]
- dzielenie:
\[
\frac{z_1}{z_2}=\frac{r_1}{r_2}\big(\cos(\varphi_1-\varphi_2)+i\sin(\varphi_1-\varphi_2)\big),\; r_2\neq 0.
\]
Dodawanie/odejmowanie najwygodniejsze są w postaci algebraicznej.

---

## 5. Wyznacznik Laplace’a i własności
**Pytanie:** Podać definicję wyznacznika macierzy wg Laplace’a i opisać 4 własności.

**Odpowiedź:**
Dla macierzy \(A=[a_{ij}]\in M_n\):
\[
\det A=\sum_{j=1}^{n}a_{ij}(-1)^{i+j}M_{ij}
\]
(przy rozwinięciu względem \(i\)-tego wiersza), gdzie \(M_{ij}\) to minor.

**Własności (przykładowe 4):**
1. Zamiana dwóch wierszy (lub kolumn) zmienia znak wyznacznika.
2. Gdy dwa wiersze są proporcjonalne (lub równe), \(\det A=0\).
3. Wyłączenie skalaru z wiersza mnoży wyznacznik przez ten skalar.
4. \(\det(AB)=\det A\cdot\det B\).

---

## 6. Macierz odwrotna: definicja, sposób wyznaczania, warunek istnienia
**Pytanie:** Zdefiniować macierz odwrotną oraz podać sposób jej wyznaczania i warunek konieczny istnienia.

**Odpowiedź:**
Dla macierzy kwadratowej \(A\), macierz \(A^{-1}\) spełnia
\[
AA^{-1}=A^{-1}A=I.
\]
Istnieje wtedy i tylko wtedy, gdy
\[
\det A\neq 0.
\]
Wyznaczanie: metodą dopełnień algebraicznych
\[
A^{-1}=\frac{1}{\det A}\operatorname{adj}(A)
\]
lub metodą Gaussa-Jordana: \([A|I]\to[I|A^{-1}]\).

---

## 7. Najprostsze równania macierzowe
**Pytanie:** Omówić rozwiązywanie najprostszych równań macierzowych.

**Odpowiedź:**
Przykłady:
- \(AX=B\): jeśli \(A\) odwracalna, to \(X=A^{-1}B\).
- \(XA=B\): \(X=BA^{-1}\).
- \(AXB=C\): \(X=A^{-1}CB^{-1}\), gdy \(A,B\) odwracalne.
Trzeba zachować kolejność mnożenia (nieprzemienność).

---

## 8. Układy Cramera
**Pytanie:** Omówić układy równań liniowych Cramera.

**Odpowiedź:**
Dla układu \(A\mathbf{x}=\mathbf{b}\), \(A\in M_n\):
- jeśli \(\det A\neq 0\), układ ma jedno rozwiązanie,
- wzory Cramera:
\[
x_k=\frac{\det A_k}{\det A},\quad k=1,\dots,n,
\]
gdzie \(A_k\) powstaje z \(A\) przez zamianę \(k\)-tej kolumny na \(\mathbf{b}\).

---

## 9. Metoda Gaussa
**Pytanie:** Omówić metodę Gaussa rozwiązywania układów równań liniowych.

**Odpowiedź:**
Tworzymy macierz rozszerzoną i wykonujemy operacje elementarne:
1. zamiana wierszy,
2. mnożenie wiersza przez liczbę \(\neq 0\),
3. dodanie wielokrotności jednego wiersza do drugiego.
Doprowadzamy układ do postaci schodkowej, wyznaczamy rzędy i:
- \(r(A)<r([A|b])\): brak rozwiązań,
- \(r(A)=r([A|b])=n\): jedno rozwiązanie,
- \(r(A)=r([A|b])<n\): nieskończenie wiele rozwiązań.

---

## 10. Iloczyn skalarny i zastosowania
**Pytanie:** Omówić iloczyn skalarny i jego zastosowania.

**Odpowiedź:**
Dla \(\mathbf{a},\mathbf{b}\in\mathbb{R}^n\):
\[
\mathbf{a}\cdot\mathbf{b}=\sum a_ib_i=|\mathbf{a}|\,|\mathbf{b}|\cos\theta.
\]
Zastosowania:
- kąt między wektorami,
- warunek prostopadłości: \(\mathbf{a}\cdot\mathbf{b}=0\),
- rzut wektora,
- odległości i normy (\(|\mathbf{a}|=\sqrt{\mathbf{a}\cdot\mathbf{a}}\)).

---

## 11. Iloczyn wektorowy i zastosowania
**Pytanie:** Omówić iloczyn wektorowy i jego zastosowania.

**Odpowiedź:**
Dla \(\mathbf{a},\mathbf{b}\in\mathbb{R}^3\):
\[
\mathbf{a}\times\mathbf{b}=\begin{vmatrix}
\mathbf{i}&\mathbf{j}&\mathbf{k}\\
a_1&a_2&a_3\\
b_1&b_2&b_3
\end{vmatrix}.
\]
Wynik jest prostopadły do obu wektorów,
\[
|\mathbf{a}\times\mathbf{b}|=|\mathbf{a}|\,|\mathbf{b}|\sin\theta.
\]
Zastosowania:
- pole równoległoboku/trójkąta,
- wyznaczanie wektora normalnego do płaszczyzny,
- orientacja prawoskrętna.

---

## 12. Iloczyn mieszany i zastosowania
**Pytanie:** Omówić iloczyn mieszany i jego zastosowania.

**Odpowiedź:**
Dla \(\mathbf{a},\mathbf{b},\mathbf{c}\in\mathbb{R}^3\):
\[
[\mathbf{a},\mathbf{b},\mathbf{c}]=(\mathbf{a}\times\mathbf{b})\cdot\mathbf{c}=\det[\mathbf{a}\,\mathbf{b}\,\mathbf{c}].
\]
Interpretacja geometryczna:
\(|[\mathbf{a},\mathbf{b},\mathbf{c}]|\) to objętość równoległościanu.
Jeśli iloczyn mieszany = 0, wektory są współpłaszczyznowe.

---

## 13. Równanie płaszczyzny w \(\mathbb{R}^3\)
**Pytanie:** Omówić równanie płaszczyzny w przestrzeni 3-wymiarowej.

**Odpowiedź:**
Postać ogólna:
\[
Ax+By+Cz+D=0,
\]
gdzie \(\mathbf{n}=(A,B,C)\) jest wektorem normalnym.
Postać punkt-normalna:
\[
\mathbf{n}\cdot(\mathbf{r}-\mathbf{r}_0)=0.
\]
Postać parametryczna (punkt \(P_0\), dwa niezależne kierunki \(\mathbf{u},\mathbf{v}\)):
\[
\mathbf{r}=\mathbf{r}_0+s\mathbf{u}+t\mathbf{v}.
\]

---

## 14. Równanie prostej w \(\mathbb{R}^3\)
**Pytanie:** Omówić równanie prostej w przestrzeni 3-wymiarowej.

**Odpowiedź:**
Postać wektorowa:
\[
\mathbf{r}=\mathbf{r}_0+t\mathbf{v}.
\]
Postać parametryczna:
\[
\begin{cases}
x=x_0+at,\\
y=y_0+bt,\\
z=z_0+ct.
\end{cases}
\]
Postać symetryczna (gdy \(a,b,c\neq 0\)):
\[
\frac{x-x_0}{a}=\frac{y-y_0}{b}=\frac{z-z_0}{c}.
\]

---

## 15. Wzajemne położenie prostej i płaszczyzny w \(\mathbb{R}^3\)
**Pytanie:** Omówić wzajemne położenie prostej i płaszczyzny.

**Odpowiedź:**
Dla prostej o kierunku \(\mathbf{v}\) i płaszczyzny o normalnej \(\mathbf{n}\):
- \(\mathbf{n}\cdot\mathbf{v}\neq 0\) — prosta przecina płaszczyznę (1 punkt),
- \(\mathbf{n}\cdot\mathbf{v}=0\) i punkt prostej spełnia równanie płaszczyzny — prosta zawarta,
- \(\mathbf{n}\cdot\mathbf{v}=0\) i punkt nie spełnia równania — prosta równoległa (brak punktów wspólnych).

---

## 16. Wzajemne położenie dwóch prostych w \(\mathbb{R}^3\)
**Pytanie:** Omówić wzajemne położenie dwóch prostych w przestrzeni 3-wymiarowej.

**Odpowiedź:**
Dwie proste mogą być:
1. **przecinające się** — mają punkt wspólny,
2. **równoległe** — wektory kierunkowe proporcjonalne, brak punktu wspólnego,
3. **pokrywające się** — równoległe i mają nieskończenie wiele punktów wspólnych,
4. **skośne** — nie są równoległe i nie przecinają się.

Dla prostych skośnych odległość:
\[
d=\frac{|(\mathbf{P_2}-\mathbf{P_1})\cdot(\mathbf{v_1}\times\mathbf{v_2})|}{|\mathbf{v_1}\times\mathbf{v_2}|}.
\]
