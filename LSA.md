# LSA

A Análise Semântica Latente (LSA, do inglês "Latent Semantic Analysis") é uma técnica de PLN e recuperação de informação que ajuda a identificar padrões e relações semânticas entre palavras e textos em grandes conjuntos de dados. A LSA a decomposição de valor singular (SVD, do inglês "Singular Value Decomposition"), para reduzir a dimensionalidade de matrizes de termos por documentos e capturar as relações semânticas latentes entre eles.

### Como Funciona a LSA

1. **Construção da Matriz Termo-Documento**: O primeiro passo na LSA é a construção de uma matriz que representa os termos (palavras) nas linhas e os documentos nas colunas. Cada entrada nesta matriz contém o peso de um termo em um documento, que pode ser calculado usando TF-IDF ou outra medida de frequência de termo.

2. **Decomposição de Valor Singular (SVD)**: A matriz Termo-Documento é então decomposta em três matrizes menores: $U$, $S$, e $V^\top$, onde $U$ representa os termos nos conceitos latentes, $S$ é uma matriz diagonal contendo os valores singulares (que indicam a importância de cada conceito latente), e $V^\top$ representa os documentos nos conceitos latentes.

$$
\text{Matriz Termo-Documento} = U \cdot S \cdot V^\top
$$

O SVD reduz a dimensionalidade dos dados mantendo apenas os $k$ maiores valores singulares e seus correspondentes vetores singulares em $U$ e $V$. Esse valor $k$ é um hiperparâmetro que determina o número de conceitos latentes a serem mantidos.

3. **Interpretação dos Conceitos Latentes**: As colunas de $U$ e as linhas de $V^\top$ agora representam os termos e documentos, respectivamente, em um espaço de conceitos latentes. Esses conceitos podem não corresponder diretamente a categorias claras ou tópicos específicos, mas eles capturam associações semânticas entre palavras que coocorrem em contextos similares.