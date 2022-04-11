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

Rode primeiro a sumarização

```python
import numpy as np
import textwrap
import nltk
from nltk.corpus import stopwords
from sklearn.feature_extraction.text import TfidfVectorizer
```

```python
noticia = ["A economia da China cresceu apenas 4% no último trimestre de 2021, seu ritmo mais lento em um ano e meio, momento em que enquanto o país enfrentava uma crise imobiliária cada vez mais profunda, novos surtos de Covid-19 e a estrita abordagem de não-tolerância de Pequim para controlar o vírus. Ainda assim, esse número foi maior do que o esperado pelos economistas. Para todo o ano de 2021, o PIB cresceu 8,1%, praticamente em linha com as expectativas dos analistas. O governo chinês estabeleceu uma meta na primavera passada para que sua economia expandisse pelo menos 6% no ano."]
noticia = vectorizer.transform(noticia)
resultado = model.predict(noticia)
print("resultado: ", resultado)
```

A saída do resultado:

```python
resultado: ['negócio']
```

Na sequência o contador de vetores

- Token =>
- CountVectorizer() => **Converte uma coleção de documentos de texto em uma matriz de contagens de token.**

```python
df = pd.read_csv('textos_bbc_cls.csv')
df.head()
```

Resultado
| id | text | labels |
|--- |--- |--- |
| 0 | Vendas de anúncios aumentam lucro da Time Warn... | negócio |
| 1 | Dólar ganha com discurso de Greenspan\n\nO dól... | negócio |
| 2 | Comprador de unidade da Yukos enfrenta pedido ... | negócio |
| 3 | Preços elevados dos combustíveis atingem os lu... | negócio |
| 4 | Negociação de aquisição da Pernod eleva Domecq... | negócio |
