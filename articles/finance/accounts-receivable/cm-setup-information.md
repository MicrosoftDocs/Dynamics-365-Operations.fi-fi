---
title: Luotonhallinnan määritys
description: Tässä ohjeaiheessa kuvataan luottohallinnan edellyttämät määritykset.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c54c74af6f2c1be9aedfa792d0676d1165fb0ab8
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015209"
---
# <a name="credit-management-setup"></a>Luotonhallinnan määritys 

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="credit-management-workflows"></a>Luotonhallinnan työnkulut

Siirry kohtaan **Luotonvalvonta \> Määritys \> Luotonhallinnan työnkulut** määrittämään työnkulut, joita käytetään luottorajojen muutoksiin.

- Voit luoda työnkulun, jonka avulla voit hyväksyä luottorajojen muutoksia erittäin yhdellä hyväksynnällä.
- Voit lisätä työnkulun rivitasolla, jolloin luottorajan muutokset voidaan hyväksyä yksitellen.
- Voit luoda vapauttavat työnkulun, joka ohjaa pidot automaattisesti työnkulkuprosessiin.

## <a name="blocking-rules"></a>Estosäännöt

### <a name="ranking-payment-terms"></a>Maksuehtojen järjestäminen

Voit asettaa myyntitilauksen pitoon, jos sen maksuehdot eivät vastaa asiakkaan oletusarvoisia maksuehtoja. Joskus maksuehdot kuitenkin eroavat toisistaan, mutta ovat riittävän samankaltaiset sille, ettei tilausta haluta asettaa pitoon. Voit järjestää maksuehtoja siten, että joillakin niistä on sama järjestysnumero ja toisilla on korkeampi tai matalampi järjestysnumero.

Jos maksuehtojen järjestysnumerot ovat käytössä, myyntitilaukset siirretään pitoon, jos tilauksen maksuehdot ovat järjestyksessä asiakkaan oletusmaksuehtoja korkeammalla.

### <a name="ranking-settlement-discounts"></a>Tilitysalennusten järjestäminen

Voit asettaa myyntitilauksen pitoon, jos sen käteisalennus ei vastaa asiakkaan oletusarvoista käteisalennusta. Joskus käteisalennukset kuitenkin eroavat toisistaan, mutta ovat riittävän samankaltaiset sille, ettei tilausta haluta asettaa pitoon. Voit järjestää käteisalennuksia siten, että joillakin niistä on sama järjestysnumero ja toisilla on korkeampi tai matalampi järjestysnumero.

Jos käteisalennusten järjestysnumerot ovat käytössä, myyntitilaukset siirretään pitoon, jos tilauksen käteisalennus on järjestyksessä asiakkaan oletuskäteisalennusta korkeammalla.

## <a name="reasons"></a>Syyt

Luotonhallinnassa käytetään monenlaisia syitä:

- Pidon syyt ilmaisevat, miksi myyntitilaus on asetettu pitoon.
- Vapautuksen syyt määritetään tilaukselle, kun se vapautetaan pidosta.
- Tilan syyt ilmaisevat, miksi asiakkaalle on määritetty tietty tilin tila.

Voit määrittää syitä **Luotonhallinnan syyt** -sivulla (**Luotonhallinta \> Määritys \> Luotonhallinta \> Luotonhallinnan syyt**).

1. Valitse **Syyn tyyppi** -kentässä syyn tyyppi: **Pito**, **Vapautus** tai **Tila**.
2. Syötä **Syy**-kenttään syyn nimi.
3. Anna **Kuvaus**-kentässä syykoodin kuvaus.

## <a name="credit-management-groups"></a>Luotonhallinnan ryhmät

Luotonhallintaryhmiä käytetään sellaisten asiakkaiden tai asiakasryhmien tunnistamineen, joilla on samat luotonhallinnan ominaisuudet. Luotonhallintaryhmien avulla voidaan esimerkiksi määrittää asiakkaiden estävät ja poissulkevat luotonhallintasäännöt.

Voit luoda luotonhallintaryhmiä **Luotonhallintaryhmät**-sivulla (**Luotonhallinta \> Määritys> Ryhmien määritys \> Luotonhallinnan ryhmät**).

1. Valitse **Uusi** luodaksesi rivin.
2. Syötä ryhmälle tunnus. Tunnuksessa voi olla jopa 10 merkkiä.
3. Syötä ryhmälle nimi **Kuvaus**-kenttään. Nimessä voi olla jopa 60 merkkiä.

Luotonhallintaryhmä osoitetaan asiakkaalle **Luotonvalvonta**-pikavälilehdessä sivulla **Kaikki asiakkaat** (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**).

## <a name="account-statuses"></a>Tilin tilat

Voit luoda tilitiloja asiakastilin luottokelpoisuuden tunnistamista varten. Voit määrittää tilan ja sen vaikutuksen laskutuksen ja toimituksen pidossa oleviin prosesseihin. Tilitiloja voi käyttää myös asiakkaan esto ääntöjen määrittämiseen.

Voit luoda tilitiloja **Tilitilat**-sivulla (**Luotonhallinta \> Määritys> Ryhmien määritys \> Tilitilat**).

1. Lisää tilitila ja anna sille kuvaus, joka edustaa asiakkaan luottokelpoisuutta. Käytä esimerkiksi tilaa **Normaali** ilmaisemaan, että asiakkaan kelpoisuus on hyvä ja että avoimiin tilauksiin sovelletaan tavanomaista luotonhallintakäsittelyä.
2. Valitse kentissä **Laskutus** ja **Toimitus pidossa** pidon tyyppi, joka toteutetaan niiden asiakkaiden osalta, joilla on tämä tilitila. Voit asettaa kaiken käsittelyn pitoon, asettaa pitoon vain laskujen käsittelyn tai olla asettamatta pitoon mitään käsittelyä, kun luottorajasääntöjä sovelletaan.

## <a name="scoring-groups"></a>Pisteytysryhmät

Voit määrittää pisteytysryhmiä määrittämään riskitekijöitä sekä kriteerejä, joiden perusteella niitä mitataan. Kun asiakasta koskevia tietoja käytetään pisteytysryhmässä, kullekin riskitekijälle lasketaan pistemäärä, jonka perusteella asiakas asetetaan riskiryhmään. Riskiryhmää voidaan käyttää luottokelpoisuuden tunnistamiseen ja automaattisten luottorajojen laskemiseen.

Vuot luoda pisteytysryhmiä **Pisteytysryhmät** -sivulla (**Luotonhallinta \> Määritys \> Riskinmääritys \> Pisteytysryhmät**).

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

## <a name="risk-assessments"></a>Riskinarvioinnit

Voit määrittää riskinarviointeja, jotka voidaan osoittaa asiakkaille niiden riskipisteiden perusteella. Riskipisteet lasketaan vertaamalla asiakkaan tietoja kuhunkin pisteytysryhmään. Tulokset lasketaan yhteen ja kokonaispistemäärää verrataan riskiryhmän määrityksiin, jotta asiakkaan edustama riskiryhmä voidaan tunnistaa. Riskiryhmän pistemäärää käytetään sitten luotonhallinnan esto- ja poissulkemissääntöjen määrittämiseen asiakkaalle.

Voit määrittää riskiryhmiä **Riskinarvioinnit** -sivulla (**Luotonhallinta \> Määritys \> Riskinmääritys \> Riskinarvioinnit**).

1. Syötä riskiryhmän tunnus.
2. Anna kuvaus tarkempia riskiryhmän tietoja varten.
3. Määritä pistealue, jota käytetään sen selvittämiseen, mitkä asiakkaat kuuluvat riskiryhmään.
4. Valitse riskiryhmän ilmaisin valitaksesi symbolin, joka edustaa riskiryhmää.

## <a name="guaranteeinsurance-types"></a>Takaus-/vakuutustyypit

Voit määrittää takaus-/vakuutustyyppejä **Takaus-/vakuutustyypit**-sivulla (**Luotonhallinta \> Määritys \> Takausten/vakuutuksien määritys \> Takaus-/vakuutustyypit**).

1. Määritä takaus- tai vakuutustyyppi, joka ilmaisee takaajan tai vakuutuksenvälittäjän nimen.
2. Anna takaajalle/vakuutuksenvälittäjälle kuvaus.

## <a name="coverage-types"></a>Kattavuustyypit

Kattavuustyyppejä voidaan käyttää vakuutuskäytäntöjen tarkempaan luokitteluun. Niitä ei voi käyttää takuiden yhteydessä.

Voit lisätä kattavuustyyppejä **Kattavuustyypit**-sivulla (**Luotonhallinta \> Määritys \> Takuun/vakuutuksen määritys \> Coverage types**).

1. Anna kattavuustyyppi sen kattavuustyypin määrittämiseksi, joka lisätään vakuutuksena tai takuuna.
2. Anna kattavuustyypille kuvaus.

## <a name="automatic-credit-limits"></a>Automaattiset luottorajat

Voit luoda automaattisten luottorajojen kriteerejä **Automaattiset luottorajat** -sivulla (**Luotonhallinta \> Määritys \> Riskinmääritys \> Automaattiset luottorajat**).

1. Valitse riskiryhmä, jolle automaattinen luottoraja määritetään.
2. Valitse automaattisen luottorajan valuutta. Voit luoda useita automaattisia luottorajoja eri valuutoissa samalle riskiryhmälle.
3. Syötä se tuottosumma, joka edustaa suurinta yrityksen tuottoa, jota tässä automaattisessa luottorajassa voi käyttää. Kun luottorajoja luodaan, tuottosummaa verrataan tuottoarvoon **Taloushallinto** -sivulla (**Myyntireskontra \> Kaikki asiakkaat \> Valitse asiakas \> Yleistä \> Tilastot \> Talous**). Järjestelmä käyttää **Yleiskatsaus**-osan viimeisintä arvoa.

Seuraavien vaiheiden avulla voit lisätä valittujen kriteerien perusteella luotavaa luottorajaa edustavia rivejä.

1. Valitse pisteytysryhmä, joka määrittää luottorajan laskemisessa käytettävät asiakastiedot.
2. Valitse vertailuoperaattori, joka määrittää, miten pisteytysryhmän tiedot arvioidaan.
3. Määritä arvo, jota verrataan pisteytysryhmälle määritettyyn arvoon.
4. Määritä luottoraja, joka määritetään, jos asiakastiedot vastaavat pisteytysryhmälle määritettyä arvoa. Voit esimerkiksi luoda automaattisen luottorajan **Alahainen pistemäärä** -ryhmälle. Jos toiminta-aika on yksi pisteytysryhmistä, voit määrittää yhden rivin, joka määrittää luottorajaksi 100 000, jos asiakas on toiminut viisi vuotta ja toisen rivin, joka määrittää luottorajaksi 200 000, jos asiakas on toiminut 10 vuoden ajan.
