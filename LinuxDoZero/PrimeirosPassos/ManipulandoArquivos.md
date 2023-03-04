# Manipulando Arquivos

## Terminal Linux

&emsp;&emsp;O terminal do Linux tem os seguintes elementos: 

        usuario@localHost:~$

Sendo que o "usuario" refere-se o usuário atual ou que esta *logado* atualmente. Já o "localHost" é o nome da máquina. O "~" indica o local atual dentro do Sistema de Arquivos referente ao usuário. E o "$" signfica que o usuário *logado* não é superusuário.   

É interessante ressaltar que todos os comandos do Linux são ***sensitive case***, ou seja, diferencia as letras maiúsculas das minúsculas.

## Navegando pelo sistema de arquivos e diretórios

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| pwd | print work directory                       | Imprime o caminho do diretório atual |
| ls       | list              | Lista os arquivos e diretórios do diretório atual          |
| cat | concatenate                       | Imprime conteúdo de um ou mais arquivos sem precisar abrir o arquivo para edição |
| clear       | -              | Limpa a tela do terminal |
| cd \<nome\> | change directory  | Troca o diretório atual para o diretório **nome** indicado |   
| cd / | change directory  | Troca o diretório atual para o diretório **Raiz** (Root)  |
| cd ~ | change directory  | Troca o diretório atual para o diretório de **Usuário** (User)  |
| cd .. | change directory  | Troca o diretório atual para o diretório anterior  |

## Filtrando a exibição de arquivos e diretórios

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| ls \| more | list              | Lista os arquivos e diretórios do diretório atual , permitindo a visualização de 1 arquivo por vez       |
| ls \<nome\> | list              | Lista os arquivos e/ou diretórios com o **nome** indicado  |
| ls \<letra\>* | list              | Lista os arquivos e/ou diretórios iniciados com a  **letra** indicada, sendo o '*' (asterisco) usado para indicar que existe uma ou mais letras ou números a partir da posição especificada, onde o símbolo foi utilizado |
| ls \<letra\>? | list              | Lista os arquivos e/ou diretórios iniciados com a  **letra** indicada, sendo a '?' (interrogação) usada para indicar que existe apenas uma letra ou número a partir da posição especificada, onde o símbolo foi utilizado |
| ls \<nome\>[x-y] | list              | Lista os arquivos e/ou diretórios com o '**nome**' indicado, sendo que 'x' e 'y' são números que indicam uma listagem. Exemplo: ls arquivo[1-3]; caso existam os arquivos, deverá ser listado: arquivo1, arquivo2 e arquivo3 |

## Localizando arquivos e diretórios


| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| find -name \<nome\> | -              | Procura os arquivos e subdiretórios do diretório atual, sendo que '-name' é parâmetro para buscar pelo nome, e '**nome**' é o nome do arquivo/subdiretório procurado  |

## Criando arquivos e diretórios

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| mkdir \<nome\> | make directory              | Cria um novo diretório dentro do diretório atual, e '**nome**' é o nome do diretório criado  |
| touch \<nome\> | -              | Cria um novo arquivo dentro do diretório atual, e '**nome**' é o nome do arquivo criado  |


## Excluindo arquivos e diretórios

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| rmdir \<nome\> | remove directory              | Exclui um subdiretório dentro do diretório atual, e '**nome**' é o nome do subdiretório excluído  |
| rm \<nome\> | remove              | Exclui um arquivo dentro do diretório atual, e '**nome**' é o nome do arquivo excluído  |
| rm -rf \<nome\> | remove -recursively forced             | Exclui um subdiretório dentro do diretório atual, com parâmetro '-rf' que força a exclusão recursiva de todos os diretórios e arquivos dentro do subdiretório indicado pelo '**nome**', que é o nome do diretório excluído  |

## Obtendo ajuda

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| \<nome\> --help | -              | Obtém ajuda sobre os parâmetros do comando, cujo '**nome**' representa o nome do comando  |

## Executando tarefas administrativas como root

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| sudo \<nome\> | -              | Realiza o comando como root, cujo '**nome**' representa o nome do comando  |

## Logando como usuário root

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| sudo passwd root | sudo password root              | Cria uma senha para o *Root* (Raiz)  |
| su | super user              | Troca do usuário atual para o usuário *Root* (Raiz) |

## Histórico de comandos

| Comando | Sigla/Acrônimo | Significado |
| -       | -              | -          |
| history | -              | Imprime o histórico dos últimos comandos realizados pelo usuário atual |
| history \<x\> | -              | Imprime o histórico dos últimos '**x**' números  comandos realizados pelo usuário atual |
| history \| grep \<nome_arq_ou_dir\> | -              | Imprime o histórico dos últimos comandos que possuem o nome do arquivo ou diretório procurado, sendo que '**nome_arq_ou_dir**' é o nome do arquivo ou diretório |
| !\<numero_comando\> | -              | Realiza o comando que possui um número no histórico, sendo que '**numero_comando**' é o número do comando no histórico |
| !! | -              | Realiza o último comando do histórico |
