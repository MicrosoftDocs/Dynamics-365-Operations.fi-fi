---
title: Etujen hallinnan parametrien määrittäminen yrityskohtaisesti
description: Määritä etujen hallinnan parametrit yrityskohtaisesti Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805655"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="66aa9-103">Etujen hallinnan parametrien määrittäminen yrityskohtaisesti</span><span class="sxs-lookup"><span data-stu-id="66aa9-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="66aa9-104">Jokaiselle etuja tarjoavalle yritykselle on määritettävä asetukset etujen vahvistussähköposteja varten.</span><span class="sxs-lookup"><span data-stu-id="66aa9-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="66aa9-105">Vahvistussähköpostiasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="66aa9-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="66aa9-106">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="66aa9-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="66aa9-107">Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="66aa9-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="66aa9-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="66aa9-108">Field</span></span> | <span data-ttu-id="66aa9-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="66aa9-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="66aa9-110">**Lähetä vahvistussähköposti**</span><span class="sxs-lookup"><span data-stu-id="66aa9-110">**Send confirmation email**</span></span> | <span data-ttu-id="66aa9-111">Kun tämä toiminto on käytössä, vahvistussähköposti lähetetään työntekijöille näiden poistuessa etuihin rekisteröitymisen kokemuksesta työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="66aa9-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="66aa9-112">**Vahvistussähköpostin malli**</span><span class="sxs-lookup"><span data-stu-id="66aa9-112">**Confirmation email template**</span></span> | <span data-ttu-id="66aa9-113">Valitse organisaation sähköpostiviestimalli, jota käytetään rekisteröitymisvahvistuksen lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="66aa9-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="66aa9-114">Jos et valitse mallia, lähetetään seuraavat yleiset sähköpostiviestit:</span><span class="sxs-lookup"><span data-stu-id="66aa9-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="66aa9-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="66aa9-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="66aa9-116">Onnittelut!</span><span class="sxs-lookup"><span data-stu-id="66aa9-116">Congratulations!</span></span> <span data-ttu-id="66aa9-117">Etuihin rekisteröityminen onnistui.</span><span class="sxs-lookup"><span data-stu-id="66aa9-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="66aa9-118">Kiitos,</span><span class="sxs-lookup"><span data-stu-id="66aa9-118">Thank you,</span></span><br><span data-ttu-id="66aa9-119"><Yrityksen/organisaation nimi> - edut.</span><span class="sxs-lookup"><span data-stu-id="66aa9-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="66aa9-120">**Lähettäjän oletussähköpostiosoite**</span><span class="sxs-lookup"><span data-stu-id="66aa9-120">**Default email sender address**</span></span> | <span data-ttu-id="66aa9-121">Sähköpostiosoite, jota käytetään vahvistussähköpostiviestin lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="66aa9-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="66aa9-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="66aa9-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]