---
title: Tuotedimensioiden näyttöasetusten kohdistaminen
description: Tässä artikkelissa kerrotaan tuotedimensioiden näyttöasetuksista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d7575e205a9732259b00e424f66eeadfe8c659ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899172"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Tuotedimensioiden näyttöasetusten kohdistaminen

[!include [banner](includes/banner.md)]


Tässä artikkelissa kerrotaan tuotedimensioiden näyttöasetuksista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce tukee koko-, tyyli- ja väridimensioita, jotta tuotemuuttujat erotetaan toisistaan. Dimensiot näytetään yleensä tekstiarvoina, kuten "pieni", "keskikokoinen" ja "suuri" kokoja varten, ja väreistä "musta" ja "ruskea". Jos tuote tukee useita muunnelmia, tuotemuuttujan selaaminen voi olla vaikeaa, koska kunkin muuttujan kuvan tarkasteleminen edellyttää useita valintoja. Commercen versio 10.0.20 voi helpottaa tuotemuuttujan selaamista, koska se käyttää kuvia ja heksadesimaalikoodeja (hex) dimensioiden näyttämiseen väriruutuina.

Commercen sivustotyökalussa dimensioasetukset määritetään kohdassa **Sivuston asetukset \> Laajennukset \> Dimensioasetukset**. Seuraavassa kuvassa on esimerkki sivustonmuodostuksen dimensioasetuksista.

![Esimerkki Commercen sivustonmuodostustyökalun sivustoasetuksista.](./dev-itpro/media/swatch_site_settings.PNG)

Käytettävissä on kaksi dimensioasetusta:

- **Dimensiot, jotka näytetään kuvana** – Määritä, mitkä dimensiot näkyvät väriruutuina sähköisen kaupankäynnin verkkosivuilla, kuten tuotetietosivuilla (PDF-sivut) ja hakutulosluettelosivuilla. Mikä tahansa väri-, koko- ja tyylidimensioiden yhdistelmä voidaan näyttää väriruutuna. Jos dimensio on valittu näytettäväksi väriruutuna silloin, Commerce-moduulin muodostaminen näyttää käytettävissä olevan hex-koodimallin väriruutukonfiguraation. Jos hex-koodia ei ole määritetty, järjestelmälogiikka etsii kuvan URL-osoitteen väriruudun konfiguraatiota. Jos hex-koodia eikä kuvan URL-osoitetta ei ole määritetty, teksti tulee näkyviin.

    Seuraavassa kuvassa on esimerkki, jossa sähköisen kauppasivuston PDP sisältää väri- ja kokoväriruudut. Tässä esimerkissä väridimensiolle on konfiguroitu heksadesimaalikoodi. Näin ollen väriruudut näytetään väreinä. Kokodimensiolle ei kuitenkaan ole määritetty heksadesimaalikoodia eikä kuvan URL-osoitetta. Näin ollen näkyvissä on teksti.

    ![Esimerkki sähköisen kaupan tuotetietosivulla väriruutuina näkyvistä väridimensioista.](./dev-itpro/media/swatch_pdp.png)

- **Tuotekortissa näytettävät dimensiot** – Määritä, mitkä dimensiot näkyvät luetteloissa ja luettelosivuilla näkyvissä tuotekorteissa. Ennen kuin dimensio voidaan näyttää tuotekortissa, tämän asetuksen on oltava käytössä dimensiolle. Myös **Kuvana näytettävät dimensiot** -asetus tulisi ottaa käyttöön. Tuotekorttien väriruudun valinta on optimoitu väridimension mukaan. Muiden dimensioiden osalta saattaa olla tarpeen käyttää näkymän alanumeroa, jotta valintaa voidaan mukauttaa.

    Seuraavassa kuvassa on esimerkki, jossa sähköisen kauppasivuston luettelosivu sisältää tuotekortteja, joilla on väriruudut.

    ![Esimerkki sähköisen kaupan luettelosivulla väriruutuina näkyvistä väridimensioista.](./dev-itpro/media/swatch_searchresults.PNG)

Lisätietoja tuotedimensioiden konfiguroinnista niin, että ne näkyvät verkkosivuilla väriruutuina, on kohdassa [Tuotedimension arvojen konfiguroiminen näkymään väriruutuina](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Hakutulosmoduuli](search-result-module.md)

[Ostoruutumoduuli](add-buy-box.md)

[Tuotedimensioarvojen konfiguroiminen näkymään väriruutuina](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
