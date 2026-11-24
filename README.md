# PrimeAuto

Calculateur de prime d'assurance auto en C# (application console). Les tarifs sont fictifs.

## Ce que le programme fait

Il demande les informations du conducteur, calcule la prime annuelle et mensuelle, et affiche un devis aligné.

## Entrées

- âge : entier de 18 à 99
- années de permis : entier de 0 à (âge − 18)
- véhicule : citadine, berline, SUV ou sportive
- zone : rurale, urbaine ou grande ville
- sinistres sur les 5 dernières années : entier de 0 à 10

## Règles de calcul

Prime = base × tous les coefficients.

| Critère | Valeur |
|---|---|
| Base par véhicule | citadine 400 €, berline 550 €, SUV 650 €, sportive 900 € |
| Âge | moins de 25 ans ×1,5 · 25 à 64 ans ×1,0 · 65 ans et plus ×1,2 |
| Permis | moins de 3 ans ×1,3 · sinon ×1,0 |
| Zone | rurale ×0,9 · urbaine ×1,0 · grande ville ×1,2 |
| Sinistres | 0 → ×0,95 · 1 → ×1,0 · 2 → ×1,25 · 3 ou plus → ×1,5 |

La prime mensuelle est la prime annuelle divisée par 12.

## Lancer le projet

```
cd PrimeAuto
dotnet run
```
