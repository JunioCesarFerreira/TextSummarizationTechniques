# TF-IDF

O TF-IDF (*Term Frequency-Inverse Document Frequency*), é uma estatística numérica utilizada para indicar a importância de uma palavra em um documento dentro de um corpus. Esse valor aumenta proporcionalmente ao número de vezes que uma palavra aparece no documento, mas é compensado pelo número de documentos no corpus que contêm a palavra.

### Componentes do TF-IDF

1. **Frequência do Termo (TF)**: Mede a frequência de uma palavra em um documento específico. Existem várias formas de calcular a TF. A mais simples é a contagem bruta de ocorrências de uma palavra em um documento. No entanto, uma abordagem mais comum é normalizar essa contagem pelo comprimento do documento para evitar a preferência por documentos mais longos. A fórmula básica para TF é:

$$
\text{TF}(t, d) = \frac{\text{número de vezes que o termo } t \text{ aparece no documento } d}{\text{número total de termos no documento } d}
$$

2. **Frequência Inversa do Documento (IDF)**: Calcula o logaritmo da divisão do número total de documentos pelo número de documentos que contêm o termo. Isso ajuda a reduzir o peso de termos que aparecem com muita frequência em todo o corpus e, portanto, são menos informativos. A fórmula para IDF é:

$$
\text{IDF}(t, D) = \log \left(\frac{N}{|\{d \in D : t \in d\}|}\right)
$$
   
onde $N$ é o número total de documentos no corpus $D$ e $|\{d \in D : t \in d\}|$ é o número de documentos que contêm o termo $t$.

### Cálculo do TF-IDF

A pontuação TF-IDF para um termo em um documento é simplesmente o produto de sua TF e IDF:

$$
\text{TF-IDF}(t, d, D) = \text{TF}(t, d) \times \text{IDF}(t, D)
$$