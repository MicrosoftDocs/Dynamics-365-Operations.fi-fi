---
title: Ehdollisten päätösten konfiguroiminen työnkulkuun
description: Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a593d4e188f47b73967f0c5468f7d7c3e9f64dc8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567457"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Ehdollisten päätösten konfiguroiminen työnkulkuun

[!include [banner](../includes/banner.md)]

Määritä seuraavan menettelyn avulla ehdollisten päätöksen ominaisuudet.

Ehdollista valintaa voidaan edellyttää, kun työnkulku jakautuu kahteen haaraan. Ehdollinen päätös konfiguroidaan työnkulkueditorissa napsauttamalla ehdollista päätöstä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun.

## <a name="name-a-decision"></a>Nimeä päätös

Kirjoita näiden ohjeiden avulla nimi ehdolliselle päätökselle.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Kirjoita ehdollisen päätöksen yksilöivä nimi **Nimi**-kenttään.

## <a name="set-conditions"></a> Ehtojen asetus

Järjestelmä päättää käytettävän haaran arvioimalla, täyttääkö lähetetty asiakirja erityisehdot.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Valitse **Lisää ehto**.
3. Määritä ehto.
4. Kirjoita kaikki muut tarvittavat ehdot.
5. Voit tarkistaa, onko ehdot määritetty oikein käymällä läpi seuraavat ohjeet:

    1. Valitse **Testi**, jolloin **Testaa työnkulun ehto** -lomake tulee näyttöön.
    2. Valitse tietue lomakkeen **Tarkista ehto** -alueelta.
    3. Valitse **Testi**. Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.
    4. Palaa **Ominaisuudet**-lomakkeeseen valitsemalla **OK** tai **Peruuta**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]