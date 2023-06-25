
# ElGamal Cryptosystem

## Deskripsi

Algoritma ElGamal merupakan salah satu algoritma kriptografi kunci publik (asimetris) yang dibuat berdasarkan algoritma pertukaran kunci Diffie-Hellman. Algoritma ini dikemukakan oleh Taher Elgamal pada tahun 1985 dan umum digunakan pada skema digital signature.  
Letak keamanan dari algoritma ini terdapat pada sulitnya memecahkan permasalahan logaritma diskrit.   
Permasalahan logaritma diskrit berbunyi:  
Jika p adalah bilangan prima dan g dan y adalah sembarang bilangan bulat, carilah x sedemikian sehingga:  

$$ \Huge a^{x} \equiv y \hspace{-8pt} \pmod{p} $$

## Parameter

### Input
- p, bilangan prima besar&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;=> PUBLIK
- g, bilangan bulat generator (umumnya kecil)  
  **g harus primitive root modulo terhadap p**
- d, kunci privat untuk mendekripsi pesan  
  **1 <= d <= (p - 2)**
- m, pesan yang ingin dienkripsi  
  **0 <= m <= (p - 1)**
- k, bilangan bulat acak  
  **0 <= k <= (p - 1)**
- k_pub, kunci publik  
  $ k\_{pub} \equiv a $
- k_ephemeral
- k_mask


### Output

## Skenario

Alice dan Bob ingin bertukar pesan pada saluran publik dengan menggunakan algoritma ElGamal.  
Setelah melalui proses diskusi maka diputuskan bahwa Alice akan berperan dalam proses pembangkitan kunci.  
Alice kemudian akan menghasilkan kunci publik dan kunci privat.  
Kunci publik akan digunakan oleh Bob untuk mengenkripsi pesan.  
Pesan yang sudah dienkripsi akan dikirimkan kepada Alice.  
Alice kemudian mendekripsi pesan menggunakan kunci privat yang dimilikinya.

### Pembangkitan Kunci

Proses pembangkitan kunci dilakukan oleh Bob.  
Pada tahap ini Bob akan memilih
### Enkripsi

### Dekripsi

## Ilustrasi