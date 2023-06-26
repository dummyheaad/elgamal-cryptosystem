
# ElGamal Cryptosystem

## Deskripsi

Algoritma ElGamal merupakan salah satu algoritma kriptografi kunci publik (asimetris) yang dibuat berdasarkan algoritma pertukaran kunci Diffie-Hellman. Algoritma ini dikemukakan oleh Taher Elgamal pada tahun 1985 dan umum digunakan pada skema digital signature.  
Letak keamanan dari algoritma ini terdapat pada sulitnya memecahkan permasalahan logaritma diskrit.   
Permasalahan logaritma diskrit berbunyi:  
Jika p adalah bilangan prima dan g dan y adalah sembarang bilangan bulat, carilah x sedemikian sehingga:  

$$\Huge a^{x} \equiv y \hspace{-8pt} \pmod{p}$$

## Parameter

### Input

- p, bilangan prima besar  
  **(PUBLIK)**  
  
- g, bilangan bulat generator (umumnya kecil)  
  **g harus primitive root modulo terhadap p**  
  **(PUBLIK)**  
 
- d, kunci privat untuk mendekripsi pesan)  
  **1 <= d <= (p - 2)**  
  **(RAHASIA)**  
  
- m, pesan yang ingin dienkripsi  
  **0 <= m <= (p - 1)**  
  **(RAHASIA)**  
  
- k, bilangan bulat acak  
  **0 <= k <= (p - 1)**  
  **(RAHASIA)**  
  
- k_pub, kunci publik  
  $\large k\\_pub \equiv g^{d} \pmod{p}$  
  **(PUBLIK)**  
  
- k_ephemeral, kunci sementara untuk membentuk k_mask pada penerima pesan  
  $\large k\\_ephemeral \equiv g^{k} \pmod{p}$  
  **(PUBLIK)**  
  
- k_mask, kunci yang digunakan untuk enkripsi dan dekripsi  
  $\large k\\_mask \equiv (k\\_pub)^{k} \pmod{p}$  
  **(RAHASIA)**  
  

### Output

- c, ciphertext hasil enkripsi  
  $\large c \equiv m*k\\_mask \pmod{p}$  
  **(PUBLIK)**  

- x, plaintext hasil dekripsi
  $\large k\\_mask \equiv (k\\_ephemeral)^{d} \pmod{p}$
  
  $\large k\\_mask\*inv\\_k\\_mask \equiv 1 \pmod{p}$
  
  $\large inv\\_k\\_mask \equiv (k\\_ephemeral)^{p - 1 - d} \pmod p$ => (Fermat's little theorem)
  
  $\large x \equiv c\*inv\\_k\\_mask \pmod{p}$  
  **(RAHASIA)**
  
### (Tambahan) Fermat's little theorem

  Jika a dan p adalah *coprime* maka:  
  $\large a^{p - 1} \equiv 1 \pmod{p}$  
  
  sehingga, kita bisa menghitung inverse dari a dalam mod p, yaitu:  
  $\large a^{p - 1} \equiv 1 \pmod{p}$  
  $\large a\*a^{p - 2} \equiv 1 \pmod{p}$  
  
  maka $\large a^{p - 2}$ adalah inverse a dalam mod p  
  Dapat dituliskan dalam bentuk umum:  
  
  $\large a^{d}\*a^{p - 1 - d} \equiv 1 \pmod{p}$  
  diperoleh inverse dari $\large a^{d}$ bernilai $\large a^{p - 1 - d}$


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