---
title: Commerce-sivustonmuodostimen käyttöoikeusryhmän määrittäminen ei onnistu ensimmäisen käyttöönoton yhteydessä
description: Tämä ohjeaihe antaa vianmääritysohjeita, jotka voivat auttaa ongelmassa, jossa Commerce-sivustonmuodostimen Microsoft Azure Active Directory (Azure AD) -suojausryhmä ei näy vaihtoehtona, kun luot sähköisen kaupankäynnin komponentteja Microsoft Dynamics Lifecycle Servicesissä (LCS) uuden sähköisen kaupankäynnin vuokraajan ensimmäisen käyttöönoton yhteydessä.
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
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585306"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="ed7b1-103">Commerce-sivustonmuodostimen käyttöoikeusryhmän määrittäminen ei onnistu ensimmäisen käyttöönoton yhteydessä</span><span class="sxs-lookup"><span data-stu-id="ed7b1-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed7b1-104">Tämä ohjeaihe antaa vianmääritysohjeita, jotka voivat auttaa ongelmassa, jossa Commerce-sivustonmuodostimen Microsoft Azure Active Directory (Azure AD) -suojausryhmä ei näy vaihtoehtona, kun luot sähköisen kaupankäynnin komponentteja Microsoft Dynamics Lifecycle Servicesissä (LCS) uuden sähköisen kaupankäynnin vuokraajan ensimmäisen käyttöönoton yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="ed7b1-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ed7b1-105">Description</span></span>

<span data-ttu-id="ed7b1-106">Kun luot sähköisen kaupankäynnin komponentit osana uutta sähköisen kaupankäynnin vuokraajaa, joka sisältää Commerce-sivuston luontiohjelman komponentin, Azure AD -suojausryhmä ei näy valintaikkunassa vaihtoehtona.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed7b1-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ed7b1-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="ed7b1-108">Sähköisen kaupankäynnin valmistelu käyttäjälle oikeassa vuokraajassa</span><span class="sxs-lookup"><span data-stu-id="ed7b1-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="ed7b1-109">Siirry [Azure-portaaliin](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="ed7b1-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="ed7b1-110">Noudata [Luo perusryhmä ja lisää jäsenet Azure Active Directoryn avulla](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) -ohjeita siinä vuokraajassa, jolle sähköisen kaupankäynnin sivuston LCS-projekti valmisteltiin.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="ed7b1-111">Siirry [LCS](https://lcs.dynamics.com/)-palveluun ja kirjaudu sisään käyttäen tiliä, jossa on sama vuokraaja kuin juuri luomallasi Azure AD -suojausryhmällä.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="ed7b1-112">Tilin on oltava käyttöoikeus, jotta se voi tarkastella Azure AD -suojausryhmää.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="ed7b1-113">Konfiguroi sähköisen kaupankäynnin sivusto suorittamalla määritysvaiheet.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="ed7b1-114">Kun olet valmistellut sähköisen kaupankäynnin komponentit, suojausryhmän pitäisi nyt näkyä valintaikkunan vaihtoehtona.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="ed7b1-115">Jotta voit varmistaa, että valintaikkunan kenttään tulee suojausryhmien luettelo, paina **Enter** sen jälkeen, kun olet kirjoittanut luomasi Azure AD- suojausryhmän nimen.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="ed7b1-116">Hakutulokset luetteloivat kaikki hakutekstillä alkavat Azure AD -suojausryhmät, joihin käyttäjällä on käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="ed7b1-117">Voit käyttää lyhyempää hakutermiä, kun haluat sallia laajemmat hakutulokset.</span><span class="sxs-lookup"><span data-stu-id="ed7b1-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed7b1-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ed7b1-118">Additional resources</span></span>

[<span data-ttu-id="ed7b1-119">Perusryhmän luominen ja jäsenten Azure Active Directoryn avulla</span><span class="sxs-lookup"><span data-stu-id="ed7b1-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="ed7b1-120">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="ed7b1-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
