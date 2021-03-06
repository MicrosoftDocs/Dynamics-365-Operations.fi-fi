---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (1. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f872b0907e0f48e0b734c87f0b8fb1a4cfe20cb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460990"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a>Dynamics 365 Talent: Core HR:n uudet tai muuttuneet ominaisuudet (1. lokakuuta 2018)

**Koontiversio 8.1.1035.0**

Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.

## <a name="turn-off-electronic-payment-validation"></a>Sähköisten maksujen oikeellisuustarkistuksen poistaminen käytöstä

Sähköisten maksujen tietojen oikeellisuustarkistus suoritetaan, jos määritit suoritukset suoraa talletusta varten joko **Työntekijän itsepalvelun** työtilassa (ESS) tai suoraan työntekijän lomakkeessa. Tämän vaihtoehdon avulla voit joustavasti poistaa oikeellisuustarkistuksen, jos sitä ei tarvita määrien ja jäännösarvojen oikeellisuustarkistuksia varten. Tämä toiminto on hyödyllinen integroitaessa ulkoista palkkajärjestelmää, jossa on erilaiset vaatimukset.

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a>Esimiehen itsepalvelu – Lisää tavoitteet tiimin jäsenille Tiimin suorituskykytavoitteet -ruudussa

Ennen tätä versiota esimiehet pystyivät lisäämään tavoitteita työntekijöille erikseen kuhunkin työntekijään liittyvien suorituskykytavoitteiden kautta. Tämän päivityksen myötä esimiehet voivat luoda **Tiimin suorituskykytavoitteet** -ruudussa uusia tavoitteita valitsemalla jonkin suoran alaisensa.

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a>Esimiehen itsepalvelu – Lisää arvioinnit tiimin jäsenille Tiimin suorituskykyarvioinnit -ruudussa

Ennen tätä versiota esimiehet pystyivät lisäämään arvioita työntekijöille erikseen kuhunkin työntekijään liittyvien arviointien kautta. Tämän päivityksen myötä esimiehet voivat luoda **Tiimin suorituskykyarvioinnit** -ruudussa uusia arviointeja valitsemalla jonkin suoran alaisensa.

## <a name="configure-proration-options-by-leave-plan"></a>Suhteellisen jaon asetusten määrittäminen lomasuunnitelman mukaan

Organisaatiot myöntävät poissaoloja eri tavalla sen mukaan, milloin työntekijät liittyvät yritykseen ja lähtevät yrityksestä. Joissakin organisaatioissa työntekijät saavat palkkion täysimääräisen kohdistuksen aloituspäivänä kun taas toisissa palkkioon sovelletaan suhteellista jakoa. Tässä versiossa on uusia vaihtoehtoja sen valintaan, miten palkkioiden ja jaksotusten suhteellista jakoa sovelletaan työntekijöihin, jotka liittyvät organisaatioon tai lähtevät siitä. Vaihtoehtoja ovat suhteutettu, täysi jaksotus ja ei jaksotusta.

## <a name="other-changes"></a>Muut muutokset

-   Työntekijän yksikköä päivitetty – **Henkilötiedot**-ruutua voidaan nyt päivittää Excel-lisäosien/tietojen hallinnan avulla.

-   Suojauksen muutos, jotta voidaan poistaa **Poista**- ja **Poista aktivointi** -painikkeet työntekijän itsepalvelussa maksutietojen osalta.

## <a name="known-issue"></a>Tunnettu ongelma

-   **Ongelma:** Lisättäessä uuden liitteen työntekijään, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. **Ratkaisuehdotus:** Varmista ennen liitesivun avaamista, että olet sulkenut **Työntekijä**-sivulla olevat tietoruudut. Kun tietoruudut on suljettu ladattaessa **Työntekijä**-sivua, **Liitteet**-painikkeet otetaan käyttöön. (Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]