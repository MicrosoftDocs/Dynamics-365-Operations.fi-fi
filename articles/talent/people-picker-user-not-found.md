---
title: Käyttäjää ei löydetä henkilöiden valitsimessa Attractissa tai Onboardissa
description: 'Tässä ohjeaiheessa käsitellään, miten toimitaan, kun yritysvuokraajan käyttäjät eivät näy henkilöiden valitsimessa Dynamics 365 Talent: Attract- tai Dynamics 365 Talent: Onboard -sovelluksissa.'
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a6d916f87ca30aa7405a51841e56ab31bbe31ac8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461088"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a>Käyttäjää ei löydetä henkilöiden valitsimessa Attractissa tai Onboardissa

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Lähetä

Tietyt vuokraajan kelvolliset Microsoft Azure Active Directory (Azure AD) -käyttäjät eivät tule näkyviin, kun heitä haetaan nimellä henkilöiden valitsimessa Dynamics 365 Talent: Attract- tai Dynamics 365 Talent: Onboard -sovelluksissa.

## <a name="cause"></a>Syy

Tietyn tyyppisiä käyttäjiä ei tueta tällä hetkellä Attract- ja Onboard-sovelluksissa. Varmista, että käyttäjä ei ole Azure AD:n yritysten välinen vieraileva käyttäjä. Käyttäjätyyppiä koskeva tiedot sijaitsevat Azure-portaalini Azure Active Directory -lehdessä.

Lisätietoja yritysten välisestä Azuresta on kohdassa [Vierailevan käyttäjän käyttöoikeudet yritysten välisessä Azure Active Directoryssa](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).

Tietyillä muilla kuin yritysten välisillä käyttäjillä **Käyttäjä**-objektin käyttäjätyyppiominaisuus voi olla vaillinainen. Se voidaan tarkistaa ja korjata Azure AD Powershell -moduulissa. Lisätietoja on kohdassa [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Ratkaisu

Voit ratkaista ongelman seuraavien ohjeiden mukaisesti. Tarvitset kuitenkin Azure Active Directory -vuokraajan yleisen järjestelmänvalvojan käyttöoikeudet tai **User.ReadWrite.All**-käyttöoikeudet.

Tarkista sen käyttäjän käyttäjätyyppi, jota ongelma koskee.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Komento palauttaa seuraavat tiedot:
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Katso, mikä on käyttäjän **UserType**-ominaisuus. Jos **UserType** on tyhjä eikä esimerkiksi Jäsen tai Vieras, päivitä **UserType** seuraavalla komennolla.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]