---
title: Varaston näkyvyyden vihjeet
description: Tässä ohjeaiheessa on muutamia vinkkejä, jotka kannattaa ottaa huomioon varaston näkyvyyden lisäosaa määrittäessäsi ja käyttäessäsi.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920800"
---
# <a name="inventory-visibility-tips"></a>Varaston näkyvyyden vihjeet

[!include [banner](../includes/banner.md)]

Tässä on muutamia vinkkejä, jotka kannattaa ottaa huomioon varaston näkyvyyden lisäosaa määrittäessäsi ja käyttäessäsi:

- Varastonäkyvyyden lisäosa tukee tällä hetkellä vain Microsoft Dataverse -ympäristöjä, jotka on luotu käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palveluja. Jos Dataverse-ympäristö luotiin jollain muulla tavalla (esimerkiksi Power Apps -hallintakeskuksessa) ja jos se on linkitetty Dynamics 365 Supply Chain Management -ympäristöön, yhdistämismäärityksen ongelma voidaan korjata ottamalla ensin yhteys varaston näkyvyyden tuotetiimiin. Voit ottaa yhteyttä tiimiin osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Tiimi kertoo sinulle, milloin ympäristösi on valmis asentamaan varaston näkyvyyden lisäosan.
- Jos sinulla on useita LCS-ympäristöjä, luo kullekin ympäristölle erilainen Azure Active Directory (Azure AD) -sovellus. Jos käytät samaa sovellustunnusta ja vuokraajatunnusta varaston näkyvyyden lisäosan asentamisessa eri ympäristöihin, vanhemmissa ympäristöissä ilmenee tunnusongelma. Vain viimeinen asennettu varaston näkyvyyden lisäosa on voimassa.
- Varaston näkyvyyttä ei tueta tällä hetkellä pilvipalveluympäristöissä. Sitä tuetaan vain Tier-2+-ympäristöissä.
- Sovellusrajapinta (API) tukee tällä hetkellä kyselyä, jossa on enintään 100 yksittäistä nimikettä `ProductID`-arvon mukaan. Jokaisessa kyselyssä voi määrittää myös useita `SiteID`- ja `LocationID`-arvoja. Enimmäisrajaksi määritetään `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- `fno`-tietolähde on varattu Supply Chain Managementia varten. Jos varaston näkyvyyden lisäosa on integroitu Supply Chain Management -ympäristöön, on suositeltavaa, ettei `fno`-[tietolähteeseen](inventory-visibility-configuration.md#data-source-configuration) liittyviä konfiguraatioita poisteta.
- Tällä hetkellä [osiointimääritys](inventory-visibility-configuration.md#partition-configuration) koostuu kahdesta perusdimensiosta (`SiteId` ja `LocationId`), jotka ilmaisevat tietojen jakelun. Samaan osiointiin liittyvät toiminnot voivat tuottaa suuremman suorituskyvyn alhaisemmin kustannuksin. Ratkaisu sisältää oletusarvon mukaan tämän osiointimäärityksen. Näin ollen *sinun ei tarvitse määrittää sitä itse*. Älä mukauta oletusosiointimääritystä. Jos poistat tai muutat sitä, se aiheuttaa todennäköisesti odottamattoman virheen.
- Osiomäärityksessä määritettyjä perusdimensioita ei saa määrittää [tuotteen indeksihierarkian määrityksissä](inventory-visibility-configuration.md#index-configuration).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
