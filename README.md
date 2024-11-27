# Easy-to-Install-Torch-GPU-for-YOLO
Cara mudah install Torch-GPU untuk YOLO semua versi

Langkah pertama: Install Torch Cuda
1. Download dan install Anaconda x64 for windows, link https://www.anaconda.com/download
2. Buka Anaconda Prompt
   
   ![image](https://github.com/user-attachments/assets/35b0c59a-775a-41bd-aa4c-26bbcf16cdff)
   
3. Buat environment, ketik 'conda create env -n nama-env python=3.10' lalu enter, nama-env bisa diganti sesuai kebutuhan, misalnya torch-gpu
   
![image](https://github.com/user-attachments/assets/0cc60d5b-abf1-45d5-bdb1-cb1185d7c9d1)

4. Jika muncul seperti gambar berikut, ketik 'y' lalu enter

   ![image](https://github.com/user-attachments/assets/ab2d0500-74ea-40cb-ae3c-10db66a84d23)

4. Buka env yang sudah dibuat tadi, ketik 'conda activate nama-env'
5. Install dulu torch, cuda, dll, ketik 'conda install pytorch torchvision torchaudio pytorch-cuda=12.4 -c pytorch -c nvidia', pun kalo mau versi lain bisa buka link https://pytorch.org/
6. Kalo sudah selesai, test cuda gpu dengan ketik python
