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
ms.openlocfilehash: ba7c84e5b1d15fb7a4894af31bbf6793b402b9e4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008751"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a>Dynamics 365 Talent: Core HR:n uudet tai muuttuneet ominaisuudet (1. lokakuuta 2018)

[!include [banner](includes/banner.md)]

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
