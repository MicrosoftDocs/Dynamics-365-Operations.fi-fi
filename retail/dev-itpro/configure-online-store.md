---
title: "Määritä online-myymälä"
description: "Tässä artikkelissa on linkkejä ohjeaiheisiin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Retail, UnifiedOperations
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 1191ad3180544a70668aef8dbdb4f0a3d8bfc937
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Määritä online-myymälä
<a id="configure-an-online-store" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Tässä artikkelissa on linkkejä ohjeaiheisiin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa.

Seuraavassa taulukossa on luettelo ohjeaiheista, jotka auttavat määrittämään Retail-komponentit ja Retail-verkkokaupan asiakasohjelmassa.

## Määritä online-myymälä
<a id="configure-an-online-store" class="xliff"></a>
| Tehtävä                                                | Erittely                                                                                                                                                                                                                                                                                                                                                   | Aiheet                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä Retail-komponentit.                        | Määritä ja ylläpidä vähittäismyyntitoimintojen tietoja. Näitä tietoja ovat myymälät, verot, tuotteet, lahjakortit, tarjoukset ja alennukset.                                                                                                                                                                                                          | [Retailin määritys ja ylläpito](https://technet.microsoft.com/en-us/library/hh597201.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                                                                                                                                                                          |
| Määritä vähittäismyyntikanavan siirtymishierarkia.    | Luo vähittäismyyntikanavan siirtymisluokkahierarkia, jonka avulla voidaan määrittää verkkokaupan kautta tarjottujen tuotteiden luokkarakenne. Voit määrittää luokkahierarkian ja liittää tämän jälkeen tuotteet, tuotemääriteryhmät ja määritearvot luokkiin. Liitä luokkahierarkia tämän jälkeen verkkokauppaan.                            | [Vähittäismyyntihierarkian määrittäminen](https://technet.microsoft.com/en-us/library/hh580593.aspx) (AX 2012:n TechNet-sisältö) [Määritteiden ja määritetyyppien määrittäminen](https://technet.microsoft.com/en-us/library/hh227548.aspx) (AX 2012:n TechNet-sisältö) [Vähittäismyynnin määriteryhmien määrittäminen](https://technet.microsoft.com/en-us/library/jj728713.aspx) (AX 2012:n TechNet-sisältö) |
| Lisää verkkokauppa organisaatiohierarkiaan. | Liitä kauppa vähintään yhteen organisaatiohierarkiaan, ennen kuin voit liittää tuotevalikoimia luotuun verkkokauppaan, täyttää kyseisen verkkokaupan tilauksia tai luoda raportteja, jotka sisältävät sen tietoja. Vähintään verkkokauppa on määritettävä organisaatiohierarkiaan, joka sisältää tuotevalikoimia. | [Verkkokaupan määrittäminen](https://technet.microsoft.com/en-us/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |
| Lisää toimitustapoja verkkokauppaan.          | Valitse verkkokaupan tarjoamat toimitustavat.                                                                                                                                                                                                                                                                                                 | [Verkkokaupan määrittäminen](https://technet.microsoft.com/en-us/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |
| Yhdistä määritteet ja lisää metatiedot.                   | Valitse vaihtoehdot, jotka osoittavat, miten luokan tai kanavan tuotteen määritteiden tulee toimia Microsoft SharePoint -sivuston verkkokaupassa.                                                                                                                                                                                              | [Verkkokaupan määrittäminen](https://technet.microsoft.com/en-us/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |

## Verkkokauppatuotteiden konfigurointi
<a id="configure-online-store-products" class="xliff"></a>
| Tehtävä                                 | Erittely                                                                                                                                           | Aiheet                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lisää valikoimia verkkokauppaan. | Lisää tuotevalikoimat, joihin kuuluvat verkkokaupassa saatavilla olevat tuotteet.                                                                  | [Verkkokaupan määrittäminen](https://technet.microsoft.com/en-us/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                              |
| Luetteloiden hallinta.                     | Voit käyttää tuote-esitteitä tunnistaaksesi tuotteet, joita haluat tarjota kaupoissasi.                                                              | [Päätehtävät: Vähittäismyynnin tuoteluetteloiden luominen](https://technet.microsoft.com/en-us/library/jj728712.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                           |
| Hintojen hallinta.                       | Määritä ja käytä hintaryhmiä, jotka ovat keskeinen linkki hintojen ja alennusten sekä kanavien, luetteloiden, liitoksien ja kanta-asiakasohjelmien välillä. | [Hintojen määrittäminen hintaryhmien avulla](https://technet.microsoft.com/en-us/library/hh597169.aspx) (AX 2012:n TechNet-sisältö) [Verojen määrittäminen](https://technet.microsoft.com/en-us/library/hh580571.aspx) (AX 2012:n TechNet-sisältö) |
| Hallitse alennuksia.                    | Määritä ja hallitse hinnanoikaisut ja neljä erilaista alennusta.                                                                                  | [Hinnanoikaisujen ja alennusten määrittäminen](https://technet.microsoft.com/en-us/library/hh597114.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                          |
| Hallitse toimitusmaksuja.             | Määritä ja hallitse kuljetusmaksut, jotka liittyvät verkkokauppaan.                                                                     | [Verkkokaupan kuljetusmaksujen määrittäminen](https://technet.microsoft.com/en-us/library/jj728714.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                           |
| Hallitse toimitustapoja.            | Hallitse verkkokaupan tarjoamia toimitustapoja.                                                                                        | [Toimitustapojen määrittäminen](https://technet.microsoft.com/en-us/library/jj728719.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                            |

## Microsoft Dynamics 365 for Retailin ja verkkokaupan välisen tiedonsiirron määrittäminen
<a id="set-up-data-exchange-between-microsoft-dynamics-365-for-retail-and-the-online-store" class="xliff"></a>
| Tehtävä                                 | Erittely                                                                                                                               | Aiheet                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä kanavan integrointiprofiilit. | Profiilien avulla Retail-komponentit voivat kommunikoida toistensa kanssa. Määritä profiilit ennen tietojen vaihdon asetusten määrittämistä. | [Real-time Service -profiilin määrittäminen](https://technet.microsoft.com/en-us/library/hh580631.aspx) (AX 2012:n TechNet-sisältö) [Kanavaprofiilin määrittäminen](https://technet.microsoft.com/en-us/library/jj677402.aspx) (AX 2012:n TechNet-sisältö) |

 




