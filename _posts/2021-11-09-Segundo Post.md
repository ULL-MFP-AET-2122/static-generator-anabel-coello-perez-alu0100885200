---
alumnos: 20
titulo: "Un día tranquilo" 
chuchu: 4
agricolita: "esta perdida"
esmartes: false
frutas:
  - naranjas
  - peras
  - limones
  - fresas
---

# {{page.titulo}}

{% for x in page.frutas %}
1. Me gusta mucho comer {{ x }}
{% endfor %}

# Título: Segundo Post

![](https://static.vecteezy.com/system/resources/previews/000/527/023/non_2x/vector-tree-with-roots.jpg)

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