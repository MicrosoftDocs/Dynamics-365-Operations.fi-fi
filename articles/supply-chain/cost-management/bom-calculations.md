---
title: BOM-laskelmat
description: Kustannusten koontilaskelmia ja myyntihintalaskelmia kutsutaan tuoterakennelaskelmiksi, koska ne käynnistetään Laskelmat-sivulta. Tässä aiheessa on tietoja BOM-laskelmista.
author: AndersGirke
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, ProdSetupCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 2a3939d092bcba00aa9dc63c0fe7546beed2041d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575942"
---
# <a name="bom-calculations"></a>BOM-laskelmat

[!include [banner](../includes/banner.md)]

Kustannusten koontilaskelmia ja myyntihintalaskelmia kutsutaan tuoterakennelaskelmiksi, koska ne käynnistetään Laskelmat-sivulta. Tässä aiheessa on tietoja BOM-laskelmista.

Kustannusten koontilaskelmia ja myyntihintalaskelmia kutsutaan tuoterakennelaskelmiksi, koska ne käynnistetään **Laskelmat**-sivulta. **Laskelmat** -sivulla voit suorittaa seuraavat tehtävät:

-   laskea valmistetun nimikkeen kustannukset sekä muodostaa siihen liittyvän nimikkeen kustannustietue kustannuslaskelmaversioon.
-   laskea valmistetun nimikkeen myyntihinta ja muodostaa siihen liittyvä nimikkeen myyntihintatietue kustannuslaskelmaversioon.

**Laskelmat**-sivun käyttö määräytyy osaltaan sen mukaan, kuinka tuoterakennelaskelmat käynnistetään **Laskelmat**-sivun käyttämiseen vaikuttaa myös se, käytetäänkö tuoterakennelaskelmissa standardikustannusten vai suunniteltuja kustannusten kustannuslaskelmaversiota. Muita vaikuttavia tekijöitä ovat erinäiset käytännöt, jotka on määritetty tuoterakennelaskelmissa käytettävässä kustannuslaskelmaversiossa. **Huomautus:** erästä muunnelmaa **Laskelmat**-sivusta käytetään myyntitilauksen, myyntitarjouksen tai myyntitarjousrivin nimikkeen yhteydessä. Nämä laskelmat ovat tilauskohtaisia tuoterakennelaskelmia. Tilauskohtainen tuoterakennelaskenta ei luo kustannuslaskelmaversioon nimikkeen kustannustietuetta. Sen sijaan se luo laskelmatietueen, joka näkyy **Tuoterakenteen laskentatiedot** -sivulla. Laskelmatietueessa ovat mukana lasketut kustannukset ja laskettu myyntihinta. **Laskelmat**-sivun voi avata yksittäiselle valmistetulle nimikkeelle tai kustannuslaskentaversiolle:

-   Käynnistä tuoterakennelaskelmat **Nimikkeen hinta** -lomakkeesta, kun haluat laskea yksittäisen valmistetun nimikkeen kustannukset. **Laskelmat**-sivu perii nimikkeen tunnisteen. Kustannuslaskentaversio, tuoterakenteen versio, reititysversio, laskentamäärä, laskentapäivämäärä ja sijainti on määritettävä.
    -   Tuoterakenneversiossa ja reititysversiossa näkyy ensin nimikkeen, toimipaikan, päivämäärän ja laskelman määrän aktiiviset versiot. Oletusasetuksen voi kuitenkin ohittaa hyväksytyillä versioilla.
    -   Laskelman määrä asetetaan oletuksena nimikkeen vakiotilausmääräksi. Käyttäjä voi kuitenkin ohittaa oletusarvon.
    -   Kustannuslaskelmaversio voi määrätä laskentapäivän tai toimipaikan, tai käyttäjän määrittämät arvot voivat olla sallittuja, kun kustannuslaskelmaversio ei määrää päivämäärää tai toimipaikkaa. Tuleva laskentapäivä määrittää odottavien kustannustietueiden käyttämisen. Tuoterakennelaskelmissa käytetään odottavaa kustannustietuetta, jonka lähin aloituspäivämäärä on laskentapäivä tai jokin laskentapäivää edeltävä päivä.
-   Käynnistä tuoterakennelaskelmat **Kustannuslaskelmaversion määritys** -lomakkeesta (tai **Kustannuslaskelmaversion ylläpito** -lomakkeesta), kun haluat laskea kaikkien valmistettujen nimikkeiden kustannukset tai vain valittujen nimikkeiden kustannukset tai päivittää nimikkeet käyttökohteen perusteella. **Laskelmat**-sivu perii kustannuslaskentaversion.
    -   Laskelmien lähtökohtana on, että valmistetussa nimikkeessä (ja siihen liittyvässä toimipaikassa, päivämäärässä ja määrässä) käytetään aktiivista tuoterakenneversiota ja reititysversiota – paitsi jos valmistetulle komponentille on määritetty alituoterakenne tai alireititys.
    -   Laskelmien lähtökohtana on, että valmistetuille nimikkeille käytetään vakiotilausmääriä. Vakiotilausmäärä toimii perustana komponenttimäärien laskennassa, oikeiden tuoterakenne- ja reititysversioiden selvittämisessä (kun käytössä on määrästä riippuvainen tuoterakenne ja reititys) ja vakiokustannusten kuoletuksessa. Lähtökohta ei kuitenkaan päde, kun valmistetun komponentin tuoterakennerivin tyyppi on **Tuotanto** tai **Toimittaja**, tai kun tilausta varten tehtyä hajotustilaa käytetään tuoterakennelaskelmissa, koska määrät riippuvat määritetystä laskelman määrästä.
    -   Kustannuslaskelmaversio voi määrätä laskentapäivän tai toimipaikan, tai käyttäjän määrittämät arvot voivat olla sallittuja, kun kustannuslaskelmaversio ei määrää päivämäärää tai toimipaikkaa.

Muut variaatiot tuoterakennelaskelmissa kuvastavat kustannuslaskennan tyyppiä ja kustannuslaskentaversion rajoituksia:

-   Standardikustannuksia käyttävät tuoterakennelaskelmat on rajoitettava kustannuslaskelmaversion käytännöillä; rajoitukset varmistavat, että kustannuslaskennan vakiokäytäntöjä käytetään. Kustannuslaskennan vakioperiaatteet edellyttävät, että rajoituksia vakiokustannusten käytöstä ostetuille nimikkeille, yksitasoisen hajotustilan käytöstä ja muiden kulujen sisällyttämisestä nimikekustannuksiin valvotaan.
-   Tuoterakennelaskelmissa, joissa käytetään suunniteltuja kustannuksia ei tarvitse noudattaa standardinmukaisia kustannuslaskentaperiaatteita. Näissä tuoterakennelaskelmissa voi käyttää eri hajotustiloja ja vaihtoehtoisia ostettujen nimikkeiden kustannustietojen lähteitä sekä valinnaista kustannuslaskelmaversion rajoitusten valvontaa.

### <a name="bom-calculations-that-use-standard-costs"></a>Standardikustannuksia käyttävät tuoterakennelaskelmat

Kustannuslaskelmaversion (standardikustannuksia koskevat) käytännöt voivat määrittää, että viittä tuoterakenteen laskentakäytäntöä on pakko käyttää. Kustannuslaskelmaversion **Tallennusrajoitus**-vaihtoehto määrää yhden näistä käytännöistä, jossa muutu kulut täytyy sisällyttää yksikköhintaan. Ostettujen nimikkeiden muut kulut voi lisätä manuaalisesti, mutta valmistettujen nimikkeiden muut kulut ovat pysyvien kustannusten lasketun kuoletuksen mukaisia. Kustannuslaskelmaversion **laskentarajoitusasetus** määrää neljä muuta tuoterakenteen laskentakäytäntöä:

-   Ostettujen nimikkeiden kustannusten osuuksien lähteen täytyy perustua standardikustannuksiin. Toisin sanoen, tuoterakennelaskelmissa täytyy käyttää nimikkeen kustannustietueita, jotka sisältyvät määritettyyn kustannuslaskelmaversioon tai standardikustannuksia sisältävään periaatteeseen.
-   Hajotustilan täytyy olla yksitasoinen, jotta standardikustannukset lasketaan varmasti oikein ja yhdenmukaisesti.
-   Voiton asetuksen täytyy olla määrätty, jotta nimikkeen myyntihinnan laskennassa päästään yhdenmukaisiin tuloksiin. Kustannuslaskelmaversion täytyy sallia myyntihintojen sisältö, jotta voiton asetusta voi käyttää ja jotta nimikkeen myyntihintatietueet voidaan muodostaa.
-   Varmistusperiaatteen täytyy olla määrätty, jolloin periaate voi olla **Ei mitään**, **Aktiivinen** (aktiivisille kustannusten tietueille) tai **Kustannuslaskelmaversio** (määritetylle kustannuslaskelmaversiolle).

### <a name="bom-calculations-that-use-planned-costs"></a>Suunniteltuja kustannuksia käyttävät tuoterakennelaskelmat

Kustannuslaskelmaversion (suunniteltuja kustannuksia koskevat) käytännöt voivat vapaaehtoisesti määrittää, että viittä tuoterakenteen laskentakäytäntöä on pakko käyttää. Käytännöt voivat myös käyttää yksinkertaisesti oletusarvoja. Kustannuslaskelmaversion **tallennusrajoitusasetus** määrittää, onko muita kuluja koskevaa tuoterakennelaskelman käytäntöä pakko käyttää vai toimiiko se oletusarvona. Muut kulut voi lisätä yksikköhintaan, mutta se ei ole pakollista. Kustannuslaskelmaversion **laskentarajoituksen** asetus määrittää, onko neljää muuta tuoterakennelaskelman käytäntöä pakko käyttää vai toimivatko ne ainoastaan oletusarvoina:

-   Ostetun nimikkeen kustannusten osuuksien lähde voi olla kustannuslaskelmaversion nimikkeen kustannustietue, tai nimikkeeseen määritetty tuoterakenteen laskelmaryhmä voi määrittää lähteen. Tuoterakenteen laskelmaryhmä voi esimerkiksi määrittää, että ostohinnan kauppasopimukset ovat kustannusten osuuksien tietojen lähde.
-   Hajotustila voi olla yksitasoinen, monitasoinen tai tilannekohtainen, tai se voi perustua tuoterakenteen rivin nimikkeeseen. Tuoterakenteen rivityypin hajotustila toisintaa kustannuslaskennan logiikan tuotantotilausten arvioita varten.
-   Voiton asetus voi olla määrätty tai oletusarvo. Kustannuslaskelmaversion täytyy sallia myyntihintojen sisältö, jotta voiton asetusta voi käyttää ja jotta nimikkeen myyntihintatietueet voidaan muodostaa.
-   Varmistusperiaate voi olla määrätty tai oletusarvo. Varmistusperiaate voi olla **Ei mitään**, **Aktiivinen** (aktiivisille kustannusten tietueille) tai **Kustannuslaskelmaversio** (määritetylle kustannuslaskelmaversiolle).

Tuoterakennelaskelmat muodostavat varoitussanomia ja muun tyyppisiä sanomia. Useat tuoterakenteen laskelmakäytännöt määrittävät sanomien tyypin. Varoitusehdot on määritetty nimikkeille asetetussa tuoterakennelaskelmaryhmässä. Voit kuitenkin korvata nämä sovellettavat varoitusehdot aloittaessasi tuoterakennelaskennan. Kun varmistusperiaatetta käytetään, varmistustiedot kannattaa usein esittää tietosanomana. Kun sellaisten nimikkeiden laskettuja kustannuksia yritetään päivittää, joilla on puuttuvia kustannustietueita, on hyödyllistä, jos nimikkeet, joita ei voitu päivittää voi tunnistaa tietosanomasta.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Varmistusmenettelyä käyttävät tuoterakennelaskelmat
Seuraavassa on kuvattu varmistusmenettelyn kaksi käyttötilannetta:

-   **Kahden version menetelmä standardikustannusten päivityksissä** − Kustannuslaskelmaversio voi sisältää lisäyksiä standardikustannuksiin, kuten odottavia kustannustietueita, jotka edustavat uusia nimikkeitä tai kustannusmuutoksia. Tässä tapauksessa varmistusmenettelyn avulla voi määrittää muissa kustannuslaskelmaversioissa olevien aktiivisten standardikustannusten käytön.
-   **Kustannusmuutosten vaikutusten simulointi suunniteltujen kustannusten avulla** - Suunniteltujen kustannusten kustannuslaskelmaversio voi sisältää simulointiin tarkoitettuja lisäyksiä. Tämä kustannuslaskelmaversio sisältää odottavia kustannustietueita, jotka edustavat simuloituja kustannusmuutoksia nimikkeisiin, kustannusluokkiin ja epäsuoran kustannuksen laskentakaavoihin. Tässä tapauksessa varmistusmenettelyn avulla voi määrittää muissa kustannuslaskelmaversioissa olevien aktiivisten standardikustannusten käytön.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Ehdotetun myyntihinnan tuoterakennelaskelma
Hinta+hinnankorotus-mallia käytettäessä nimikkeen laskettu myyntihinta vastaa tuoterakennelaskelmalle määritettyä tuottovaatimusprosenttien joukkoa sekä kustannuksia, jotka liittyvät sen komponenttinimikkeisiin, reitityksen työvaiheisiin ja sovellettavissa oleviin valmistuksen yleiskustannuksiin. Hinnankorotus vastaa kustannusryhmille määritettyjä tuottovaatimusprosentteja ja nimikkeille määritettyjä kustannusryhmiä, reitityksen työvaiheiden kustannusluokkia sekä valmistuksen yleiskustannusten epäsuorien kustannusten laskentakaavoja. Tuottovaatimusprosenttien joukoille määritetään nimet **Vakio**, **Voitto 1**, **Voitto 2** ja **Voitto 3**. Esimerkiksi Voitto 1 -joukossa ostetulle materiaalille määritetylle kustannusryhmälle voidaan määrittää tuottovaatimusprosentti 50 ja reitityksen työvaiheiden kustannusluokille määritetylle kustannusryhmälle tuottovaatimusprosentti 80. Tuoterakennelaskelman konteksti määrittää, kuinka lasketun myyntihinnan tulokset käsitellään:

-   **Nimikkeen ja määritetyn kustannuslaskelmaversion tuoterakennelaskelma** − Tuoterakennelaskelma luo odottavan myyntihintatietueen kustannuslaskelmaversioon. Tämä myyntihintatietue toimii lähtökohtana, kun laskelman tietoja, esimerkiksi **Laske nimikekustannus** -sivua, tarkastellaan. Myyntihintatietue toimii pääasiassa viitetietoina, eikä myyntitilausten myyntihintaa lasketa sen perusteella.
-   **Tilauskohtainen tuoterakennelaskelma** − **Tuoterakennelaskelmasivun** variaatiota käytetään myyntitilausten, myyntitarjousten ja huoltotilausrivien nimikkeiden kontekstissa. Tilauskohtainen tuoterakennelaskenta ei luo kustannuslaskelmaversioon tietuetta. Sen sijaan se luo laskelmatietueen, joka näkyy **Tuoterakenteen laskemisen tulokset** -sivulla. Tämä laskelmatietue toimii lähtökohtana, kun laskelman tietoja, esimerkiksi **Laske nimikekustannus** -sivua, tarkastellaan. Valitun laskelmatietueen tiedot on mahdollista siirtää alkuperäiseen rivinimikkeeseen. Esimerkiksi lasketun myyntihinnan voi siirtää myyntitilausrivin nimikkeeseen.

## <a name="order-specific-bom-calculations"></a>Tilauskohtaiset tuoterakennelaskelmat
Tilauskohtainen tuoterakennelaskenta on valmistetun nimikkeen tuoterakennelaskennan muunnelma. Tilauskohtainen tuoterakennelaskenta tehdään myyntitilauksen, myyntitarjouksen tai huoltotilausrivin nimikkeen yhteydessä. Tilauskohtainen tuoterakennelaskelma luo laskelmatietueen, joka näytetään **Tuoterakenteen laskelman tulokset** -sivulla. Laskelmatietue sisältää lasketun painoarvon, aktiivisiin kustannustietueisiin perustuvan lasketun kustannuksen sekä lasketun myyntihinnan. Kukin tilauskohtainen reseptin laskenta luo **Reseptin laskennan tulokset** -sivulle laskelmatietueen, jolla on yksilöivä tunnusnumero. Laskelmatietueen tulokset voi valinnaisesti siirtää alkuperärivin nimikkeelle. Tilauskohtainen tuoterakennelaskenta eroaa valmistetun nimikkeen tuoterakennelaskennasta kahdella tavalla:

-   Tilauskohtainen tuoterakennelaskenta ei luo kustannuslaskelmaversioon nimikkeen kustannustietuetta. Tämä tarkoittaa, että tuoterakenteen laskentamenettelyt eivät koske nimikkeen kustannustietueen luomista tai kustannustietueen korvaamista.
-   Tilauskohtainen tuoterakennelaskenta käyttää aina komponenttien, kustannusluokkien ja epäsuoran kustannuksen laskentakaavojen aktiivisia kustannustietueita.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]