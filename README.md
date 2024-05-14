## Projeto 1 (um) - "Login"

- Autor Moisés Ademir Chiaretto
  
- Descrição das explicações de cada item da 'estrutura do projeto "Login" desenvolvido' em Apache JMeter.

- O Apache JMeter irá medir o desempenho e testar a carga de **N Usuário durante o Login** no site Web informado, realizando a leitura de um arquivo com o nome de **"Dados_Login.csv"** com o dados do login como **o CPF e a Senha dos Usuários.**

- Site oficial do Apache JMeter:

  https://jmeter.apache.org

![01_Logo_Apache_JMeter](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/7bba3d9a-4173-43bc-9aa5-8b5eacc11e17)



## Estrutura do Projeto "Login"

![02_Estrutura_Projeto_Login](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/9386619a-48d6-475d-9aa1-83b71c6b46f1)



## Criar o "Plano de Teste"

- Dentro do **Plano de Testes** será inserido todas os cenários de execuções de desempenho, carga e análise de resultados.

![03_Plano_de_Testes](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/99f4289d-a8b7-43bb-a73d-f7bdf7e0af8d)



## Adicionar o "Grupo de Usuários"

  - Contém o campo com o nome **Number of Threads (users):** onde pode ser informado **a quantidade de usuários para a simulação de login** do site Web especificado.

![04_Grupo_de_Usuarios](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/fccf1c06-d7fb-4e75-9f2c-2592a31569f7)



## Adicionar a "Configuração dos dados CSV"

- Contém as configurações indicando basicamente:

    - **Filename:** caminho do arquivo.CSV
 
    - **Exemplo:** C:/jmeter_testes/Dados_Login.csv
 
    - **Variable Names:** os nomes das variáveis que serão utilizadas, por exemplo, em uma requisição HTTP (POST Login).
 
    - **Exemplos:** USERNAME,PASSWORD
 
![05_Configuracoes_dos_dados_CSV](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/21d91717-29ae-4252-93bb-4bd166b6153d)



## Adicionar um grupo "GET"

  - O grupo **GET** é para organizar todas as **requisições HTTP com o método GET.

  ![06_Grupo_GET](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/4d27f043-957c-4f05-8c55-dc90d724945f)


## Adicionar a "Requisição HTTP (GET Login)"

  - A **Requisição HTTP (GET Login)** contém as informações do site Web que será acessado para a realização dos testes, por exemplos:

      - **HTTP Request** informar o **Nome:** da request.
      
      - **Guia Basic**

          - **Protocol [http]:** informar **HTTPS**
       
          - **Server Name or IP:** informar **wwws.bradescosaude.com.br**
       
          - **Port Number:** informar **443**
       
          - **HTTP Request:** selecionar o método HTTP, neste caso **GET**
       
          - **Path:** informar como se fosse o "endpoint", neste caso **/#/login**

       
![07_Requisicao_HTTP_GET](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/858839eb-f547-40d7-bab2-9d205037db76)



## Adicionar Response Assertion GET

  - Informar na assertiva do **método GET o status code igual a 200.**

![08_Assert_GET](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/33284b3d-3c61-47f0-b3c7-406b3f3955c5)



## Adicionar um grupo "POST"

  - O grupo **POST** é para organizar todas as **requisições HTTP com o método POST.**

![09_Grupo_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/3e3a8db5-9ef0-4625-a086-22305413f241)


## Adicionar a "Requisição HTTP (POST Login)"
  
  - Para entrar com os dados do **arquivo "Dados_Login.csv", que contém o CPF e a Senha de Login.**

![16_Dados_Login_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/9d865fed-db1d-4a0f-baa2-b244e653e0ea)


![10_Requisicao_HTTP_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/50d90714-f9c4-4ddf-aa76-17c700da5f8d)


# Adicionar Response Assertion POST

  - Informar na assertiva do **método POST o status code igual a 200.**

![11_Assert_POST](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/276e4184-1348-4b52-b3db-62699c865424)

 

## Adicionar "Ver Árvore de Resultados"

  - Resultado da execução considerando **3 (três) Threads,, conforme na imagem e tópico acima "Grupo de Usuários".**

  - Contém o campo com o nome **Number of Threads (users):** onde pode ser informado **a quantidade de usuários para a simulação de login** do site Web especificado.

![13_Ver_Arvore_Resultados](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/cc24c0cb-e778-44d1-8880-1211a15c3961)


## Adicionar "Relatório de Sumário"

![14_Relatorio_Sumario](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/7a8d8a70-93e0-4fc4-ae82-02f91fbcf92c)



## Adicionar "Relatório de Agregado"

![15_Relatorio_Agregado](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/a8446fe7-b693-46bd-bdbd-7e122fab4541)


## Considerando a Execução do "Plano de Testes" para "30 Threads"

- Em **Grupo de Usuários** no campo com o nome **Number of Threads (users):** informar o **número de Threads = 30 (trinta).**

![01_Grupo_Usuarios_Execucao_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/56b4af47-89ea-4a1e-9f6e-75cb0426633f)


![02_Resultados_Asserts_GET_POST_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/cb8e33c8-72dd-4c6d-b566-28a509e86251)


![03_Ver_Arvore_Resultados_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/f2771853-eaf6-48b9-a920-042e6cbfec2f)


![04_Relatorio_Sumario_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/a0386379-165b-4aa8-87ac-3d44291b02b2)


![05_Relatorio_Agregado_30_Threads](https://github.com/moiseschiaretto/JMeter_Testes/assets/84775466/3c3ca425-cf65-4068-a847-4e4b4a5ac175)


## Projeto 2 (dois) - "API REST"

- Autor Moisés Ademir Chiaretto

- Descrição das explicações de cada item da 'estrutura do projeto "API REST" desenvolvido' em Apache JMeter.

- API REST conversão da Collection ou das Requisiçõe selecionadas do Postman (Loadium, Code) para o Apache JMeter, Smoke Test (checklist), Testes de Regressão, Análise de Resultados.

**Documentação em construção ...**


