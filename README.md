# Easy-to-Install-Torch-GPU-Local-for-YOLO
Cara mudah install Torch-GPU untuk YOLO semua versi

Requirement hardware: Only for GPU Nvidia

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

2. Lalu ketik 'import torch', dan 'torch.cuda.is_available()', seperti pada gambar berikut

   ![image](https://github.com/user-attachments/assets/c3946439-93c2-4a0f-a29c-17b8c2b9595a)

3. Jika hasilnya True, berarti torch-gpu telah siap digunakan. Selamat anda telah bisa mkentraning model YOLO menggunakan torch-gpu Nvidia.
4. Untuk keluar ketik saja 'exit()'

   ![image](https://github.com/user-attachments/assets/97f0c137-3fb4-4bb2-bff4-775962238855)


## Melakukan test inferensi menggunakan yolov5

1. Download repository yolov5 menggunakan 'git clone', ketik 'git clone https://github.com/ultralytics/yolov5.git', link yolov5: https://github.com/ultralytics/yolov5

   ![image](https://github.com/user-attachments/assets/f1ed9abf-b9cd-42f0-9a92-2401320e5633)

2. Jika git belum terinstall, silakan install dengan ketik 'conda install git'
3. Lalu masuk ke directory yolov5 dengan ketik, 'cd yolov5' sepeti pada gamnbar:

   ![image](https://github.com/user-attachments/assets/b0dda3fc-6ab6-4071-b9ba-bed105650fc1)

   Dan working directory akan berubah menjadi directory yolov5

4. Untuk melihat isi directory ketik 'dir'

   ![image](https://github.com/user-attachments/assets/7074a662-3815-4a32-b52e-765718ad0820)

5. Untuk menjalankan test inferensi, install requirements yang dibutuhkan, ketik 'pip install -r requirements.txt'

   ![image](https://github.com/user-attachments/assets/2a62777a-99ed-4335-ae3a-0db5861cd748)

6. Jika sudah terinstall semua, kita bisa melanjutkan untuk menjalankan inferensi, ketik 'python detect.py --imgsz 640 --weights yolov5m.pt --source 0'
  
   ![image](https://github.com/user-attachments/assets/09dfd327-1827-4731-a15a-151abb708a76)

   Source 0, port webcam internal laptop, jika menggunakan webcam external ganti dengan 1 atau 2

7. Dan hasilnya seperti berikut:

   ![image](https://github.com/user-attachments/assets/fdd5ceb3-3794-4283-a08b-e2b4faee6a48)

   Buka task manager dan arahkan ke GPU maka dapat dilihat bahwa GPU sedang bekerja untuk torch gpu dan persentasi processing dapat dilihat lebih besar, seperti pada gambar saya 71%.

8. Selamat model yolo anda telah berhasil berjalan pada GPU local!

## Menjalankan inferensi menggunakan yolov5 dengan model custom atau model yang dibuat sendiri

1. Siapkan model dan simpan pada directory yolov5/models, buat nama model atau nama default dari hasil training yaitu best.pt
2. Untuk menjalankan inferensi ketik 'python detect.py --imgsz 640 --weights models/best.pt --source 0
3. Semoga berhasil dan berjalan lancar.

## Jika ingin training custom menggunakan jupyter
1. Install jupyter anaconda dengan ketik 'conda install -c anaconda jupyter',

   ![image](https://github.com/user-attachments/assets/36817168-b851-4272-84d2-a82ea26ceec4)

2. Install ipykernel dengan ketik 'pip install --user ipykernel'

   ![image](https://github.com/user-attachments/assets/5fa0767c-8c97-4ebc-b033-fcf177691ff7)

3. Add environment ke ipykernel dengan ketik 'python -m ipykernel install --user --name='environment_name', misalnya 'python -m ipykernel install --user --name=torchgpu-env'

   ![image](https://github.com/user-attachments/assets/87676c20-3ae0-45b0-a1c1-0c3e4359a69c)

   Jika ada pesan, 

   ![image](https://github.com/user-attachments/assets/9d6e65d4-4989-424a-992e-4043d8451256)

   Maka proses add env berhasil

4. Buka jupyter dengan ketik 'jupyter lab'

   ![image](https://github.com/user-attachments/assets/802591df-8192-4146-aeca-cb0aa7f2a2c6)

   Jika berhasil, hasilnya seperti berikut:

   ![image](https://github.com/user-attachments/assets/b6adc1eb-15fa-401c-b139-46ddf2dc781b)

5. Pilih environemnet yang terinstall GPU, pada Notebook, pilih torchgpu-env karena tadi torch gpu terinstall pada env ini,

   ![image](https://github.com/user-attachments/assets/513fd76a-627e-45a8-8baf-9f097eb2f21f)

6. Jika sudah masuk ke notebook editor, lihat pada gambar berikut:

   ![image](https://github.com/user-attachments/assets/47addde2-0df1-468d-933a-4a0a2ab96fc7)

   torchgpu-env menandakan bahwa kita sedang bekerja pada kernel gpu yang kita install sebelumnya.

7. Dapat kita testing agar yakin, ketik seperti pada gambar:

   ![image](https://github.com/user-attachments/assets/6e30328f-f2e8-4229-8809-dee597e00e7b)

   Jika True, selamat anda bisa menlanjutkan training model anda.
   
8. Selamat anda telah bisa menggunakan jupyter host local untuk training custom model yolo anda, sama seperti anda menggunakan google colab.
