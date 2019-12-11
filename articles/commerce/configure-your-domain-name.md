---
title: Toimialueen nimen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770455"
---
# <a name="configure-your-domain-name"></a>Toimialueen nimen määrittäminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään. 

## <a name="add-domains-during-e-commerce-initialization"></a>Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen aikana

Jos haluat liittää toimialueet sähköisen kaupankäynnin ympäristöön, alusta sähköinen kaupankäynti kohdassa [Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md) kuvatulla tavalla. Alustuksen aikana sinua pyydetään antamaan tietoja, joita käytetään sähköisen kaupankäynnin ympäristössä. Lisää **Tuetut isäntänimet** -kenttään toimialueet, joita aiot käyttää tämän ympäristön kanssa. Jos toimialueita on useita, erota ne puolipisteellä. Näin toimialueet määritetään kaikissa vaadituissa sähköisen kaupankäynnin osissa. Ne ovat valmiita käytettäviksi, kun siirrät liikenteen omasta CDN-verkosta tai verkkopalvelimelta sähköisen kaupankäynnin edustalle.

## <a name="add-domains-after-e-commerce-initialization"></a>Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen jälkeen

Jos haluat liittää sähköisen kaupankäynnin ympäristöön uusia toimialueita sähköisen kaupankäynnin alustamisen jälkeen, sinun on lähetettävä palvelupyyntö.

## <a name="additional-resources"></a>Lisäresurssit

[Verkkokaupan yleiskatsaus](online-store-overview.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)
