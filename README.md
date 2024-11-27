# Easy-to-Install-Torch-GPU-for-YOLO
Cara mudah install Torch-GPU untuk YOLO semua versi

## A. Langkah pertama: Install Torch Cuda

1. Download dan install Anaconda x64 for windows, link https://www.anaconda.com/download
2. Buka Anaconda Prompt
   
   ![image](https://github.com/user-attachments/assets/35b0c59a-775a-41bd-aa4c-26bbcf16cdff)
   
3. Buat environment, ketik 'conda create env -n nama-env python=3.10' lalu enter, nama-env bisa diganti sesuai kebutuhan, misalnya torch-gpu
   
![image](https://github.com/user-attachments/assets/0cc60d5b-abf1-45d5-bdb1-cb1185d7c9d1)

4. Jika muncul seperti gambar berikut, ketik 'y' lalu enter

   ![image](https://github.com/user-attachments/assets/ab2d0500-74ea-40cb-ae3c-10db66a84d23)

5. Tunggu hingga proses seelsai sampai muncul seperti berikut,

   ![image](https://github.com/user-attachments/assets/dd8075df-f332-43ce-b618-0b6d18c10ec0)

6. Buka env yang sudah dibuat tadi, ketik 'conda activate nama-env', lalu enter

   ![image](https://github.com/user-attachments/assets/2578b8ec-dd8f-4c7a-823b-47ea7cb8c33a)

7. Jika sudah aktif jadi seperti berikut,

   ![image](https://github.com/user-attachments/assets/df5a5a27-df78-45a6-a08c-c2c070d5b692)

8. Lalu install torch, cuda, dll, ketik 'conda install pytorch torchvision torchaudio pytorch-cuda=12.4 -c pytorch -c nvidia', pun kalo mau versi lain bisa buka link https://pytorch.org/

   ![image](https://github.com/user-attachments/assets/ec79c39b-71e5-46d5-a33a-f735c33d8778)

9. Kalo sudah selesai, tampilan menjadi seperti berikut

   ![image](https://github.com/user-attachments/assets/4dea6259-99ba-4c11-ac0c-77b4d79b10c4)

## B. Langkah kedua: Test Cuda GPU yang terinstall

1. Ketik 'python' seperti pada gambar

   ![image](https://github.com/user-attachments/assets/08a484b9-58ec-4c09-bb74-94d98ff480e0)

