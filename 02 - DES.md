# 02 - DES
Caratteristiche:
- cifratura simmetrica (secret-key cryptography)
- funziona in blocchi da 64 bit (non è uno stream cipher)
- chiavi a 64 bit, di cui solo 58 sono usati (i rimanenti 8 servono per parity checks)

#### Operazioni

**Permutation**
![[Pasted image 20220601120114.png]]
Un bit dell'input determina un bit dell'output

**Substitution**
![[Pasted image 20220601120241.png]]
Il blocco di bit in input viene convertito in un blocco univoco in output

**Expansion**
![[Pasted image 20220601120331.png]]
Alcuni bit dell'input vengono ripetuti diverse volte nell'output

**Choice** (contraction) 
![[Pasted image 20220601120346.png]]
Alcuni bit dell'input non appaiono nell'output (vengono ignorati)
**Permuted choice:**
![[Pasted image 20220601120447.png]]

### Generale
![[Pasted image 20220601120623.png]]

**IP e FP box**
![[Pasted image 20220601120706.png]]
Sono invertite

**PC1 e PC2 box**
![[Pasted image 20220601120738.png]]
Alcuni bit sono mancanti (8,16,24, 32, 40, 48, 56, 64) in PC1
Alcuni bit sono mancanti (9,18, 25, 35, 38, 43, 45, 54) in PC2

**Un round in dettaglio**
![[Pasted image 20220601120905.png]]

**E-box**
![[Pasted image 20220601120932.png]]

**S-box**
![[Pasted image 20220601120955.png]]
I bit 1 e 6 selezionano la riga, i bit 2-5 selezionano la colonna in cui leggere un valore a 4-bit tra une delle 8 possibili mappe
![[Pasted image 20220601121110.png]]

**P-box**
Permutazione di 32-bit
![[Pasted image 20220601121136.png]]

Dal 1999 DES è considerata insicura per via della sua chiave troppo corta.

**AVG bruteforce**:
![[Pasted image 20220601121239.png]]