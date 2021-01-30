# Criando uma arquitetura para testes de API com RestAssured

## Conceituação

- Pirâmide de Testes Original

Unite Test:

Service Test:

UI Tests:

- Pirâmide de Testes Ideal

Automated Unit Tests

Automated Component Tests - Automated Integration Test - Automated API Tests

Automated e2e Tests

Manual Exploratory Testing

## Arquitetura

- BackEnd - API: Testes funcionais e de aceitação para fronted web e/ou mobile

- FrontEnd - API Gateway: Testes na API de consumo, testes unitários e interação no backend

## APIs Individuais

API -> API -> API -> API -> API -> API

Obs: Assumimos que as API já possuem testes  unitários, "Testes Unitários done!"

## Individual APIs

Precisamos testa funcionalmente as APIs em separado

API = API = API = API = API= API = API

## Testes de Contrato e E2E

API {Contrato & E2E} API

## Contract and E2E testing

"Garante a comunicação entre APIs"

Contrato -- & E2E

"Garantir que as APIs podem ser utilizadas em conjunto"

Como serão os projetos de testes ?

## Modelo 1

Um projeto de teste para todos os microserviço

- Projeto Teste: TEST

- BackEnd: API - API - API

## Modelo 2

Um projeto de teste para cada microserviço dividido em projetos de cliente e testes

- Projeto Teste: Client = TEST, Client = TEST, Clint TEST

- BackEnd: API - API - API

## Recapitulando
Rest-Assured
http://rest-assured.io

DSL Java para simplificar a execução de testes para serviços REST

import static io.restassured.RestAssured.*;
import status. org.hamcrest.Matchers.*;

public class RestAssuredExampleTest {

   @Test

   public void welcome(){

     given().
         param("nome", "Mateus").
     when().
         post("/registro").
     then().
         body("mensagem", is("OI Mateus"));
   }
}

Passos...

1. Entender a documentação da API
2. Pensar nos testes com uma divisão de pipiline
3. Criar uma versão inicial da arquitetura
4. Criar os testes e difinir as suítes de testes

# Cobertura de teste
