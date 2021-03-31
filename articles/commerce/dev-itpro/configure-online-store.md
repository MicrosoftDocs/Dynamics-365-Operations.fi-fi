---
title: Määritä online-myymälät
description: Tässä artikkelissa on linkkejä ohjeaiheisiin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cf7adf76cb547ffbf516ce475380ddafaca1dfc6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215459"
---
# <a name="configure-online-stores"></a>Määritä online-myymälät

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on linkkejä ohjeaiheisiin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa.

Seuraavassa taulukossa on luettelo ohjeaiheista, jotka auttavat määrittämään Commerce-komponentit ja verkkokaupan asiakasohjelmassa.

## <a name="configure-an-online-store"></a>Määritä online-myymälä

| Tehtävä                                                | Yksityiskohdat                                                                                                                                                                                                                                                                                                                                                   | Aiheet                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfiguroi komponentit.                        | Määritä ja ylläpidä kaupankäyntitoimintojen tietoja. Näitä tietoja ovat myymälät, verot, tuotteet, lahjakortit, tarjoukset ja alennukset.                                                                                                                                                                                                          | [Retailin määritys ja ylläpito](https://technet.microsoft.com/library/hh597201.aspx) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                                                                                                                                                                          |
| Määritä kanavan siirtymishierarkia.    | Luo kanavan siirtymisluokkahierarkia, jonka avulla voidaan määrittää verkkokaupan kautta tarjottujen tuotteiden luokkarakenne. Voit määrittää luokkahierarkian ja liittää tämän jälkeen tuotteet, tuotemääriteryhmät ja määritearvot luokkiin. Liitä luokkahierarkia tämän jälkeen verkkokauppaan.                            | [Aseta vähittäismyyntihierarkia](https://technet.microsoft.com/library/hh580593.aspx)</br> (AX 2012:n TechNet-sisältö)</br> [Määritä määritteet ja määritetyypit](https://technet.microsoft.com/library/hh227548.aspx) (AX 2012:n TechNet-sisältö)</br> [Määritä vähittäismyynnin määriteryhmiä](https://technet.microsoft.com/library/jj728713.aspx) (AX 2012:n TechNet-sisältö) |
| Lisää verkkokauppa organisaatiohierarkiaan. | Liitä kauppa vähintään yhteen organisaatiohierarkiaan, ennen kuin voit liittää tuotevalikoimia luotuun verkkokauppaan, täyttää kyseisen verkkokaupan tilauksia tai luoda raportteja, jotka sisältävät sen tietoja. Vähintään verkkokauppa on määritettävä organisaatiohierarkiaan, joka sisältää tuotevalikoimia. | [Verkkokaupan määrittäminen](https://technet.microsoft.com/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |
| Lisää toimitustapoja verkkokauppaan.          | Valitse verkkokaupan tarjoamat toimitustavat.                                                                                                                                                                                                                                                                                                 | [Verkkokaupan määrittäminen](https://technet.microsoft.com/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |
| Yhdistä määritteet ja lisää metatiedot.                   | Valitse vaihtoehdot, jotka osoittavat, miten luokan tai kanavan tuotteen määritteiden tulee toimia Microsoft SharePoint -sivuston verkkokaupassa.                                                                                                                                                                                              | [Verkkokaupan määrittäminen](https://technet.microsoft.com/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Verkkokauppatuotteiden konfigurointi

| Tehtävä                                 | Yksityiskohdat                                                                                                                                           | Aiheet                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lisää valikoimia verkkokauppaan. | Lisää tuotevalikoimat, joihin kuuluvat verkkokaupassa saatavilla olevat tuotteet.                                                                  | [Verkkokaupan määrittäminen](https://technet.microsoft.com/library/jj682095.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                              |
| Luetteloiden hallinta.                     | Voit käyttää tuote-esitteitä tunnistaaksesi tuotteet, joita haluat tarjota kaupoissasi.                                                              | [Päätehtävät: Vähittäismyynnin tuoteluetteloiden luominen](https://technet.microsoft.com/library/jj728712.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                           |
| Hintojen hallinta.                       | Määritä ja käytä hintaryhmiä, jotka ovat keskeinen linkki hintojen ja alennusten sekä kanavien, luetteloiden, liitoksien ja kanta-asiakasohjelmien välillä. | [Hintojen määrittäminen hintaryhmien avulla](https://technet.microsoft.com/library/hh597169.aspx) (AX 2012:n TechNet-sisältö)</br> [Verojen määritys](https://technet.microsoft.com/library/hh580571.aspx) (AX 2012:n TechNet-sisältö) |
| Hallitse alennuksia.                    | Määritä ja hallitse hinnanoikaisut ja neljä erilaista alennusta.                                                                                  | [Hinnanoikaisujen ja alennusten määrittäminen](https://technet.microsoft.com/library/hh597114.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                          |
| Hallitse toimitusmaksuja.             | Määritä ja hallitse kuljetusmaksut, jotka liittyvät verkkokauppaan.                                                                     | [Verkkokaupan kuljetusmaksujen määrittäminen](https://technet.microsoft.com/library/jj728714.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                           |
| Hallitse toimitustapoja.            | Hallitse verkkokaupan tarjoamia toimitustapoja.                                                                                        | [Toimitustapojen määrittäminen](https://technet.microsoft.com/library/jj728719.aspx) (AX 2012:n TechNet-sisältö)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Määritä Commercen ja verkkokaupan välinen tiedonsiirto

| Tehtävä                                 | Yksityiskohdat                                                                                                                               | Aiheet                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä kanavan integrointiprofiilit. | Profiilien avulla Commerce-komponentit voivat kommunikoida toistensa kanssa. Määritä profiilit ennen tietojen vaihdon asetusten määrittämistä. | [Reaaliaikaisen palveluprofiilin määritys](https://technet.microsoft.com/library/hh580631.aspx) (AX 2012:n TechNet-sisältö)</br> [Kanavaprofiilin määritys](https://technet.microsoft.com/library/jj677402.aspx) (AX 2012:n TechNet-sisältö) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]