# L'opérateur nullsafe

Permet d'eviter une vérification intermédiare de non null avant un appel de fonction

## Version PHP 7
```
$startDate = $booking->getStartDate();

$dateAsString = $startDate ? $startDate->asDateTimeString() : null;
```
## Version PHP 8
```
$dateAsString = $booking->getStartDate()?->asDateTimeString();
```