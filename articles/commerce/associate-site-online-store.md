---
title: Dynamics 365 Commerce -sivuston liittäminen online-kanavaan
description: Tässä ohjeaiheessa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -sivusto sidotaan yhteen tai useaan verkkomyymälään.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6ae02d34499275fa303358f7dae4d3835d438e1
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517327"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a>Dynamics 365 Commerce -sivuston liittäminen online-kanavaan

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka Microsoft Dynamics 365 Commerce -sivusto sidotaan yhteen tai useaan verkkomyymälään. 

Kun olet valmistellut sähköisen kaupankäynnin Dynamics 365 Commerce -ympäristön Microsoft Dynamics Lifecycle Services (LCS) -portaalin avulla, olet valmis muodostamaan ensimmäisen sähköisen kaupankäynnin sivuston. Liitä sivusto ensimmäisen sivuston luonnin osana verkkomyymälään, joka luotiin aiemmin. Tämä vaihe sitoo sivuston verkkokanavaan ja antaa sivuston näyttää siirtymishierarkian, tuotteet, luokat, hinnat, toimitusvaihtoehdot ja kaiken muun verkkomyymälässä määritetyn tiedon.

Jos haluat luoda uuden sivuston ja liittää siihen verkkomyymälän, valitse LCS:ssä sivuston muokkausympäristön linkki. Valitse sitten sivuston muokkausympäristön aloitussivulla **Uusi sivusto**. Anna **Uusi sivusto** -valintaikkunassa joitakin perustietoja sivustosta. Lisätietoja annettavista tiedoista on kohdassa [Uuden sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md).

Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle. Voit käyttää avattavaa kenttää sivun vasemmassa yläosassa, jos haluat käyttää tuotteita luokan mukaan.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)
