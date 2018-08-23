-
--
description: CRUD - Veículo
---

# Veículo

{% api-method method="post" host="https://api.brschaffen-it.com" path="/api/frota/veiculo" %}
{% api-method-summary %}
Cadastro de veículos
{% endapi-method-summary %}

{% api-method-description %}
Rota para cadastrar um veículo no módulo Frota.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Token de autenticação JWT.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="placa" type="string" required=true %}
Placa do registro do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="modelo" type="string" required=false %}
Modelo do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="municipio" type="string" required=false %}
Município\(Cidade\) de registro do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="uf" type="string" required=false %}
Unidade Federativa\(Estado\) abreviada.
{% endapi-method-parameter %}

{% api-method-parameter name="cor" type="string" required=false %}
Cor do veículo
{% endapi-method-parameter %}

{% api-method-parameter name="ano" type="integer" required=false %}
Ano do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="identificador" type="string" required=false %}
Código alpha-númerico externo\(controle\) do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="renavam" type="integer" required=false %}
Renavam do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="chassi" type="string" required=false %}
NIV do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="km\_inicial" type="number" required=true %}
Quilometragem inicial do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="tipo\_combustivel" type="integer" required=true %}
Código de identificação do combustível.
{% endapi-method-parameter %}

{% api-method-parameter name="proprietario" type="string" required=true %}
Pes\_codigo do Proprietário do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="seguradora" type="integer" required=false %}
Pes\_codigo da Seguradora do veículo.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
"status":true,
"data":{
"codigo": "1",
"placa": "ABC1234",
"modelo": "Del Rey",
"municipio": "Ponta Grossa",
"uf": "PR",
"cor": "Azul Bebê",
"ano": "1987",
"numero": "FROTA01",
"renavam": "12345678910",
"chassi": "9BWZZZ377VT004251",
"km_inicial": "300000,00",
"tipo_combustivel": "1",
"proprietario": "1",
"seguradora": "230"
},
"errors":{},
"message":"Cadastro realizado com sucesso"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
"status":false,
"data":{),
"errors":{},
"message":"Não foi possível realizar o cadastro"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.brschaffen-it.com" path="/api/frota/veiculo/:codigo" %}
{% api-method-summary %}
Edição de veículos
{% endapi-method-summary %}

{% api-method-description %}
Rota para editar um veículo no módulo Frota.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Token de autenticação JWT.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="placa" type="string" required=false%}
Placa do registro do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="modelo" type="string" required=false %}
Modelo do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="municipio" type="string" required=false %}
Município\(Cidade\) de registro do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="uf" type="string" required=false %}
Unidade Federativa\(Estado\) abreviada.
{% endapi-method-parameter %}

{% api-method-parameter name="cor" type="string" required=false %}
Cor do veículo
{% endapi-method-parameter %}

{% api-method-parameter name="ano" type="integer" required=false %}
Ano do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="identificador" type="string" required=false %}
Código alpha-númerico externo\(controle\) do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="renavam" type="integer" required=false %}
Renavam do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="chassi" type="string" required=false %}
NIV do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="km\_inicial" type="number" required=false%}
Quilometragem inicial do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="tipo\_combustivel" type="integer" required=false %}
Código de identificação do combustível.
{% endapi-method-parameter %}

{% api-method-parameter name="proprietario" type="string" required=false %}
Pes\_codigo do Proprietário do veículo.
{% endapi-method-parameter %}

{% api-method-parameter name="seguradora" type="integer" required=false %}
Pes\_codigo da Seguradora do veículo.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
"status":true,
"data":{
"codigo": "1",
"placa": "ABC1234",
"modelo": "Del Rey",
"municipio": "Ponta Grossa",
"uf": "PR",
"cor": "Azul Bebê",
"ano": "1987",
"numero": "FROTA01",
"renavam": "12345678910",
"chassi": "9BWZZZ377VT004251",
"km_inicial": "300000,00",
"tipo_combustivel": "1",
"proprietario": "1",
"seguradora": "230"
},
"errors":{},
"message":"Cadastro realizado com sucesso"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
"status":false,
"data":{),
"errors":{},
"message":"Não foi possível realizar o cadastro"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


