## Projeto 1 (um) - "Login"

- Autor Moisés Ademir Chiaretto
  
- Descrição das explicações de cada item da 'estrutura do projeto "Login" desenvolvido' em Apache JMeter.

- O Apache JMeter irá medir o desempenho e testar a carga de **N Usuário durante o Login** no site Web informado, realizando a leitura de um arquivo com o nome de **"Dados_Login.csv"** com o dados do login como **o CPF e a Senha dos Usuários.**

- Site oficial do Apache JMeter:

  https://jmeter.apache.org


![01_Logo_Apache_JMeter](https://github.com/moiseschiaretto/JMeterTestes/assets/84775466/1f5edcd8-7316-4317-a606-cc22d49d751d)

## Estrutura do Projeto "Login"

![02_Estrutura_Projeto_Login](https://github.com/moiseschiaretto/JMeterTestes/assets/84775466/89ddd2c7-1f03-433c-be76-b3e638eff033)


## Criar o "Plano de Teste"

- Dentro do **Plano de Testes** será inserido todas os cenários de execuções de desempenho, carga e análise de resultados.

![03_Plano_de_Testes](https://github.com/moiseschiaretto/JMeterTestes/assets/84775466/0c05f131-c39e-458b-b56e-2a297fe1731f)


## Adicionar o "Grupo de Usuários"

  - Contém o campo com o nome **Number of Threads (users):** onde pode ser informado **a quantidade de usuários para a simulação de login** do site Web especificado.

![04_Grupo_de_Usuarios](https://github.com/moiseschiaretto/JMeterTestes/assets/84775466/50e5e78d-7ed5-4ad4-8291-d1e4901cba6b)


## Adicionar a "Configuração dos dados CSV"

- Contém as configurações indicando basicamente:

    - **Filename:** caminho do arquivo.CSV
 
    - **Exemplo:** C:/jmeter_testes/Dados_Login.csv
 
    - **Variable Names:** os nomes das variáveis que serão utilizadas, por exemplo, em uma requisição HTTP (POST Login).
 
    - **Exemplos:** USERNAME,PASSWORD
 
![05_Configuracoes_dos_dados_CSV](https://github.com/moiseschiaretto/JMeterTestes/assets/84775466/3d81db98-307a-48b7-8167-3b3ee49bdd12)


## Adicionar um grupo "GET" e a "Requisição HTTP (GET Login)"

  - O grupo **GET** é para organizar todas as **requisições HTTP com o método GET.

  ![06_Grupo_GET](https://github.com/moiseschiaretto/JMeterTestes/assets/84775466/f814dbe1-4411-4446-b429-907169c2283e)


  - A **Requisição HTTP (GET Login)** contém as informações do site Web que será acessado para a realização dos testes, por exemplos:

      - **HTTP Request** informar o **Nome:** da request.
      
      - **Guia Basic**

          - **Protocol [http]:** informar **HTTPS**
       
          - **Server Name or IP:** informar **wwws.bradescosaude.com.br**
       
          - **Port Number:** informar **443**
       
          - **HTTP Request:** selecionar o método HTTP, neste caso **GET**
       
          - **Path:** informar como se fosse o "endpoint", neste caso **/#/login**
       
  ![07_Requisicao_HTTP_GET](https://github.com/moiseschiaretto/JMeterTestes/assets/84775466/d4eee264-cf9b-461c-be27-a9f3d89a29d6)



## Documentação em construção ....


## Adicionar um grupo "POST" e a "Requisição HTTP (POST Login)"


## Adicionar "Ver Árvore de Resultados"


## Adicionar "Relatório de Sumário"



## Projeto 2 (dois) - "API REST"

- Autor Moisés Ademir Chiaretto

- Descrição das explicações de cada item da 'estrutura do projeto "API REST" desenvolvido' em Apache JMeter.

- API REST conversão da Collection ou das REquisiçõe selecionadas do Postman (Loadium, Code) para o Apache JMeter, Smoke Test (checklist), Testes de Regressão, Análise de Resultados.

