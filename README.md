# Processamento, compressão e transmissão de informações utilizando imagens de satélite
# Processing, compression and transmission of information using satellite images
## Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação EA979A - Introdução a Computação Gráfica e Processamento de Imagens, oferecida no primeiro semestre de 2022, na Unicamp, sob supervisão da Profa. Dra. Paula Dornhofer Paro Costa, do Departamento de Engenharia de Computação e Automação (DCA) da Faculdade de Engenharia Elétrica e de Computação (FEEC).

|         Nome          |  RA    |    Curso      |
|         :---:         |  :---: |    :---:      |
| João Vitor da Silva   | 174931 | Física Médica |

# Descrição do projeto

A análise de imagens contituí um importante meio de transmitir informações sobre o mundo e propriedades interessantes também podem ser extraídas a partir desse estudo. Atualmente, bancos de dados com imagens da superfície terrestre são encontradas com facilidade e abundância, assim como imagens que representam fenômenos meteorológicos, que servirão de base para a análise da seguinte questão: Quais as implicações do limite de compressão de imagens de satélite sem perda de informações significativas para o estudo em questão.

O processamento de tais imagens, na grande maioria das vezes, requer uma máquina com memória em grande escala e um processamento tão rápido quanto. A alternativa de comprimir as imagens de satélite sem perdas de informações úteis é uma forma de abranger o alcance desse tópico para computadores mais acessíveis e de menor potência, acarretando na melhora da troca de informações em uma ciência recente que ainda permitirá novas descobertas nas mais diversas formas.  

# Abordagem Adotada

Foram utilizadas imagens de satélite que apresentam a intensidade de chuvas na região de Campinas. O processamento foi baseado em, após a conversão das imagens de .tif para png, organizar as imagens convertidas em uma pasta no ambiente Google Colab e então executar o comando "resize" em uma amostra de imagens que retornavam diferenças visuais em comparação a imagem original. Definindo uma função para aplicar threshold na imagem original e na imagem reduzida, podemos estabelecer que a imagem reduzida apresenta, em regiões de maior intensidade de chuvas, as mesmas configurações que a imagem original, isto é, não perdemos informações no que diz respeito às grandes tempestades por exemplo. Na seção de resultados finais será exposto um caso em que há pouca precipitação como um todo, porém com regiões concentradas que fornecem conclusões acerca da quantidade de chuva naquela porção da imagem [3].


# Resultados Finais

Foi obtido um conjunto de imagens redimensionadas (de 480x480 pixels para 100x100 pixels) que retratam a diferença na questão de intensidade de chuvas antes e após a compressão. A escolha da mudança para 100x100 pixels foi feita baseando-se em um valor comum que representa o limite para a alteração no tamanho da imagem que, a partir dele, isto é, menor do que ele, informações crucias são perdidas em definitivo de acordo com o threshold definido. Segue um exemplo aplicado a uma das imagens antes e após a compressão, respectivamente:

![image](https://user-images.githubusercontent.com/103368895/177041254-a1f58460-3453-4ae7-b0fb-e1145547acf8.png)
![image](https://user-images.githubusercontent.com/103368895/177041263-5d3cc217-8936-4748-9b06-2845e759ea74.png)

Aplicando o threshold na imagem, temos os seguintes resultados:

Imagem original

![image](https://user-images.githubusercontent.com/103368895/177041307-29248926-723f-4a53-8aba-2b0470a7c714.png)

Imagem reduzida

![image](https://user-images.githubusercontent.com/103368895/177041330-c8188443-0a5f-48ee-928e-c1e5bb7bf4ef.png)


# Discussão

Em algumas partes da imagem comprimida, há a perda parcial do pixel que representava a intensidade (em branco) na imagem original, porém, ainda conseguimos chegar à conclusão de que a área atingida pela chuva possui um contraste visível em comparação ao fundo preto da imagem. Tal conclusão é reforçada após a aplicação do threshold na imagem, sendo que, com threshold na imagem reduzida, ainda conseguimos ter visualização total da região com intensidade de chuvas elevada quando a distribuição de tempestades se encontra dispersa, exemplificado no caso descrito. 
As principais dificuldades encontradas durante a realização do projeto foram: Converter a imagem tiff para png com o python; normalizar a imagem tiff; definir um parâmetro para a redução máxima de tamanho sem perda significativa na informação transmitida.  


# Referências Bibliográficas

[1] Processamento digital de imagens com python. YouTube, 26/11/2020. Disponível em: <https://youtu.be/uy5ZpPJLBFA>

[2] Como comprimir imagens usando Python e PIL. Acervo Lima, 2022. Disponível em: <https://acervolima.com/como-comprimir-imagens-usando-python-e-pil/>

[3] Image Processing with Python — Blob Detection using Scikit-Image. Disponível em: <https://towardsdatascience.com/image-processing-with-python-blob-detection-using-scikit-image-5df9a8380ade>

[4] Satellite Imagery Analysis 101: Handling TIFF Files. Disponível em: <https://syamkakarla.medium.com/satellite-imagery-analysis-101-handling-tiff-files-22e4d2da236d>



 
