---
title: Varaston näkyvyyden vihjeet
description: Tässä artikkelissa on muutamia vinkkejä, jotka kannattaa ottaa huomioon varaston näkyvyyden lisäosaa määrittäessäsi ja käyttäessäsi.
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
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306082"
---
# <a name="inventory-visibility-tips"></a>Varaston näkyvyyden vihjeet

[!include [banner](../includes/banner.md)]

Tässä on muutamia vinkkejä, jotka kannattaa ottaa huomioon varaston näkyvyyden lisäosaa määrittäessäsi ja käyttäessäsi:

- Varastonäkyvyyden lisäosa tukee tällä hetkellä vain Microsoft Dataverse -ympäristöjä, jotka on luotu käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palveluja. Jos Dataverse-ympäristö luotiin jollain muulla tavalla (esimerkiksi Power Apps -hallintakeskuksessa) ja jos se on linkitetty Dynamics 365 Supply Chain Management -ympäristöön, yhdistämismäärityksen ongelma voidaan korjata ottamalla ensin yhteys varaston näkyvyyden tuotetiimiin. Voit ottaa yhteyttä tiimiin osoitteessa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Tiimi kertoo sinulle, milloin ympäristösi on valmis asentamaan varaston näkyvyyden lisäosan.
- Jos sinulla on useita LCS-ympäristöjä, luo kullekin ympäristölle erilainen Azure Active Directory (Azure AD) -sovellus. Jos käytät samaa sovellustunnusta ja vuokraajatunnusta varaston näkyvyyden lisäosan asentamisessa eri ympäristöihin, vanhemmissa ympäristöissä ilmenee tunnusongelma. Vain viimeinen asennettu varaston näkyvyyden lisäosa on voimassa.
- Varaston näkyvyyttä ei tueta tällä hetkellä pilvipalveluympäristöissä. Sitä tuetaan vain Tier-2+-ympäristöissä.
- Sovellusrajapinta (API) tukee tällä hetkellä kyselyä, jossa on enintään 100 yksittäistä nimikettä `ProductID`-arvon mukaan. Jokaisessa kyselyssä voi määrittää myös useita `SiteID`- ja `LocationID`-arvoja. Enimmäisrajaksi määritetään `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Joukkotoimintosovellusliittymä voi palauttaa kullekin pyynnölle enintään 512 tietuetta.
- `fno`-tietolähde on varattu Supply Chain Managementia varten. Jos varaston näkyvyyden lisäosa on integroitu Supply Chain Management -ympäristöön, on suositeltavaa, ettei `fno`-[tietolähteeseen](inventory-visibility-configuration.md#data-source-configuration) liittyviä konfiguraatioita poisteta.
- Varaston näkyvyys ei voi muuttaa `fno`-tietolähteen tietoja. Tietovirta on yksisuuntainen, mikä tarkoittaa, että `fno`-tietolähteen kaikkien määrän muutosten on oltava peräisin Supply Chain Management -ympäristöstä. Siksi et voi lähettää `fno`-tietolähteelle käytettävissä olevan varaston muutos- tai varauspyyntöjä sovellusliittymän avulla.
- Jos lisäät Supply Chain Management -ympäristöön uusia toimenpiteitä, lisää ne myös varaston näkyvyyteen. Kaikkien uusien toimenpiteiden määrän muutosten on kuitenkin oltava peräisin Supply Chain Management -ympäristöstä.
- Tällä hetkellä [osiointimääritys](inventory-visibility-configuration.md#partition-configuration) koostuu kahdesta perusdimensiosta (`SiteId` ja `LocationId`), jotka ilmaisevat tietojen jakelun. Samaan osiointiin liittyvät toiminnot voivat tuottaa suuremman suorituskyvyn alhaisemmin kustannuksin. Ratkaisu sisältää oletusarvon mukaan tämän osiointimäärityksen. Näin ollen *sinun ei tarvitse määrittää sitä itse*. Älä mukauta oletusosiointimääritystä. Jos poistat tai muutat sitä, se aiheuttaa todennäköisesti odottamattoman virheen.
- Osiomäärityksessä määritettyjä perusdimensioita ei saa määrittää [tuotteen indeksihierarkian määrityksissä](inventory-visibility-configuration.md#index-configuration).
- Sinulla on oltava vähintään yksi indeksihierarkia (esimerkiksi joka sisältää perusdimension `Empty`) [tuotteen indeksihierarkian määrityksessä](inventory-visibility-configuration.md#index-configuration), muussa tapauksessa kyselyt epäonnistuvat virheellä "Indeksihierarkiaa ei ole määritetty".
- Tietolähde `@iv` on ennalta määritetty tietolähde. Kohdassa `@iv` etuliitteen `@` kanssa määritetyt fyysiset mittausarvot ovat ennalta määritettyjä mittausarvoja. Nämä mittausarvot ovat kohdistustoiminnon ennalta määritetty määritys, joten niitä ei voi muuttaa eikä poistaa. Jos näin tehdään, kohdistustoiminnon käyttämisen yhteydessä tapahtuu todennäköisesti odottamattomia virheitä.
- Voit lisätä uusia fyysisiä mittausarvoja ennalta määritettyyn laskettuun mittausarvoon `@iv.@available_to_allocate`, mutta sen nimeä ei saa muuttaa.
- Jos palautat Supply Chain Management -tietokannan, palautettu tietokanta voi sisältää tietoja, jotka ovat ristiriidassa niiden tietojen kanssa, jotka varaston näkyvyys on synkronoinut aiemmin Dataverseen. Tämä ristiriita tiedoissa voi aiheuttaa järjestelmävirheitä ja muita ongelmia. Tämän vuoksi on tärkeää, että tyhjennät aina kaikki liittyvät varaston näkyvyyden tiedot Dataversesta ennen Supply Chain Management -tietokannan palautusta. Lisätietoja on kohdassa [Varaston näkyvyyden tietojen tyhjentäminen Dataversesta ennen Supply Chain Management -tietokannan palauttamista](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
