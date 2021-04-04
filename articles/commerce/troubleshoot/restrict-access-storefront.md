---
title: Verkkokaupan käytön rajoittaminen testauksen tai kehityksen aikana
description: Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -verkkokaupan käyttöä rajoitetaan sisäisen testin tai kehityksen aikana.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585307"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Verkkokaupan käytön rajoittaminen testauksen tai kehityksen aikana

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -verkkokaupan käyttöä rajoitetaan sisäisen testin tai kehityksen aikana.

## <a name="description"></a>kuvaus

Sisäisen testauksen tai aktiivisen kehityksen aikana kannattaa ehkä rajoittaa sivuston käyttö, jotta ulkoiset käyttäjät eivät voi käyttää julkaistuja verkkokauppasivuja.

## <a name="resolution"></a>Ratkaisu

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Azure AD B2C:n määrittäminen vakiokäyttäjätyönkulkujen avulla

Lisätietoja Azure Active DirectoryB2C:n (Azure AD B2C) konfiguroinnista verkkokauppasivustolle on kohdassa [Commercen B2C-vuokraajan määrittäminen](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Rajoita käyttäjien pääsyä verkkokaupan sivuille ja estä uusien käyttäjien luominen

Rajoita verkkokaupan sivujen käyttöä Commerce-sivustonmuodostimen avulla noudattamalla seuraavia ohjeita.

1. Siirry sivustoosi.
1. Valitse **Sivut** ja valitse sitten sivu, jonka käyttöä haluat rajoittaa.
1. Valitse moduuli tai katkelmapaikka ja valitse sitten **Muokkaa**.
1. Valitse ominaisuusruudusta **Edellyttääkö kirjautumista?** ja valitse sitten **Lopeta muokkaus**.
1. Valitse **Julkaise**.

Estä uusien käyttäjien luominen Azure AD:ssä noudattamalla seuraavia ohjeita.

1. Siirry [Azure-portaaliin](https://portal.azure.com/).
1. Valitse Azure AD B2C -sovellus, jonka loit sivuston käyttöön.
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Käyttäjätyönkulut**.
1. Valitse **Käyttäjätyönkulut** -sivun yläosassa **Uusi käyttäjän työnkulku**.
1. Valitse **Käyttäjätyönkulun tyyppi** -sivulla **Esikatselu**.
1. Valitse sivun keskiosasta **Kirjautuminen v2**. Noudata sitten [B2C-vuokraajan määritys Commercessa](../set-up-b2c-tenant.md) -ohjeen vaiheita, kun haluat määrittää työnkulun sivuston vakiokäyttäjätyönkuluksi Azure AD B2C:lle testauksen tai kehityksen aikana.

## <a name="additional-resources"></a>Lisäresurssit

[Kuluttajakaupan vuokraajan määrittäminen Commercessa](../set-up-b2c-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten](../custom-pages-user-logins.md)
