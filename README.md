# AnthonyPytorch
Anthony Project Pytorch Python

Python with Pytorch
===================

Apa itu Pytorch??
PyTorch adalah sebuah framework open-source untuk deep learning yang dikembangkan oleh Facebook. PyTorch dirancang untuk memudahkan para peneliti dan praktisi machine learning dalam mengembangkan model neural networks secara fleksibel dan mudah dipahami. PyTorch memiliki arsitektur yang dinamis, sehingga memungkinkan pengguna untuk melakukan perubahan pada arsitektur model pada saat runtime. Selain itu, PyTorch juga menyediakan berbagai macam fungsi dan tool untuk mempermudah proses preprocessing, training, dan deployment model neural networks. PyTorch juga memiliki komunitas yang besar dan aktif, sehingga pengguna dapat dengan mudah menemukan berbagai tutorial dan referensi terkait penggunaan framework ini.

Install package python:       or      install package in requirementspytorch.txt  
===============
asttokens==2.2.1
backcall==0.2.0
colorama==0.4.6
comm==0.1.2
contourpy==1.0.7
cycler==0.11.0
debugpy==1.6.6
decorator==5.1.1
executing==1.2.0
fonttools==4.38.0
ipykernel==6.21.1
ipython==8.9.0
ipywidgets==8.0.4
jedi==0.18.2
joblib==1.2.0
jupyter_client==8.0.2
jupyter_core==5.2.0
jupyterlab-widgets==3.0.5
kiwisolver==1.4.4
matplotlib==3.6.3
matplotlib-inline==0.1.6
nest-asyncio==1.5.6
numpy==1.24.2
packaging==23.0
pandas==1.5.3
parso==0.8.3
patsy==0.5.3
pickleshare==0.7.5
Pillow==9.4.0
platformdirs==3.0.0
plotly==5.13.0
prompt-toolkit==3.0.36
psutil==5.9.4
pure-eval==0.2.2
Pygments==2.14.0
pyparsing==3.0.9
python-dateutil==2.8.2
pytz==2022.7.1
pywin32==305
pyzmq==25.0.0
scikit-learn==1.2.1
scipy==1.10.0
seaborn==0.12.2
six==1.16.0
stack-data==0.6.2
statsmodels==0.13.5
tenacity==8.2.0
threadpoolctl==3.1.0
torch==1.13.1
tornado==6.2
tqdm==4.64.1
traitlets==5.9.0
typing_extensions==4.4.0
wcwidth==0.2.6
widgetsnbextension==4.0.5
wincertstore==0.2

Catatan Penting :
=================
PyTorch membutuhkan data dalam bentuk tensor untuk dimasukkan ke dalam model, Pada proses Pytorch kita membutuhkan data dengan tipe float dan membentuk data ke tensor 1D.

import torch
# merubah data ke bentuk tensor lalu reshape ke bentuk view(-1)
train_tensor = torch.FloatTensor(train_scale).view(-1)
test_tensor = torch.FloatTensor(test_scale).view(-1)

Catatan Penting :
=================
Recurrent Neural Network (RNN) memanfaatkan informasi sequential dari data kita, kita perlu memecah bentuknya menjadi beberapa kelompok data, menggunakan fungsi berikut :

# Membuat fungsi untuk membuat data menjadi berurutan
def input_data(data, seq_size):
    out = []
    length = len(data)
    
    for i in range(length-seq_size):
        feature = data[i : i+seq_size]
        target = data[i+seq_size : i+seq_size+1]
        out.append((feature, target))
    
    return out
