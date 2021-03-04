---
title: Copyright-ilmoituksen lisääminen
description: Tässä ohjeaiheessa kerrotaan, miten voit lisätä sähköisen kaupankäynnin sivustoon copyright-ilmoituksen.
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 838047cac694c65047332e146a7c43ee2ae0f401
ms.sourcegitcommit: 1a12b42cc17f004a981c716aed3da6cf538475a5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4412098"
---
# <a name="add-a-copyright-notice"></a>Copyright-ilmoituksen lisääminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit lisätä sähköisen kaupankäynnin sivustoon copyright-ilmoituksen.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit lisätä copyright-ilmoituksen sivustoon, siinä on oltava seuraavat nimikkeet:

- Malli, joka sisältää jaetun alatunnisteen osan.
- Sivu, joka käyttää kyseistä mallia.

## <a name="add-a-copyright-notice"></a>Copyright-ilmoituksen lisääminen

Voit lisätä copyright-ilmoituksen jokaisen tiettyä mallia käyttävän sivun alaosaan seuraavasti.

1. Siirry kohtaan **Fragmentit** ja valitse sitten **Uusi**.
1. Valitse **Uusi osa** -valintaikkunassa **Alatunniste**-moduuli ja anna osalle nimi. Kirjoita esimerkiksi **Alatunniste - copyright**.
1. Valitse **OK**.
1. Valitse siirtymisruudussa kolmen pisteen painike (**...**) **Alatunniste**-kohdan vieressä ja valitse sitten **Lisää moduuli**.
1. Valitse valintaikkunassa **Alatunnisteluokka** ja valitse sitten **OK**.
1. Valitse siirtymisruudussa kolmen pisteen painike **Alatunnisteluokka**-kohdan vieressä ja valitse sitten **Lisää moduuli**.
1. Valitse valintaikkunassa **Tekstilohko** ja valitse sitten **OK**.
1. Valitse siirtymisruudussa **Tekstilohko**.
1. Lisää oikealla olevassa ominaisuusruudussa **Kappale**-kenttään copyright-sanoma. Syötä esimerkiksi teksti **(C) Fabrikam 2019**.
1. Valitse **Tallenna**. Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise**.
1. Siirry **Mallit**-kohtaan, valitse malli ja valitse sitten **Muokkaa**.
1. Laajenna **Sivun jäsennys** -kohdassa **Tekstiosa** ja laajenna sitten **Oletussivu**-kohta.
1. Valitse **Ylätunnistepaikka**-kohdan vieressä oleva kolmen pisteen painike ja valitse sitten **Lisää osa**.
1. Valitse aiemmin luomasi osa ja valitse sitten **Valitse**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

Copyright-ilmoituksen sisältävä alatunniste näkyy automaattisesti kaikkien valittua mallia käyttävien sivujen alaosassa.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Tervetuloviestin lisääminen](add-welcome-message.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]