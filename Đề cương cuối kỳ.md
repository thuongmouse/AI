## Trí tuệ nhân tạo

### Các mốc phát triển của trí tuệ nhân tạo?

Giải:

- Năm 1956 Thuật ngữ trí tuệ nhân tạo ra đời.
- Năm 1957 Chương trình đầu tiên chứng minh tự động định lý
- Năm 1960 GPS \(general problem solving\) chương trình giải quyết bài toán vạn năng
- Năm 1963 Phần mềm chơi cờ vua của Samuel
- Năm 1964 giải đại số sơ cấp ELIZA
- Năm 1965 AI STUDENT phân tích và tổng hợp tiếng nói.
- Năm 1971 Hệ chuyên gia MYCIN \(Stanford\). 
- Năm 1972 ProLog \(Programmation en Logique\) ra đời do Alain Calmerauer. 
- Năm 1997 Deepblue chơi cờ thắng kiện tướng Kasparov

### Hãy giới thiệu các chuyên ngành của trí tuệ nhân tạo và ứng dụng của nó?

Giải:

1. Tri thức
2. Lập luận
3. Hệ chuyên gia
4. Dịch máy \+ ngôn ngữ
5. Nhìn máy \(computer vision\)
6. Học máy \(machine learning\)
7. ANN \(mạng neuron\)
8. Robotics

### Phân biệt sự khác nhau giữa quá trình trí tuệ nhân tạo và quá trình xử lí dữ liệu truyền thống?

Giải:
Trang 22

## Tri thức

### Hãy liệt kê kĩ thuật thể hiện, biểu diễn tri thức?

Giải:

1. OAV \(Object attribute value\) Đối tượng \- thuộc tính \- giá trị.
2. Luật
3. Bảng đen
4. Mạng ngữ nghĩa
5. Khung
6. Phụ thuộc khái niệm
7. Logic mệnh đề
8. Logic vị từ

### Phân loại tri thức ra sao?

Giải:

- Theo Locke:
  - Tri thức trực giác
  - Tri thức mô tả
  - Tri thức cảm xúc
- Theo MIT:
  - Tri thức thủ tục.
  - Tri thức mô tả
  - Tri thức meta
  - Tri thức may rủi
  - Tri thức cấu trúc

### Tri thức TACIT và các chuyển hóa của nó

Giải:

- Tri thức ẩn (tacit knowledge)
- Các chuyển hóa: trang 32

### Hãy giới thiệu về tri thức LUẬT và lấy thí dụ?

Giải:
Trang 46 - 50

### Hãy giới thiệu về tri thức KHUNG và lấy thí dụ minh họa ?

Giải:
TRang 55 - 59

### Hãy giới thiệu về tri thức mạng ngữ nghĩa và lấy thí dụ minh họa

Giải:
Trang 52 - 54

## Giải vấn đề và lập luận

### Hãy phát biểu cơ sở của việc giải vấn đề trong hệ thống logic

Giải:


### Hãy giới thiệu về các kĩ thuật lập luận ?

Giải:

### Hãy giới thiệu về suy diễn và lấy thí dụ minh họa ?

Giải:

### Hãy giới thiệu về suy luận tiến và lấy thí dụ minh họa

Giải:

### Hãy nêu các ưu và nhược điểm của suy luận tiến ?

Giải:

### Hãy giới thiệu về suy luận lùi và lấy thí dụ minh họa

Giải:

### Hãy nêu các ưu và nhược điểm của suy luận lùi ?

Giải:

### Hãy phân biệt việc tìm sâu với tìm rộng trên cây khi giải vấn đề, và cho thí dụ minh họa ?

Giải:

### Hãy phát biểu thuật toán Robison để giải vấn đề trong hệ thống logic?

Giải:

### Hãy phát biểu thuật toán LEO NÚI ?

Giải:

## Hệ chuyên gia

### Hãy giới thiệu cấu trúc của hệ chuyên gia ?

Giải:

### Hãy nêu vai trò của STM trong cấu trúc của hệ chuyên gia ?

Giải:

### Hãy nêu vai trò của LTM trong cấu trúc của hê chuyên gia

Giải:

### Hãy nêu một số đặc điểm của CHUYÊN GIA trong hệ chuyên gia?

Giải:

### Hãy cho biết năng lực của KĨ SƯ TRI THỨC trong hệ chuyên gia?

Giải:

### Hãy nêu vai trò của NGƯỜI DÙNG trong cấu trúc của hệ chuyên gia ?

Giải:

### Hãy cho biết hệ chuyên gia MYCIN

Giải:

### Hãy giới thiệu về CF trong lí thuyết chắc chắn ?

Giải:

### Hãy đưa giải pháp về lan truyền CF đối với các luật có nhiều giả thiết ?

Giải:

# Lập trình Prolog

## Bài tập lẻ

### Tìm anh em của một người trên cây gia phả ?

Giải:

```
predicates
  cha(symbol,symbol)
  anhem(symbol,symbol)
clauses
  cha(man,mo).
  cha(man,dao).
  cha(tao,man).
  cha(tao,le).
  cha(le,dua).

  anhem(X,Y) :- cha(P,X), cha(P,Y), X >< Y.
  anhem(X,Y) :- cha(P,X), cha(Q,Y), anhem(P,Q).
```

### Chứng minh Mơ khỏe?

1. Mơ, Mận là bạn
2. Bạn sẽ học cùng môn
3. Mơ học môn bóng chuyền
4. Mận học bơi
5. Ai học bơi sẽ khoẻ

Giải:

```
predicates
  ban(symbol,symbol)
  hoc(symbol,symbol)
  khoe(symbol)
clauses
  ban(man, mo).
  ban(mo, man).
  hoc(mo,bongchuyen).
  hoc(man,boi).

  hoc(P1,X) :- ban(P1,P2), hoc(P2,X).
  khoe(X) :- hoc(X,boi).
```

### Phát hiện một số có chia hết cho 7 và 3 hay không?

Giải:

```
predicates
  chiahet(integer)
clauses
  chiahet(X):- X mod 7 = 0, X mod 3 = 0.
```

### Kiểm tra ba giá trị đọc vào A, B, C có thể là ba cạnh của một tam giác không ?

Giải:

```
predicates
  tamgiac(integer, integer, integer)
clauses
  tamgiac(A, B, C) :- A + B > C, B + C > A, A + C > B.
```

## Bài tập tính toán

### Tìm tổng các số chẵn từ 1 đến N ?

Giải:

```
predicates
  tongchan(integer, real)
clauses
  tongchan(0, K) :- K = 0, !.
  tongchan(0, 0) :- !.
  tongchan(N, K) :- N mod 2 = 1, N1 = N - 1, tongchan(N1, K).
  tongchan(N, K) :- N mod 2 = 0, N1 = N - 1, tongchan(N1, K1), K = K1 + N.
```

### Tìm tổng của các số nguyên chẵn từ M đến N?

Giải cách 1:

```
predicates
  tong(integer,integer,integer)
clauses
  tong(M, M, M) :- M mod 2 = 0, !.
  tong(M, M, 0) :- M mod 2 = 1, !.
  tong(M, N, K) :- M < N, N mod 2 = 0, N1 = N - 1, tong(M, N1, K1), K = K1 + N.
  tong(M, N, K) :- M < N, N mod 2 = 1, N1 = N - 1, tong(M, N1, K).
```

Giải cách 2:

```
predicates
  tong(integer,integer,integer)
clauses
  tong(M, M, M) :- M mod 2 = 0, !.
  tong(M, M, 0) :- M mod 2 = 1, !.
  tong(M, N, K) :- M < N, M mod 2 = 0, M1 = M + 1, tong(M1, N, K1), K = K1 + M.
  tong(M, N, K) :- M < N, M mod 2 = 1, M1 = M + 1, tong(M1, N, K).
```

### Tìm tổng của các số nguyên chia hết cho 3 từ M đến N?

Giải cách 1:

```
predicates
  tong(integer,integer,integer)
clauses
  tong(M, M, M) :- M mod 3 = 0, !.
  tong(M, M, 0) :- M mod 3 >< 0, !.
  tong(M, N, K) :- M < N, N mod 3 = 0, N1 = N - 1, tong(M, N1, K1), K = K1 + N.
  tong(M, N, K) :- M < N, N mod 3 >< 0, N1 = N - 1, tong(M, N1, K).
```

Giải cách 2:

```
predicates
  tong(integer,integer,integer)
clauses
  tong(M, M, M) :- M mod 3 = 0, !.
  tong(M, M, 0) :- M mod 3 >< 0, !.
  tong(M, N, K) :- M < N, M mod 3 = 0, M1 = M + 1, tong(M1, N, K1), K = K1 + M.
  tong(M, N, K) :- M < N, M mod 3 >< 0, M1 = M + 1, tong(M1, N, K).
```

### Tìm tổng của các số nguyên không chia hết cho 5 từ M đến N ?

Giải cách 1:

```
predicates
  tong(integer,integer,integer)
clauses
  tong(M, M, M) :- M mod 5 >< 0, !.
  tong(M, M, 0) :- M mod 5 = 0, !.
  tong(M, N, K) :- M < N, N mod 3 = 0, N1 = N - 1, tong(M, N1, K1), K = K1 + N.
  tong(M, N, K) :- M < N, N mod 3 >< 0, N1 = N - 1, tong(M, N1, K).
```

Giải cách 2:

```
predicates
  tong(integer,integer,integer)
clauses
  tong(M, M, M) :- M mod 5 >< 0, !.
  tong(M, M, 0) :- M mod 5 = 0, !.
  tong(M, N, K) :- M < N, M mod 5 >< 0, M1 = M + 1, tong(M1, N, K1), K = K1 + M.
  tong(M, N, K) :- M < N, M mod 5 = 0, M1 = M + 1, tong(M1, N, K).
```

## Bài tập giải phương trình

### Tìm giá trị X thỏa mãn aX + b = 0, khi biết a và b?

Giải cách 1:

```
predicates
  giaipt(real,real)
clauses
  giaipt(0,0) :- write("VSN"), nl, !.
  giaipt(0,_) :- write("Phuong trinh vo nghiem"), fail, !.
  giaipt(A,B) :- X = -B/A, write("X =", X), nl, !.
```

Giải cách 2: (Đừng dùng vì tắt warning mới chạy)

```
predicates
  giaipt(real,real,real)
clauses
  giaipt(0,0,_) :- write("VSN"), nl, !.
  giaipt(0,_,_) :- fail, !.
  giaipt(A,B,X) :- A <> 0, X= -B/A, !.
```

### Tìm A khi biết x, y, z và Ax + y = z ?

Giải:

```
predicates
  giaipt(real,real,real)
clauses
  giaipt(0,A,A) :- write("VSN"), nl, !.
  giaipt(0,_,_) :- write("Phuong trinh vo nghiem"), fail, !.
  giaipt(X,Y,Z) :- A = (Z-Y)/X, write("A =", A), nl, !.
```

## Bài tập danh sách

### Đếm số các phần tử của một danh sách số thực?

Giải:

```
domains
  ds = real*
predicates
  length(ds,real)
clauses
  length([],0) :- !.
  length([_|T],L):- length(T,N), L = N+1, !.
```

### Phát hiện trong danh sách số nguyên có số 1 liền kề với số 2 hay không?

Giải cách 1:

```
domains
  ds = integer*
predicates
  ke(ds)
clauses
  ke([]) :- fail, !.
  ke([1|T]) :- T = [2|_], !.
  ke([2|T]) :- T = [1|_], !.
  ke([_|T]) :- ke([T]), !.
```

Giải cách 2:

```
domains
  ds = integer*
predicates
  tim12(ds)
clauses
  tim12([]) :- fail, !.
  tim12([1|_]) :- !.
  tim12([2|_]) :- !.
  tim12([_,A|T]) :- tim12([A|T]),!.
```

### Phát hiện hai danh sách có giống nhau hay không ?

Giải:

```
domains
  ds = integer*
predicates
  compare(ds,ds)
clauses
  compare([],[]) :- !.
  compare([X|T1],[X|T2]) :- compare(T1,T2), !.
  compare([_],[_]) :- fail, !.
```

### Tìm số nguyên lớn nhất trong danh sách các số nguyên ?

Giải cách 1:

```
domains
  ds=integer*
predicates
  max(ds,integer)
clauses
  max([],_) :- fail.
  max([X],X) :- !.
  max([H|T],X) :- max(T,X), X > H, !.
  max([H|T],H) :- max(T,X), X < H, !.
```

Giải cách 2:

```
domains
  ds=integer*
predicates
  max(ds,integer)
clauses
  max([],_) :- fail.
  max([X],X) :- !.
  max([A,B|T],X) :- A > B, max([A|T],X), !.
  max([A,B|T],X) :- B > A, max([B|T],X), !.
```

### Kiểm tra một số nguyên có thuộc vào danh sách các số nguyên hay không?

Giải:

```
domains
  ds = integer*
predicates
  thuoc(integer,ds)
clauses
  thuoc(X,[X|_]) :- !.
  thuoc(X,[H|T]) :- X <> H, thuoc(X,T).
  thuoc(_,[]) :- fail, !.
```

### Tìm hợp của hai danh sách số thực?

Giải cách 1 (Không có lọc trùng):

```
domains
  ds=real*
predicates
  hop(ds,ds,ds)
clauses
  hop([],L2,L2) :- !.
  hop([X|T1],L2,[X|T3]) :- hop(T1,L2,T3), !.
```

Giải cách 2 (Có lọc trùng):

```
domains
  ds = real*
predicates
  hop(ds,ds,ds)
  thuoc(real,ds)
clauses
  thuoc(X,[X|_]) :- !.
  thuoc(X,[H|T]) :- X <> H, thuoc(X,T).
  thuoc(_,[]) :- fail, !.

  hop([],L,L) :- !.
  hop([H|T],L,L2):- thuoc(H,L),!, hop(T,L,L2).
  hop([H|T1],L2,[H|T3]):- hop(T1,L2,T3).
```

### Tìm giao của hai danh sách số nguyên?

Giải:

```
domains
  ds = integer*
predicates
  thuoc(integer,ds)
  giao(ds,ds,ds)
clauses
  thuoc(X,[X|_]) :- !.
  thuoc(X,[H|T]) :- X <> H, thuoc(X,T).
  thuoc(_,[]) :- fail, !.

  giao([],_,[]) :- !.
  giao(_,[],[]) :- !.
  giao([H|T],L2,[H|L]) :- thuoc(H,L2), !, giao(T,L2,L).
  giao([_|T],L2,L) :- giao(T,L2,L).
```

## Bài tập cơ sở dữ liệu

Trong cơ sở dữ liệu NG (tên, tuổi, địachỉ), ĐIỂM (tên, toán, văn), Tìm TUỔI của người

Dữ liệu ví dụ (xuống dưới đoạn này sẽ được thay bằng cụm này `%DLVD` cho gọn trong code, thi viết có thể bỏ):

```
  ng(mo,20,"HANOI").
  ng(man,19,"Ha Noi").
  ng(dao,20,"Hanoi").
  ng(le,19,"HANOI").
  ng(tao,20,"Ha Noi").
  ng(dua,19,"Hanoi").

  diem(mo,6.8,7.4).
  diem(man,9.5,3.8).
  diem(dao,9.1,4.6).
  diem(le,2.8,6.0).
  diem(tao,4.4,7.8).
  diem(dua,9,10).
```

### Có điểm TOÁN trên 7?

Giải:

```
predicates
  ng(symbol,integer,string)
  diem(symbol,real,real)
  toant7(integer)
clauses
  %DLVD

  toant7(Z):- diem(X,Y,_), Y > 7, ng(X,Z,_).
```

### Có điểm trung bình trên 7?

Giải:

```
predicates
  ng(symbol,integer,string)
  diem(symbol,real,real)
  tbt7(integer)
clauses
  %DLVD

  tbt7(Z):- diem(X,T,V), (T + V) / 2 > 7, ng(X,Z,_).
```

### Sống tại HANOI?

Giải:

```
predicates
  ng(symbol,integer,string)
  diem(symbol,real,real)
  tuoihn(integer)
clauses
  %DLVD

  tuoihn(Z):- ng(_,Z,"HANOI").
```

# Bài tập Suy luận

## Cho 5 tri thức sau. Chứng minh X bằng

1. $A \rightarrow B \lor C$
2. $A$
3. $A \rightarrow B \land D$
4. $B \rightarrow X \land Y$
5. $C \rightarrow X$

### Suy luận tiến ?

Giải:

1. Ta có trạng thái ban đầu $STM = \{\}$
2. Theo $Rule 2$ ta có $STM = STM \cup \{A\} = \{A\}$
3. Ta thấy $STM$ khớp với vế trái $Rule 3 \rightarrow Rule 3$ cháy, ta có $STM = STM \cup \{B \land D\} = \{A,B,D\}$.
4. Ta thấy $STM$ khớp với vế trái $Rule 4 \rightarrow Rule 4$ cháy, ta có $STM = STM \cup \{X \land Y\} = \{A,B,D,X,Y\}$.
5. Ta thấy $X$ trong $STM \rightarrow$ điều phải chứng minh là đúng

### Suy luận lùi ?

Giải:

1. Ta có đích $G_0=\{X\}$ cần phải chứng minh
2. Xét $Rule4$, để $G_0$ đúng ta cần có vế trái đúng tức $G_1=\{B\}$ đúng 
3. Xét $Rule3$, để $G_1$ đúng, ta cần có vế trái đúng tức $G_2=\{A\}$ đúng
4. Xét $Rule2$, do $Rule2$ nên $G_2$ đúng 

$\Rightarrow$ Kết luận: bài toán được chứng minh

### Thuật toán Robison ?

Giải:

1. Viết lại các luật và Skolem hóa chuyển $E_i, R_F$ thành câu chuẩn

- R1: $A \rightarrow B \lor C \Rightarrow \overline{A} \lor B \lor C$
- E1: $A$
- R2a: $A \rightarrow B \Rightarrow \overline{A} \lor B$
- R2b: $A \rightarrow D \Rightarrow \overline{A} \lor D$
- R3a: $B \rightarrow X \Rightarrow \overline{B} \lor X$
- R3b: $B \rightarrow Y \Rightarrow \overline{B} \lor Y$
- R4: $C \rightarrow X \Rightarrow \overline{C} \lor X$

2. Ta có $F = \{ \overline{A} \lor B \lor C, \overline{A} \lor B, \overline{A} \lor D, \overline{B} \lor X, \overline{B} \lor Y, \overline{C} \lor X, A\}$
3. Sử dụng phương pháp phản chứng, ta chứng minh $X$ sai, $F' = F \cup \{\overline{X}\} = F = \{ \overline{A} \land B, \overline{A} \land C, \overline{A} \lor B, \overline{A} \lor D, \overline{B} \lor X, \overline{B} \lor Y, \overline{C} \lor X, A, \overline{X}\}$
4. Ta chọn $\overline{X}$ và $\overline{B} \lor X$, ta có $F'_1 =\{\overline{X}\} \cup \{\overline{B} \lor X\} = \overline{B}$
5. Ta chọn $\overline{A} \lor B$ kết hợp với $F'_1$ ta có $F'_2 = \{\overline{B}\} \cup \{\overline{A} \lor B\} = \overline{A}$
6. Ta chọn $A$ kết hợp $F'_2$ ta có $\{\overline{A}\} \cup \{A\} = nil$. Vô lý

$\Rightarrow$ Kết luận: bài toán nghịch vô lý, bài toán được chứng minh đúng

## Cho 6 tri thức sau. Chứng minh x bằng

1. $a \lor b \rightarrow c$
2. $c \land d \rightarrow e \land f \land g$
3. $a$
4. $d$
5. $f \rightarrow x$
6. $x \land d \rightarrow y$

**Luật thành:**  
1.1 $a \rightarrow c$  
1.2 $b \rightarrow c$  
2.1 $c \land d \rightarrow e$  
2.2 $c \land d \rightarrow f$  
2.3 $c \land d \rightarrow g$  
3. $a$  
4. $d$  
5. $f \rightarrow x$  
6. $x \land d \rightarrow y$

### Suy luận tiến ?

Giải:

1. Ta có trạng thái ban đầu $STM = \{\}$
2. Theo $Rule 3$ ta có $STM = STM \cup \{a\} = \{a\}$  
3. Ta thấy $STM$ khớp với vế trái $Rule 1 \rightarrow Rule 1$ cháy, ta có $STM = STM \cup \{c\} = \{a,d,c\}$.
4. Ta thấy $STM$ khớp với vế trái $Rule 2 \rightarrow Rule 2$ cháy, ta có $STM = STM \cup \{e,f,g\} =  \{a,d,c,e,f,g\}$.
5. Ta thấy $STM$ khớp với vế trái $Rule 5 \rightarrow Rule 5$ cháy, ta có $STM = STM \cup \{x\} =\{a,d,c,e,f,g,x\}$
6. Ta thấy $X$ trong $STM \rightarrow$ điều phải chứng minh là đúng

### Suy luận lùi ?

Giải:

1. Ta có đích $G_0=\{x\}$ cần phải chứng minh
2. Xét $Rule5$, để $G_0$ đúng ta cần có vế trái tức $G_1=\{f\}$ đúng
3. Xét $Rule2$, để $G_1$ đúng, ta cần có vế trái tức $G_2=\{c \land d\}$ đúng hay ta cần $G_{21} = \{c\}$ đúng và $G_{22} = \{d\}$ đúng
4. Xét $Rule1$, để $G_{21}$ đúng ta cần có vế trái tức $G_3=\{a \lor b\}$ đúng hay ta cần $G_{31} = \{a\}$ đúng hoặc $G_{32} = \{b\}$ đúng
5. Xét $Rule3$, do $Rule3$ nên $G_{31}$ đúng
6. Xét $Rule4$, do $Rule4$ nên $G_{22}$ đúng

$\Rightarrow$ Kết luận: bài toán được chứng minh

### Thuật toán Robison ?

Giải:

1. Viết lại các luật và Skolem hóa chuyển $E_i, R_F$ thành câu chuẩn

- R1a: $a \rightarrow c \Rightarrow \overline{a} \lor c$
- R1b: $b \rightarrow c \Rightarrow \overline{b} \lor c$
- R2a: $c \land d \rightarrow e \Rightarrow \overline{c} \lor \overline{d} \lor e$
- R2b: $c \land d \rightarrow f \Rightarrow \overline{c} \lor \overline{d} \lor f$
- R2c: $c \land d \rightarrow g \Rightarrow \overline{c} \lor \overline{d} \lor g$
- E3: $a$
- E4: $d$
- R3b: $f \rightarrow x \Rightarrow \overline{f} \lor x$
- R4: $x \land d \rightarrow y  \Rightarrow \overline{x} \lor \overline{d} \lor y$

2. Theo bài, áp dụng thuật toán Skolem hóa, ta chuyển $E_i, R_F$ thành câu chuẩn, ta có $F = \{\overline{a} \lor c, \overline{b} \lor c, \overline{c} \lor \overline{d} \lor e, \overline{c} \lor \overline{d} \lor f, \overline{c} \lor \overline{d} \lor g, \overline{f} \lor x, \overline{x} \lor \overline{d} \lor y, a, d \}$
3. Sử dụng phương pháp phản chứng, ta chứng minh $X$ sai, $F' = F \cup \{\overline{x}\} = F = \{\overline{a} \lor c, \overline{b} \lor c, \overline{c} \lor \overline{d} \lor e, \overline{c} \lor \overline{d} \lor f, \overline{c} \lor \overline{d} \lor g, \overline{f} \lor x, \overline{x} \lor \overline{d} \lor y, a, d , \overline{x}\}$
4. Ta chọn $\overline{x}$ và $\overline{f} \lor x$, ta có $F'_1 =\{\overline{x}\} \cup \{\overline{f} \lor x\} = \overline{f}$
5. Ta chọn $\overline{c} \lor \overline{d} \lor f$ kết hợp $F'1$ ta có $F'_2 = \{\overline{c} \lor \overline{d} \lor f\} \cup \{\overline{f}\} = \{\overline{c} \land \overline{d}\}$
6. Ta chọn $d$ kết hợp $F'2$ ta có $F'_3 = \{\overline{c} \land \overline{d}\} \cup \{d\} = \{\overline{c}\}$
7. Ta chọn $\overline{a} \lor c$ kết hợp $F'3$, ta có $F'_4 =\{\overline{a} \lor c\} \cup \{c\} = \overline{a}$
8. Ta chọn $a$ kết hợp $F'_4$ ta có $\{\overline{a}\} \cup \{a\} = nil$. Vô lý

$\Rightarrow$ Kết luận: bài toán nghịch sai, bài toán được chứng minh đúng

## Cho các tri thức sau, hãy chứng minh Mơ khỏe bằng thuật toán Robison?

1. Mơ, Mận là bạn.
2. Bạn sẽ học cùng môn 
3. Mơ học môn bóng chuyền
4. Mận học bơi
5. Ai học bơi sẽ khoẻ

Giải:

1. Chuyển mệnh đề sang dạng câu

- $ban(mo,man)$ 
- $ban(X,Y) \rightarrow hoc(X,Z) \land hoc(Y,Z)$ với $X, Y$ là người, Z là môn học
- $hoc(mo, bongchuyen)$
- $hoc(man,boi)$
- $khoe(X) \rightarrow boi(X)$ với $X$ là người

2. Theo bài, áp dụng thuật toán Skolem hóa, ta chuyển $E_i, R_F$ thành câu chuẩn

- $E_1:$ $ban(mo,man)$ 
- $E_2:$ $hoc(mo, bongchuyen)$
- $E_3:$ $hoc(man,boi)$
- $R_1:$ $\sim ban(X,Z) \ \lor (hoc(X,Z) \ \lor hoc(Y,Z))$
- $R_2:$ $\sim khoe(X) \land hoc(X,boi)$

3. Sử dụng phương pháp phản chứng, ta chứng minh $G=\{khoe(mo)\}$ sai
4. Kết hợp $G$ với $R_2$ $\rightarrow$ ta được $G_1 = \sim hoc(mo,boi)$
5. Kết hợp $R_1$ với $G_1$ $\rightarrow$ ta được $G_2 = \{ \sim ban(mo,Y) \ \lor hoc(Y,boi)\}$. 
6. Kết hợp $E_3$ với $G_2$ $\rightarrow$ ta được $G_3=\{\sim ban(mo,man)\}$
7. Kết hợp $E_1$ với $G_3$ $\rightarrow$ ta được $\{\sim ban(mo,man)\} \cup \{ban(mo,man)\} = nil$. Vô lý

$\Rightarrow$ Kết luận: bài toán nghịch sai, bài toán được chứng minh đúng

