---
title: std::strcat
---

Definit în headerul `<cstring>` astfel:
{% highlight C++ %}
char *strcat( char *dest, const char *src );
{% endhighlight %}

Adaugă o copie a șirului de caractere care este arătat de către `src` la sfârșitul șirului de caractere arătat de către `dest`. Caracterul `src[0]` înlocuiește terminatorul nul de la sfârșitul lui `dest`. Șirul de caractere ce rezultă este nul-terminat. <br>
Comportamentul este nedefinit dacă șirul destinație nu este suficient de mare simultan pentru conținutul lui `src`, conținutui lui `dest` și pentru terminatorul nul. <br>
Comportamentul este nedefinit dacă șirurile se suprapun.

# Parametri

| Parametru | Descriere                                                   |
| --------: | :---------------------------------------------------------- |
|  **dest** | pointer către șirul de caractere nul-terminat de adăugat în |
|   **src** | pointer către șirul de caractere nul-terminat de copiat     |

# Valuare returnată

`dest`

# Notițe

Pentru că `strcat` trebuie să caute până la sfârșitul lui `dest` la fiecare apel, este ineficient să se concateneze multe șiruri de caractere într-unul singur folosind `strcat`.

# Exemplu

{% highlight C++ %}
#include <iostream>
#include <cstring>

using namespace std;

int main()
{
    char str[50] = "Hello ";
    char str2[50] = "World!";
    strcat(str, str2);
    strcat(str, " Goodbye World!");
    cout << str;

    return 0;
}
{% endhighlight %}

Output:
```
Hello World! Goodbye World!
```

(Tradus și adaptat după [cppreference.com](https://en.cppreference.com/w/cpp/string/byte/strcat) - CC-BY-SA-3.0)
