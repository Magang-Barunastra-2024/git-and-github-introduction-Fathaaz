[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/tbEHDGEc)
# Git and Github Introduction

| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Fatharanni Faza   | ELC | Electrical Design |

## Early Procedure
### 1. Melakukan instalasi Git ke PC/Laptop
	https://git-scm.com/downloads
 ![screenshot-1732147697821](https://github.com/user-attachments/assets/4869d690-5eae-4456-a8ea-e3fe0da6c0ce)
### 2. Membuat akun Github
	https://github.com/join
 ![screenshot-1732147814907](https://github.com/user-attachments/assets/309c90cd-8883-4085-8ae2-536ab54f01c0)
### 3. Melakukan setting pada Terminal
   ```
   git config --global user.name (masukkan username)
   git config --global user.email (masukkan email)
   ```
![Screenshot 2024-11-21 124034](https://github.com/user-attachments/assets/e0060b5b-243a-4e75-985f-73e741b1fa57)
### 4. Membuat SSH Keys dan Menghubungkannya Pada Github
#### a. Membuat Key pada Terminal dengan Menggunakaan Command Line Berikut
   ```
   ssh-keygen -t ed25519 -C (masukkan email)
   ### Lalu pencet enter 2x ###
   ```
 ![Screenshot 2024-11-21 072328](https://github.com/user-attachments/assets/e3b171e1-6490-4ec9-8741-95c37a8bd3d4)
   #### b. Copy SSH Key yang Telah Dibuat dengan Command Line Berikut
   ```
   cat ~/.ssh/id_ed25519.pub
   ```
![Screenshot 2024-11-21 072335](https://github.com/user-attachments/assets/fc4c73b1-de8f-40ad-ac3a-9e5cfe5a5dd3)
   #### c. Menambahkan SSH Key yang Telah Dibuat ke Github
   ```
Masuk ke laman berikut:
https://github.com/settings/ssh/new
Copy paste SSH Key yang telah dibuat
Lalu klik Add SSH Key
```
![Screenshot 2024-11-21 124249](https://github.com/user-attachments/assets/8134eea0-49b7-46be-bd75-cde581dd7183)

#### d. Pastikan SSH Key dapat digunakan dengan menggunakan command line berikut
```
ssh -T git@github.com
```
![Screenshot 2024-11-21 072554](https://github.com/user-attachments/assets/26330a4e-3105-4123-afe5-b2bdb783d0a6)

## Create Repository
### 1. Buat Repository Baru 
```
https://github.com/new
Masukkan nama dan tipenya (Public atau Private)
```
![Screenshot 2024-11-21 124519](https://github.com/user-attachments/assets/cc1c3ff0-6ca8-4ac3-a0af-2e6b523e4151)

### 2. Buka Repository yang Telah Dibuat

### 3. Salin link SSH
```
Klik Code, lalu klik bagian SSH kemudian pencet tombol berbentuk 2 persegi untuk langsung meng-copy
```
![Screenshot 2024-11-21 124607](https://github.com/user-attachments/assets/a7afee25-f747-41a3-ba14-197555c403ee)

### 4. Untuk Menghubungkan File Lokal dengan Repositori yang Telah Dibuat Digunakan Cara Berikut

#### a. Buka Terminal pada File Local yang Diinginkan lalu gunakan Command Berikut 
```
git clone (Link ssh yang telah di copy tadi)
```
![Screenshot 2024-11-21 124642](https://github.com/user-attachments/assets/f609b2d4-345b-4a6a-bcdd-b1ce5d186073)

#### b. Jika Langkah Sebelumnya Berhasil akan Muncul Folder Baru 
#### c. Buka Folder Tersebut lalu Buka Terminal atau Gunakan Command Line Berikut.
```
cd (Lokasi Folder Baru )
```
#### d. Masukkan command line berikut pada Git Bash
```
git branch -m main
```
![Screenshot 2024-11-21 124740](https://github.com/user-attachments/assets/37c9a1ad-5a0b-4641-89c0-c38bb6b44172)

## Push File from Local to Github
### 1. Pada Folder Baru Tadi Dapat Diisi File Apa saja
### 2. Pada Terminal di Folder Baru Tadi Masukkan Command Line Berikut
```
git add . 
git commit -m "(Deskripsi perubahan)"
git push origin (branch yang ingin dituju)
```
![Screenshot 2024-11-21 130114](https://github.com/user-attachments/assets/5d6b800d-e133-4b63-9067-24b1df69f8ed)

### 3. Jika Langkah Di Atas Berhasil akan Muncul File Baru Pada Branch yang Dituju
![image](https://github.com/user-attachments/assets/5ec1d0cc-b1e2-4191-b79d-aea2bd2d4ead)

## Create New Branch in Github 
### 1. Branch adalah versi lainnya dari suatu folder di Github, memungkinkan pekerjaan terpisah tanpa mengganggu branch utama (main)
### 2. Buka folder yang diinginkan yang telah terhubung dengan github
### 3. Buat branch dengan menggunakan command berikut
```
git checkout -b (Nama branch yang ingin dibuat)
```
![image](https://github.com/user-attachments/assets/87e1465d-66cb-4fe9-b13c-5e6f3f4e58b5)
### 4. Untuk memastikan kita telah pindah ke branch yang baru digunakan command line berikut
```
git checkout (Nama branch yang baru dibuat)
```
![image](https://github.com/user-attachments/assets/5e6c4b95-a854-44d6-9be8-e989b9988ce4)
### 5. Upload branch yang baru dibuat ke Github
```
git push origin (Nama brannch yang baru dibuat)
```
![image](https://github.com/user-attachments/assets/99b5580f-59b0-4240-b0cb-9fe38a8914b3)
### 6. Apabila langkah berhasil akan muncul branch baru pada repository
![Screenshot 2024-11-21 125133](https://github.com/user-attachments/assets/3b74115a-ce25-4fb9-9635-610228654e88)
## Delete Branch in Github
### 1. Pada folder tadi buka terminal
### 2. Pindah ke branch lain (Selain yang akan dihapus)
```
git checkout (nama branch lain)
```
### 3. Untuk menghapus branch yang diinginkan gunakan command berikut 
```
git branch -d (nama branch yang ingin dihapus)
```
### 4. Untuk menghapus branch di Github gunakan command berikut
```
git push origin --delete (nama branch pada Github yang sama dengan lokal yang ingin dihapus)
```

![Screenshot 2024-11-21 125433](https://github.com/user-attachments/assets/cedd0c0b-4f8c-4a2e-8425-59a68bc320ed)

### 5. Apabila berhasil pada repository branch tadi akan hilang

![Screenshot 2024-11-21 125451](https://github.com/user-attachments/assets/dbfb865c-321d-4777-9d2c-5439a7a579f4)

## Merging Branch in Github
### 1. Pada terminal pindah ke branch yang ingin digabungkan dengan command berikut
```
git checkout (nama branch tujuan yang ingin digabungkan)
```
### 2. Untuk memastikan branch up to date gunakan command line berikut
```
git pull origin (nama branch tujuan yang ingin digabungkan)
```
### 3. Gabungkan branch dengan menggunakan command berikut
```
git merge (nama branch yang ingin digabungkan dengan branch tujuan)
```

![Screenshot 2024-11-21 154452](https://github.com/user-attachments/assets/232adbfd-8e93-43b2-b94e-f60ca6c82caa)

### 4. Upload merge yang telah dilakukan ke github
```
git push origin (nama branch tujuan)
```
![image](https://github.com/user-attachments/assets/c8b1332c-38e6-419e-8946-ca398e123133)

### 5. Cek perubahan pada repositori

![image](https://github.com/user-attachments/assets/68831641-0696-476f-af50-b60271d49fb0)

## Other Procedure
