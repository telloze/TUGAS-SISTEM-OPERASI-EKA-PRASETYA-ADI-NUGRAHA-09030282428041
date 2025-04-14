# TUGAS-SISTEM-OPERASI-EKA-PRASETYA-ADI-NUGRAHA-09030282428041

---

## 📝 1. Login sebagai studentOS dan lihat status proses, perhatikan kolom keluaran ps –au sebagai berikut :
  
## A. Sebutkan nama-nama proses yang bukan root
![image](https://github.com/user-attachments/assets/13d9450f-30b7-400f-83f3-788c808861f1)
  
Yang bukan root :  
* */usr/bin/zsh*  
* *ps -au*  

## B. Tulis PID dan COMMAND dari proses yang paling banyak menggunakan CPU time 

**COMMAND** : /usr/lib/xorg/Xorg  
**PID** : 625  

## C. Sebutkan buyut proses dan PID dari proses tersebut.  


![image](https://github.com/user-attachments/assets/dd4fb306-9bf2-47f4-b555-bbd243f614a8)

![image](https://github.com/user-attachments/assets/16121bfd-6afd-49a6-a330-a62985101a07)  
**Buyut Proses** : systemd (1)  

## D. Sebutkan beberapa proses daemon.  

![image](https://github.com/user-attachments/assets/f7b2f8cd-8210-4034-b27d-fe81e274d3fb)  
**Proses daemon** 
* */usr/bin/dbus-daemon --system ...*  
* */usr/libexec/rtkit-daemon*  
* */usr/bin/gnome-keyring-daemon*  
* *usr/sbin/NetworkManager --no-daemon*  
* */usr/libexec/accounts-daemon*

## E. Pada prompt login lakukan hal-hal sebagai berikut :  
```bash
$ csh
```
```bash
$ who
```
```bash
$ bash
```
```bash
$ ls
```
```bash
$ sh
```
```bash
$ ps
```
![image](https://github.com/user-attachments/assets/9e924c52-85d2-46ce-a336-51d425cfb274)  

#

## 📝 2. Modifikasi program prog.sh sebagai berikut :  
```bash
$ vi prog.sh
#!/bin/sh
trap “echo Hello Goodbye ; exit 0 “ 1 2 3 15
echo “Program berjalan …”
while :
do
echo “X”
sleep 20
done
```
![image](https://github.com/user-attachments/assets/0f56ab90-2c64-4159-840b-5cfb3c2062c6)  
  
Jalankan program tersebut sebagai background. Coba lakukan kil dengan nomor sinyal 1, 2, 3
dan 15 pada nomor PID proses tersebut. Apakah proses berhenti atau tetap berjalan ? Nomor
sinyal berapa yang digunakan untuk menghentikan proses diatas ?  

![image](https://github.com/user-attachments/assets/89349f8c-7930-457c-a4e8-f4977e512eb9)  
**Program berhenti menggunakan sinyal 1**  

#

## 📝 3. Modifikasi program  

myjob.sh. Buatlah trap sedemikian rupa, sehingga bila proses tersebut dihentikan (kill), otomatis
file berkas akan terhapus. 
```bash
$ vi myjob.sh
#!/bin/sh
trap ______________________________
i=1
while :
do
 find / -print > berkas
 sort berkas –o hasil
 echo “Proses selesai pada „date‟” >> proses.log
sleep 60
done
$ kill –15 [Nomor PID]
$ ls -l
```

![image](https://github.com/user-attachments/assets/9123d638-27f4-4be4-b205-97fa2fdda04b)  

**Running Program**  
![image](https://github.com/user-attachments/assets/a04c6f19-ac70-428c-a034-d9a73f900d27)
![image](https://github.com/user-attachments/assets/1b998fa5-4ad8-4a6c-9f91-6e521bf42c8c)  

**Stop Program**  
![image](https://github.com/user-attachments/assets/564a43ba-b90a-4524-9d2c-3f5a71b78524)  

**Program terhapus otomatis**  
![image](https://github.com/user-attachments/assets/465afd7b-87b1-4c21-a9e3-a93f6c21f61f)

























    
  



