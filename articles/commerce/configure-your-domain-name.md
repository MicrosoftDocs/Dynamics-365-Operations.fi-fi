---
title: Toimialueen nimen määrittäminen
description: Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään.
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 298ce84008e60cc82a494320b6a41f35338508c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278621"
---
# <a name="configure-your-domain-name"></a>Toimialueen nimen määrittäminen


[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365:n sähköisen kaupankäynnin sivuston toimialueen nimi määritetään. 

## <a name="add-domains-during-e-commerce-initialization"></a>Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen aikana

Jos haluat liittää toimialueet sähköisen kaupankäynnin Dynamics 365 Commerce -ympäristöön, alusta sähköinen kaupankäynti kohdassa [Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md) kuvatulla tavalla. Alustuksen aikana sinua pyydetään antamaan tietoja, joita käytetään sähköisen kaupankäynnin ympäristössä. Lisää **Tuetut isäntänimet** -kenttään toimialueet, joita aiot käyttää tämän ympäristön kanssa. Jos toimialueita on useita, erota ne puolipisteellä. Näin toimialueet määritetään kaikissa vaadituissa sähköisen kaupankäynnin osissa. Ne ovat valmiita käytettäviksi, kun siirrät liikenteen omasta CDN-verkosta tai verkkopalvelimelta sähköisen kaupankäynnin edustalle.

## <a name="add-domains-after-e-commerce-initialization"></a>Toimialueiden lisääminen sähköisen kaupankäynnin alustamisen jälkeen

Jos haluat liittää sähköisen kaupankäynnin ympäristöön uusia toimialueita sähköisen kaupankäynnin alustamisen jälkeen, sinun on lähetettävä palvelupyyntö.

## <a name="additional-resources"></a>Lisäresurssit

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
