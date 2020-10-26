---
title: Azure Active Directory -todennuksen käyttöönotto myyntipisteen sisäänkirjauksessa
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commercen myyntipisteen sisäänkirjauskokemus määritetään käyttämään Azure Active Directory -todennusta.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 6946cb5f8bc8aa451f72d1eebcd324f408ad5f7a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975068"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="1669c-103">Azure Active Directory -todennuksen käyttöönotto myyntipisteen sisäänkirjauksessa</span><span class="sxs-lookup"><span data-stu-id="1669c-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="1669c-104">Useat Microsoft Dynamics 365 Commercea käyttävät asiakkaat käyttävät myös muita Microsoftin pilvipalveluita. He voivat hallita näiden palveluiden käyttäjän tunnistetietoja Azure Active Directoryn (Azure AD) avulla.</span><span class="sxs-lookup"><span data-stu-id="1669c-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="1669c-105">Näissä tapauksissa asiakkaat saattavat haluta käyttää samaa Azure AD -tiliä kaikissa sovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="1669c-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="1669c-106">Tässä ohjeaiheessa kerrotaan, miten Commercen myyntipisteen sisäänkirjauskokemus määritetään käyttämään Azure AD -todennusta.</span><span class="sxs-lookup"><span data-stu-id="1669c-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="1669c-107">Azure AD -todennuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1669c-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="1669c-108">Jos haluat määrittää Azure AD:n todennusmenetelmäksi myymälän myyntipisteen sisäänkirjauksessa, määritä myymälän toimintoprofiilin asetukset ja ota ne sitten käyttöön myyntipisteen asiakassovelluksissa.</span><span class="sxs-lookup"><span data-stu-id="1669c-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="1669c-109">Määritä uusi toimintoprofiili seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1669c-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="1669c-110">Siirry kohtaan **Retail ja Commerce** \> **Kanavan asetukset** \> **POS-asetukset** \> **POS-profiilit** \> **Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="1669c-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="1669c-111">Valitse muutettava toimintoprofiili.</span><span class="sxs-lookup"><span data-stu-id="1669c-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="1669c-112">Muuta **Toiminnot**-pikavälilehden **Myyntipisteen henkilöstön sisäänkirjaus** -osassa **Sisäänkirjauksen todennusmenetelmä** -kentän arvo **Henkilöstön tunnus ja salasana** -arvosta **Azure Active Directory** -arvoksi.</span><span class="sxs-lookup"><span data-stu-id="1669c-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="1669c-113">Oletusarvoisesti kaikki toimintoprofiilit käyttävät myyntipisteen todennusmenetelmänä **Henkilöstön tunnus ja salasana** -arvoa.</span><span class="sxs-lookup"><span data-stu-id="1669c-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="1669c-114">Tämän vuoksi sinun on muutettava **Sisäänkirjauksen todennusmenetelmä** -kentän arvoa, jos haluat käyttää Azure AD:ta.</span><span class="sxs-lookup"><span data-stu-id="1669c-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="1669c-115">Tämä muutos vaikuttaa jokaiseen valittuun toimintoprofiiliin linkitettyyn vähittäismyymälään.</span><span class="sxs-lookup"><span data-stu-id="1669c-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="1669c-116">Voit ottaa asetukset käyttöön myyntipisteen asiakassovelluksissa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1669c-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="1669c-117">Mene kohtaan **Retail ja Commerce** \> **Retail ja Commerce IT** \> **Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="1669c-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="1669c-118">Suorita **1070** (**Kanavan määritys**) -jakeluaikataulu.</span><span class="sxs-lookup"><span data-stu-id="1669c-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="1669c-119">Azure AD -todennus vaatii Internet-yhteyden.</span><span class="sxs-lookup"><span data-stu-id="1669c-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="1669c-120">Todennus ei toimi, jos myyntipiste on offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="1669c-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="1669c-121">**Esimiehen ohitus** -toiminto ei tällä hetkellä tue Azure AD:tä todennusmenetelmänä.</span><span class="sxs-lookup"><span data-stu-id="1669c-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="1669c-122">Operaattoritunnus ja salasana ovat pakollisia, vaikka Azure AD olisi määritetty myyntipistekirjautumisen todennusmenetelmäksi.</span><span class="sxs-lookup"><span data-stu-id="1669c-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="1669c-123">Azure AD -tilin liittäminen työntekijään</span><span class="sxs-lookup"><span data-stu-id="1669c-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="1669c-124">Ennen kuin myymälän työntekijä voi käyttää Azure AD -tiliä myyntipistesovellukseen kirjautumisessa, Azure AD -tili on liitettävä kyseiselle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="1669c-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="1669c-125">Voit liittää Azure AD -tilin työntekijälle seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="1669c-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="1669c-126">Siirry kohtaan **Vähittäismyynti ja kauppa** \> **Työntekijät** \> **Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="1669c-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="1669c-127">Avaa työntekijän tietosivu.</span><span class="sxs-lookup"><span data-stu-id="1669c-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="1669c-128">Valitse toimintoruudun **Kauppa**-välilehden **Ulkoinen tunnus** -ryhmässä **Liitä aiemmin luotu tunnus**.</span><span class="sxs-lookup"><span data-stu-id="1669c-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="1669c-129">Valitse **Käytä aiemmin määritettyä ulkoista tunnusta** -valintaikkunassa **Hae sähköpostiosoitteen avulla**, anna Azure AD -sähköpostiosoite ja valitse **Hae**.</span><span class="sxs-lookup"><span data-stu-id="1669c-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="1669c-130">Valitse palautettu Azure AD -tili ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="1669c-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="1669c-131">Työntekijän tietosivun **Alias**, **Täydellinen käyttäjätunnus**- ja **Ulkoinen alitunnus** -kentät **Kauppa**-välilehdessä täytetään.</span><span class="sxs-lookup"><span data-stu-id="1669c-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="1669c-132">Kun työntekijän tietue on päivitetty esimerkiksi uuden Azure AD -tilin liittämisen, salasanan muuttamisen tai työntekijän osoitekirjan päivittämisen vuoksi, on suositeltavaa suorittaa **1060** (**Henkilöstö**) -jakeluaikataulu ja synkronoida uusimmat henkilöstötiedot kanavaan.</span><span class="sxs-lookup"><span data-stu-id="1669c-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="1669c-133">Näin myyntipistesovellus voi hakea oikeat tiedot käyttäjän valtuutusta ja valtuutuksen tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="1669c-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1669c-134">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1669c-134">Additional resources</span></span>

[<span data-ttu-id="1669c-135">Laajennetun MPOS- ja pilvimyyntipistekirjautumisen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1669c-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="1669c-136">Vähittäismyynnin toimintoprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="1669c-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="1669c-137">Työntekijän konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="1669c-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
