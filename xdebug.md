# xDebug werkend maken met PHP en XAMPP.
De stappen zijn vrij simpel, dit is overgenomen van de video van [De Youtube video](https://www.youtube.com/watch?v=eE6oxEhqqoU)

## Stap 1
Installeer de PHP debug (Extensions ID: felixfbecker.php-debug) in VSCode en zorg dat je een PHPinfo pagina hebt zoals in de video.

## Stap 2
Zorg ervoor dat je naar de docs van PHP Debug heb gekeken en dat je de volgende in je PHP ini heb staan vanuit de Extensions

```
[XDebug]
xdebug.remote_enable = 1
xdebug.remote_autostart = 1
zend_extension = "C:\xampp\php\ext\php_xdebug-2.9.8-7.4-vc15-x86_64.dll"
```

## Stap 3
Kijk naar je PHPinfo en maak een copy van het eerste stuk en plak deze in de [xdebug wizard](https://xdebug.org/wizard).

Je krijgt een file en die moet ik de XAMPP path en daarin naar `php/ext` en zet de downloaded file daarin.

## Stap 4
Zorg ervoor dat in je settings.json van VS code de volgende variable staat;
```json
"php.validate.executablePath": "C:\\xampp\\php\\php.exe",
```

## Stap 5
Daarna druk op het icoontje van de PLay met het bug ernaast. en create een launch.json op basis van PHP (en NIET chrome) en probeer je de code debuggen van de workspace door breakpoints te zetten.
