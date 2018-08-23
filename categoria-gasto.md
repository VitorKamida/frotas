---
description: CRUD - categoria gasto
---

# Categoria Gasto

{% api-method method="post" host="https://api.brschaffen-it.com" path="/api/frota/categoria" %}
{% api-method-summary %}
Cadastro Categoria
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Token de autenticação JWT
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="descricao" type="string" required=true %}
Descrição da categoria
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
"status":true,
"data":{
"codigo": "1",
"descricao": "Categoria"
},
"errors":{},
"message":"Cadastro realizado com sucesso"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
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



