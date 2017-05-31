---
title: Dynamics AX 7.0.1 -sovellusversion uudet ja muuttuneet ominaisuudet (toukokuu 2016)
description: "Tässä artikkelissa käsitellään Microsoft Dynamics AX 7.0.1 -sovellusversion uusia tai muuttuneita ominaisuuksia. Tämä versio julkaistiin toukokuussa 2016 ja sen koontiversio on 7.0.1265.23014."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8b58cb4f9de393b3f381dbe0aa4330d5ebd62795
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Dynamics AX 7.0.1 -sovellusversion uudet ja muuttuneet ominaisuudet (toukokuu 2016)

[!include[banner](../includes/banner.md)]


Tässä artikkelissa käsitellään Microsoft Dynamics AX 7.0.1 -sovellusversion uusia tai muuttuneita ominaisuuksia. Tämä versio julkaistiin toukokuussa 2016 ja sen koontiversio on 7.0.1265.23014.

<a name="electronic-reporting-er"></a>Sähköinen raportointi (ER)
-------------------------

|                                                                                                                                                                                        |                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mitä voit tehdä?**                                                                                                                                                                   | **Miksi tämä on tärkeää?**                                                                                                                                                                                                                                                                                                                             |
| Määritä sähköisen raportoinnin (ER) raporttisuunnittelun suorituksenaikainen valintaikkuna, jotta käyttäjät voivat valita sopivat taloushallinnon dimensiot.                                     | Käyttäjät voivat valita suorituksen aikana useita taloushallinnon dimensioita ER-raportin suorittamisen valintaikkunassa. Valittujen taloushallinnon dimensioiden tiedot näytetään luotavassa sähköisessä asiakirjassa.                                                                                                                              |
| Määritä useiden taloushallinnon dimensioiden käyttöoikeus ER-raportin suunnittelun aikana yhdellä yhdistämismäärityksellä haluttuun tietolähteeseen.                                                  | Samaa ER-raporttimääritystä voidaan käyttää luomaan sähköisiä asiakirjoja, jotka esittävät tapahtumatiedot yhdessä taloushallinnon dimensioiden tiedot, riippumatta käyttäjän valitsemien tai nykyiselle yritykselle tai -esiintymälle määritettyjen taloushallinnon dimensioiden määrästä.                                             |
| Määritä ER-raportti antamaan tiedot OPENXML-laskentataulukkomuodossa luodun sähköisen asiakirjan dynaamisesti luotuihin sarakkeisiin.                                           | ER-raportti voi antaa tiedot luotavaan OPENXML-laskentataulukkoon replikoimalla sarakkeet vaakasuunnassa. Tämän vuoksi samaa ER-raportin määritystä voidaan käyttää uudelleen luomaan sähköisiä asiakirjoja, joilla on eri määrä dynaamisesti luotuja sarakkeita.                                                                                 |
| Määritä ER-kohteet niin, että muodon tulos on ohjattava tiettyyn kohteeseen: tiedosto, sähköposti tai arkisto (Microsoft SharePoint -kansio tai Microsoftin Azuren tallennustila). | Kun ER-määritys suoritettiin aiemmin, avautuva sanomaruutu pyysi käyttäjää tallentamaan tai avaamaan tiedoston. Voit nyt määrittää kohteen valmiiksi erikseen kullekin muotomääritykselle ja tuloskomponentille (kansio tai tiedosto). Käyttäjät, joilla on tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>Myyntipiste – Microsoft Dynamics AX Retail
|                                |                                                                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mitä voit tehdä?**           | **Miksi tämä on tärkeää?**                                                                                                                                                              |
| Käytä Google Chrome -selainta. | Vähittäismyyjät voivat nyt käynnistää pilvimyyntipisteen Chrome-selaimesta ja saada käyttöönsä kaikki pilvimyyntipisteen Microsoft Edgessä ja Internet Explorerissa käytettävissä olevat toiminnot. |

## <a name="financial-reporting"></a>Talousraportointi
|                                                                     |                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mitä voit tehdä?**                                                | **Miksi tämä on tärkeää?**                                                                                                                                                                                                                                                                                         |
| Luo talousraportoinnin tietovarasto.                          | Kun siirrät Dynamics AX -tietokantoja ympäristöjen välillä tai teet muita perusteellisia muutoksia Dynamics AX -ympäristössä, talousraportointitietokanta on ehkä muodostettava uudelleen. Windows PowerShell -komentosarja on nyt käytettävissä tietokannan uudelleenmuodostusta varten.                                                                |
| Et voi enää valita raportin suunnittelutoiminnon asetuksia, jotka eivät kelpaa. | Useita Management Reporterin markkinointiversioissa käytettyjä raportin suunnittelutoiminnon asetuksia ei voi käyttää tässä Dynamics AX -versiossa. Nämä asetukset liittyivät talousraportin suunnitteluun, tulostukseen ja linkittämiseen. Nämä asetukset on poistettu talousraportin suunnittelutoiminnosta käyttäjän virheiden estämiseksi. |

## <a name="financial-management"></a>Taloushallinto
|                                                            |                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------|
| **Mitä voit tehdä?**                                       | **Miksi tämä on tärkeää?**                                       |
| Luo positiivisia maksutiedostoja ostoreskontramaksuille. | Positiivisia maksutiedostoja voidaan luoda sekkipetosten ehkäisemiseksi. |

## <a name="warehouse-and-production"></a>Fyysinen varasto ja tuotanto
|                                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mitä voit tehdä?**                                                                                                                                                                                                                                                                                                                                                                    | **Miksi tämä on tärkeää?**                                                                                                                                                                                                                                                                                                                                                                                                              |
| Määritä fyysisen varaston työkäytäntö ohjaamaan työn luontia työjoukolle tietyissä sijainneissa.                                                                                                                                                                                                                                                                          | Varastointiprosessit eivät aina sisällä työtä. Voit käyttää uutta fyysisen varaston työkäytäntöä estämään raaka-aineen keräilytyön ja valmiiden tuotteiden poispanotöiden luonti tietyille tuotejoukoille tietyissä sijainneissa.                                                                                                                                                                                                     |
| Määritä, että tuotannon tuotossijainti ei ole rekisterikilpiohjattu.                                                                                                                                                                                                                                                                                                               | Voit nyt määrittää, että tuotteen tuotossijainti ei ole rekisterikilpiohjattu. Tämä ominaisuus on kätevä, kun ylöspäinsuuntautuva tuotantotilaus raportoi nimikkeet valmistuneiksi suoraan sijaintiin, joka toimii alaspäinsuuntautuvan tuotantotilauksen syöttösijaintina.                                                                                                                                                     |
| Tue saman nimikkeen eri tuotedimensioita sisältävien nimikkeiden tuoterakenteita.                                                                                                                                                                                                                                                                                                     | Kun tuotannossa käytetään yhtä tuotedimensiota tai useita dimensioita, voi syntyä tilanne, jossa haluat tuottaa nimikkeen saman nimikkeen eri variantin perusteella. Lisätietoja on [tässä blogissa](https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/).                                                                  |
| Tuoterakenteet, joiden tuoterakenteiden ensimmäisellä tasolla on kehärakenteita, jätetään materiaalin resurssisuunnittelun tuoterakennetason laskennan ulkopuolelle.                                                                                                                                                                                                                                     | Tuoterakennehierarkiaan kehäkiertoa aiheuttavien tuotantotilausten tuotevarianteille ei voi määrittää oikeita tuoterakennetasoja.                                                                                                                                                                                                                                                                                                  |
| Laske erilliset tuoterakennetasot materiaalin resurssisuunnittelulle ja kustannuslaskennalle: • Materiaalin resurssisuunnittelun tuoterakennetasot lasketaan uudessa **ReqItemLevel**-taulussa. Päättyneet tuotantotilaukset ohitetaan laskennassa. • Tuotannon kustannuslaskennan tuoterakennetasot lasketaan **InventTable**-taulussa. Päättyneet tuotantotilaukset sisällytetään laskentaan. | • Kun suoritetaan materiaalin resurssisuunnittelua, kuten pääsuunnittelun suunnitelman ajoitusta ja hajotusta, vain materiaalin resurssisuunnittelussa käytetyt tuoterakennetasot on laskettava uudelleen. Toisin sanoen tuotannon kustannuslaskennassa käytettyjä tuoterakennetasoja ei tarvitse laskea. • Kun suoritetaan kustannuslaskentatoimintoja, kuten varaston sulkemista, vain tuotannon kustannuslaskennan tuoterakennetasot on laskettava uudelleen. |

 

<a name="see-also"></a>Lisätietoja
--------

[Uudet ja muuttuneet ominaisuudet](whats-new-changed.md)

[Uudet tai päivitetyt tehtäväoppaat (toukokuu 2016)](new-updated-task-guides-available-may-2016.md)




