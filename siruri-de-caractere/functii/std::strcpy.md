---
title: std::strcpy
---

Definit în headerul `<cstring>` astfel:
{% highlight C++ %}
char* strcpy( char* dest, const char* src );
{% endhighlight %}

Copiază șirul de caractere spre care arată `src`, inclusiv terminatorul nul, la șirul de caractere al cărui prim element este arătat de către `dest`. <br>
Comportamentul este nedefinit dacă șirul `dest` nu este suficient de mare. Comportamentul este nedefinit dacă șirurile se suprapun.

# Parametri

Parametru | Descriere
---: | :---
**dest** | 	pointer către șirul de caractere de scris în
**src**  | 	pointer către șirul de caractere nul-terminat de copiat

# Valuare returnată

`dest`

(Tradus și adaptat după [cppreference.com](https://en.cppreference.com/w/cpp/string/byte/strcpy) - CC-BY-SA-3.0)
