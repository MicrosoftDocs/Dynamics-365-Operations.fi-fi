---
title: Asiakkaan työnkulku
description: Tässä ohjeaiheessa on tietoja asiakkaan työnkulusta. Muutat tietyt kentät asiakkaalle ja lähetät muutokset sen jälkeen hyväksyttäviksi työnkulkua käyttämällä ennen kuin ne lisätään asiakkaan nimiin.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1b0e1621b256e6bbb42f97134b87dd65fa146193
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "302225"
---
# <a name="customer-workflow"></a><span data-ttu-id="0250c-104">Asiakkaan työnkulku</span><span class="sxs-lookup"><span data-stu-id="0250c-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0250c-105">Asiakkaan työnkulku on lisätty Microsoft Dynamics 365 for Finance and Operations -ohjelman versioon 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="0250c-105">The customer workflow has been added to Microsoft Dynamics 365 for Finance and Operations version 8.0.4.</span></span> <span data-ttu-id="0250c-106">Voit muuttaa tietyt kentät asiakkaalle ja lähettää muutokset sen jälkeen hyväksyttäviksi työnkulkua käyttämällä ennen kuin ne lisätään asiakkaan nimiin.</span><span class="sxs-lookup"><span data-stu-id="0250c-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="0250c-107">Määritä asiakkaan työnkulku</span><span class="sxs-lookup"><span data-stu-id="0250c-107">Set up the customer workflow</span></span>

<span data-ttu-id="0250c-108">Ennen kuin käytät asiakkaan työnkulku -toimintoa, sinun on otettava se käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0250c-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="0250c-109">Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="0250c-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="0250c-110">**Yleiset** -välilehdellä **asiakkaan hyväksyntä** -pikavälilehdellä, määritä **Ota käyttöön asiakkaan hyväksynnät** -asetukseksi **Kyllä** ottaaksesi ominaisuuden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0250c-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="0250c-111">Valitse **Tietoyksikön toiminnot**, -kenttä, valitse toiminto, jota tietoyksikköjen pitäisi käyttää tietoja tuotaessa:</span><span class="sxs-lookup"><span data-stu-id="0250c-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="0250c-112">**Salli muutokset hyväksymättä** – Toimija voi päivittää asiakastietueen käsittelemättä sitä työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="0250c-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="0250c-113">**Hylkää muutokset** – Asiakastietueeseen ei voi tehdä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="0250c-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="0250c-114">Tuonti ei onnistu kentille, jotka ovat käytössä työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="0250c-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="0250c-115">**Luo muutosehdotuksia** -Kaikki kentät muutetaan lukuun ottamatta työnkulussa käytössä olevia kenttiä.</span><span class="sxs-lookup"><span data-stu-id="0250c-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="0250c-116">Näiden kenttien uudet arvot lisätään asiakkaalle ehdotettuina muutoksina, ja työnkulku käynnistyy automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="0250c-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="0250c-117">Valitse sitten asiakkaan kenttien luettelossa **Ota käyttöön** -valintaruutu jokaiseen kenttään, joka on hyväksyttävä ennen kuin muutokset voidaan tehdä.</span><span class="sxs-lookup"><span data-stu-id="0250c-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="0250c-118">Valitse **Myyntireskontra \> Asetukset \> Myyntireskontran työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="0250c-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="0250c-119">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0250c-119">Select **New**.</span></span>
7. <span data-ttu-id="0250c-120">Valitse **Ehdotettu asiakkaan muutoksen työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="0250c-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="0250c-121">Määritä työnkulku siten, että se sopii yrityksesi hyväksyntäprosessiin.</span><span class="sxs-lookup"><span data-stu-id="0250c-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="0250c-122">**Työnkulun hyväksyntä ehdotetulle asiakkaan muutokselle** -työnkulun hyväksyntäelementti lisää muutokset asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="0250c-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="0250c-123">Muuta asiakastietoja ja lähetä muutokset työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="0250c-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="0250c-124">Kun muutat kenttää, joka on käytössä työnkulussa, **Ehdotetut muutokset** -sivu tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="0250c-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="0250c-125">Tämä sivu näyttää sekä alkuperäisen kentän arvon että uuden kirjoittamasi kentän arvon.</span><span class="sxs-lookup"><span data-stu-id="0250c-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="0250c-126">Kenttä, johon olet tehnyt muutoksia, on palautettu alkuperäiseen arvoonsa.</span><span class="sxs-lookup"><span data-stu-id="0250c-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="0250c-127">Sivulla oleva tilailmoitus  kertoo, että tekemiäsi muutoksia ei ole lähetetty.</span><span class="sxs-lookup"><span data-stu-id="0250c-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="0250c-128">Aina kun muutat kenttää, joka on käytössä työnkulussa, kyseinen kenttä lisätään ehdotettujen muutosten luetteloon.</span><span class="sxs-lookup"><span data-stu-id="0250c-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="0250c-129">Hylätäksesi ehdotetun kentän arvon käytä **Hylkää**-painiketta luettelosta kentän vieressä.</span><span class="sxs-lookup"><span data-stu-id="0250c-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="0250c-130">Hylätäksesi kaikki muutokset käytä **Hylkää kaikki muutokset** -painiketta sivun alareunassa.</span><span class="sxs-lookup"><span data-stu-id="0250c-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="0250c-131">Valitse **OK** sulkeaksesi sivun.</span><span class="sxs-lookup"><span data-stu-id="0250c-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="0250c-132">Kun sinulla on vähintään yksi ehdotettu muutos, kaksi uutta valikkoa tulee näkyviin Toimintopaneelissa: **Ehdotetut muutokset** ja **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="0250c-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="0250c-133">Valitse **Ehdotetut muutokset** avataksesi **Ehdotetut muutokset** -sivun ja tarkistaaksesi muutoksesi.</span><span class="sxs-lookup"><span data-stu-id="0250c-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="0250c-134">Valitse **Työnkulku \> Lähetä** lähettääksesi Työnkulun muutokset.</span><span class="sxs-lookup"><span data-stu-id="0250c-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="0250c-135">Sivun tilaksi muutetaan **Hyväksymistä odottavat muutokset**.</span><span class="sxs-lookup"><span data-stu-id="0250c-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="0250c-136">Työnkulku noudattaa Finance and Operations -palvelun vakiotyönkulkuprosessia.</span><span class="sxs-lookup"><span data-stu-id="0250c-136">The workflow follows the standard workflow process in Finance and Operations.</span></span> <span data-ttu-id="0250c-137">Hyväksyjä ohjataan **Asiakas**-sivulle, jossa hän voi tarkastella muutoksia **Ehdotetut muutokset** -sivulla ja valita sitten **Työnkulku \> Hyväksy** hyväksyäkseen työnkulun.</span><span class="sxs-lookup"><span data-stu-id="0250c-137">The approver is directed to the **Customer** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="0250c-138">Kun kaikki hyväksynnät on käyty läpi, kentät päivitetään ehdottamillasi arvoilla.</span><span class="sxs-lookup"><span data-stu-id="0250c-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
