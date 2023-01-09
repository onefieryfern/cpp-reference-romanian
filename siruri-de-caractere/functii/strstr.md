---
title: strstr
---

Definit în headerul `<cstring>` astfel:
{% highlight C++ %}
const char* strstr( const char* haystack, const char* needle );
      char* strstr(       char* haystack, const char* needle );
{% endhighlight %}

Găsește prima apariție a șirului de caractere `needle` (traducere: ac) în șirul de caractere spre care arată pointerul `haystack` (traducere: car de fân). Caracterele nul de terminare nu sunt comparate.

# Parametri

Parametru | Descriere
---: | :---
**haystack** | pointer către șirul de caractere nul-terminat de examinat
**needle**   | pointer către șirul de caractere nul-terminat de căutat

# Valuare returnată

Pointer către primul caracter al subșirului găsit în `haystack` sau un pointer nul (`nullptr`) dacă nu se găsește un astfel de caracter. Dacă `needle` este un pointer către un șir gol, se returnează `haystack`.

{% unless true %}
Reason for exclusion: "Clearer example needed"

# Exemplu

{% highlight C++ %}
#include <iostream>
#include <cstring>

using namespace std;

int main()
{
    char str[] = "Try not. Do, or do not. There is no try.";
    char target[] = "not";
    char rezultat[41];
    strcpy(rezultat, str);

    for ( ; rezultat; rezultat = std::strstr(rezultat, target)) {
        cout << "Am gasit '" << target 
             << "' incepand la '" << rezultat << "'\n";

        // Incrementează „rezultat”, altfel vom găsi „target” la aceeași locație
        rezultat++;
    }

    return 0;
}
{% endhighlight %}

Output:

```
Am gasit 'not' incepand la 'not. Do, or do not. There is no try.'
Am gasit 'not' incepand la 'not. There is no try.'
```

{% endunless %}

(Tradus și adaptat după [cppreference.com](https://en.cppreference.com/w/cpp/string/byte/strstr) - CC-BY-SA-3.0)
