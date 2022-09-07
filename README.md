# DL X ray Image Classifier

Classificador de raio-X pulmonar feito usando a biblioteca TensorFlow.

---

# Datasets

 - [Covid-19](https://github.com/ieee8023/covid-chestxray-dataset): São 931 imagens de Raio-X (JPEG, JPG e PNG).

 - [Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia): São 5.863 imagens de Raio-X (JPEG) e 2 categorias 
 (Pneumonia/Normal). A base foi dividida em 3 pastas; 1 : 'Normal', 2: 'Pneumonia viral', 3: 'Pneumonia bacterial'.

# Modelo
Foi usado a arquitetura do ResNet50 (tranferência de aprendizagem), onde as primeiras camadas convolucionais são utilizadas para extrair características gerais 
das imagens (bordas, linhas) e as últimas camadas são utilizadas para classificação. Isso tudo juntamente com o TensorFlow para criar algumas camadas e OpenCV 
para o processamento das imagens.

## Tranferência de aprendizagem
É uma técnica na qual uma rede neural foi treinada para realizar uma determinada tarefa e é reusada como ponto de partida para uma tarefa similar. Muito útil 
porque reduz drasticamente o tempo de treinamento. No código foram re-treinadas apenas as 10 últimas camadas e criada uma camada densa com TF.
