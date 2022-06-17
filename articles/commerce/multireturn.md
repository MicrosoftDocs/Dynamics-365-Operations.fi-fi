---
title: Nimikkeiden palauttaminen useista eri asiakkaan ostotilauksista ja laskuista
description: Tässä artikkelissa kuvataan Dynamics 365 Commercen toiminnallisuus, joka mahdollistaa palautukset useista eri asiakkaan ostotilauksista ja laskuista.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890318"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Nimikkeiden palauttaminen useista eri asiakkaan ostotilauksista ja laskuista

[!include [banner](includes/banner.md)]


Palautuksia voidaan tehdä useista eri asiakkaan ostotilauksista ja laskuista. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Määritä Commerce tukemaan palautuksia useista asiakkaan ostotilauksista ja laskuista.

1. Siirry kohtaan **Kaupan parametrit \> Asiakastilaukset**.
1. Ota käyttöön **Mahdollista palautukset useille ostotilauksille** -parametri. 

## <a name="process-returns"></a>Palautusten käsittely

Sen jälkeen, kun parametri on käytössä ja muutokset on synkronoitu myymälöihin, myymälän kassanhoitaja voi valita useita asiakkaan myyntitilauksia palautusta varten.

Kun tilaukset on valittu, näytetään lista kaikista palautuskelpoisista tuotteista kaikilta laskuilta. Kassanhoitaja voi tällöin valita palautettavat tuotteet. Kaikille valituille tuotteille luodaan yksi yhteinen palautustilaus.
