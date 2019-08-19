---
title: Toimittajan työnkulku
description: Muokkaa toimittajatietojen ja hyväksy ne työnkulun avulla.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 112f9d6adeee583a63da8ab700d7adc179de2c1d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835307"
---
# <a name="vendor-workflow"></a><span data-ttu-id="4b8ca-103">Toimittajan työnkulku</span><span class="sxs-lookup"><span data-stu-id="4b8ca-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b8ca-104">Toimittajan työnkulkua käytettäessä tiettyihin kenttiin tehdyt muutokset lähetään työnkulkuun hyväksyttäväksi, ennen kuin ne lisätään toimittajaan.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="4b8ca-105">Toimittajan työnkulun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4b8ca-105">Set up the vendor workflow</span></span>

<span data-ttu-id="4b8ca-106">Ennen kuin voit käyttää työnkulkuominaisuutta, se on otettava käyttöön.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="4b8ca-107">Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="4b8ca-108">Määritä **Yleinen**-välilehden **Toimittajan hyväksyntä** -pikavälilehdessä **Ota toimittajan hyväksynnät käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="4b8ca-109">Valitse **Tietoyksikön toiminnot** -kentässä toiminto, jota on käytettävä tietoja tuotaessa:</span><span class="sxs-lookup"><span data-stu-id="4b8ca-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="4b8ca-110">**Salli muutokset hyväksymättä** – Tietoyksikkö voi päivittää toimittajatietueen ilman, että se käsitellään työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="4b8ca-111">**Hylkää muutokset** – Toimittajatietueeseen ei voi tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="4b8ca-112">Työnkulkua varten käyttöönotettujen kenttien tuonti epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="4b8ca-113">**Luo muutosehdotuksia** – Kaikki muut paitsi työnkulussa käytössä olevat kentät muutetaan.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="4b8ca-114">Näiden kenttien uudet arvot lisätään toimittajille ehdotettuina muutoksina ja työnkulku käynnistyy automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="4b8ca-115">Valitse sitten toimittajan kenttien luettelossa **Ota käyttöön** -valintaruutu jokaisessa kentässä, joka on hyväksyttävä ennen kuin muutokset voidaan tehdä.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="4b8ca-116">Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran työnkulut**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="4b8ca-117">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-117">Select **New**.</span></span>
7. <span data-ttu-id="4b8ca-118">Valitse **Ehdotettu toimittajan muutosten työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="4b8ca-119">Määritä työnkulku siten, että se vastaa hyväksyntäprosessia.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="4b8ca-120">**Työnkulun hyväksyntä ehdotetulle toimittajan muutokselle** -työnkulun hyväksyntäelementti lisää muutokset toimittajaan.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="4b8ca-121">Toimittajatietojen muuttaminen ja muutosten lähettäminen työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="4b8ca-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="4b8ca-122">Kun muutat kenttää, joka on käytössä työnkulussa, **Ehdotetut muutokset** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="4b8ca-123">Tämä sivu näyttää sekä alkuperäisen kentän arvon että uuden kirjoittamasi kentän arvon.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="4b8ca-124">Alkuperäinen arvo on palautettu kenttään, johon olet tehnyt muutoksia.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="4b8ca-125">Tilailmoitus ilmaisee myös, että tekemiäsi muutoksia ei ole lähetetty.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="4b8ca-126">Aina kun muutat kenttää, joka on käytössä työnkulussa, kyseinen kenttä lisätään **Ehdotetut muutokset** -sivulla olevaan luetteloon.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="4b8ca-127">Hylkää ehdotetun kentän arvo kentän vieressä olevalla **Hylkää**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="4b8ca-128">Hylkää kaikki muutokset sivun alareunassa olevalla **Hylkää kaikki muutokset** -painikkeella.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="4b8ca-129">Sulje sivu valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="4b8ca-130">Kun sinulla on vähintään yksi ehdotettu muutos, kaksi uutta välilehteä tukee toimintopaneeliin: **Ehdotetut muutokset** ja **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="4b8ca-131">Avaa **Ehdotetut muutokset** -sivu ja tarkista muutokset valitsemalla **Ehdotetut muutokset**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="4b8ca-132">Lähetä muutoksen työnkulkuun valitsemalla **Työnkulku \> Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="4b8ca-133">Sivun tilaksi muutetaan **Hyväksymistä odottavat muutokset**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="4b8ca-134">Työnkulku noudattaa Microsoft Dynamics 365 for Finance and Operationsin vakiotyönkulkua.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="4b8ca-135">Hyväksyjä ohjataan **Toimittaja**-sivulle, jossa hän voi tarkastella muutoksia **Ehdotetut muutokset** -sivulla ja hyväksyä sitten työnkulun valitsemalla **Työnkulku \> Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="4b8ca-136">Kun kaikki hyväksynnät on käyty läpi, kentät päivitetään ehdottamillasi arvoilla.</span><span class="sxs-lookup"><span data-stu-id="4b8ca-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
