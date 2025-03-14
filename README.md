# TEMA 1 Analiza algoritmilor

## Introducere

- Am rezolvat primele 3 cerinte pentru a putea combina masina
- Fiecare cerinta alte denumiri la stari, pentru a putea sa le combin mai usor intre ele
- Pe metoda pe care am mers, ar fi fost mai usor sa fac direct masina completa, am realizat asta cand am ajuns la task 3
- Am luat fiecare caz in parte pentru a putea rezolva cerinta 3
- Daca as fi rezolvat direct toata masina, stiu ca aveam un cod de 14000 de linii, insa terminam toate verificarile in 500 de pasi

## Cerinta 1 - skyscrapers_lines

- Am parcurs pana la :
- In acel moment schimbam starea, pentru a vedea daca apare 1, daca apare, se muta in starea de yes_1
- yes_1 se muta pana la urmatoarele : si daca nu era alt 1, se muta in starea sa vedem daca exista 2
- Asa se repeta si pentru 2, 3 si 4
- Dupa ce verificam pentru toate, eram pe cele : din stanga, trebuia sa trecem peste cele din dreapta, asa ca am luat o alta stare
- Cand atingeam acele puncte, ne mutam intr-o alta stare si cautam celelate :, apoi incepem iar verificarea pt 1, 2, 3 si 4
- Cand ajungem la _ este clar ca a fost totul corect si programul se termina cu Y

## Cerinta 2 - skyscrapers_columns

- Pentru aceasta cerinta am schimbat numerele ca sa reprezinte fiecare coloana, adica am folosit 4x4 charactere, se vad in fisierul numere.txt
- Am parcurs din stanga pana in dreapta, pentru a modifica numerele de dupa : in caractere
- Apoi am parcurs de la dreapta la stanga, pana cand am gasit primul numar, ma mut in starea de verificare daca mai exista alt numar la fel si il transform inapoi in cifra
- Ma duc pana in partea cealalta de sir si continui cu alt caracter din dreapta
- Cand nu mai era niciun caracter din cele 4x4, insemna ca a fost totul corect si programul se termina cu Y

## Cerinta 3 - skyscrapers_visibility

- Am inceput cu rezolvarea coloanelor, pentru ca am considerat ca trebuie sa incep cu ce este mai greu, ar fi fost putin mai eficient din punct de vedere al pasilor daca incepeam cu liniile
- Am aplicat aceeasi metoda ca la 2
- Am schimbat fiecare cifra cu un caracter
- Ajuns in partea din dreapta a sirului, incepem sa verificam cu prima cifra din dreapta si am folosit un patern, la fel cum scrie in numere.txt
- Am cautat fiecare pereche de numere pana in stanga de tot, verificand pe coloane, adica per fiecare caracter
- Spre exemplu, in dreapta de tot, am inceput cu coloana 4, adica am verificam perechea pe coloana 4
- Apoi in dreapta am inceput cu coloana 1, apoi din dreapta cu coloana 3, stanga coloana 2, dreapta coloana 2, stanga coloana 3, dreapta coloana 1, stanga coloana 4
- Cand am fost in stanga si am ajuns la final in dreapta, a trebuit sa modific din nou caracterele in cifre, pentru am fi mai usor pentru linii
- Prin modificarea de caractere am ajuns inapoi in stanga
- Am parcurs din stanga in dreapta, cand dadeam de semnul #, insemna ca trebuie sa citesc primul numar de dupa #
- Vedeam care este numarul, si apoi aplicam patern-ul pt cifrele de dupa :, pana intalneam urmatoarele :
- Daca ajungeam sa atingem celelalte :, insemna ca a fost corect si cautam urmatorul #, pentru a continua
- Cand ajungeam in dreapta la "_", insemna ca trebuies sa fac verificarea spre stanga, asa ca am aplicat aceeasi metoda
- Daca si din dreapta spre stanga se ajungea la "_" programul se termina cu Y

## Lipirea pentru tot programul - skyscrapers_final

- Pentru a lipii tot programul, dupa cerinta 1, am realizat ca raman in dreapta, dar eu trebuie sa fiu in stanga pentru a incepe rezolvarea pt cerinta 2, asa ca m-am mutat in stanga
- Am schimbat din programul de la cerinta 1 `"Y,_,-"` in start_cerinta2,_,>
- Dupa cerinta 2, sunt intros la inceput, ceea ce imi permite sa incep direct cerinta 3
- Am schimbat la cerinta 2 din `"Y,_,-"` in "start_cerinta3,_,>"
- Apoi se rezolva cerinta 3, si cand se ajunge la final programul se termina cu Y