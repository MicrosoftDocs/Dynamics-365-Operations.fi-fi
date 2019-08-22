---
title: Resurssin asiakirjat
description: Tässä ohjeaiheessa kerrotaan resurssien asiakirjoista resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1c90788da7ad536fb9978db18160ccf6c158033
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783225"
---
# <a name="asset-documents"></a>Resurssin asiakirjat

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Tässä ohjeaiheessa kerrotaan resurssien asiakirjoista resurssien hallinnassa.

Resurssien hallinnassa voit määrittää asiakirjoja niin, että ne liittyvät automaattisesti esimerkiksi työtyyppeihin, resurssien valmistajiin, resurssityyppeihin tai resursseihin. Tämä toiminto on hyödyllinen, kun päivitetyt tiedostoversiot vapautetaan. Tällöin sinun on vain asetettava päivitetty asiakirja Microsoft Dynamics 365 for Finance and Operationsin asiakirjojen vakiosijaintiin ja liitettävä asiakirja luomaasi resurssin asiakirjatietueeseen. Päivitettyä asiakirjaa voi sitten käyttää valikkokohteissa **Kaikki resurssit**, **Aktiiviset resurssit**, **Omat aktiiviset resurssit**, **Kaikki työtilaukset** ja **Aktiivisten työtilausten työt**. Prosessi, jossa asiakirjoja liitetään resurssin asiakirjatietueeseen, käyttää Finance and Operationsin asiakirjojen vakiokäsittelyjärjestelmää.

**Esimerkki 1:** työtyyppiin liittyvä tiedosto voi kuvata kyseisen työlajin proseduurin.

**Esimerkki 2:** resurssityypin, valmistajan ja mallin yhdistelmään liittyvä asiakirja voi olla valitun resurssin valmistajan mallin vakiokäsikirja.

## <a name="create-asset-document-relation"></a>Luo resurssin ja asiakirjan suhde

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Resurssin asiakirjat**.
2. Luo resurssin asiakirjatietue valitsemalla **Uusi**.
3. Tee tarvittavat valinnat seuraavista kentistä sen mukaan, miten tiedostosuhde halutaan määrittää: **resurssityyppi**, **valmistaja**, **malli**, **resurssi**, **Työtyypin luokka**, **Työtyyppi**, **Työtyypin variantti** ja **Työtarve**. **Työtyypin variantti**- ja **Työtarve**-kentissä käytettävissä olevat vaihtoehdot määräytyvät **Työtyyppi**-kentässä tehdyn valinnan mukaan.

    > [!NOTE]
    > Kun järjestelmä etsii asiakirjoja, jotka liittyvät resurssiiin tai työtilaukseen, resurssien hallinta käy läpi kaikki resurssiasiakirjan tietueet ja tarkistaa mahdollisen vastaavuuden. Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin. Toisin sanoen resurssien hallinta tarkistaa ensin **Työtarve**-kentän vastaavuuden. Jos vastaavuutta ei löydy, se tarkistaa **Työtyypin variantti** -kentän vastaavuuden. Jos vastaavuutta ei löydy, se tarkistaa **Työtyyppi** -kentän vastaavuuden ja niin edelleen. Kuten näet **Resurssin asiakirjat** -sivun asettelussa, tämä tarkoittaa sitä, että jos haluat löytää erityisen yhdistelmän, omaisuuden hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta se vastaa toisiaan. Useita asiakirjoja voi liittyä resurssiin tai työtilaukseen. Voit muokata ylläpitopyynnössä tai työtilauksessa palvelutasoa.

4. Valitse **Liitteet**. Näkyviin tulee Finance and Operationsin tavanomainen **Tiedoston käsittely** -sivu.
5. Määritä asiakirjat tai huomautukset, jotka liitetään resurssin asiakirjatietueeseen. Kun olet liittänyt tiedostot, **Liitteet**-kentässä näkyy tietueeseen liittyvien tiedostojen määrä.
