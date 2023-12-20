# Rossmann Store Sales
Este repositório contém arquivos e scripts python

## Instalação
Ao baixar o projeto com o _git clone_

-  Python 3.11
-  O comando "**python -m venv .venv**" é usado para criar um ambiente virtual
-  Depois de criar o ambiente virtual com o comando acima, você geralmente precisa ativá-lo "**.venv/Script/activate**"
-  Instalar as dependências listadas no arquivo requirements.txt: "**pip install -r requirements.txt**"

## Fonte
Dados importado da base do kaggle: <a href="https://www.kaggle.com/c/rossmann-store-sales" target="_blank">Rossmann Store Sales</a>

A competição "Rossmann Store Sales" envolveu a previsão das vendas de uma cadeia de lojas da Rossmann, que é uma rede de farmácias e lojas de produtos para a saúde. Os participantes foram desafiados a criar modelos preditivos que pudessem prever as vendas diárias das lojas com base em vários recursos, como promoções, feriados, sazonalidade e informações sobre as lojas.

## Arquivos

O projeto final contém somente 2 arquivo python
  -  ./handler.py
      -  O arquivo principal que tem a rota chamada "/rossmann/predict" usando o metodo POST
      -  Para não ficar pesado, importamos o **pickle** e gravamos o algoritmo de aprendizado de máquina e os scaler em pkl
      -  O **pickle** nos ajuda com a minimizar o tempo. Por exemplo, usamos o XGBoost como aprendizado de máquina, e não vamos precisar de treinar os modelos tudo novamente, pois já tempos um treinado e gravado em um pkl. Então agora é somente chamar esse arquivo pkl, e passar os valores para ele prever. 
  -  ./rossmann/Rossmann.py
      -  É uma classe com varias funções
      -  Limpar os dados
      -  As feature engineering (geração de novas variáveis com base nas existentes)
      -  Preparar os dados para o modelo receber "bonitinho"
      -  E até que enfim, obter previsão

## Sobre o projeto

O que usamos:
  -  pickle
  -  XGBoost
  -  scikit-learn =>
  -  inflection
  -  Flask, request, Response
  -  os => os.environ.get( 'PORT', '5000' )
  -  datetime
  -  pandas
  -  numpy
  -  math

O projeto final foi criado para subir para um servidor. E testar, porém não tivemos sucesso, pois não achamos servidores free.
Então, por enquando não podemos fazer o teste desse algoritmo em tempo real. Fico devendo!

Fizemos o deploy do projeto no Streamlit, você pode acompanhar: <a href="https://fernandobatistads-challenge-main-page-8lreld.streamlit.app" target="_blank">Por aqui</a>



