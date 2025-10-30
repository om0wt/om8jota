# Hra na agenta

Hrá na agenta je hrá pre 1-2 členné družstvá detí (skautov), tieto družstva sú nazvané **STANICE**, alebo "agenti" (volacie znaky: JOTA1, JOTA2...). STANICE prijímajú povely od **RIADIACEJ STANICE** (volací znak JOTA), a na základe jej povelov jej naspäť komunikujú svoje zistenia. Na konci hry každá STANICA odovzdá RIADIACEJ STANICI **PROTOKOL** s výsledkami svojich zistení. RIADIACA STANICA vyhodnoti protokoly všetkých staníc a oznámi výsledok hry. Jednotlivé stanice "agenti" tak majú spolu zložiť "kodovanu správu", ktorú zachráni svet a jej znenie sa dozvedia na konci hry.

Zmyslom celej hry je precvicit u deti/skautov slovenskú hláskovaciu abecedu používanú v radioamaterskom svete a naučiť ich komunikácii podľa všeobecnej schémy pre fonické radioamaterske spojenia.

## Priebeh hry

1. Na začiatku hry skauti vytvoria 1-2 clenne družstva. Každé družstvo dostane PMR446 vysielačku. Všetky vysielačky sú nastavené na rovnaký kanál. RIADIACA STANICA odovzdá každému družstvu tvrdú papierovú dosku s perom a PROTOKOLOM STANICE a oznámi všetkým druzstvam sifrovaci kľúč - dve písmena, pomocou ktorého budú ďalej desifrovat slova podľa pokynov na protokole.  

2. Jednotlivé družstvá sa rozídu do priestoru (napríklad na luke), tak aby sa navzájom nepočuli.

3. Riadiaca stanica spraví kontrolu spojenia s jednotlivými stanicami (x je poradové číslo stanice) podľa nasledujúcej schémy:

    ```
    JOTAx volá ťa JOTA
    JOTA tu JOTAx Na prijme
    JOTAx JOTA Ďakujem
    ```
4. Riadiaca stanica postupne nadväzuje spojenia s jednotlivými stanicami a odovzdáva im slova, medzi jednotlivými slovám počká chvíľu:

    ```
    JOTAx volá ťa JOTA
    JOTA JOTAx Počúvam
    JOTx JOTA Prvé slovo: Tomas Xaver Bozena Peter Adam, opakujem: Tomas Xaver Bozena Peter Adam. Máš zapísané?
    JOTA JOTAx Áno, mám všetko zapísané, môžeš pokračovať druhým slovom
    JOTAx JOTA Druhé slovo: Jozef Adam Norbert Karol Oto, opakujem: Jozef Adam Norbert Karol Oto. Máš zapísané?
    JOTA JOTAx Všetko prijaté, môžeš pokračovať na ďalšiu stanicu.
    ```

    Stanica JOTAx poskladá na základe hláskovacej abecedy z vyhláskovaných písmen slovo 1 a slovo 2 a zápise ho do protokolu. Potom začne spracovávať slová podľa pokynov v protokole - desifruje slovo 2 podľa kľúča. Riadiaca stanica pokračuje spojením s ďalšou JOTAx stanicou

5. Riadiaca stanica nechá čas všetkým staniciam čas na spracovanie úlohy (cca 10 minút od komunikácie s poslednou stanicou) a následne zavolá všeobecnú výzvu, na ktorú budú stanice JOTAx odpovedať statusom o pripravenosti:

    ```
    Výzva pre všetky stanice, tu JOTA: JOTA1 až JOTAn, oznámte svoju pripravenost odpovedať na úlohy!
    ```
    
    Jednotlivé stanice odpovedajú:

    ```
    JOTA JOTAx: Pripravená/Potrebujeme ešte čas
    ```
    
    V prípade, že niektoré stanice nebudú ešte pripravené, riadiaca stanica im nechá čas a neskôr zopakuje výzvu znova. Keď sú všetky JOTAx stanice pripravené, začne fáza odovzdavania riešení úloh

6. Riadiaca stanica postupne volá všetky stanice a žiada o vyhláskovanie dešifrovaného 1. slova. Výsledok skontroluje podľa protokolu riadiacej stanice, v riadku KONTROLA a označí zakrúžkovaním stanicu ak správne desifrovala slovo 2.

    ```
    JOTAx volá ťa JOTA Vyhlaskuj desifrovane 1. slovo
    JOTA JOTAx Slovo je: Cyril Adam Rudolf Norbert Ivan
    JOTAx JOTA Ďakujem, Sedem Tri.
    ```


## Ukončenie hry

Po odovzdaní všetkých dekodovaných slov stanicami sa všetky družstvá zídu pri Riadiacej stanici, ktorá vyhodnotí protokoly jednotlivých staníc a prejdú si spolu jednotlivé problemove momenty, s ktorými stanice mohli máť ťažkosti.

Nakoniec Riadiaca stanica oznámi všetkým staniciam spoločne dešifrovanú správu, ktorá pomohla zachrániť svet a rozdá družstvám prípadne odmeny.

## Priklady sprav:

```
1. CARNI	BOCAN	NOZKI	ZMOCI	HLAVU	VNORI	ZABKU	CHICI	DOBRE	CHUTI
2. DZIVA    LABUT   PLAVA   ZOBAK   VNARA   RYBKU   CHYTA
```

## Protokol stanice

Protokol stanice je formátu A4. V dolnej pravej časti je fixny kruh s malými pismenkami anglickej abecedy vo vonkajších poliach. Súčasťou protokolu je aj externý rotovaci klucovaci krúžok, ktorý sa vloží do vnútorného poľa fixneho kruhu a nastavi sa podľa zdeleneho kľúča. Písmena v tomto rotovacom kruhu sú veľké, oba kruhy predstavujú šifrovanie Albertiho šifrou. Okrem tohto protokol obsahuje polia pre jednotlivé slová popísané vyššie vo vysvetlení hry. 

Priklad protokolu stanice:

![Protokol stanice](./PROTOKOL_STANICA.png)

Tu je príklad protokolu aj s vnútorným dešifrovacím kolieskom nastaveným na kľúč **xA**

![Protokol s kolieskom](./PROTOKO_S_KOLIESKOM.png)

## Protokol riadiacej stanice.

Protokol riadiacej stanice obsahuje páry slov pre každú stanicu a v kontrolnom riadku je dešifrované 1. slovo na základe kľúča

Príklad protokolu riadiacej stanice:

![Protokol riadiacej stanice](./PROTOKOL_RIADIACEJ_STANICE.png)




