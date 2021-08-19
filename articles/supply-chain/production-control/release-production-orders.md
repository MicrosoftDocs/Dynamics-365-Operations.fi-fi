---
title: Tuotantotilausten vapauttaminen
description: Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 740ac516ffa01d8930aedabb9873834b07b7debf700dc61b14d93ac8d6dcd086
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718867"
---
# <a name="release-production-orders"></a>Tuotantotilausten vapauttaminen

[!include [banner](../includes/banner.md)]

Vapautettu tuotantotilaus on tilaus, joka on hyväksytty tuotantoon. Termillä "Vapautettu" kuvataan tuotantotilauksen elinkaaren tilaa, jossa tuotantotilaus voidaan suorittaa tuotannossa ja varastoprosesseissa.

## <a name="characteristics-of-the-released-state"></a>Vapautettu-tilan ominaisuudet

**Vapautettu**-tila on yksi tuotantotilauksen elinkaaren tiloista. Tuotantotilaukset, joiden tilana on **Vapautettu**, voidaan suorittaa tuotannossa ja varastoprosesseissa. **Vapautettu**-tilalla on seuraavat ominaisuudet:

- Tuotantotila voidaan siirtää **Vapautettu**-tilaan tuotantotilauksesta tai eräprosessin avulla. Tuotantotilaus voidaan myös päivittää automaattisesti suunnitelluista tuotantotilauksista, jotka on vahvistettu **Vahvistuksen aikaraja** -kentässä **Pääsuunnitelma**-sivulla.
- **Vapautettu**-tila osoittaa tuotannon käyttäjille (operaattoreille), että tuotantotyöt voidaan aloittaa.
- Tuotannon dokumentit, kuten reitityskortit ja -työt sekä työkortit sisältävät tuotantotöitä koskevia tietoja, ja niitä voidaan lähettää.
- Fyysisesti varatuille materiaaleille luodaan varastotyö, jolla materiaalit kerätään tuotantotilausta varten.

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

- Raaka-aineiden keräilyn sijaintidirektiivi, joka määrittää, mistä varastosijainnista materiaalit keräillään
- Raaka-aineiden aaltomalli, jossa on määritetty varastotyön suorittamisen käytännöt
- Tuotannon varastosijainti, joka määrittää, minne materiaalit sijoitetaan.

Rekisterikilvillä hallittuja sijainteja käytettäessä voit valita, poimitaanko nimikkeen tilattu määrä vai täysi käytettävissä oleva määrä, kun käsitellään raaka-aineiden poimintatöitä. tämä asetus määritetään seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet** ja avaa asianomainen nimike.
1. Laajenna **Varasto**-pikavälilehti.
1. Valitse **Materiaalin poiminta rekisterikilpisijainneissa**-kentälle jokin seuraavista vaihtoehdoista:
    - *Tilauksen keräily*: Vain tilattu määrä kerärään.
    - *Valmistelu*: Mahdollisuuksien mukaan poimitaan täysi rekisterikilvellä saatavilla oleva määrä. Jotta työntekijä voi poimia rekisterikilven täyden määrän, rekisterikilpi ei saa sisältää sekaisin olevia nimikkeitä eikä erilaisia dimensioita. Jos rekisterikilpi sisältää erilaisia dimensioita tai nimikkeitä, poiminta käsitellään samalla tavalla kuin, jos kyseessä olisi *Tilauksen keräily*.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]