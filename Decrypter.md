## Arquivo com comando do Python para descriptografar.

- import os
- import pyaes

### Abrir o arquivo criptografado

- file_name = 'Auditoria_Financeira.txt.ransomwaretroll'
- file = open(file_name, 'rb')
- file_data = file.read()
- file.close()

### Chave de descriptação

- key = b"cryptoransowares"
- aes = pyaes.AESModeOfOperationCTR(key)
- decrypt_data = aes.decrypt(file_data)

### Remover o arquivo criptografado

- os.remove(file_name)

### Criar novo arquivo descriptografado

- new_file = 'Auditoria_Financeira.txt'
- new_file = open(f'{new_file}','wb')
- new_file.write(decrypt_data)
- new_file.close()