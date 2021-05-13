---
title: Työntekijät, joilla ei työsuhdetta
description: Työntekijät, joilla ei ole organisaatiossasi tulevia, aktiivisia tai historiallisia työtehtäviä, näkyvät Työntekijät, joilla ei ole työsuhdetta -lomakkeessa.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924568"
---
# <a name="workers-without-employment"></a><span data-ttu-id="313f8-103">Työntekijät, joilla ei työsuhdetta</span><span class="sxs-lookup"><span data-stu-id="313f8-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="313f8-104">Työntekijät, joilla ei ole organisaatiossasi tulevia, aktiivisia tai historiallisia työtehtäviä, näkyvät **Työntekijät, joilla ei ole työsuhdetta** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="313f8-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="313f8-105">Tämä tila voi tulla näkyviin työntekijän kohdalla, kun tuot työntekijöitä ilman työntekijän tietuetta tai kun poistat työntekijän työsuhteen kohdassa **Työntekijät > Työhistoria**.</span><span class="sxs-lookup"><span data-stu-id="313f8-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="313f8-106">Oletusarvon mukaan **Työntekijät, joilla ei ole työsuhdetta** -lomake on seuraavien roolien käytettävissä:</span><span class="sxs-lookup"><span data-stu-id="313f8-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="313f8-107">Henkilöstöapulainen</span><span class="sxs-lookup"><span data-stu-id="313f8-107">Human Resources Assistant</span></span>
- <span data-ttu-id="313f8-108">Henkilöstöpäällikkö</span><span class="sxs-lookup"><span data-stu-id="313f8-108">Human Resources Manager</span></span>
- <span data-ttu-id="313f8-109">Työhönottaja</span><span class="sxs-lookup"><span data-stu-id="313f8-109">Recruiter</span></span>
- <span data-ttu-id="313f8-110">Kompensaatioiden ja etujen päällikkö</span><span class="sxs-lookup"><span data-stu-id="313f8-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="313f8-111">Palkanlaskentakoordinaattori</span><span class="sxs-lookup"><span data-stu-id="313f8-111">Payroll Administrator</span></span>
- <span data-ttu-id="313f8-112">Palkanlaskentapäällikkö</span><span class="sxs-lookup"><span data-stu-id="313f8-112">Payroll Manager</span></span>
- <span data-ttu-id="313f8-113">Koulutuspäällikkö</span><span class="sxs-lookup"><span data-stu-id="313f8-113">Training Manager</span></span>

<span data-ttu-id="313f8-114">Voit poistaa **Työntekijät, joilla ei ole työsuhdetta** -luettelossa olevat henkilöt.</span><span class="sxs-lookup"><span data-stu-id="313f8-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="313f8-115">Oletusarvon mukaan tämä oikeus annetaan henkilöstöapulaisen roolille.</span><span class="sxs-lookup"><span data-stu-id="313f8-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="313f8-116">Voit antaa oikeuden muille rooleille seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="313f8-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="313f8-117">Valitse **Järjestelmän hallinta** ja valitse sitten **Suojauskonfiguraatio**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="313f8-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="313f8-118">Suodata **Oikeudet**-välilehdessä **Oikeudet**-luettelo ja **Ylläpidä työntekijöitä**.</span><span class="sxs-lookup"><span data-stu-id="313f8-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="313f8-119">[![Suodata Oikeudet-luettelo](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="313f8-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="313f8-120">Valitse **viitteet**-sarakkeesta **Näytä valikon vaihtoehdot**.</span><span class="sxs-lookup"><span data-stu-id="313f8-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="313f8-121">Valitse **Näytä valikon vaihtoehdot**-sarakkeesta **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="313f8-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="313f8-122">[![Valitse lomake](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="313f8-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="313f8-123">Määritä **Poisto**-oikeudeksi **Myönnä**.</span><span class="sxs-lookup"><span data-stu-id="313f8-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="313f8-124">Valitse **Julkaisemattomat objektit** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="313f8-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="313f8-125">Valitse **Julkaise kaikki**.</span><span class="sxs-lookup"><span data-stu-id="313f8-125">Select **Publish all**.</span></span>

   <span data-ttu-id="313f8-126">[![Julkaise muutokset](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="313f8-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]