---
title: Verkkokaupan käytön rajoittaminen testauksen tai kehityksen aikana
description: Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -verkkokaupan käyttöä rajoitetaan sisäisen testin tai kehityksen aikana.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018335"
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
