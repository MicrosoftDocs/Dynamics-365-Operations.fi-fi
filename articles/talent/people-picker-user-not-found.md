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
ms.openlocfilehash: 2a3c83fcc3f48aa235ffb2db2dc492b34a306c4c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024185"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="80cb4-103">Azure Active Directory -käyttäjiä ei löydy People Pickerissä</span><span class="sxs-lookup"><span data-stu-id="80cb4-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="80cb4-104">Lähetä</span><span class="sxs-lookup"><span data-stu-id="80cb4-104">Issue</span></span>

<span data-ttu-id="80cb4-105">Tietyt vuokraajan kelvolliset Microsoft Azure Active Directory (Azure AD) -käyttäjät eivät tule näkyviin, kun heitä haetaan nimellä henkilöiden valitsimessa Dynamics 365 Talent: Attract- tai Dynamics 365 Talent: Onboard -sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="80cb4-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="80cb4-106">Syy</span><span class="sxs-lookup"><span data-stu-id="80cb4-106">Cause</span></span>

<span data-ttu-id="80cb4-107">Tietyn tyyppisiä käyttäjiä ei tueta tällä hetkellä Attract- ja Onboard-sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="80cb4-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="80cb4-108">Varmista, että käyttäjä ei ole Azure AD:n yritysten välinen vieraileva käyttäjä.</span><span class="sxs-lookup"><span data-stu-id="80cb4-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="80cb4-109">Käyttäjätyyppiä koskeva tiedot sijaitsevat Azure-portaalini Azure Active Directory -lehdessä.</span><span class="sxs-lookup"><span data-stu-id="80cb4-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="80cb4-110">Lisätietoja yritysten välisestä Azuresta on kohdassa [Vierailevan käyttäjän käyttöoikeudet yritysten välisessä Azure Active Directoryssa](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="80cb4-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="80cb4-111">Tietyillä muilla kuin yritysten välisillä käyttäjillä **Käyttäjä**-objektin käyttäjätyyppiominaisuus voi olla vaillinainen.</span><span class="sxs-lookup"><span data-stu-id="80cb4-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="80cb4-112">Se voidaan tarkistaa ja korjata Azure AD Powershell -moduulissa.</span><span class="sxs-lookup"><span data-stu-id="80cb4-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="80cb4-113">Lisätietoja on kohdassa [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="80cb4-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="80cb4-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="80cb4-114">Resolution</span></span>

<span data-ttu-id="80cb4-115">Voit ratkaista ongelman seuraavien ohjeiden mukaisesti. Tarvitset kuitenkin Azure Active Directory -vuokraajan yleisen järjestelmänvalvojan käyttöoikeudet tai **User.ReadWrite.All**-käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="80cb4-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="80cb4-116">Tarkista sen käyttäjän käyttäjätyyppi, jota ongelma koskee.</span><span class="sxs-lookup"><span data-stu-id="80cb4-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="80cb4-117">Komento palauttaa seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="80cb4-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="80cb4-118">Katso, mikä on käyttäjän **UserType**-ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="80cb4-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="80cb4-119">Jos **UserType** on tyhjä eikä esimerkiksi Jäsen tai Vieras, päivitä **UserType** seuraavalla komennolla.</span><span class="sxs-lookup"><span data-stu-id="80cb4-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
