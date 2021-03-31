---
title: Määritä toimittajan laskutuskäytännöt
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajan laskutuskäytännöt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 678ef8f0b7df00aec615af26cbcadec984331060
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220056"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="84684-103">Määritä toimittajan laskutuskäytännöt</span><span class="sxs-lookup"><span data-stu-id="84684-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="84684-104">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajan laskutuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="84684-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="84684-105">Toimittajan laskukäytännöt suoritetaan, kun toimittajan lasku kirjataan Toimittajan lasku -sivun avulla ja kun Toimittajan laskukäytäntöjen rikkeet -sivu avataan.</span><span class="sxs-lookup"><span data-stu-id="84684-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="84684-106">Voit myös määrittää toimittajan laskun työnkulun, kun haluat suorittaa toimittajan laskukäytännöt aina, kun lasku lähetetään työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="84684-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="84684-107">Toimittajan laskukäytännöt eivät koske laskurekisteriin tai laskukirjauskansioon luotuja laskuja.</span><span class="sxs-lookup"><span data-stu-id="84684-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="84684-108">Laskun täsmäytyksen vahvistuksessa ei käytetä toimittajan laskukäytäntöjä, vaan Ostoreskontran parametrit -määritettyjä käytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="84684-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="84684-109">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="84684-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="84684-110">Nämä vaiheet suorittaa ostoreskontran esimies tai laskentapäällikön rooli.</span><span class="sxs-lookup"><span data-stu-id="84684-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="84684-111">Varmista ennen aloittamista, että laskun täsmäytyksen konfigurointiavain on valittuna.</span><span class="sxs-lookup"><span data-stu-id="84684-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="84684-112">Toimittajan laskujen käytäntöjen luomisen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="84684-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="84684-113">Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra > Asetukset > Ostoreskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="84684-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="84684-114">Valitse **Laskun oikeellisuustarkistus** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="84684-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="84684-115">Valitse **Päivitetäänkö laskun otsikon tila automaattisesti** -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="84684-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="84684-116">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="84684-116">Select **OK**.</span></span>
5. <span data-ttu-id="84684-117">Valitse **Kirjaa lasku, jossa on ristiriitoja** -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="84684-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="84684-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="84684-118">Close the page.</span></span>
7. <span data-ttu-id="84684-119">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="84684-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="84684-120">Valitse **Parametrit**.</span><span class="sxs-lookup"><span data-stu-id="84684-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="84684-121">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="84684-121">Select **Add**.</span></span>
10. <span data-ttu-id="84684-122">Palaa kotisivulle sulkemalla sivu.</span><span class="sxs-lookup"><span data-stu-id="84684-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="84684-123">Toimittajan laskujen käytäntösääntöjen tyyppien luominen</span><span class="sxs-lookup"><span data-stu-id="84684-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="84684-124">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytäntösääntöjen tyypit**.</span><span class="sxs-lookup"><span data-stu-id="84684-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="84684-125">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="84684-125">Select **New**.</span></span>
3. <span data-ttu-id="84684-126">Kirjoita arvot **Säännön nimi**- ja **Kuvaus**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="84684-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="84684-127">Avaa haku valitsemalla **Kyselyn nimi**-kentässä avattavan valikon painike ja valitse haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="84684-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="84684-128">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="84684-128">Select **Save**.</span></span>
6. <span data-ttu-id="84684-129">Palaa kotisivulle sulkemalla sivu.</span><span class="sxs-lookup"><span data-stu-id="84684-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="84684-130">Toimittajan laskujen käytännön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="84684-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="84684-131">Siirry siirtymisruudussa kohtaan **Moduulit > Ostoreskontra > Käytännön asetukset > Toimittajan laskukäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="84684-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="84684-132">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="84684-132">Select **New**.</span></span>
3. <span data-ttu-id="84684-133">Kirjoita arvot **Nimi**- ja **Kuvaus**-kenttiin.</span><span class="sxs-lookup"><span data-stu-id="84684-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="84684-134">Laajenna tai tiivistä **Käytännön organisaatiot** -osa.</span><span class="sxs-lookup"><span data-stu-id="84684-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="84684-135">Valitse puussa solmu **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="84684-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="84684-136">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="84684-136">Select **Add**.</span></span>
7. <span data-ttu-id="84684-137">Laajenna tai tiivistä **Käytäntösäännöt**-osa.</span><span class="sxs-lookup"><span data-stu-id="84684-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="84684-138">Valitse **Luo käytäntösääntö**.</span><span class="sxs-lookup"><span data-stu-id="84684-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="84684-139">Kirjoita **Käytäntösäännön kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="84684-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="84684-140">Valitse **Suodata**.</span><span class="sxs-lookup"><span data-stu-id="84684-140">Select **Filter**.</span></span>
11. <span data-ttu-id="84684-141">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="84684-141">Select **Add**.</span></span> <span data-ttu-id="84684-142">Valitse haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="84684-142">Select the desired record.</span></span>
12. <span data-ttu-id="84684-143">Valitse tai kirjoita kentissä **Taulu**, **Johdettu taulu** ja **Kenttä** arvot avattavista valikoista.</span><span class="sxs-lookup"><span data-stu-id="84684-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="84684-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="84684-144">Close the page.</span></span>
14. <span data-ttu-id="84684-145">Kirjoita arvo **Ehdot**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="84684-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="84684-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="84684-146">Select **OK**.</span></span>
16. <span data-ttu-id="84684-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="84684-147">Select **OK**.</span></span>
17. <span data-ttu-id="84684-148">Palaa kotisivulle sulkemalla sivut.</span><span class="sxs-lookup"><span data-stu-id="84684-148">Close the pages to return to the home page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]