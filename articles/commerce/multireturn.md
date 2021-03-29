---
title: Nimikkeiden palauttaminen useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä aiheessa kuvataan Dynamics 365 Commercen toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4d1be6606793d498d01be91de6205e3a45c6dfdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251256"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Nimikkeiden palauttaminen useista eri asiakkaan ostotilauksista ja laskuista

[!include [banner](includes/banner.md)]


Tässä artikkelissa kuvataan kaksi ominaisuutta, jotka optimoivat asiakastilausten palautukset useista laskuista. 

## <a name="enable-refunds-over-multiple-captures"></a>Salli palautukset useista tietojen tallennuksista

Tämän ominaisuuden avulla samasta asiakastilauksesta voi tehdä useita linkitettyjä palautuksia. 

1. Siirry **Ominaisuuksien hallinta** -työtilaan ja tee haku hakusanoilla **Salli palautukset useista tietojen tallennuksista**.
2. Valitse **Ota käyttöön palautukset useista tilauksista** ja valitse sitten **Ota käyttöön**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille

Tämä ominaisuus varmistaa, että kun tilaus palautetaan käyttäen useaa laskua, verot täsmäävät alun perin veloitetun verosumman kanssa. 

1. Siirry **Ominaisuuksien hallinta** -työtilaan ja tee haku hakusanoilla **Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille**.
2. Valitse **Ota käyttöön oikea verojen laskeminen osittaisen määrän palautuksille** ja valitse sitten **Ota käyttöön**. 


## <a name="process-returns"></a>Palautusten käsittely

Kun nämä ominaisuudet on otettu käyttöön ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.

Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta. Kassanhoitaja voi tällöin valita palautettavat tuotteet. Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.

Jos tilaus palautetaan kokonaan, asiakkaalle palautettujen verojen summa on sama kuin alun perin veloitettu verosumma.



[!INCLUDE[footer-include](../includes/footer-banner.md)]