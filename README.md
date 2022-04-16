# PUCMinas

Trabalho de conclusão de curso da pós graduação na PucMinas em IA e AM.
O objetivo do projeto é após a sumarização do texto, classificar o texto original e o sumarizado em:
'negócio', 'entretenimento', 'política', 'esporte' e 'tecnologia'.
Em seguida compará-los para ver se seguem o mesmo padrão de classificação.

# Criar o ambiente virtual

Sequência de linhas de comando no prompt do terminal:

```linux
$ python3.10 -m venv env --upgrade-deps
$ source env/bin/activate
$ pip install wheel
$ pip install ipython ipykernel
$ pip install pandas
$ pip install nltk
$ pip install sklearn
$ python -V
```

# Utilizar o projeto

### Rode primeiro a sumarização

Esse processo vai gerar os textos sumarizados do temas escolhidos. Ver exemplo do temas:

```python
files = [
    'texto_entretenimento_original.txt',
    'texto_esporte_original.txt',
    'texto_negocio_original.txt',
    'texto_politica_original.txt',
    'texto_tecnologia_original.txt'
]
```

### Na sequência, rode o processo vetorização de contagem do textos

Esse processo classificará os textos originais e sumarizados nessas categorias: entretenimento, esporte, negócio, política e tecnologia.
