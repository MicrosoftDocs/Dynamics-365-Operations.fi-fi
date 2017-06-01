---
title: Tuotantotilausten vapauttaminen
description: "Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä &quot;Vapautettu&quot; kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1b033e4bf6705b3c9a33f2184666158049909a80
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="release-production-orders"></a>Tuotantotilausten vapauttaminen

[!include[banner](../includes/banner.md)]


Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa. 

<a name="characteristics-of-the-released-state"></a>Vapautettu-tilan ominaisuudet
-------------------------------------

**Vapautettu**-tila on yksi tuotantotilauksen elinkaaren tiloista. Tuotantotilaukset, joiden tilana on **Vapautettu**, voidaan suorittaa tuotannossa ja varastoprosesseissa. **Vapautettu**-tilalla on seuraavat ominaisuudet:

-   Tuotantotila voidaan siirtää **Vapautettu**-tilaan tuotantotilauksesta tai eräprosessin avulla. Tuotantotilaus voidaan myös päivittää automaattisesti suunnitelluista tuotantotilauksista, jotka on vahvistettu **Vahvistuksen aikaraja** -kentässä **Pääsuunnitelma**-sivulla.
-   **Vapautettu**-tila osoittaa tuotannon käyttäjille (operaattoreille), että tuotantotyöt voidaan aloittaa.
-   Tuotannon dokumentit, kuten reitityskortit ja -työt sekä työkortit sisältävät tuotantotöitä koskevia tietoja, ja niitä voidaan lähettää.
-   Fyysisesti varatuille materiaaleille luodaan varastotyö, jolla materiaalit kerätään tuotantotilausta varten.

## <a name="releasing-jobs-to-the-shop-floor"></a>Töiden vapauttaminen tuotantoon
Kun tuotantotilaus on vapautettu, siihen liittyvät tuotantotyöt ovat näkyvissä ja valmiina rekisteröitäviksi. Operaattorit voivat tehdä työrekisteröintejä, kuten Käynnistä, Pysäytä ja Valmistuminen, joko **Työkorttipääte**- tai **Työkorttilaite**-sivulla. Rekisteröity aika ja määrä siirretään automaattisesti rekisteröintisivuilta tuotantokirjauskansioihin, jotta käytettyä aikaa ja määrää voidaan seurata.

## <a name="route-cards"></a>Reitityskortit
Reitityskortissa on yhteenveto reitityksen ja työvaiheen asetuksista sekä työvaiheen ja työn ajoitusmenetelmistä saatavista tiedoista.

## <a name="route-jobs"></a>Reititystyöt
Reititystyö luetteloi työvaiheen kunkin työn tarkat tiedot sekä asetus-, käsittely-, jonotus- ja kuljetusajat. Esimerkiksi maalaaminen on työvaihe, johon saatetaan tarvita yksittäisiä töitä, kuten asetusaika, maalausprosessin suoritusaika ja kuivumisen jonotusaika.

## <a name="job-cards"></a>Työkortit
Työkortti luetteloi tietyn työvaiheen yksittäiset työnumerot. Kullakin sivulla näkyy yksi työ. Työt, jotka sisällytetään työkorttiin, sekä niiden arvioidut ajat saadaan reititys- ja työvaiheen asetustiedoista. Voit avata työkortissa **Tuotantokirjauskansion rivit**, **työkortti** -sivun. Operatiivisia resursseja hoitavat henkilöt voivat antaa palautetta tuotantoprosessista. Esimerkiksi kulutustiedoille ja virhemäärille on omat kenttänsä.

## <a name="warehouse-work-for-raw-material-picking"></a>Raaka-aineiden keräilyn varastotyö
Raaka-aineiden keräilytyö luodaan vapautuksen yhteydessä. Työ luodaan vain sille materiaalimäärälle, joka tuotantotilaukselle oli varattu fyysisesti ennen tilauksen vapauttamista. Raaka-aineiden keräilyn varastotyö luodaan seuraavien asetusten avulla:

-   Raaka-aineiden keräilyn sijaintidirektiivi, joka määrittää, mistä varastosijainnista materiaalit keräillään
-   Raaka-aineiden aaltomalli, jossa on määritetty varastotyön suorittamisen käytännöt
-   Tuotannon varastosijainti, joka määrittää, minne materiaalit sijoitetaan.





