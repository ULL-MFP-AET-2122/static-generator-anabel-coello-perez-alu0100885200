---
title: "Post de Prueba"
alumnos: 20
titulo: "Aprendiendo" 
chuchu: 4
agricolita: "esta perdida"
esmartes: false
frutas:
  - naranjas
  - peras
  - limones
  - fresas
---
{{site.author.bio}}
# {{page.titulo}}

{% for x in page.frutas %}
1. Me gusta mucho comer {{ x }}
{% endfor %}

# <span style="color:purple"> *Martes, 9 de noviembre de 2021*

![](https://i.pinimg.com/564x/4d/81/5c/4d815cda58fbe6bf197771f4b6ea9a9c.jpg)

<h2> un título </h2>

<h3> un título más pequeño </h3>

Somos {{page.alumnos}} alumnos

Mi usuario de twitter es {{site.twitter.username}}

La respuesta a cuanto vale chuchu es {{ page.chuchu }}

¿Qué pasa con agricolita? {{ page.agricolita }}

{% if page.esmartes %}

## socorro

{% else %}

## socorro socorro

{% endif %}

{% if page.esmartes %}

## socorro

{% else %}

## socorro socorro

{% endif %}