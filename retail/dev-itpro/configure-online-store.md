---
title: "Määritä online-myymälä"
description: "Tässä artikkelissa on linkkejä aiheisiin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa Microsoft Dynamics 365 for Operationsista."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Retail
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 563d11fb99c8aebce78f8962dbeeac41fb469041
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="configure-an-online-store"></a>Määritä online-myymälä

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on linkkejä aiheisiin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa Microsoft Dynamics 365 for Operationsista.

Seuraavassa taulukossa luetellut aiheet auttavat määrittämään Dynamics 365 for Operations - Retail -komponentit ja Retail-verkkokaupan Dynamics 365 for Operations -asiakasohjelmassa.

## <a name="configure-an-online-store"></a>Määritä online-myymälä
| Tehtävä                                                | Erittely                                                                                                                                                                                                                                                                                                                                                   | Aiheet                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä Retail-komponentit.                        | Määritä ja ylläpidä vähittäismyyntitoimintojen tietoja. Näitä tietoja ovat myymälät, verot, tuotteet, lahjakortit, tarjoukset ja alennukset.                                                                                                                                                                                                          | [Retailin määritys ja ylläpito](https://technet.microsoft.com/en-us/library/hh597201.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                                                                                                                                                                          |
| Määritä vähittäismyyntikanavan siirtymishierarkia.    | Luo vähittäismyyntikanavan siirtymisluokkahierarkia, jonka avulla voidaan määrittää verkkokaupan kautta tarjottujen tuotteiden luokkarakenne. Voit määrittää luokkahierarkian ja liittää tämän jälkeen tuotteet, tuotemääriteryhmät ja määritearvot luokkiin. Liitä luokkahierarkia tämän jälkeen verkkokauppaan.                            | [Vähittäismyyntihierarkian määrittäminen](https://technet.microsoft.com/en-us/library/hh580593.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle) [Määritteiden ja määritetyyppien määrittäminen](https://technet.microsoft.com/en-us/library/hh227548.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle) [Määritä vähittäismyynnin määriteryhmät](https://technet.microsoft.com/en-us/library/jj728713.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle) |
| Lisää verkkokauppa organisaatiohierarkiaan. | Liitä kauppa vähintään yhteen organisaatiohierarkiaan, ennen kuin voit liittää tuotevalikoimia luotuun verkkokauppaan, täyttää kyseisen verkkokaupan tilauksia tai luoda raportteja, jotka sisältävät sen tietoja. Vähintään verkkokauppa on määritettävä organisaatiohierarkiaan, joka sisältää tuotevalikoimia. | [Määritä verkkokauppa](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                                                                                                                                                                                     |
| Lisää toimitustapoja verkkokauppaan.          | Valitse verkkokaupan tarjoamat toimitustavat.                                                                                                                                                                                                                                                                                                 | [Määritä verkkokauppa](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                                                                                                                                                                                     |
| Yhdistä määritteet ja lisää metatiedot.                   | Valitse vaihtoehdot, jotka osoittavat, miten luokan tai kanavan tuotteen määritteiden tulee toimia Microsoft SharePoint -sivuston verkkokaupassa.                                                                                                                                                                                              | [Määritä verkkokauppa](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Verkkokauppatuotteiden konfigurointi
| Tehtävä                                 | Erittely                                                                                                                                           | Aiheet                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lisää valikoimia verkkokauppaan. | Lisää tuotevalikoimat, joihin kuuluvat verkkokaupassa saatavilla olevat tuotteet.                                                                  | [Määritä verkkokauppa](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                              |
| Luetteloiden hallinta.                     | Voit käyttää tuote-esitteitä tunnistaaksesi tuotteet, joita haluat tarjota kaupoissasi.                                                              | [Päätehtävät: Luo vähittäismyynnin tuoteluettelot](https://technet.microsoft.com/en-us/library/jj728712.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                           |
| Hintojen hallinta.                       | Määritä ja käytä hintaryhmiä, jotka ovat keskeinen linkki hintojen ja alennusten sekä kanavien, luetteloiden, liitoksien ja kanta-asiakasohjelmien välillä. | [Hintojen määrittäminen hintaryhmien avulla ](https://technet.microsoft.com/en-us/library/hh597169.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle) [Verojen määrittäminen](https://technet.microsoft.com/en-us/library/hh580571.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle) |
| Hallitse alennuksia.                    | Määritä ja hallitse hinnanoikaisut ja neljä erilaista alennusta.                                                                                  | [Hinnanoikaisujen ja alennusten määritys](https://technet.microsoft.com/en-us/library/hh597114.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                          |
| Hallitse toimitusmaksuja.             | Määritä ja hallitse kuljetusmaksut, jotka liittyvät verkkokauppaan.                                                                     | [Määritä verkkokaupan kuljetusmaksut](https://technet.microsoft.com/en-us/library/jj728714.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                           |
| Hallitse toimitustapoja.            | Hallitse verkkokaupan tarjoamia toimitustapoja.                                                                                        | [Määritä toimitustavat](https://technet.microsoft.com/en-us/library/jj728719.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                            |

## <a name="set-up-data-exchange-between-dynamics-365-for-operations-and-the-online-store"></a>Määritä Dynamics 365 for Operationsin ja verkkokaupan välinen tiedonsiirto
| Tehtävä                                 | Erittely                                                                                                                               | Aiheet                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä kanavan integrointiprofiilit. | Profiilien avulla Retail-komponentit voivat kommunikoida toistensa kanssa. Määritä profiilit ennen tietojen vaihdon asetusten määrittämistä. | [Määritä Real-time Service -profiili](https://technet.microsoft.com/en-us/library/hh580631.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle) [Kanavaprofiilin määrittäminen](https://technet.microsoft.com/en-us/library/jj677402.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle) |

 




