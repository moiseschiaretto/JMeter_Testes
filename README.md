## Projeto 1 (um) - "Login"

- Autor Moisés Ademir Chiaretto
  
- Descrição das explicações de cada item da 'estrutura do projeto "Login" desenvolvido' em Apache JMeter.

- O Apache JMeter irá medir o desempenho e testar a carga de **N Usuário durante o Login** no site Web informado, realizando a leitura de um arquivo com o nome de **"Dados_Login.csv"** com o dados do login como **o CPF e a Senha dos Usuários.**

Site oficial do Apache JMeter:

https://jmeter.apache.org


<br>


|JMeter         |JMeter Performance           |Postman        |API          |JSON          |
|---------------|-----------------------------|---------------|-------------|--------------|
| ![01_Logo_Apache_JMeter](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/eafb6c1d-9a94-42eb-af9d-321ba78d321a) | ![02_Logo_Apache_JMeter](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/7873c059-177d-4ee2-884a-04ed68c83cb1) | ![01_Logo_Postman](https://github.com/moiseschiaretto/Postman_API_REST/assets/84775466/9a62ed55-bcd1-4297-abc6-380c7dc6153d) | ![10_API_REST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/62a0ef45-48ec-4cb4-b514-b3d246cea9b7) | <img width="164" alt="04_JSON" src="https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/7faed896-35a3-4447-bbc0-f4ae52b7c87c"> |
<br>


## Estrutura do Projeto "Login"

![02_Estrutura_Projeto_Login](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/9386619a-48d6-475d-9aa1-83b71c6b46f1)



## "Plano de Testes"

- Dentro do **Plano de Testes** será inserido todas os cenários de execuções de desempenho, carga e análise de resultados.

![03_Plano_de_Testes](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/99f4289d-a8b7-43bb-a73d-f7bdf7e0af8d)



## "Grupo de Usuários"

  - Contém o campo com o nome **Number of Threads (users):** onde pode ser informado **a quantidade de usuários para a simulação de login** do site Web especificado.

![04_Grupo_de_Usuarios](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/fccf1c06-d7fb-4e75-9f2c-2592a31569f7)



## "Configuração dos dados CSV"

- Contém as configurações indicando basicamente:

    - **Filename:** caminho do arquivo.CSV
 
    - **Exemplo:** C:/jmeter_testes/Projeto1_Login/Dados_Login.csv
 
    - **Variable Names:** os nomes das variáveis que serão utilizadas, por exemplo, em uma requisição HTTP (POST Login).
 
    - **Exemplos:** USERNAME,PASSWORD
 
![05_Configuracoes_dos_dados_CSV](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/21d91717-29ae-4252-93bb-4bd166b6153d)

  - Arquivo "Dados_Login.csv", com **o CPF e a Senha dos Usuários.**

![16_Dados_Login_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/2fd9d765-db45-4163-b85d-c4c4532e7d1a)


## Grupo "GET"

  - O grupo **GET** é para organizar todas as **requisições HTTP com o método GET.

  ![06_Grupo_GET](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/4d27f043-957c-4f05-8c55-dc90d724945f)


## "Requisição HTTP GET"

  - A **Requisição HTTP (GET Login)** contém as informações do site Web que será acessado para a realização dos testes, por exemplos:

      - **HTTP Request** informar o **Nome:** da request.
      
      - **Guia Basic**

          - **Protocol [http]:** informar **HTTPS**
       
          - **Server Name or IP:** informar **wwws.bradescosaude.com.br**
       
          - **Port Number:** informar **443**
       
          - **HTTP Request:** selecionar o método HTTP, neste caso **GET**
       
          - **Path:** informar como se fosse o "endpoint", neste caso **/#/login**

       
![07_Requisicao_HTTP_GET](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/858839eb-f547-40d7-bab2-9d205037db76)



## "Response Assertion GET"

  - Informar na assertiva do **método GET o status code igual a 200.**

![08_Assert_GET](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/33284b3d-3c61-47f0-b3c7-406b3f3955c5)



## Grupo "POST"

  - O grupo **POST** é para organizar todas as **requisições HTTP com o método POST.**

![09_Grupo_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/3e3a8db5-9ef0-4625-a086-22305413f241)


## "Requisição HTTP POST"
  
  - Para entrar com os dados do **arquivo "Dados_Login.csv", que contém o CPF e a Senha de Login.**

![16_Dados_Login_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/9d865fed-db1d-4a0f-baa2-b244e653e0ea)


![10_Requisicao_HTTP_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/50d90714-f9c4-4ddf-aa76-17c700da5f8d)


# "Response Assertion POST"

  - Informar na assertiva do **método POST o status code igual a 200.**

![11_Assert_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/276e4184-1348-4b52-b3db-62699c865424)


## Execução do "Plano de Testes"

  - Utilizar o botão **"Start"** para executar o "Plano de Testes".

  ![18_botao_Start](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/e003f4d6-64e6-403d-bdb7-94ec96f9a43d)

  - Utilizar o botão **"Clear All"** para limpar todos os resultados da execução, caso desejar.

  ![19_Botao_Clear_All](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/ba438e1e-11b0-4cb7-bd99-f748054f1e5f)



## "Assertion Results"

  - Exibe o resultado de todas as asserções do "Plano de Testes", neste caso os métodos GET e POST.

![12_Resultados_Asserts_GET_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/c9ba5cde-c09f-4424-8f60-9e7781b6a35d)


## "Ver Árvore de Resultados"

  - Resultado da execução considerando **3 (três) Threads, conforme na imagem e tópico acima "Grupo de Usuários".**

  - Contém o campo com o nome **Number of Threads (users):** onde pode ser informado **a quantidade de usuários para a simulação de login** do site Web especificado.

![13_Ver_Arvore_Resultados](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/cc24c0cb-e778-44d1-8880-1211a15c3961)


## "Relatório de Sumário da Execução"

  - No grid da tela, na coluna **"Label"** é informado a quantidade de vezes em que foram realizados os "testes de login", neste caso foram 3 (três) testes, informados em **"Grupo de Usuários",** campo com o nome **Number of Threads (users).**

![20_Grade_Arvore_Resultados](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/cbecc5ee-e54c-4dd0-8b42-eb7911761b38)


  - No canto superior direito da tela também é informado a  quantidade de vezes em que foram realizados os "testes de login", e os erros ocorridos.

![21_Erros_Qtde_Execucoes](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/5b5a1782-9d02-4d6e-b09b-3480e7d0e807)


![14_Relatorio_Sumario](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/7a8d8a70-93e0-4fc4-ae82-02f91fbcf92c)



## "Relatório de Agregado"

![15_Relatorio_Agregado](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/a8446fe7-b693-46bd-bdbd-7e122fab4541)



## Considerando a Execução do "Plano de Testes" para "30 Threads"

- Em **Grupo de Usuários** no campo com o nome **Number of Threads (users):** informar o **número de Threads = 30 (trinta).**

![01_Grupo_Usuarios_Execucao_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/56b4af47-89ea-4a1e-9f6e-75cb0426633f)


![02_Resultados_Asserts_GET_POST_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/80135cc7-6929-4d28-95fd-b0531f43b673)


- No grid da tela, na coluna **"Label"** é informado a quantidade de vezes em que foram realizados os "testes de login", neste caso foram 30 (trinta) testes, informados em **"Grupo de Usuários",** campo com o nome **Number of Threads (users).**

![22_Grade_Arvore_Resultados](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/91ccc22e-f353-4b47-a68b-811a4fe6cb2d)


- No canto superior direito da tela também é informado a  quantidade de vezes em que foram realizados os "testes de login", e os erros ocorridos.

![23_Erros_Qtde_Execucoes](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/24ec6ab4-89b1-4582-87b7-a9962568153e)


![03_Ver_Arvore_Resultados_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/1acff2c7-ba71-4f8d-8d70-49dd42bfdbd9)


![04_Relatorio_Sumario_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/a0386379-165b-4aa8-87ac-3d44291b02b2)


![05_Relatorio_Agregado_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/3c3ca425-cf65-4068-a847-4e4b4a5ac175)



# Projeto 2 (dois) - "API REST"

- Autor Moisés Ademir Chiaretto

- Descrição das explicações de cada item da 'estrutura do projeto "API REST" desenvolvido' em Apache JMeter.

- API REST conversão da Collection ou das Requisições selecionadas do Postman (Loadium, Code) para o Apache JMeter, Execução dos Testes, Análise de Resultados.


## Estrutura do Projeto "API_REST"

![01_Estrutura_Projeto_API_REST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/8ea450ef-5ed2-4958-8152-736fad827bea)



## Ver a Árvore de Resultados da Execução

![02_Ver_Arvore_de_Resultados](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/09ecbc69-03e0-4bfe-aa6e-45aa892f1e51)



## Relatório de Sumário da Execução

![03_Relatório_Sumario](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/f5c19afd-d3a2-4b05-a96f-a740f54fa7df)


**Documentação em construção ...**


