---
title: Resurssin elinkaaren tilat
description: Tässä ohjeaiheessa käsitellään resurssien elinkaaren tiloja ja elinkaarimalleja resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566036c6361194d910a0fc34bd5d72147585ec4f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426979"
---
# <a name="asset-lifecycle-states"></a>Resurssin elinkaaren tilat

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa käsitellään resurssien elinkaaren tiloja ja elinkaarimalleja resurssien hallinnassa. Resurssien elinkaaritiloja käytetään määritettäessä, onko resurssi aktiivinen vai passiivinen. Voit esimerkiksi määrittää resurssin elinkaaritilat, kuten **Luotu**, **Aktiivinen** ja **Lopetettu**.

> [!NOTE]
> - Pyynnön elinkaaritilat on linkitetty resurssin elinkaaritiloihin. Tämän vuoksi, kun pyyntö muutetaan uuden pyynnön elinkaaritilaan, pyyntöön liitetty resurssi muutetaan uuteen resurssin elinkaaren tilaan. Jos esimerkiksi pyynnön elinkaaritilaksi muutetaan **saapuva**, liittyvän resurssin elinkaaritilaksi muutetaan **Saapuva elinkaaren tila** -kentässä valittuun elinkaaren tilaan **Resurssin elinkaaren tila** -välilehdessä **Resurssin elinkaarimallit** -sivulla. 


Resurssin elinkaaritilat voidaan määrittää resurssien elinkaarimalleissa, jossa voit määrittää erityyppisille resursseille vaaditut elinkaaritilat. Määrität ensin elinkaaritilat. Luo sitten elinkaarimalli ja valitse sen elinkaaritilat.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **resurssit** \> **Elinkaaren tilat**.
2. Luo uusi resurssin elinkaaren tila valitsemalla **Uusi**.
3. Kirjoita **elinkaaren tila** -kenttään elinkaaren tilan tunnus.
4. Anna kuvaus **nimi**-kenttään.

    **Elinkaarimallit**-kentässä näkyy niiden resurssien elinkaarimallien määrä, jotka käyttävät resurssin elinkaaritilaa.

5. Määritä **aktiivinen**-asetukseksi **Kyllä**, jos tämän elinkaaren tilan on oltava aktiivinen elinkaaritila (toisin sanoen, jos tässä elinkaaren tilassa oleville resursseille voidaan luoda työtilauksia).
6. Määritä **Poista avoimet kalenteririvit** -asetukseksi **Kyllä**, jos avoimet resurssikalenterin rivit, joiden resurssin elinkaaren tila on **Luotu**, poistetaan, kun ne ovat tässä elinkaaren tilassa. Tämä asetus on hyödyllinen, jos haluat puhdistaa avoimet ylläpitoaikataulut, jotka eivät enää ole olennaisia resurssin kannalta (jos esimerkiksi resurssi ei ole enää aktiivinen).

> [!NOTE]
> Resurssin elinkaaritilat, resurssin elinkaarimallit ja resurssityypit liittyvät toisiinsa. Niitä käytetään samalla tavalla kuin työtilauksen elinkaaritiloja, työtilauksen elinkaarimalleja ja työtilaustyyppejä. 


Kun olet luonut vaaditut resurssin elinkaaritilat, voit määrittää elinkaaritilat resurssien elinkaarimalleissa.

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **resurssit** \> **Elinkaarimallit**.
2. Luo uusi resurssin elinkaarimalli valitsemalla **Uusi**.
3. Kirjoita **Elinkaarimalli** -kenttään elinkaarimallin tunnus.
4. Anna kuvaus **nimi**-kenttään.

    **Elinkaaren tilat**-kentässä näkyy niiden resurssien elinkaaren tilojen määrä, jotka on valittu resurssin elinkaarimallissa. **Resurssityypit**-kentässä näkyy elinkaarimallia käyttävien resurssityyppien määrä.

5. Valitse **Elinkaaren tilat** -pikavälilehdessä ne resurssin elinkaaren tilat, jotka sisällytetään resurssi elinkaarimalliin.

    - Jos haluat käyttää mallin elinkaaritilaa, valitse se **Jäljellä olevat elinkaaren tilat** -osiosta ja siirrä se sitten **Valitut elinkaaren tilat** -osaan valitsemalla ![oikea nuoli](media/15-setup-for-objects.png).
    - Jos haluat käyttää mallin kaikkia käytettävissä olevia elinkaaritiloja, valitse **Kaikki käytettävissä olevat elinkaaren tilat** -painike ![Kaikki käytettävissä olevat elinkaaren tilat](media/20-setup-for-objects.png). Kaikki elinkaaritilat siirretään **Valitut elinkaaren tilat** -osioon.
    - Jos haluat poistaa elinkaaritilan mallista, valitse se **Valitut elinkaaren tilat** -osiosta ja siirrä se sitten **Jäljellä olevat elinkaaren tilat** -osaan valitsemalla ![vasen nuoli](media/16-setup-for-objects.png).

6. Valitse **Elinkaaren tilan päivitykset** määrittääksesi, mitkä resurssin elinkaaren tilat voivat seurata valittua elinkaaren tilaa.
7. Voit käyttää **Resurssin tila** -pikavälilehteä, jos käsittelet resursseja, jotka vastaanotat korjattavaksi. **Saapuva/lähtevä**-osassa voit valita resurssin elinkaaritilat ilmaisemaan korjausta varten vastaanotetun resurssin työnkulun. Jos tarjoat lainaresursseja asiakkaille tai osastoille, **Laina**-osassa voit valita elinkaaritilat lainaresursseille.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]