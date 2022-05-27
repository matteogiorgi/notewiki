## Sbagliato

```
START

G = { <? ? ? ?> }
S = { <x x x x> }

Esempio 1: <0 0 1 0> negativo
    S = { <x x x x> }
    G = { <1 ? ? ?> <? 1 ? ?> <? ? 0 ?> <? ? ? 1>  }

Esempio 2: <0 1 0 0> negativo
    S = { <x x x x> }
    G = { <1 ? ? ?>, <1 1 ? ?>, <? 1 1 ?>, <? 1 ? 1>, <? ? 0 ?>, <? ? ? 1> }
        rimozione: <1 1 ? ?>, <? 1 ? 1>
        G = { <1 ? ? ?>, <? 1 1 ?>, <? ? 0 ?>, <? ? ? 1>  }

Esempio 3: <0 0 1 1> positivo
    G = { <1 ? ? ?>, <? 1 1 ?>, <? ? 0 ?>, <? ? ? 1> }
        rimozione: <1 ? ? ?>, <? 1 1 ?>, <? ? 0 ?>
        G = { <? ? ? 1> }
    S = { <0 0 1 1> }

Esempio 4: <1 0 0 1> positivo
    G = { <? ? ? 1> }
    S = { <? 0 ? 1> }

Esempio 5: <0 1 1 0> negativo
    S = { <? 0 ? 1> }
    G = { <? ? ? 1> }

Esempio 6: <1 1 0 0> negativo
    S = { <? 0 ? 1> }
    G = { <? ? ? 1> }

Esempio 7: <0 1 0 1> negativo
    S = { <? 0 ? 1> }
    G = { <? ? ? 1> }
        rimozione: <? ? ? 1>
        G = { <? 0 ? 1> }

RETURN:
    G = { <? 0 ? 1> }
    S = { <? 0 ? 1> }
END

G==S => l'unica ipotesi contenuta nel version-space e' not(x_2) and x_4
```




## Correzione

```
START

G = { <? ? ? ?> }
S = { <x x x x> }

Esempio 1: <0 0 1 0> negativo
    S = { <x x x x> }
    G = { <1 ? ? ?> <? 1 ? ?> <? ? 0 ?> <? ? ? 1>  }

Esempio 2: <0 1 0 0> negativo
    S = { <x x x x> }
    G = { <1 ? ? ?>, <1 1 ? ?>, <? 1 1 ?>, <? 1 ? 1>, <1 ? 0 ?>, <? 0 0 ?>, <? ? 0 1> <? ? ? 1> }
        rimozione: <1 1 ? ?>, <? 1 ? 1>, <? ? 0 1>, <1 ? 0 ?>
        G = { <1 ? ? ?>, <? 1 1 ?>, <? 0 0 ?>, <? ? ? 1>  }

Esempio 3: <0 0 1 1> positivo
    G = { <1 ? ? ?>, <? 1 1 ?>, <? 0 0 ?>, <? ? ? 1> }
        rimozione: <1 ? ? ?>, <? 1 1 ?>, <? 0 0 ?>
        G = { <? ? ? 1> }
    S = { <0 0 1 1> }

Esempio 4: <1 0 0 1> positivo
    G = { <? ? ? 1> }
    S = { <? 0 ? 1> }

Esempio 5: <0 1 1 0> negativo
    S = { <? 0 ? 1> }
    G = { <? ? ? 1> }

Esempio 6: <1 1 0 0> negativo
    S = { <? 0 ? 1> }
    G = { <? ? ? 1> }

Esempio 7: <0 1 0 1> negativo
    S = { <? 0 ? 1> }
    G = { <? ? ? 1> }
        rimozione: <? ? ? 1>
        G = { <? 0 ? 1> }

RETURN:
    G = { <? 0 ? 1> }
    S = { <? 0 ? 1> }
END

G==S => l'unica ipotesi contenuta nel version-space e' not(x_2) and x_4
```
