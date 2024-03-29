---
title: Online-myymälöiden määrittäminen
description: Tässä artikkelissa on linkkejä artikkeleihin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.openlocfilehash: 0af8d9fe39585b0710e97a345dd6a25e3e30273f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281059"
---
# <a name="configure-online-stores"></a>Online-myymälöiden määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on linkkejä artikkeleihin, joiden avulla voit keskitetysti määrittää ja hallita verkkokauppaa.

Seuraavassa taulukossa on luettelo artikkeleista, jotka auttavat määrittämään Commerce-komponentit ja verkkokaupan asiakasohjelmassa.

## <a name="configure-an-online-store"></a>Määritä online-myymälä

| Tehtävä                                                | Lisätietoja                                                                                                                                                                                                                                                                                                                                                   | Artikkelit                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfiguroi komponentit.                        | Määritä ja ylläpidä kaupankäyntitoimintojen tietoja. Näitä tietoja ovat myymälät, verot, tuotteet, lahjakortit, tarjoukset ja alennukset.                                                                                                                                                                                                          | [Retailin määritys ja ylläpito](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-retail) (TechNet-sisältöä Microsoft Dynamics AX 2012:lle)                                                                                                                                                                                                                                                                                          |
| Määritä kanavan siirtymishierarkia.    | Luo kanavan siirtymisluokkahierarkia, jonka avulla voidaan määrittää verkkokaupan kautta tarjottujen tuotteiden luokkarakenne. Voit määrittää luokkahierarkian ja liittää tämän jälkeen tuotteet, tuotemääriteryhmät ja määritearvot luokkiin. Liitä luokkahierarkia tämän jälkeen verkkokauppaan.                            | [Aseta vähittäismyyntihierarkia](/dynamicsax-2012/appuser-itpro/set-up-a-retail-hierarchy)</br> (AX 2012:n TechNet-sisältö)</br> [Määritä määritteet ja määritetyypit](/dynamicsax-2012/appuser-itpro/set-up-attributes-and-attribute-types) (AX 2012:n TechNet-sisältö)</br> [Määritä vähittäismyynnin määriteryhmiä](/dynamicsax-2012/appuser-itpro/set-up-retail-attribute-groups) (AX 2012:n TechNet-sisältö) |
| Lisää verkkokauppa organisaatiohierarkiaan. | Liitä kauppa vähintään yhteen organisaatiohierarkiaan, ennen kuin voit liittää tuotevalikoimia luotuun verkkokauppaan, täyttää kyseisen verkkokaupan tilauksia tai luoda raportteja, jotka sisältävät sen tietoja. Vähintään verkkokauppa on määritettävä organisaatiohierarkiaan, joka sisältää tuotevalikoimia. | [Verkkokaupan määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |
| Lisää toimitustapoja verkkokauppaan.          | Valitse verkkokaupan tarjoamat toimitustavat.                                                                                                                                                                                                                                                                                                 | [Verkkokaupan määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |
| Yhdistä määritteet ja lisää metatiedot.                   | Valitse vaihtoehdot, jotka osoittavat, miten luokan tai kanavan tuotteen määritteiden tulee toimia Microsoft SharePoint -sivuston verkkokaupassa.                                                                                                                                                                                              | [Verkkokaupan määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (AX 2012:n TechNet-sisältö)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Verkkokauppatuotteiden konfigurointi

| Tehtävä                                 | Lisätietoja                                                                                                                                           | Artikkelit                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lisää valikoimia verkkokauppaan. | Lisää tuotevalikoimat, joihin kuuluvat verkkokaupassa saatavilla olevat tuotteet.                                                                  | [Verkkokaupan määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (AX 2012:n TechNet-sisältö)                                                                                                                                              |
| Luetteloiden hallinta.                     | Voit käyttää tuote-esitteitä tunnistaaksesi tuotteet, joita haluat tarjota kaupoissasi.                                                              | [Päätehtävät: Vähittäismyynnin tuoteluetteloiden luominen](/dynamicsax-2012/appuser-itpro/key-tasks-create-retail-product-catalogs) (AX 2012:n TechNet-sisältö)                                                                                                                           |
| Hintojen hallinta.                       | Määritä ja käytä hintaryhmiä, jotka ovat keskeinen linkki hintojen ja alennusten sekä kanavien, luetteloiden, liitoksien ja kanta-asiakasohjelmien välillä. | [Hintojen määrittäminen hintaryhmien avulla](/dynamicsax-2012/appuser-itpro/setting-up-prices-using-price-groups) (AX 2012:n TechNet-sisältö)</br> [Verojen määritys](/dynamicsax-2012/appuser-itpro/setting-up-taxes) (AX 2012:n TechNet-sisältö) |
| Hallitse alennuksia.                    | Määritä ja hallitse hinnanoikaisut ja neljä erilaista alennusta.                                                                                  | [Hinnanoikaisujen ja alennusten määrittäminen](/dynamicsax-2012/appuser-itpro/setting-up-price-adjustments-and-discounts) (AX 2012:n TechNet-sisältö)                                                                                                                          |
| Hallitse toimitusmaksuja.             | Määritä ja hallitse kuljetusmaksut, jotka liittyvät verkkokauppaan.                                                                     | [Verkkokaupan kuljetusmaksujen määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-shipping-charges-for-online-stores) (AX 2012:n TechNet-sisältö)                                                                                                                           |
| Hallitse toimitustapoja.            | Hallitse verkkokaupan tarjoamia toimitustapoja.                                                                                        | [Toimitustapojen määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) (AX 2012:n TechNet-sisältö)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Määritä Commercen ja verkkokaupan välinen tiedonsiirto

| Tehtävä                                 | Lisätietoja                                                                                                                               | Artikkelit                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Määritä kanavan integrointiprofiilit. | Profiilien avulla Commerce-komponentit voivat kommunikoida toistensa kanssa. Määritä profiilit ennen tietojen vaihdon asetusten määrittämistä. | [Reaaliaikaisen palveluprofiilin määritys](/dynamicsax-2012/appuser-itpro/set-up-a-real-time-service-profile) (AX 2012:n TechNet-sisältö)</br> [Kanavaprofiilin määritys](/dynamicsax-2012/appuser-itpro/set-up-a-channel-profile) (AX 2012:n TechNet-sisältö) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
