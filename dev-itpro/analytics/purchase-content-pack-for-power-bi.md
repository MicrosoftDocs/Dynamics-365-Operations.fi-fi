---
title: "Osto kuluttavat virtaa BI sisällön analyysi"
description: "Tässä aiheessa kuvataan, mitä sisältyy oston analyysi sisältö pack Microsoft Power BI-aktiviteettiin. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietoja tietomallin ja yksiköt, joita käytetään rakentaa sisältö pack."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Osto kuluttavat virtaa BI sisällön analyysi

Tässä aiheessa kuvataan, mitä sisältyy oston analyysi sisältö pack Microsoft Power BI-aktiviteettiin. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietoja tietomallin ja yksiköt, joita käytetään rakentaa sisältö pack.

<a name="overview"></a>Yleiskuvaus
--------

Osto varojen käytön analyysi sisällön Microsoft Power BI pack on luotu päälliköt ja johtajat, jotka ovat vastuussa budjetit ostoa varten. Se on suunniteltu auttamaan tarkkaile menoja osto. Osto tapahtumiin liittyviä tietoja Microsoft Dynamics-365 käyttää toimintoja ja tarjoaa sekä koko yrityksen osto luvut yhteenlaskettu tutkimuksen ja ostotilauksen toimittaja-ja varojen käyttörajat jakautuminen. Raporttien Korosta muutokset Purchase menoja pitkällä aikavälillä. Tämän vuoksi ne voidaan ilmoitus esimiehet, positiivinen ja negatiivinen kaupankäynnin kulujen trendeistä yksittäisten toimittajien ja tuotteiden. Näyttävät eri hankintaluokat ja toimittajaryhmien menoja osto. Luokka ja aluepäälliköille ehkä hyödyllistä auttaa tunnistamaan muutoksia kasvamisen toiminta kaavioiden avulla. Sisältö pack nyt osto-päälliköt ja johtajat, jotka ovat vastuussa budjetit analysoida osto varojen käyttörajat seuraavilla tavoilla:

-   Vuoden alusta ostamisesta (toimittajaryhmän ja yksittäisten toimittajien hankintaluokka ja yksittäisten tuotteiden ja toimittajan sijainti)
-   Muutos vuoden vuosittaisen Osto (toimittajan ryhmän ja hankintojen luokan mukaan)

## <a name="accessing-the-content-pack"></a>Sisältö pack käyttäminen
Osto varojen käytön analyysi sisältö pack toteutus varoiksi Microsoft Dynamics Lifecycle Services (LCS) on julkaistu ja voi käyttää Microsoft Dynamics-365 operaatioille. Saat lisätietoja siitä, kuinka access ja avaa Power BI [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Mittareita, jotka sisältyvät sisältö pack
Osto varojen käytön analyysi sisältö pack sisältää raportin, joka koostuu joukko mittareita. Nämä mittarit ovat visualized laatat, kaavioiden ja taulukoiden muodossa. Seuraavassa taulukossa on yhteenveto sisältö Pack visualisointeja.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Raportti-sivu</th>
<th>Kaaviot</th>
<th>Laatat</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Oston toimittajan mukaan</td>
<td><ul>
<li>10 suurinta toimittajaa (pinottu palkkikaavio) ostotilauksen mukaan</li>
<li>Ostot toimittajan mukaan yhteensä ryhmän / maa / nimi (Ympyräkaavio)</li>
<li>Ostot toimittajan mukaan ryhmä / maa / nimi (pylväskaavio)</li>
<li>Ostot toimittajan mukaan keskimääräinen ryhmän / maa / nimi (pylväskaavio)</li>
</ul></td>
<td><ul>
<li>Osto yhteensä</li>
<li>VS ostojen kasvu</li>
<li>Yhteensä # toimittajat</li>
<li>Aktiivisten toimittajien yhteensä #</li>
</ul></td>
</tr>
<tr class="even">
<td>Ostaa tuotteen mukaan</td>
<td><ul>
<li>Osto hankintaluokittain / tuotteen nimi (pylväskaavio)</li>
<li>Yhteensä Osto hankintaluokittain / tuotteen nimi (Ympyräkaavio)</li>
<li>Top 10 tuotteiden osto (pinottu palkkikaavio)</li>
</ul></td>
<td><ul>
<li>Tuotteita yhteensä #</li>
<li>Active tuotteet yhteensä osuus yhteensä # tuotteiden</li>
<li>Tuotteiden osto 80 % kirjanpidollinen määrä</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ostaa ajan *</td>
<td><ul>
<li>Ostamisesta kuukausi / päivä (pylväskaavio)</li>
<li>Kumulatiivinen vs Ostovaihtelu (vesiputoukselle kaavio)</li>
<li>Oston summa vs kasvu (pylväskaavio)</li>
<li>Hankintojen lause (matriisi)</li>
</ul></td>
<td><ul>
<li>VS ostojen kasvu</li>
<li>VS ostojen kasvu %</li>
</ul></td>
</tr>
<tr class="even">
<td>Osto-toimittajan sijainnin mukaan</td>
<td><ul>
<li>Kaupunki ostaa</li>
<li>Osto vs kasvu %</li>
<li>Maan osto</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Osto hankintaluokittain analyysin aika</td>
<td><ul>
<li>Kuluvan vuoden kuukausittain osto / päivä (viivakaavion)</li>
<li>Ostaa nykyisen ja edellisen vuoden (rivi- ja kaavio)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Osto varojen käytön analyysi toimittajan mukaan</td>
<td><ul>
<li>Top 10 toimittajaa % osto Osto (suppilo)</li>
<li>10 suurinta toimittajaa ja parantaa kaupankäynnin kulujen vs</li>
<li>10 suurinta toimittajaa on heikentynyt kaupankäynnin kulujen vs</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Osto hankintaluokittain tämän vuoden ja viime vuonna ja kasvu

## <a name="data-model-and-entities"></a>Tietomallin ja yksiköt
Dynamics 365-osto-raportin tietoja käytetään työvaiheiden kulutus analyysi sisältöpaketti. Nämä tiedot esitetään koostaa mitat, jotka lisätään yrityksen säilössä, joka on Microsoft SQL-tietokannan, joka on optimoitu analytics. Saat lisätietoja kohteen myymälä [Power BI Dynamics yksikön Myymälän integrointi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogimerkintä. Tämä sisältö pack koostaa mitat ovat yhteenlaskettu mittauksia, jotka olivat osto datakuution Microsoft Dynamics AX 2012: n ja Microsoft Dynamics-365 toimintojen 2012 R3: n osajoukko. Vaiheittainen kuution yksikön kaupan koosta mitat, sinun on tehtävä ne esikunnista. Lisätietoja menettelyn väliaikaisen yksikön kauppa koostaa mitat [virtaa BI Dynamics yksikön Myymälän integrointi](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogikirjoituksessa. Avaimen koostaa mitat ovat käytettävissä suoraan laskun rivit-yksikön ja niitä käytetään perustana sisältö pack.

| Kokonaisuus        | Avaimen koosta mittaukset | Tietolähteen Dynamics 365 operaatioille | Kenttä              | kuvaus                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Laskurivit | Osto                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa kirjanpitovaluuttana |

Seuraavassa taulukossa on esitetty tärkeimmät mitat, jotka lasketaan laskun rivit kohteesta sisältöpaketti.

| Mitta               | Laskelma                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Osto kuluvan vuoden | Osto kuluvan vuoden = summa ('laskurivit\[oston\])                                            |
| Ostaa viime vuonna    | Osto viime vuonna = Laske (summa ('laskurivit\[oston\]), SAMEPERIODLASTYEAR (päivämäärät\[päivä\])) |
| VS ostojen kasvu   | VS ostaa kasvu = \[ostaa kuluvan vuoden\] – \[ostaa viime vuonna\]                            |

Sisältö Pack seuraavat tärkeimmät mitat käytetään suodattimina koostaa mitat osittaa niin, että voit saavuttaa enemmän rakeisuus ja syvemmälle analyyttinen asuun.

| Kokonaisuus                 | Esimerkkejä määritteet                                |
|------------------------|-------------------------------------------------------|
| Toimittajat                | Toimittajaryhmiä, toimittaja maan tai alueiden toimittajan nimi |
| Tuotteet               | Tuotenumero, tuotteen nimi, nimi ryhmät        |
| Hankintaluokat | Hankintaluokka-hankintojen luokkien nimet      |
| Oikeushenkilöt         | Yrityksen nimi                                     |
| Päivämäärät                  | Päivämääriä, vuosi vastakirjaus                                    |

Sisältö pack näyttää oletusarvon mukaan tiedot kuluvan kalenterivuoden. Voit kuitenkin muuttaa raportin suodattimia osassa Pvm-suodatus. Voit myös muuttaa oman yrityksen suodatus.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)



