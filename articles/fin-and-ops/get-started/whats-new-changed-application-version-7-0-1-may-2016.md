---
title: Dynamics AX -sovelluksen version 7.0.1 uudet ja muuttuneet ominaisuudet (toukokuu 2016)
description: Tässä artikkelissa käsitellään Microsoft Dynamics AX -sovellusversion 7.0.1 uusia tai muuttuneita ominaisuuksia. Tämä versio julkaistiin toukokuussa 2016 ja sen koontiversio on 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c830952b5d9e4887a816b5ab66d0944bddf5b505
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "314506"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Dynamics AX -sovelluksen version 7.0.1 uudet ja muuttuneet ominaisuudet (toukokuu 2016)

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics AX -sovellusversion 7.0.1 uusia tai muuttuneita ominaisuuksia. Tämä versio julkaistiin toukokuussa 2016 ja sen koontiversio on 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Sähköinen raportointi (ER)

| Mitä voit tehdä? | Miksi tämä on tärkeää? |
|------------------|------------------------|
| Määritä sähköisen raportoinnin (ER) raporttisuunnittelun suorituksenaikainen valintaikkuna, jotta käyttäjät voivat valita sopivat taloushallinnon dimensiot. | Käyttäjät voivat valita suorituksen aikana useita taloushallinnon dimensioita ER-raportin suorittamisen valintaikkunassa. Valittujen taloushallinnon dimensioiden tiedot näytetään luotavassa sähköisessä asiakirjassa. |
| Määritä useiden taloushallinnon dimensioiden käyttöoikeus ER-raportin suunnittelun aikana yhdellä yhdistämismäärityksellä haluttuun tietolähteeseen. | Samaa ER-raporttimääritystä voidaan käyttää luomaan sähköisiä asiakirjoja, jotka esittävät tapahtumatiedot yhdessä taloushallinnon dimensioiden tiedot, riippumatta käyttäjän valitsemien tai nykyiselle yritykselle tai -esiintymälle määritettyjen taloushallinnon dimensioiden määrästä. |
| Määritä ER-raportti antamaan tiedot OPENXML-laskentataulukkomuodossa luodun sähköisen asiakirjan dynaamisesti luotuihin sarakkeisiin. | ER-raportti voi antaa tiedot luotavaan OPENXML-laskentataulukkoon replikoimalla sarakkeet vaakasuunnassa. Tämän vuoksi samaa ER-raportin määritystä voidaan käyttää uudelleen luomaan sähköisiä asiakirjoja, joilla on eri määrä dynaamisesti luotuja sarakkeita. |
| Määritä ER-kohteet niin, että muodon tulos on ohjattava tiettyyn kohteeseen: tiedosto, sähköposti tai arkisto (Microsoft SharePoint -kansio tai Microsoft Azuren tallennustila). | Kun ER-määritys suoritettiin aiemmin, avautuva sanomaruutu pyysi käyttäjää tallentamaan tai avaamaan tiedoston. Voit nyt määrittää kohteen valmiiksi erikseen kullekin muotomääritykselle ja tuloskomponentille (kansio tai tiedosto). Käyttäjät, joilla on tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>Myyntipiste – Microsoft Dynamics AX vähittäismyynti

| Mitä voit tehdä? | Miksi tämä on tärkeää? |
|------------------|------------------------|
| Käytä Google Chrome -selainta. | Vähittäismyyjät voivat nyt käynnistää pilvimyyntipisteen Chrome-selaimesta ja saada käyttöönsä kaikki pilvimyyntipisteen Microsoft Edgessä ja Internet Explorerissa käytettävissä olevat toiminnot. |

## <a name="financial-reporting"></a>Taloushallinnan raportointi

| Mitä voit tehdä? | Miksi tämä on tärkeää? |
|------------------|------------------------|
| Luo talousraportoinnin tietovarasto. | Kun siirrät Dynamics AX -tietokantoja ympäristöjen välillä tai teet muita perusteellisia muutoksia ympäristössä, talousraportointitietokanta on ehkä muodostettava uudelleen. Windows PowerShell -komentosarja on nyt käytettävissä tietokannan uudelleenmuodostusta varten. |
| Et voi enää valita raportin suunnittelutoiminnon asetuksia, jotka eivät kelpaa. | Useita Management Reporterin markkinointiversioissa käytettyjä raportin suunnittelutoiminnon asetuksia ei voi käyttää tässä Dynamics AX -versiossa. Nämä asetukset liittyivät talousraportin suunnitteluun, tulostukseen ja linkittämiseen. Nämä asetukset on poistettu talousraportin suunnittelutoiminnosta käyttäjän virheiden estämiseksi. |

## <a name="financial-management"></a>Taloushallinto

| Mitä voit tehdä? | Miksi tämä on tärkeää? |
|------------------|------------------------|
| Luo positiivisia maksutiedostoja ostoreskontramaksuille. | Positiivisia maksutiedostoja voidaan luoda sekkipetosten ehkäisemiseksi. |

## <a name="warehouse-and-production"></a>Fyysinen varasto ja tuotanto

<table>
<thead>
<tr>
<th>Mitä voit tehdä?</th>
<th>Miksi tämä on tärkeää?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Määritä fyysisen varaston työkäytäntö ohjaamaan työn luontia työjoukolle tietyissä sijainneissa.</td>
<td>Varastointiprosessit eivät aina sisällä työtä. Voit käyttää uutta fyysisen varaston työkäytäntöä estämään raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonti tietyille tuotejoukoille tietyissä sijainneissa.</td>
</tr>
<tr>
<td>Määritä, että tuotannon tuotossijainti ei ole rekisterikilpiohjattu.</td>
<td>Voit nyt määrittää, että tuotteen tuotossijainti ei ole rekisterikilpiohjattu. Tämä ominaisuus on kätevä, kun ylöspäinsuuntautuva tuotantotilaus raportoi nimikkeet valmistuneiksi suoraan sijaintiin, joka toimii alaspäinsuuntautuvan tuotantotilauksen syöttösijaintina.</td>
</tr>
<tr>
<td>Tue saman nimikkeen eri tuotedimensioita sisältävien nimikkeiden tuoterakenteita.</td>
<td>Kun tuotannossa käytetään yhtä tuotedimensiota tai useita dimensioita, voi syntyä tilanne, jossa haluat tuottaa nimikkeen saman nimikkeen eri variantin perusteella. Lisätietoja on <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">tässä blogissa</a>.</td>
</tr>
<tr>
<td>Tuoterakenteet, joiden tuoterakenteiden ensimmäisellä tasolla on kehärakenteita, jätetään materiaalin resurssisuunnittelun tuoterakennetason laskennan ulkopuolelle.</td>
<td>Tuoterakennehierarkiaan kehäkiertoa aiheuttavien tuotantotilausten tuotevarianteille ei voi määrittää oikeita tuoterakennetasoja.</td>
</tr>
<tr>
<td>Laske erilliset tuoterakennetasot materiaalin resurssisuunnittelulle ja kustannuslaskennalle:
<ul>
<li>Materiaalin resurssisuunnittelun tuoterakennetasot lasketaan uudessa <strong>ReqItemLevel</strong>-taulussa. Päättyneet tuotantotilaukset ohitetaan laskennassa.</li>
<li>Tuotannon kustannuslaskennan tuoterakennetasot lasketaan <strong>InventTable</strong>-taulussa. Päättyneet tuotantotilaukset sisällytetään laskentaan.</li>
</ul>
</td>
<td>
<ul>
<li>Kun suoritetaan materiaalin resurssisuunnittelua, kuten pääsuunnittelun suunnitelman ajoitusta ja hajotusta, vain materiaalin resurssisuunnittelussa käytetyt tuoterakennetasot on laskettava uudelleen. Toisin sanoen tuotannon kustannuslaskennassa käytettyjä tuoterakennetasoja ei tarvitse laskea.</li>
<li>Kun suoritetaan kustannuslaskentatoimintoja, kuten varaston sulkemista, vain tuotannon kustannuslaskennan tuoterakennetasot on laskettava uudelleen.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Lisäresurssit

[Uudet ja muuttuneet ominaisuudet](whats-new-changed.md)

[Uudet tai päivitetyt tehtäväoppaat (toukokuu 2016)](new-updated-task-guides-available-may-2016.md)
