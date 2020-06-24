# *Brain MRI Images for Brain Tumor Detection*
## Contextualização
- O tumor cerebral é definido como um crescimento anormal de células no cérebro. É uma doença extretamente mortal e infelizmente, comum. A sua taxa de mortalidade ronda os 90% e, em países como Reino Unido, são detetados em média 11 casos diários. Estes, são alguns dos motivos que nos levaram a escolher este tema e descobrir mais sobre o mesmo.

![Brain Tumor](/images/contextualizacao.jpg)

## Objetivos

- Existiam diversos objetivos possíveis para este trabalho e, decidimos, focar-nos essencialmente nos seguintes três:
    - Dada uma imagem de um ressonância magnética, classificar se a mesma contém um tumor cerebral.
    - Construir um modelo versátil, que seja facilmente implementado num contexto real.
    - Classificar as ressonância com precisões elevadas.

## Abordagem

### Passo 1 - Data Treatment (Split):

- Inicialmente, realizamos uma divisão dos dados por pastas correspondentes a treino (75%) e teste (25%) com as respetivas classes (*yes*, *no*).
    > [1-Data_Treatment.ipynb](https://github.com/diogogsilva/tp_aa2_pg41070_pg41067/blob/master/1-Data_Treatment.ipynb)
    
![Data in Folders](/images/data-split.png)

### Passo 2 - Exploratory Data Analysis (EDA):
- Com a divisão dos dados completa, seguiu-se a exploração e análise dos dados, onde verificamos alguns exemplos das imagens do nosso *dataset* e a sua respetiva classe. Feito isso, consideramos também importante observar se o nosso *dataset* era balanceado.
    > [2-EDA.ipynb](https://github.com/diogogsilva/tp_aa2_pg41070_pg41067/blob/master/2-EDA.ipynb)
    
![Data Distribution](/images/eda.PNG)

### Passo 3 - Implementação de três possíveis abordagens para o problema
- Após termos os dados divididos e explorados, decidimos implementar três modelos que consideramos que podiam resolver o nosso problema. Para isso, começamos com três modelos "básicos" de forma a conferirmos dos três, qual o que à partida, têm melhores resultados. Os modelos considerados foram uma rede neuronal, uma rede convolucional e, por fim, uma máquina de vetores de suporte.

- #### Simple Neural Network:
    - Implementação de uma Rede Neuronal simples
        > [3-Simple_NN.ipynb](https://github.com/diogogsilva/tp_aa2_pg41070_pg41067/blob/master/3-Simple_NN.ipynb)
       
![Result NN](/images/nn_result.PNG)

- #### Simple CNN:
    - Implementação de uma Rede Neuronal Convolucional simples
        > [4-Simple_CNN.ipynb](https://github.com/diogogsilva/tp_aa2_pg41070_pg41067/blob/master/4-Simple_CNN.ipynb)
        
![Result CNN](/images/cnn_result.PNG)

- #### Simple SVM:
    - Implementação de uma Máquina de Vetores de Suporte simples
        > [5-Simple_SVM.ipynb](https://github.com/diogogsilva/tp_aa2_pg41070_pg41067/blob/master/5-Simple_SVM.ipynb)
   
- Conseguimos observar que os valores de *accuracy* nos dados de validação da rede neuronal convolucional são os mais elevados, rondando maioritariamente valores superiores a 80%. A *SVM* também obteve resultados bastante positivos com três dos *kernels*. Por fim, a rede neuronal, foi a que obteve piores resultados, porém, não significativamente.
        
![Result SVM](/images/svm_result.PNG)

### Passo 4 - Otimização do modelo
- Concluída a implementação dos três modelos e respetivas avaliações, confirmamos que, tal como esperado, o modelo de redes neuronais convolucionais foi o que nos garantiu melhores resultados. Assim sendo, para este mesmo modelo, decidimos realizar uma otimização dos seus parâmetros e verificar as melhorias.

### Passo 5 - Modelo Final
- Com os resultados obtidos na otimização, conseguimos então construir o nosso modelo final que, para além de ser mais versátil, garante-nos resultados mais precisos.

### Passo 6 - *Feature Maps*
- Após otimizado o modelo, para facilitar a compreensão das *features* que o modelo final está a selecionar, implementamos uma visualização dos *feature maps* das várias camadas da nossa arquitetura.

- ...
        
### Referências

- #### *Dataset*
    - *Brain MRI Images for Brain Tumor Detection*
        >[Brain MRI for Brain Tumor Detection](https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection)

## Realizado por:
- Diogo Silva **PG41070**
    > [GitHub](https://github.com/diogogsilva)
- Daniel Faria **PG41067**
    > [GitHub](https://github.com/DanielCoutinhoFaria)