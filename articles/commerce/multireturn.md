---
title: Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä aiheessa kuvataan Dynamics 365 Commercen toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004455"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista

[!include [banner](includes/banner.md)]


Palautuksia voidaan tehdä useista eri asiakkaan ostotilauksista ja laskuista. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Määritä Commerce tukemaan palautuksia useista asiakkaan ostotilauksista ja laskuista.

1. Siirry kohtaan **Kaupan parametrit \> Asiakastilaukset**.
1. Ota käyttöön **Mahdollista palautukset useille ostotilauksille** -parametri. 

## <a name="process-returns"></a>Palautusten käsittely

Sen jälkeen, kun parametri on käytössä ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.

Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta. Kassanhoitaja voi tällöin valita palautettavat tuotteet. Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.
