---
title: Tuotantotilausten vapauttaminen
description: "Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä &quot;Vapautettu&quot; kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c4ebedab6d7de62479d3bc80583afadbe780aac4
ms.lasthandoff: 03/31/2017


---

# <a name="release-production-orders"></a>Tuotantotilausten vapauttaminen

Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa. 

<a name="characteristics-of-the-released-state"></a>Vapautettu-tilan ominaisuudet
-------------------------------------

**Vapautettu**-tila on yksi tuotantotilauksen elinkaaren tiloista. Tuotantotilaukset, joiden tilana on **Vapautettu**, voidaan suorittaa tuotannossa ja varastoprosesseissa. **Vapautettu**-tilalla on seuraavat ominaisuudet:

-   Tuotantotila voidaan siirtää **Vapautettu**-tilaan tuotantotilauksesta tai eräprosessin avulla. Tuotantotilaus voidaan myös päivittää automaattisesti suunnitelluista tuotantotilauksista, jotka on vahvistettu **Vahvistuksen aikaraja** -kentässä **Pääsuunnitelma**-sivulla.
-   **Vapautettu**-tila osoittaa tuotannon käyttäjille (operaattoreille), että tuotantotyöt voidaan aloittaa.
-   Tuotannon dokumentit, kuten reitityskortit ja -työt sekä työkortit sisältävät tuotantotöitä koskevia tietoja, ja niitä voidaan lähettää.
-   Fyysisesti varatuille materiaaleille luodaan varastotyö, jolla materiaalit kerätään tuotantotilausta varten.

## <a name="releasing-jobs-to-the-shop-floor"></a>Töiden vapauttaminen tuotantoon
Kun tuotantotilaus on vapautettu, siihen liittyvät tuotantotyöt ovat näkyvissä ja valmiina rekisteröitäviksi. Toimijat voivat tehdä työn rekisteröinnit, kuten Start ja Stop on suoritettu, joko **työn kortin terminal** sivu tai **työn kortti laitteen** sivulla. Rekisteröity aika ja määrä siirretään automaattisesti rekisteröinnin sivuilta tuotantokirjauskansiot seuratakseen kulutettu aika ja määrä.

## <a name="route-cards"></a>Reitityskortit
Reitityskortissa on yhteenveto reitityksen ja työvaiheen asetuksista sekä työvaiheen ja työn ajoitusmenetelmistä saatavista tiedoista.

## <a name="route-jobs"></a>Reititystyöt
Reititystyö luetteloi työvaiheen kunkin työn tarkat tiedot sekä asetus-, käsittely-, jonotus- ja kuljetusajat. Esimerkiksi maalaaminen on työvaihe, johon saatetaan tarvita yksittäisiä töitä, kuten asetusaika, maalausprosessin suoritusaika ja kuivumisen jonotusaika.

## <a name="job-cards"></a>Työkortit
Työkortti luetteloi tietyn työvaiheen yksittäiset työnumerot. Kullakin sivulla näkyy yksi työ. Työt, jotka sisällytetään työkorttiin, sekä niiden arvioidut ajat saadaan reititys- ja työvaiheen asetustiedoista. Voit avata työkortissa **Tuotantokirjauskansion rivit**, **työkortti** -sivun. Operatiivisia resursseja hoitavat henkilöt voivat antaa palautetta tuotantoprosessista. Esimerkiksi kulutustiedoille ja virhemäärille on omat kenttänsä.

## <a name="warehouse-work-for-raw-material-picking"></a>Raaka-aineiden keräilyn varastotyö
Raaka-aineiden keräilytyö luodaan vapautuksen yhteydessä. Työ luodaan vain fyysisesti varattu tuotantotilauksen ennen tilauksen julkaistiin materiaalien määrä. Voit luoda fyysisen varastoinnin työn raaka-aineiden keräilyä varten tarvitaan seuraavat asetukset:

-   Raaka-aineiden keräilyn sijaintidirektiivi, joka määrittää, mistä varastosijainnista materiaalit keräillään
-   Raaka-aineiden aaltomalli, jossa on määritetty varastotyön suorittamisen käytännöt
-   Tuotannon varastosijainti, joka määrittää, minne materiaalit sijoitetaan.



