Tento projekt se zaměřuje na ovládání adresovatelných LED pásků pomocí vlastní desky plošných spojů (DPS) založené na ESP32. Autor vyvinul toto řešení po zkušenostech s problémy s holými vývojovými deskami ESP32. Klíčové vlastnosti tohoto ovladače zahrnují:

- Postaveno na modulu ESP32-C3
- Integrované relé a 10A pojistka
- Možnost měření výkonu pomocí ACS722 a děliče napětí
- Připojení pro externí tlačítko
- Teplotní senzor a IR senzor
- Různé ochranné prvky (resetovatelná PTC pojistka, ESD ochrana, diody)
- USB-C konektor a buck konvertor napájený z Vin

Projekt využívá software WLED pro snadné ovládání a nabízí mnoho funkcí. Návrh DPS a dokumentace jsou k dispozici v repozitáři, včetně 3D tisknutelného krytu.

Autor je zvláště hrdý na funkci měření výkonu, kterou v podobných projektech neviděl. Na tomto projektu pracuje již delší dobu, začínal s hrubým prototypem a postupně jej vylepšoval až do současné podoby.

Projekt je v současné době vydán pod licencí CC BY-NC-SA 4.0, s plány na přechod na permisivnější licenci CERN-OHL-S v budoucnu. Autor vítá příspěvky a zpětnou vazbu od komunity.