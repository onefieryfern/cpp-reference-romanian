---
title: std::strlen
---

Definit în headerul `<cstring>` astfel:
{% highlight C++ %}
std::size_t strlen( const char* str );
{% endhighlight %}

Returnează lungimea șirului de caractere dat, adică numărul de caractere dintr-un șir de caractere al cărei prim element este arătat de către `str` până la și fără a include primul caracter nul. Comportamentul este nedefinit dacă nu există nici un caracter nul în șirul de caractere arătat de către `str`.

# Parametri

| Parametru | Descriere                                                 |
| --------: | :-------------------------------------------------------- |
|   **str** | pointer către șirul de caractere nul-terminat de examinat |

# Valuare returnată

Lungimea șirului nul-terminat `str`.

# Exemplu

{% highlight C++ %}
#include <cstring>
#include <iostream>

using namespace std;

int main()
{
    const char str[] = "Cate caractere contine acest sir de caractere?";

    cout << strlen(str) << '\n';

    return 0;
}
{% endhighlight %}

Output:
```
46
```

(Tradus și adaptat după [cppreference.com](https://en.cppreference.com/w/cpp/string/byte/strlen) - CC-BY-SA-3.0)
