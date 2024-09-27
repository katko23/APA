# Problema: Sortare de Evenimente și Detectarea Suprapunerilor
## Descriere:
Ești responsabil pentru organizarea unui eveniment sportiv cu mai multe competiții care se desfășoară pe parcursul unei zile. Fiecare competiție are un interval de timp de start și final. Trebuie să te asiguri că nu există suprapuneri între competiții și să identifici suprapunerile acolo unde există.<br /> <br /> 

Scrie un program care, dată o listă de competiții cu intervale de timp, detectează și afișează toate suprapunerile.<br /> <br /> 

## Date de intrare:
O listă de competiții, fiecare reprezentată prin două valori: start și end, unde start este ora de început și end este ora de final a competiției.<br /> 
Fiecare competiție are loc într-o zi și este definită de ore în format 24 (de exemplu, 9 pentru 09:00 și 17 pentru 17:00).<br /> 

## Date de ieșire:
Dacă nu există suprapuneri între competiții, afișează "Nu există suprapuneri."<br /> 
Dacă există suprapuneri, afișează toate perechile de competiții care se suprapun, în formatul: (Competitie 1: start1 - end1) se suprapune cu (Competitie 2: start2 - end2)<br /> 

# Exemple:
### Intrare:

competiții = [(10, 12), (11, 13), (14, 16), (15, 17)]
### Ieșire:

(Competitie 1: 10 - 12) se suprapune cu (Competitie 2: 11 - 13) <br /> 
(Competitie 3: 14 - 16) se suprapune cu (Competitie 4: 15 - 17)<br /> 

### Intrare:

competiții = [(9, 11), (12, 14), (15, 17)]<br /> 
### Ieșire:

Nu există suprapuneri.<br /> 

## Explicație:
În Exemplul 1, competițiile (10, 12) și (11, 13) se suprapun, la fel ca și competițiile (14, 16) și (15, 17).<br /> 
În Exemplul 2, toate competițiile au intervale distincte, astfel că nu există suprapuneri.<br /> 

## Cerințe suplimentare:
Soluția trebuie să aibă complexitatea O(n log n).<br /> 
Încearcă să sortezi competițiile după ora de început și apoi să detectezi suprapunerile într-o singură trecere a listei.
## Indicații pentru rezolvare:
- Sortează competițiile după ora de început utilizând un algoritm de sortare eficient (Merge Sort sau Quick Sort).
- După sortare, parcurge lista de competiții. Dacă competiția curentă începe înainte ca cea anterioară să se fi terminat, înseamnă că există o suprapunere.
- Afișează perechile de competiții care se suprapun.
