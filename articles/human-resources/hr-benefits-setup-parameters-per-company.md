---
title: Etujen hallinnan parametrien määrittäminen yrityskohtaisesti
description: Määritä etujen hallinnan parametrit yrityskohtaisesti Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692742"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="7243f-103">Etujen hallinnan parametrien määrittäminen yrityskohtaisesti</span><span class="sxs-lookup"><span data-stu-id="7243f-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="7243f-104">Jokaiselle etuja tarjoavalle yritykselle on määritettävä asetukset etujen vahvistussähköposteja varten.</span><span class="sxs-lookup"><span data-stu-id="7243f-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="7243f-105">Vahvistussähköpostiasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7243f-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="7243f-106">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="7243f-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="7243f-107">Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="7243f-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="7243f-108">Kenttä</span><span class="sxs-lookup"><span data-stu-id="7243f-108">Field</span></span> | <span data-ttu-id="7243f-109">kuvaus</span><span class="sxs-lookup"><span data-stu-id="7243f-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7243f-110">**Lähetä vahvistussähköposti**</span><span class="sxs-lookup"><span data-stu-id="7243f-110">**Send confirmation email**</span></span> | <span data-ttu-id="7243f-111">Kun tämä toiminto on käytössä, vahvistussähköposti lähetetään työntekijöille näiden poistuessa etuihin rekisteröitymisen kokemuksesta työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="7243f-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="7243f-112">**Vahvistussähköpostin malli**</span><span class="sxs-lookup"><span data-stu-id="7243f-112">**Confirmation email template**</span></span> | <span data-ttu-id="7243f-113">Valitse organisaation sähköpostiviestimalli, jota käytetään rekisteröitymisvahvistuksen lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="7243f-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="7243f-114">Jos et valitse mallia, lähetetään seuraavat yleiset sähköpostiviestit:</span><span class="sxs-lookup"><span data-stu-id="7243f-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="7243f-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="7243f-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="7243f-116">Onnittelut!</span><span class="sxs-lookup"><span data-stu-id="7243f-116">Congratulations!</span></span> <span data-ttu-id="7243f-117">Etuihin rekisteröityminen onnistui.</span><span class="sxs-lookup"><span data-stu-id="7243f-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="7243f-118">Kiitos,</span><span class="sxs-lookup"><span data-stu-id="7243f-118">Thank you,</span></span><br><span data-ttu-id="7243f-119"><Yrityksen/organisaation nimi> - edut.</span><span class="sxs-lookup"><span data-stu-id="7243f-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="7243f-120">**Lähettäjän oletussähköpostiosoite**</span><span class="sxs-lookup"><span data-stu-id="7243f-120">**Default email sender address**</span></span> | <span data-ttu-id="7243f-121">Sähköpostiosoite, jota käytetään vahvistussähköpostiviestin lähettämisessä.</span><span class="sxs-lookup"><span data-stu-id="7243f-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="7243f-122">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7243f-122">Select **Save**.</span></span>