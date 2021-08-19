---
title: Luotonhallinnan määritys
description: Tässä ohjeaiheessa kuvataan luottohallinnan edellyttämät määritykset.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4cfb747c9a510474d0ca27a595158cd6e6d24359a37f665f64b4c640536874aa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723940"
---
# <a name="credit-management-setup"></a>Luotonhallinnan määritys 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Luotonhallinnan työnkulut

Siirry kohtaan **Luotonvalvonta \> Määritys \> Luotonhallinnan työnkulut** määrittämään työnkulut, joita käytetään luottorajojen muutoksiin.

- Voit luoda työnkulun, jonka avulla voit hyväksyä luottorajojen muutoksia erittäin yhdellä hyväksynnällä.
- Voit lisätä työnkulun rivitasolla, jolloin luottorajan muutokset voidaan hyväksyä yksitellen.
- Voit luoda vapauttavat työnkulun, joka ohjaa pidot automaattisesti työnkulkuprosessiin.

## <a name="blocking-rules"></a>Estosäännöt

### <a name="ranking-payment-terms"></a>Maksuehtojen järjestäminen

Voit asettaa myyntitilauksen pitoon, jos sen maksuehdot eivät vastaa asiakkaan oletusarvoisia maksuehtoja. Joskus maksuehdot kuitenkin eroavat toisistaan, mutta ovat riittävän samankaltaiset sille, ettei tilausta haluta asettaa pitoon. Voit järjestää maksuehtoja siten, että joillakin niistä on sama järjestysnumero ja toisilla on korkeampi tai matalampi järjestysnumero.

Jos maksuehtojen järjestysnumerot ovat käytössä ja jos tilauksen maksuehdot ovat järjestyksessä asiakkaan oletusmaksuehtoja korkeammalla, myyntitilaukset siirretään pitoon.

Määrittääksesi maksuehtojen sijoituksen, valitse **Luotonhallinta ja perintä \> Asetukset \> Luotonhallinnan asetukset \>Maksuehtojen sijoitus**  

### <a name="ranking-settlement-discounts"></a>Tilitysalennusten järjestäminen

Voit asettaa myyntitilauksen pitoon, jos sen käteisalennus ei vastaa asiakkaan oletusarvoista käteisalennusta. Joskus käteisalennukset kuitenkin eroavat toisistaan, mutta ovat riittävän samankaltaiset sille, ettei tilausta haluta asettaa pitoon. Voit järjestää käteisalennuksia siten, että joillakin niistä on sama järjestysnumero ja toisilla on korkeampi tai matalampi järjestysnumero.

Jos käteisalennusten järjestysnumerot ovat käytössä ja jos tilauksen käteisalennus on järjestyksessä asiakkaan oletuskäteisalennusta korkeammalla, myyntitilaukset siirretään pitoon.

Määrittääksesi maksuehtojen sijoituksen, valitse **Luotonhallinta ja perintä \> Asetukset \> Luotonhallinnan asetukset \>Tilitysalennusten sijoitus**  

## <a name="reasons"></a>Syyt

Luotonhallinnassa käytetään monenlaisia syitä:

- Pidon syyt ilmaisevat, miksi myyntitilaus on asetettu pitoon.
- Vapautuksen syyt määritetään tilaukselle, kun se vapautetaan pidosta.
- Tilan syyt ilmaisevat, miksi asiakkaalle on määritetty tietty tilin tila.

Voit määrittää syitä **Luotto ja perintä** -sivulla (**Luotonhallinta \> Määritys \> Luotonhallinnan asetukset \> Luotonhallinnan syyt**).

1. Valitse **Syyn tyyppi** -kentässä syyn tyyppi: **Pito**, **Vapautus** tai **Tila**.
2. Syötä **Syy**-kenttään syyn nimi.
3. Anna **Kuvaus**-kentässä syykoodin kuvaus.

## <a name="credit-management-groups"></a>Luotonhallinnan ryhmät

Luotonhallintaryhmiä käytetään sellaisten asiakkaiden tai asiakasryhmien tunnistamineen, joilla on samat luotonhallinnan ominaisuudet. Luotonhallintaryhmien avulla voidaan esimerkiksi määrittää asiakkaiden estävät ja poissulkevat luotonhallintasäännöt.

Voit luoda luotonhallintaryhmiä **Luotonhallintaryhmät**-sivulla (**Luotto ja perintä \> Määritys> Luotohallinnan määritys \> Luotonhallinnan ryhmät**).

1. Valitse **Uusi** luodaksesi rivin.
2. Syötä ryhmälle tunnus. Tunnuksessa voi olla jopa 10 merkkiä.
3. Syötä ryhmälle nimi **Kuvaus**-kenttään. Nimessä voi olla jopa 60 merkkiä.

Luotonhallintaryhmä osoitetaan asiakkaalle **Luotonvalvonta**-pikavälilehdessä sivulla **Kaikki asiakkaat** (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**).

## <a name="account-statuses"></a>Tilin tilat

Voit luoda tilitiloja asiakastilin luottokelpoisuuden tunnistamista varten. Voit määrittää tilan ja sen vaikutuksen laskutuksen ja toimituksen pidossa oleviin prosesseihin. Tilitiloja voi käyttää myös asiakkaan esto ääntöjen määrittämiseen.

Voit luoda tilitiloja **Tilitilat**-sivulla (**Luotto ja perintä \> Määritys> Luotonhallinnan määritys \> Tilitilat**).

1. Lisää tilitila ja anna sille kuvaus, joka edustaa asiakkaan luottokelpoisuutta. Käytä esimerkiksi tilaa **Normaali** ilmaisemaan, että asiakkaan kelpoisuus on hyvä ja että avoimiin tilauksiin sovelletaan tavanomaista luotonhallintakäsittelyä.
2. Valitse kentissä **Laskutus** ja **Toimitus pidossa** pidon tyyppi, joka toteutetaan niiden asiakkaiden osalta, joilla on tämä tilitila. Voit asettaa kaiken käsittelyn pitoon, asettaa pitoon vain laskujen käsittelyn tai olla asettamatta pitoon mitään käsittelyä, kun luottorajasääntöjä sovelletaan.

## <a name="scoring-groups"></a>Pisteytysryhmät

Voit määrittää pisteytysryhmiä määrittämään riskitekijöitä sekä kriteerejä, joiden perusteella niitä mitataan. Kun asiakasta koskevia tietoja käytetään pisteytysryhmässä, kullekin riskitekijälle lasketaan pistemäärä, jonka perusteella asiakas asetetaan riskiryhmään. Riskiryhmää voidaan käyttää luottokelpoisuuden tunnistamiseen ja automaattisten luottorajojen laskemiseen.

Vuot luoda pisteytysryhmiä **Pisteytysryhmät**-sivulla (**Luotto ja perintä \> Määritys \> Luotonhallinnan määritys \> Riski \> Pisteytysryhmät**).

1. Luo pisteytysryhmä ja anna sille nimi.
2. Anna kuvaus tarkempia pisteytysryhmän tietoja varten.
3. Valitse ryhmätyyppi. Esimääritettyjä tyyppejä on kahdeksan. Voit myös määrittää paremmin organisaatiollesi sopivan ryhmätyypin valitsemalla **Käyttäjän määrittämä**.
4. Valitse pistetyyppi määrittääksesi, miten pisteytysryhmä laskee riskipisteet. Käytettävissä ovat seuraavat asetukset:

    - **Alue** – Tämän vaihtoehdon avulla voit määrittää arvoalueen, jota käytetään pistemäärän laskemiseen.
    - **Käyttäjän määrittämä** – Tämän vaihtoehdon avulla voit määrittää manuaalisesti arvoluettelon, jota käytetään pistemäärän laskemiseen.

5. Jos valitsit pistetyypiksi **Alue**, lisää rivejä arvoalueen ja sitä vastaavien pisteiden määrittämiseksi.

    1. Määritä **Arvosta**-kentässä alueen alhaisin arvo.
    2. Määritä **Arvoon**-kentässä alueen korkein arvo.
    3. Syötä **Pistemäärä**-kenttään se pistemäärä, joka osoitetaan, kun annettu arvo on alueella Arvosta–Arvoon.

    Jos valitsit pistetyypiksi **Käyttäjän määrittämä**, lisää rivejä arvoalueen ja käyttäjän määrittämien pisteiden määrittämiseksi.

    1. Syötä **Arvo**-kenttään se käyttäjän määrittämä arvo, joka pitäisi saada asiakastiedoista.
    2. Syötä **Pistemäärä**-kenttään se pistemäärä, joka osoitetaan, kun annettu arvo on alueella Arvosta–Arvoon.

## <a name="risk-classification"></a>Riskiluokittelu

Voit määrittää riskinarviointeja, jotka voidaan osoittaa asiakkaille niiden riskipisteiden perusteella. Riskipisteet lasketaan vertaamalla asiakkaan tietoja kuhunkin pisteytysryhmään. Tulokset lasketaan yhteen ja kokonaispistemäärää verrataan riskiryhmän määrityksiin, jotta asiakkaan edustama riskiryhmä voidaan tunnistaa. Riskiryhmän pistemäärää käytetään sitten luotonhallinnan esto- ja poissulkemissääntöjen määrittämiseen asiakkaalle.

Voit määrittää riskiryhmiä **Riskinarvioinnit**-sivulla (**Luotto ja perintä \> Määritys \> Luotonhallinnan määritys \> Luotto \> Riskinarvioinnit**).

1. Syötä riskiryhmän tunnus.
2. Anna kuvaus tarkempia riskiryhmän tietoja varten.
3. Määritä pistealue, jota käytetään sen selvittämiseen, mitkä asiakkaat kuuluvat riskiryhmään.
4. Valitse riskiryhmän ilmaisin valitaksesi symbolin, joka edustaa riskiryhmää.

## <a name="guaranteeinsurance-types"></a>Takaus-/vakuutustyypit

Voit määrittää takaus-/vakuutustyyppejä **Takaus-/vakuutustyypit**-sivulla (**Luotto ja perintä \> Määritys \> Luotonhallinnan määritys \> Vakuutukset ja takaukset \> Vakuutus ja takaustyypit**).

1. Määritä takaus- tai vakuutustyyppi, joka ilmaisee takaajan tai vakuutuksenvälittäjän nimen.
2. Anna takaajalle/vakuutuksenvälittäjälle kuvaus.

## <a name="coverage-types"></a>Kattavuustyypit

Kattavuustyyppejä voidaan käyttää vakuutuskäytäntöjen tarkempaan luokitteluun. Niitä ei voi käyttää takuiden yhteydessä.

Voit lisätä kattavuustyyppejä **Kattavuustyypit**-sivulla (**Luotto ja perintä \> Määritys \> Luotonhallinnan määritys \> Vakuutukset ja takuut määritys \> Kattavuuslajit**).

1. Anna kattavuustyyppi sen kattavuustyypin määrittämiseksi, joka lisätään vakuutuksena tai takuuna.
2. Anna kattavuustyypille kuvaus.

## <a name="automatic-credit-limits"></a>Automaattiset luottorajat

Voit luoda automaattisten luottorajojen kriteerejä **Automaattiset luottorajat** -sivulla (**Luotto ja perintä \> Määritys \> Luotonhallinnan määritys \> Riski \> Automaattiset luottorajat**).

1. Valitse riskiryhmä, jolle automaattinen luottoraja määritetään.
2. Valitse automaattisen luottorajan valuutta. Voit luoda useita automaattisia luottorajoja eri valuutoissa samalle riskiryhmälle.
3. Syötä se tuottosumma, joka edustaa suurinta yrityksen tuottoa, jota tässä automaattisessa luottorajassa voi käyttää. Kun luottorajoja luodaan, tuottosummaa verrataan tuottoarvoon **Taloushallinto** -sivulla (**Myyntireskontra \> Kaikki asiakkaat \> Valitse asiakas \> Yleistä \> Tilastot \> Talous**). Järjestelmä käyttää **Yleiskatsaus**-osan viimeisintä arvoa.

Seuraavien vaiheiden avulla voit lisätä valittujen kriteerien perusteella luotavaa luottorajaa edustavia rivejä.

1. Valitse pisteytysryhmä, joka määrittää luottorajan laskemisessa käytettävät asiakastiedot.
2. Valitse vertailuoperaattori, joka määrittää, miten pisteytysryhmän tiedot arvioidaan.
3. Määritä arvo, jota verrataan pisteytysryhmälle määritettyyn arvoon.
4. Määritä luottoraja, joka määritetään, jos asiakastiedot vastaavat pisteytysryhmälle määritettyä arvoa. Voit esimerkiksi luoda automaattisen luottorajan **Alahainen pistemäärä** -ryhmälle. Jos toiminta-aika on yksi pisteytysryhmistä, voit määrittää yhden rivin, joka määrittää luottorajaksi 100 000, jos asiakas on toiminut viisi vuotta ja toisen rivin, joka määrittää luottorajaksi 200 000, jos asiakas on toiminut 10 vuoden ajan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]