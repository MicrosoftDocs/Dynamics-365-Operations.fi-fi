---
title: "Ehdollisen päätöksen konfiguroiminen työnkulkuun"
description: "Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c21c8e33ab3a88e1b93ca81d6f0770f1c77fe139
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Ehdollisen päätöksen konfiguroiminen työnkulkuun

[!include[banner](../includes/banner.md)]


Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.

Ehdollista valintaa voidaan edellyttää, kun työnkulku jakautuu kahteen haaraan. Ehdollinen päätös konfiguroidaan työnkulkueditorissa napsauttamalla ehdollista päätöstä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.

## <a name="name-a-decision"></a>Nimeä päätös
Kirjoita näiden ohjeiden avulla nimi ehdolliselle päätökselle.
1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Kirjoita ehdollisen päätöksen yksilöivä nimi **Nimi**-kenttään.

## <a name="set-conditions"></a> Ehtojen asetus
Järjestelmä päättää käytettävän haaran arvioimalla, täyttääkö lähetetty asiakirja erityisehdot.
1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Valitse **Lisää ehto**.
3.  Määritä ehto.
4.  Kirjoita kaikki muut tarvittavat ehdot.
5.  Voit tarkistaa, onko ehdot määritetty oikein käymällä läpi seuraavat ohjeet:
    1.  Valitse **Testi**, jolloin **Testaa työnkulun ehto** -lomake tulee näyttöön.
    2.  Valitse tietue lomakkeen **Tarkista ehto** -alueelta.
    3.  Valitse **Testi**. Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.
    4.  Palaa **Ominaisuudet**-lomakkeeseen valitsemalla **OK** tai **Peruuta**.






