---
title: Rivinimikkeiden työnkulkujen asetusten määrittäminen
description: Tässä aiheessa kerrotaan rivinimiketyönkulkuelementin määrittämisestä.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46de2bc3683ed907f1879afc13c60adce261d402
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567012"
---
# <a name="configure-line-item-workflows"></a>Rivinimikkeiden työnkulkujen asetusten määrittäminen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan rivinimiketyönkulkuelementin määrittämisestä.

Rivinimiketyönkulkuelementti konfiguroidaan työnkulkueditorissa napsauttamalla elementtiä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun. Seuraavien ohjeiden avulla voit sitten määrittää rivinimiketyönkulkuelementin eri ominaisuudet.

## <a name="name-the-line-item-workflow-element"></a>rivinimiketyönkulkuelementin nimeäminen.

Kirjoita näiden ohjeiden avulla nimi rivinimiketyönkulkuelementille.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Kirjoita **Nimi**-kenttään rivinimiketyönkulkuelementin yksilöivä nimi.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Määritä, käytetäänkö samaa työnkulkua käsittelemään kaikki nimikkeet

Voit määrittää seuraavasti, käytetäänkö samaa työnkulkua kaikkien nimikkeiden käsittelyyn asiakirjassa.

1. Napsauta vasemmassa ruudussa **Perusasetukset**.
2. Jos saman työnkulku käsittelee kaikki nimikkeet asiakirjassa, valitse **Käynnistä kaikille rivinimikkeille sama työnkulku**. Valitse työnkulku, joka käsittelee rivinimikkeet.
3. Jos tietty työnkulku käsittelee nimikkeet, jotka täyttävät tietyt ehdot, valitse **Käynnistä kullekin rivinimikkeelle eri työnkulku**. Noudata näitä ohjeita ja määritä ehtojoukko:

    1. Valitse **Lisää**.
    2. Valitse ehto taulukosta.
    3. **Ehdon nimi** -välilehdessä kirjoita nimi ehtojoukolle, jotka määrität.
    4. Kirjoita ehto valitsemalla **Lisää ehto**.
    5. Kirjoita kaikki muut tarvittavat ehdot.
    6. Voit tarkistaa, onko antamasi ehtojoukko määritetty oikein, valitsemalla **Testi**. Valitse tietue **Testaa työnkulun ehto** -sivun **Tarkista ehto** -alueella ja valitse sitten **Testi**. Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot. Palaa **Ominaisuudet**-sivulle valitsemalla **OK** tai **Peruuta**.

    Valitse **työnkulku** - välilehdessä työnkulku käsittelemään nimikkeet, jotka täyttävät määrittämäsi ehtojoukon.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]