---
title: "Ehdollisen päätöksen konfiguroiminen työnkulkuun"
description: "Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d3efb6106df7d66ebe9b1a061f9976b8978704b1
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


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






