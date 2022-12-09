---
title: Keskitettyjen maksujen tilityksen yleiskatsaus
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Financen keskitettyjen maksujen tilitystä.
author: angelad116
ms.date: 11/22/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "222414"
- intro-internal
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42c359edbe49af151ac76c9873c0d429bbe1ca12
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804223"
---
# <a name="settlement-overview-for-centralized-payments"></a>Keskitettyjen maksujen tilityksen yleiskatsaus

[!include [banner](../includes/banner.md)]

Organisaatiot, joihin kuuluu useita yrityksiä, voivat luoda ja hallita maksuja käsittelemällä kaikki yhdessä yrityksessä. Tällöin samaa tapahtumaa ei tarvitse syöttää erikseen useassa yrityksessä. Aikaa myös säästyy, kun keskitettyjen maksujen maksuehdotusprosessi, selvitysprosessi, avointen tapahtumien muokkaus ja suljettujen tapahtumien muokkaus yksinkertaistuvat. 

Kun asiakkaan tai toimittajan maksu määritetään yhdessä yrityksessä ja maksu selvitetään toisessa yrityksessä kirjatulla laskulla, kummallekin yritykselle luodaan automaattisesti soveltuva tilitys sekä erääntymiskohteen ja erääntymislähteen tapahtumat. Tilitystietue luodaan tapahtuman laskun ja maksun kullekin yhdistelmälle. Kullekin tilitystapahtumalle määritetään uusi tositenumero, joka perustuu maksutositteen numerosarjaan. Tämä numerosarja määritetään asiakkaille **Myyntireskontran parametrit** -sivulla ja toimittajille **Ostoreskontran parametrit** -sivulla. 

Jos käteisalennuksille, ulkomaanvaluutan uudelleenarvostuksille, pyöristyseroille, liian suurille maksuille tai liian pienille maksuille luodaan tilitystietueita, ne kohdistetaan maksu- tai laskutapahtuman myöhempään päivämäärään. Jos tilitys tapahtuu maksun kirjaamisen jälkeen, tilitystietueissa käytetään tilityksen kirjauspäivämäärä, joka määritettiin **Tilitä avoimet tapahtumat** -sivulla.

## <a name="posting-types-transaction-types-and-default-descriptions"></a>Kirjaustyypit, tapahtumatyypit ja oletuskuvaukset

Yritystenväliset tilitystositetapahtumat käyttävät Konserninsisäinen selvitys -kirjaustyyppiä sekä Konserniasiakkaan tilitys- ja Konsernitoimittajan tilitys -tapahtumatyyppejä. Voit määrittää tapahtumatyypin tiedot **Oletuskuvaukset**-lomakkeessa. 

Seuraavat tapahtumatyypit ovat käytettävissä yhden yrityksen tilityksille ja yritystenvälisille tilityksille:

-   Tilitys
-   Käteisalennus
-   Ulkomaanvaluutan uudelleenarvostus (sisältävät ulkomaanvaluutan uudelleenarvioinnin toteutuneissa ja toteutumattomissa transaktioissa)
-   Pyöristysero
-   Liikamaksu/alimaksu

Voit määrittää myös yritystenvälisten selvitystositteiden oletuskuvaukset.

## <a name="currency-exchange-gains-or-losses"></a>Vaihtokurssin voitot ja tappiot

Asiakas- ja toimittajatapahtumissa käytettävä vaihtokurssi tallennetaan tapahtumaan. Valuutanvaihdon realisoidut voitot ja tappiot kirjataan laskuyritykseen tai maksuyritykseen sen vaihtoehdon mukaan, joka on valittu maksuyrityksen **Valuutanvaihdon voiton tai tappion jälkeen** -kentässä **Konsernin sisäinen laskenta** -sivulla. Seuraavissa esimerkeissä käytetään näitä valuuttoja:
-   Maksun kirjanpitovaluutta: EUR
-   Laskun kirjanpitovaluutta: USD
-   Maksutapahtuman valuutta: DKK
-   Laskutapahtuman valuutta: CAD

### <a name="currency-calculations"></a>Valuuttalaskennat

Kun tilität yhdessä yrityksessä kirjatun laskun toisessa yrityksessä kirjatulla maksulla, maksutapahtuman valuutta (DKK) muunnetaan kolmessa vaiheessa:
1.  Summa muunnetaan maksun kirjanpitovaluutaksi (EUR) maksuyrityksen valuuttakurssin mukaan.
2.  Valuutta muunnetaan laskun yrityksen valuuttaan (USD).
3.  Valuutta muunnetaan laskutapahtuman valuuttaan (CAD) laskuyrityksen vaihtokurssien mukaan.

Muuntoprosessissa käytetään maksupäivämäärän valuuttakursseja. Jos tuloksena saatava maksun summa laskun valuutassa (CAD) vastaa laskun summaa (CAD), laskua pidetään täysin maksettuna. 

Kun avaat **Tilitä avoimet tapahtumat** -sivun maksukirjauskansiosta, johon maksun summaa ei kirjattu, tilitettävä summa lasketaan **Tilitä avoimet tapahtumat** -sivulta tilitettäväksi valittuihin laskuihin. Tilitettävä summa muunnetaan kolmessa vaiheessa:
1.  Summa muunnetaan laskun kirjanpitovaluutaksi (USD) laskuyrityksen maksupäivämäärän valuuttakurssin mukaan.
2.  Summa muunnetaan maksun kirjanpitovaluutaksi (EUR) laskuyrityksen maksupäivämäärän valuuttakurssien mukaan.
3.  Summa muunnetaan maksutapahtuman valuutaksi (DKK).

Tuloksena saatava maksun summa siirretään maksukirjauskansion riville, kun suljet **Tilitä avoimet tapahtumat** -sivun.

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Eri kirjanpitovaluuttojen aiheuttamien voittojen ja tappioiden kirjaaminen

Jos valuuttamuunnoksista aiheutuu voittoja tai tappioita, voitot tai tappiot kirjataan yritykseen, joka on määritetty maksuyrityksen **Valuutanvaihdon voiton tai tappion jälkeen**-kentässä **Konserniyritysten välinen laskenta**-sivulla. Voiton tai tappion summa muunnetaan sen yrityksen kirjanpitovaluuttaan, johon voiton tai tappion määrä kirjataan. Muunnossa käytetään yritykselle määritettyä vaihtokurssia.

## <a name="cash-discounts"></a>Käteisalennukset

Yritystenvälisen tilitysprosessin aikana luotavat käteisalennukset kirjataan laskuyritykseen tai maksuyritykseen sen vaihtoehdon mukaan, joka on valittu maksuyrityksen **Käteisalennuksen jälkeen** -kentässä **Konsernin sisäinen laskenta** -sivulla. Vastaava tilitystapahtuma luodaan laskuyritykselle.

## <a name="overpayments-and-underpayments"></a>Liian suuret ja pienet maksut

Liian suuret ja pienet maksut sekä pyöristyserojen toleranssit määritetään liian suurten maksujen maksuyrityksen sekä liian pienten maksujen laskuyrityksen mukaan. Käytettävä asiakkaiden kirjaustili määräytyy **Käteisalennuksen hallinta** -kentän **Myyntireskontran parametrit** -sivulla ja toimittajien kirjaustili **Käteisalennuksen hallinta** -kentän **Ostoreskontran parametrit**-sivulla.

-   Jos käteisalennuksen hallinta-asetus on **Yksilöity** tai **Yksilöimätön** ja käteisalennus kirjataan eri yritykseen liian suuren maksuna, käytetään automaattista tilityypin valintaa asiakkaan käteisalennukselle, toimittajan käteisalennukselle tai pyöristykselle kirjanpitovaluutassa. Voit määrittää nämä tilit **Automaattisten tapahtumien tilit** -sivulla.
-   Jos käteisalennuksen hallinta-asetus on **Yksilöimätön** ja käteisalennus kirjataan samaan yritykseen liian suurena maksuna (maksuyritys ja laskuyritys on sama), käteisalennustiliä oikaistaan. Jos esimerkiksi 100,00:n lasku sisältää 3,00:n käteisalennuksen ja tämä lasku tilitetään 98,00:n maksulla, käteisalennukseksi oikaistaan 1,00. Nettokäteisalennus on 2,00.
-   Jos käteisalennuksen hallinta-asetus on **Yksilöimätön**, käteisalennus kirjataan samaan yritykseen liian suurena maksuna ja liian suuri tai liian pieni maksu tilitetään useilla laskuilla, jotka sisältävät käteisalennuksia, ja käteisalennustiliä oikaistaan viimeisen laskun mukaan.

Jos käteisalennuksen hallinta-asetus on **Yksilöimätön**, yksilöimättömät maksutilityssäännöt pätevät vain seuraavissa tilanteissa:
-   Kyseessä on liian suuri maksu.
-   Liian suuri maksu tilitetään vähintään yhdellä käteisalennuksen sisältävällä laskulla.
-   Käteisalennus kirjataan samaan yritykseen kuin liian suuri maksu.

Kaikissa muissa tapauksissa liian suuret tai pienet maksut kirjataan Asiakkaan käteisalennus, Toimittajan käteisalennus tai Pyöristysero kirjanpitovaluuttana -automaattitilille.

## <a name="sales-tax"></a>Arvonlisävero
Arvonlisäverotapahtumat säilyvät siinä yrityksessä, jossa ne alun perin kirjattiin. 

Jos kirjattiin ennakkomaksun arvonlisävero, yritystenvälinen tilitys palauttaa ennakkomaksun arvonlisäveron ennakkomaksun yrityksessä. Laskuyrityksen arvonlisäverot säilyvät laskuyrityksessä.

## <a name="financial-dimensions"></a>Taloushallinnon dimensiot
Asiakasmaksujen maksuyrityksen erääntymiskohteen ja erääntymislähteen tapahtumat käyttävät tilitettävän maksun myyntireskontran yhteenvetotilin taloushallinnon dimensioita. Laskuyrityksessä erääntymiskohteen ja erääntymislähteen tapahtumat käyttävät tilitettävän laskun myyntireskontran yhteenvetotilin taloushallinnon dimensioita. 

Toimittajamaksujen maksuyrityksen erääntymiskohteen ja erääntymislähteen tapahtumat käyttävät tilitettävän maksun ostoreskontran yhteenvetotilin taloushallinnon dimensioita. Laskuyrityksessä erääntymiskohteen ja erääntymislähteen tapahtumat käyttävät tilitettävän laskun ostoreskontran yhteenvetotilin taloushallinnon dimensioita.

## <a name="withholding-tax"></a>Ennakonpidätys
Laskuun liittyvää toimittajatiliä käytetään määrittämään, pitääkö ennakonpidätys laskea. Jos ennakonpidätys lasketaan, se lasketaan laskuun liitetystä yrityksestä. Jos yritykset käyttävät eri valuuttoja, käytetään laskuun liitetyn yrityksen vaihtokurssia.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
