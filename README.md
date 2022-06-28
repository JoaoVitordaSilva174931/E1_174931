# Processamento, compressão e transmissão de informações utilizando imagens de satélite
# Processing, compression and transmission of information using satellite images
## Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação EA979A - Introdução a Computação Gráfica e Processamento de Imagens, oferecida no primeiro semestre de 2022, na Unicamp, sob supervisão da Profa. Dra. Paula Dornhofer Paro Costa, do Departamento de Engenharia de Computação e Automação (DCA) da Faculdade de Engenharia Elétrica e de Computação (FEEC).

|         Nome          |  RA    |    Curso      |
|         :---:         |  :---: |    :---:      |
| João Vitor da Silva   | 174931 | Física Médica |

## Descrição do projeto

A análise de imagens contituí um importante meio de transmitir informações sobre o mundo e propriedades interessantes também podem ser extraídas a partir desse estudo. Atualmente, bancos de dados com imagens da superfície terrestre são encontradas com facilidade e abundância, assim como imagens que representam fenômenos meteorológicos, que servirão de base para a análise da seguinte questão: Quais as implicações do limite de compressão de imagens de satélite sem perda de informações significativas para o estudo em questão.

O processamento de tais imagens, na grande maioria das vezes, requer uma máquina com memória em grande escala e um processamento tão rápido quanto. A alternativa de comprimir as imagens de satélite sem perdas de informações úteis é uma forma de abranger o alcance desse tópico para computadores mais acessíveis e de menor potência, acarretando na melhora da troca de informações em uma ciência recente que ainda permitirá novas descobertas nas mais diversas formas.  

# Abordagem Adotada

Foram utilizadas imagens de satélite que apresentam a intensidade de chuvas na região de Campinas. O processamento foi baseado em, após a conversão das imagens de .tif para png, organizar as imagens convertidas em uma pasta no ambiente Google Colab e então executar o comando "resize" em uma amostra de imagens que retornavam diferenças visuais em comparação a imagem original. Em outras palavras, foi utilizado um critério visual (no sentido de em quais regiões a área afetada pela chuva não é mais visível na imagem comprimida) para concluir de que maneira a compressão afeta o nosso julgamento

> - Testes realizados para a normalização da imagem tiff (a concluir)


# Resultados Finais

Foi obtido um conjunto de imagens redimensionadas (de 480x480 pixels para 100x100 pixels) que retratam a diferença na questão de intensidade de chuvas antes e após a compressão. A escolha da mudança para 100x100 pixels foi feita baseando-se em um valor comum que representa o limite para a alteração no tamanho da imagem que, a partir dele, isto é, menor do que ele, informações crucias são perdidas em definitivo. Segue um exemplo aplicado a uma das imagens antes e após a compressão, respectivamente:

![image](https://user-images.githubusercontent.com/103368895/176271920-633a526d-6c67-479b-8283-6a712fa389e3.png)
![image](https://user-images.githubusercontent.com/103368895/176272049-67951e69-502e-459b-8260-5911325f5f82.png)

# Discussão

Em algumas partes da imagem comprimida, há a perda parcial do pixel que representava a intensidade (em branco) na imagem original, porém, ainda conseguimos chegar à conclusão de que a àrea atingida pela chuva possui um contraste visível em comparação ao fundo preto da imagem.
As principais dificuldades encontradas durante a realização do projeto foram: Converter a imagem tiff para png com o python; normalizar a imagem tiff; definir um parâmetro para a redução máxima de tamanho sem perda significativa na informação transmitida.  


# Referências Bibliográficas

https://youtu.be/uy5ZpPJLBFA

https://acervolima.com/como-comprimir-imagens-usando-python-e-pil/



 
