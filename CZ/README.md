# Ovladač LED pixelů (TwinkleTron)

>This is a czech translation of the README file. The original file can be found [here](../README.md).

Tento projekt je open-source ovladač pro adresovatelné LED pásky, který kombinuje širokou škálu funkcí, jako je měření výkonu, IR senzory a snadná integrace do různých instalací. Projekt je navržen s ohledem na nízkou spotřebu a bezpečnost při používání.

Obsahuje:

- **ESP32-C3-WROOM-02** jako hlavní procesor.
- Integrované měření výkonu (ACS722 a dělič napětí).
- Relé pro ovládání napájení LED.
- Přepěťovou a ESD ochranu.

Více informací naleznete níže nebo v přiložené [dokumentaci](../Documentation/).

<img src="../Images/V1/Board_2.jpg" alt="Board Image" width="500" style="border-radius: 50px;"/>

## Obsah

0. [Úvod](#ovladač-led-pixelů)
1. [Co je na tomto projektu tak zajímavé?](#co-je-na-tomto-projektu-tak-zajímavé)
2. [Funkce](#funkce)
3. [Proč jsem se rozhodl tento projekt realizovat?](#proč-jsem-se-rozhodl-tento-projekt-realizovat)
4. [Vývoj](#vývoj)
5. [Dokumentace](#dokumentace)
6. [Chtěl bych ho prodávat?](#chtěl-bych-ho-prodávat)
7. [Jaká je má motivace?](#jaká-je-má-motivace)
8. [Co jsem se naučil?](#co-jsem-se-naučil)
9. [Jaké je vlastně použití?](#jaké-je-vlastně-použití)
10. [Software](#software)
11. [Závěr](#závěr)
12. [Kontribuce](#kontribuce)
13. [Licence](#licence)

### Stav

- **Verze**: 2.0 v přípravě. Něco by mělo být připraveno k objednání a otestování.

## Co je na tomto projektu tak zajímavé?

Měření výkonu, jelikož jsem chtěl vědět, kolik energie spotřebovávám. Proto jsem se rozhodl použít ACS722 a dělič napětí. Ale nikde jsem neviděl podobný projekt, který by toto měření obsahoval.

## Funkce

- ESP32-C3-WROOM-02
- Relé na desce pro co nejmenší stand by proud
- Integrovaná 10A pojistka pro ochranu LED pásků
- Měření výkonu pomocí WLED usermod (ACS722, dělič napětí)
- Vstup pro externí tlačítko
- Snímač teploty
- IR senzor

<details>
    <summary>Zobrazit více</summary>
    <ul>
        <li>Snadno použitelné šroubové svorky (výchozí)</li>
        <li>Kompatibilní s konektorem PhoenixContact PCB konektorem</li>
        <li>Ochrana ESP (PTC resetovatelná pojistka, ESD ochrana, diody)</li>
        <li>Přepěťová ochrana pro 5 a 3,3 V.</li>
        <li>Zaváděcí tlačítko lze použít jako tlačítko ve WLED</li>
        <li>Buck konvertor, který je napájen z Vin</li>
        <li>Nepoužívané GPIO je vyčleněno na desku</li>
        <li>Konektor USB-C</li>
        <li>5V logický výstup</li>
    </ul>
</details>

## Proč jsem se rozhodl tento projekt realizovat?

Protože jsem chtěl mít něco, co by bylo moje. Něco, co bych mohl vylepšovat a měnit podle svých potřeb. A hlavně jsem chtěl kontribuovat do open-source komunity. A také protože většinou nedělám projekty tak pořádně jako tento, proto jsem se rozhodl tento projekt realizovat stejně jako tuto doufám že dobrou dokumentaci. A tento projekt má několik důvodů, proč jsem se rozhodl ho realizovat. jako například:

- **Měření výkonu**: Chtěl jsem vědět, kolik energie spotřebovávám.
- **Relé**: Pro odpojení LED pásků.
- **Nízká spotřeba**: Aby LED si nebraly moc energie ve stand by.
- **Snadná integrace**: Aby bylo možné snadno integrovat do různých instalací.
- **Učit se**: Získat zkušenosti s novými technologiemi.
- **Sdílet**: Přispívat open-source komunitě.
- **Vytvořit něco pěkného**:  Mít funkční a vizuálně přitažlivé řešení.

## Vývoj

Na tomto projektu pracuji už docela dlouho.

Můj první prototyp nevypadal příliš dobře, ale fungoval skvěle. Přestože jsem zapomněl napájet integrovaný obvod SN74AHCT125, ale nic, co by se nedalo opravit pájecím můstkem.

V0.31 byla první verze, která měla všechny funkce, které jsem chtěl. Ale měla několik chyb.

V1.0 byla první verze, která byla plně funkční a měla všechny funkce, které jsem chtěl.

- A myslel jsem si že už je hotovo. Ale našlo se pár chyb třeba např: Komponenty na obou stranách což mělo za následek horší montáž, směšovač napěti z USB a Měniče řešený diodamy nebyl ideální.

v2.0 byla verze, která měla všechny chyby opraveny a byla plně funkční. Která je stále ve vývoji. Ale vypadá to že už je hotovo. Ale nikdy nevíte, co se může stát. 😅

## Dokumentace

Skvělé video pro začátečníky najdete zde [YouTube - en](https://www.youtube.com/watch?v=FvPuiWTE6ic).

Soubory KiCad jsou v adresáři [Board](../Board/).

Návod ke stavbě je k dispozici [zde](instrukce_ke_stavbě.md).  
Schéma a DPS je k dispozici v adresáři [Documentation](../Documentation/).  
A adresář [Builds](../Builds/) obsahuje binární soubor pro ESP32-C3.

Kryt pro desku je k dispozici v adresáři [Case](../Case/).
Fotografie hotového projektu jsou k dispozici v adresáři [Images](../Images/).

## Chtěl bych ho prodávat?

Ano, v blízké budoucnosti bych chtěl tento projekt prodávat jako hotový produkt. Aby každý mohl mít možnost tento ovladač používat.  
Také proto abych mohl v budoucnu pokračovat v jeho vývoji a vytváření zajímavých věcí.

## Jaká je má motivace?

- Instalace LED pásků v roce 2021.
- Problémy s ESP32 (poškození napájení, špatná aktualizace).
- Snaha vytvořit robustní a uživatelsky přívětivé řešení.

<details>
<summary>více</summary>
V roce 2021 jsem poprvé nainstaloval adresovatelné LED pásky a byl jsem jimi ohromen. Při práci s holou deskou ESP32 jsem však narazil na několik problémů. První kontrolér vypustil „magický kouř“, když jsem omylem přivedl 12 V na jeden z pinů. Druhé ESP se pak poškodilo během pokusu o opravu aktualizace, zatímco bylo stále pod napětím. Tyto zkušenosti mě inspirovaly k zahájení tohoto projektu.
</details>

## Co jsem se naučil?

Naučil jsem se mnoho nových věcí, jako například:

- Jak navrhnout DPS

<details>
<summary>více</summary>

- Jak používat ACS722
- Jak používat dělič napětí
- Jak používat IR senzor
- Jak používat teplotní senzor
- Jak používat relé
- Jak používat USB-C konektor
- Jak používat buck konvertor
- Jak používat ESP32-C3
- Jak používat WLED
- Jak používat PlatformIO
- Jak používat ESP-IDF
- Jak používat ESP32-C3
- Takže jsem se naučil mnoho nových věcí. aka skoro **všechno** s čím jsem pracoval.
- A to nejlepší je, že jsem se naučil, jak všechno toto spojit dohromady a taky že mně to baví. 😀

</details>

## Jaké je vlastně použití?

- **Ovládání adresovatelných LED**: Umožňuje přesné řízení jednotlivých LED diod.
- **LED light show**: Ideální pro vytváření světelných show a efektů.
- **Vánoční světýlka**: Perfektní pro dekoraci během svátků.
- **Snadná integrace do různých projektů**: Lze snadno začlenit do různých DIY projektů.
- **Smart home**: Vhodné pro chytré domácnosti a automatizaci osvětlení.

## Software

Používám projekt `WLED`, který je velmi jednoduchý na použití a má mnoho funkcí. Můžete si stáhnout binární soubor [zde](Builds). Nebo se podívat na [GitHub PR #4108](https://github.com/Aircoookie/WLED/pull/4108). Kde je přidán můj usermod. Předem se omluvám za jakékoliv chyby, které by se mohly vyskytnout. Jsem rád za každou zpětnou vazbu. Také nejsem skušený s gitem, takže se omlouvám za jakékoliv chyby v PR.

## Závěr

Tento projekt byl pro mě výzvou i příležitostí posunout své znalosti a schopnosti na novou úroveň. Naučil jsem se mnoho nových technologií a postupů, které jsem dříve neznal, a spojil je do funkčního řešení, na které jsem hrdý. Proces navrhování, iterací a řešení problémů mě utvrdil v tom, že otevřený přístup k technologiím a sdílení znalostí má obrovský potenciál.

Doufám, že tento projekt inspiruje další tvůrce a pomůže jim ušetřit čas či energie při realizaci vlastních nápadů. Budu rád za jakoukoli zpětnou vazbu, podněty na zlepšení či podporu, která mi umožní pokračovat v rozvoji tohoto projektu.

Děkuji za váš zájem a těším se na to, co budoucnost přinese!

### Proč to dělám?

Já vlastně ani nevím. Prostě jsem měl nějak chuť a prostředky díky podpoře své rodiny! A nakonec z toho vznikl tento open-source projekt, ale nesdílet by byla škoda.

## Kontribuce

Pokud máte nějaké nápady na vylepšení, nebo jste našli chybu, neváhejte a vytvořte pull request nebo issue. Rád se na ně podívám. Každá pomoc je vítána. :)  
Pokud by se někdo chtěl podílet na vývoji, budu rád za jakoukoliv pomoc. 😊  
A pokud někdo by rád mně chtěl finančně podpořit na další vývoj né jenom tohoto projektu, budu rád za jakoukoliv pomoc. 😊

## Licence

Projekt je aktuálně licencován pod CC BY-NC-SA 4.0, což znamená, že je možné jej sdílet a upravovat, avšak ne ke komerčním účelům. V budoucnu plánuji přechod na otevřenější licenci (CERN-OHL-S), jakmile se vrátí náklady spojené s vývojem.

**CC BY-NC-SA 4.0** [(CC)](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en) **→** **CERN-OHL-S** [(OSI Schválená OSHW licence)](https://opensource.org/license/cern-ohl-s)

Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

### Další prohlášení o vyloučení odpovědnosti (bez záruky)

Licencované dílo je poskytováno „tak, jak je“, bez jakýchkoli záruk, ať už výslovných nebo předpokládaných, mimo jiné včetně záruk prodejnosti, vhodnosti pro určitý účel nebo neporušování práv. Autor(ové) ani držitel(é) autorských práv v žádném případě neodpovídají za jakékoli nároky, škody nebo jiné závazky, ať už smluvní, deliktní nebo jiné, vyplývající z díla, z jeho užívání nebo jiného nakládání s ním nebo v souvislosti s ním.

#### Asistence AI

Umělou inteligenci jsem použil jako asistenta při překladu a opravách gramatiky. Děkuji za pochopení.
