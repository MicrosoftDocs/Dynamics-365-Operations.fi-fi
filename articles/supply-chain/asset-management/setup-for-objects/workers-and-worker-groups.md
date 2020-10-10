---
title: Ylläpitotyöntekijät ja -työntekijäryhmät
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopitotyöntekijät ja -työntekijäryhmät määritetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetWorkerGroupCopyFromResourceGroup, EntAssetWorkerGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29fb487f02c28dbe940a1e00891f1e7ed20135b2
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889886"
---
# <a name="maintenance-workers-and-worker-groups"></a>Ylläpitotyöntekijät ja -työntekijäryhmät

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopitotyöntekijät ja -työntekijäryhmät määritetään resurssien hallinnassa. Resurssien hallinnassa voit liittää kunnossapitotyöntekijöitä toiminnallisiin sijainteihin. (Lisätietoja toiminnallisista sijainneista on kohdassa [luo toiminnallisia sijainteja](../functional-locations/create-functional-locations.md).) Tämä toiminto voi olla hyödyllinen esimerkiksi silloin, kun olet aikatauluttamasta kunnossapitotyötä koneelle, joka sijaitsee toiminnallisessa sijainnissa 01, ja haluat kohdistaa ylläpitotyöntekijät samasta sijainnista, jotta työ voidaan suorittaa.

Voit myös luoda kunnossapitotyöntekijäryhmiä ja liittää niitä kunnosapitotyöntekijöihin. Tästä toiminnosta on hyötyä, kun teet yksinkertaisia työtilausten ajoituksia ja haluat ajoittaa huoltotyöntekijäryhmän työtilaukseen. Kunnossapitotyöntekijöiden ja kunnossapitotyöntekijäryhmien avulla voit määrittää ensisijaisia huoltotyöntekijöitä ja vastuuvelvollisia huoltotyöntekijöitä. 


## <a name="create-workers"></a>Luo työntekijöitä

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **työntekijät** \> **työntekijät**.
2. Lisää uusi työntekijä luetteloon valitsemalla **Uusi**.
3. Valitse **Työntekijä**-kentässä työntekijä.
4. Määritä **Aktiivinen**-asetukseksi **Kyllä**, jos haluat ajoittaa työtilaukseen työntekijän.

    **Yleiset**-pikavälilehdessä **Resurssi**- ja **Kuvaus**-kentät täytetään automaattisesti, jos työntekijälle on valittu resurssi. **Kalenteri**-kenttä täytetään myös automaattisesti, jos olet määrittänyt työntekijän resurssiksi ja osoittanut sille kalenterin **Resurssit**-sivulla (**Organisaation hallinta** \> **Resurssit** \> **Resurssit**).

5. Valitse **Ryhmät**-pikavälilehdessä **Lisää** ja valitse työntekijälle kunnossapitotyöntekijäryhmä. Työntekijä voidaan liittää useampaan kuin yhteen ryhmään.
6. Vakiomäärityksissä työntekijän kuuluminen ryhmään on voimassa päivämäärästä, kun lisäät hänet ryhmään, eikä se vanhene koskaan. Tämä päivämäärä näkyy **Voimassa** -kentässä. Jos haluat nähdä **Voimassa**-kentän valitse **Näytä** \> **Kaikki**. Jos työntekijän kuuluminen ryhmään tulisi rajoittaa tietylle kaudelle, määritä kausi käyttämällä **Voimassa**- ja **Vanhentuminen**-kenttiä.
7. Valitse **Toiminnalliset sijainnit**-pikavälilehdessä **Lisää** ja valitse ylläpitotyöntekijälle toiminnallinen sijainti. Määritä myös, mikä sijainti on työntekijän ensisijainen toiminnallinen sijainti.

    > [!NOTE]
    > Kun lisäät toiminnallisia sijainteja työntekijälle, kaikki näihin toiminnallisiin sijainteihin liittyvät aktiiviset resurssit näkyvät eri valikkokohteissa, kuten **Omat aktiiviset resurssit** ja **Omat aktiiviset toiminnalliset sijainnit**. Ne näkyvät myös resurssihauissa, jotka näytetään, kun luot uuden resurssin, kunnossapitopyynnön tai työtilauksen.

    **Tiedot**-pikavälilehden kentissä näkyy niiden kunnossapitotyöntekijäryhmien ja toiminnallisten sijaintien määrä, joihin valittu kunnossapitotyöntekijä liittyy.

## <a name="create-worker-groups"></a>Luo työntekijäryhmät

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työntekijät** \> **Ylläpitotyöntekijäryhmät**.
2. Lisää uusi työntekijäryhmä luetteloon valitsemalla **Uusi**.
3. Kirjoita ryhmän tunnus **Ylläpitotyöntekijäryhmä**-kenttään.
4. Anna nimi **Nimi**-kenttään.
5. Valitse **Työntekijät**-pikavälilehdessä **Lisää** ja valitse kunnossapitotyöntekijäryhmälle työntekijä. Lisätietoja **Voimassa**- ja **Vanheneminen**-kentistä on edellisen toimenpiteen kohdassa 6.
6. Jos resurssiryhmä liittyy valittuun kunnossapitotyöntekijäryhmään, valitse **Kopioi resurssiryhmästä**. Valitse **Ryhmä**-kentässä resurssiryhmä, josta kalenteriasetukset kopioidaan. Valitse sitten **Työntekijäryhmä**-kentästä työntekijäryhmä, johon resurssiryhmän kalenteriasetukset kopioidaan. Tämä vaihe on merkityksellinen vain, jos haluat, että kunnossapitotyöntekijät voivat käyttää resurssiin (kuormituspaikkaan) liittyvää kalenteria työtilauksen ajoittamisen aikana.

    **Tiedot**-pikavälilehden kentissä näkyy niiden kunnossapitotyöntekijöiden määrä, jotka on määritetty valitulle kunnossapitotyöntekijäryhmälle.
