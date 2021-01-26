## Detecção e Classificação de Doenças no Papaya Usando Deep Learning
Nos últimos anos as abordagens baseadas em aprendizado de máquina, mais especificamente Redes Neurais Convolucionais (CNN) e Redes Neurais Profundas (DNN), ganharam destaque para solução de problemas de visão computacional nas mais diversas áreas. Porém, este tipo de abordagem requer uma grande quantidade de imagens do problema a ser tratado para um treinamento adequado da rede neural, o que muitas vezes dificulta este tipo de abordagem. Nas aplicações de visão artificial voltadas a fruticultura este problema é mais notório,sendo que uma das principais azões da pouca evolução nesta área é a carência de grandes conjuntos de dados devidamente anotados. O presente trabalho visa contribuir para alavancar a pesquisa neste domínio, tendo como principal contribuição a criação um novo conjunto de imagens, de dimensões inéditas na literatura, com amostras das principais doenças e defeitos mecânicos do Papaya (Carica Papaya).  Dado a sua dimensão, nosso conjunto de dados deve elevar o estado da arte em trabalhos de pesquisa na área de detecção e classificação de doenças e defeitos no Papaya e coloca-se como um benchmark de referência para aferição e comparação dos resultados destes trabalhos. Nosso conjunto de dados é composto por mais de 20.000 imagens de frutos com amostras das principais doenças e defeitos mecânicos relacionados do Papaya. As imagens possuem anotações da posição do fruto e da posição da doença/defeito encontrado no mesmo.

Como segunda contribuição usamos nosso conjunto de dados para treinar uma rede neural profunda para identificar e classificar doenças e outros defeitos em uma imagem de Papaya. Nossa rede alcançou uma acuracidade de xx.xx % , o que a torna apta a ser utilizada em sistemas reais mais complexos, como sistemas embarcados de controle de qualidade ou sistemas robóticos de colheita.

### Pré-Requisitos
- Ubuntu 18
- Cuda 10.1
- Cudnn 8.0
- OpenCV 4.5

## DataSet
### DataSet B128 
- Localização : Pasta dados do projeto
- Descrição   : Base para testes de sanidade da rede. Composta por 128 imagens com a seguinte distribuições de classes:
  * FRUTO_SEM_DOENÇA 	  44
  * Antracnose		        12  
  * Phytoftora		        12	
  * Dano_Mecânico		     12
  * Mancha_Chocolate	   12	
  * Meleira			          12
  * Mancha_Fisiologica  12
  * Pinta_Preta		       12

### DataSet B1024
- Localização : Pasta dados do projeto
- Descrição   : Base para testes de sanidade da rede. Composta por 1024 imagens com a seguinte distribuições de classes:
  * FRUTO_SEM_DOENÇA 	  324
  * Antracnose		        100
  * Phytoftora		        100	 
  * Dano_Mecânico		     100
  * Mancha_Chocolate	   100	
  * Meleira			          100
  * Mancha_Fisiologica  100
  * Pinta_Preta		       100
  
  ### DataSet Bcompleta
- Localização : [Base de dados Sisfrutos-Papaya](https://drive.google.com/drive/folders/10fuLRYK2NFqAo6TMYYjl8ulD7OdlVvZ5)
- Descrição   : Base completa composta por 18750 imagens com a seguinte distribuições de classes:
  * FRUTO_SEM_DOENÇA 	  
  * Antracnose		        
  * Phytoftora		        
  * Dano_Mecânico		     
  * Mancha_Chocolate	   
  * Meleira			          
  * Mancha_Fisiologica 
  * Pinta_Preta		       


## Treinar / Testar Rede
- Hardware utilizado: Gpu Nvidia 1060 com 6gb de memória
- Tempo Treinamento :  
*Base 128
*Base 1024: ~ 54 horas
*Base completa: 
- Para treinar: 
* ./darknet detector train data/obj.data cfg/yolov4.cfg yolov4.conv.137 -map
- Para testar : 
* ./darknet detector test data/obj.data cfg/yolov4.cfg yolov4.conv.137 

## Resultados
- [Gráfico mAP Base 128](results/chartb128.png)
- [Gráfico mAP Base 1024](results/chart.png)
- [Gráfico mAP Base Completa](results/chartCompleta.png)
