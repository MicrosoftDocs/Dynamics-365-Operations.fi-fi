---
title: Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä aiheessa kuvataan ohjelman Microsoft Dynamics 365 for Retail toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2019
ms.locfileid: "373065"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Palauta nimikkeitä useista eri asiakkaan ostotilauksista ja laskuista

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Dynamics 365 for Finance and Operations -ohjelman versiossa 10.0 palautuksia voidaan tehdä useista ostotilauksista ja laskuista, kun versiota 10.0 edeltävissä ohjelmaversioissa palautuksia voitiin käsitellä ainoastaan yksi lasku kerrallaan. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfiguroi Retail tukemaan palautuksia useista asiakkaan ostotilauksista ja laskuista.

1. Siirry **Retail parametrit \> Asiakastilaukset**.
1. Ota käyttöön **Mahdollista palautukset useille ostotilauksille** -parametri. 

## <a name="process-returns"></a>Palautusten käsittely

Sen jälkeen, kun parametri on käytössä ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.

Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta. Kassanhoitaja voi tällöin valita palautettavat tuotteet. Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.
