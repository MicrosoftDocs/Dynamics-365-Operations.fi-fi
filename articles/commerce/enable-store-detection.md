---
title: Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto
description: Tässä artikkelissa kerrotaan, miten sijaintiin perustuva myymälän tunnistaminen otetaan käyttöön Dynamics 365 Commerce -sivustossa.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0e0fcea2f53a8e1fea5a411981a317eabe94bddb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892042"
---
# <a name="enable-location-based-store-detection"></a>Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten sijaintiin perustuva myymälän tunnistaminen otetaan käyttöön Dynamics 365 Commerce -sivustossa.

Sijaintiin perustuva myymälän tunnistaminen Commerce-sovelluksessa mahdollistaa soveltuvan sivustosisällön tarjoamisen asiakkaille näiden sijainnin perusteella. Kun sijaintiin perustuva myymälän tunnistaminen on käytössä, Commercen hahmonnuspalvelu käyttää maan/alueen tietoja asiakkaan verkkoselaimen IP-osoitteen avulla ja ohjaa asiakkaan parhaaseen mahdolliseen käytettävissä olevaan maantieteellisen paikan sivustomääritykseen.

## <a name="privacy-notice"></a>Tietosuojatiedot

Jos otat sijaintiin perustuvan myymälän tunnistustoiminnon käyttöön, asiakkaan selaimen tiedot lähetetään Microsoftin paikannuspalveluun. Näiden tietojen avulla tarjotaan asiakkaalle sisältöä, joka sopii asiakkaan sijaintiin. Sekä asiakkaan selaimesta lähetettävät tiedot että sijaintiin perustuvat tiedot, jotka palautetaan asiakkaalle, ovat tietoturva- ja evästekäytäntöjen alaisia.

## <a name="turn-on-location-based-store-detection"></a>Sijaintiin perustuvan myymälän tunnistuksen ottaminen käyttöön

Voit ottaa sijaintiin perustuvan myymälän tunnistamisen käyttöön Commercessa seuraavasti.

1. Siirry muokkaustyökaluissa sivustoon.
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivuston hallinta**.
1. Valitse **Sivuston asetukset**.
1. Määritä **Ota sijaintiin perustuva myymälän tunnistus käyttöön** -asetukseksi **Päällä**.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Dynamics 365 Commerce -sivuston liittäminen online-kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-uudelleenohjausten joukkolataus palveluun](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
