# Instrukce ke stavbě

Pro referenci spŕavných komponent použijte [ibom](/Documentation/ibom-TwinkleTron.html) nebo [BOM](/Documentation/TwinkleTron-BOM.xlsx).

1. Objednání desky a součástek s pomocí BOM a JLCPCB Pluginu.
2. Čekání až přijdou 
3. Vezme se DPS a vybere se metoda kterou se deska spájí

<details>
<summary>3.1. Pájení s pomocí pájky a cínu (nejlépe hrotové)</summary>

- 3.1.1. Vezme se správná součástka a připájí se.
</details>

<details>
<summary>3.2. SMT</summary>

- 3.2.1. Na desku kde není maska je třeba nanést tenkou vstvu pájecí pasty.
- 3.2.2. Poté se na desku položí správná součástka a pomocí pece se součástky připájí.
</details>

- *Dle mého názoru je nejlepší metoda pájení pomocí šablony a pájecí pece. Ale pokud nemáte přístup k peci, je možné použít i horký vzduch nebo pájku a cín.*

4. Poté se deska zkontroluje.
5. Pak se díky USB-C konektoru připojí do počítače.
6. Programování pomocí kompilovaného binárního souboru nebo PlatformIO. Pozor prvotní nahrání programu je nutno provést při držení tlačítka [boot]() při zapnutí.	

<details>
<summary>6.1. PlatformIO</summary>

Viz. [PlatformIO](https://www.youtube.com/watch?v=S82KWWgn1jc) tutoriál.

1. Nainstalujte si PlatformIO IDE.
2. Otevřete projekt v PlatformIO IDE.
3. Stiskněte tlačítko pro nahrání programu v počítači.
4. Nahrání programu.
</details>

<details>
<summary>6.2. Binární soubor - jednoduší</summary>

1. Stáhněte si předkompilovaný binární soubor.
2. Použijte nástroj jako je [ESP Web Tools](https://esp.huhn.me/) pro nahrání binárního souboru do ESP32.
3. Postupujte podle pokynů na obrazovce pro dokončení nahrávání.
</details>

7. Hotovo 🎉
