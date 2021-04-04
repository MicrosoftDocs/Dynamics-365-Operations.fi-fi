---
title: Tietuemallin luonti helpottamaan tietojen kirjaamista
description: Tässä ohjeessa kerrotaan, miten voit luoda tietuemallin, jolloin usein käytettyjen kenttien arvoja ei tarvitse lisätä erikseen kussakin uudessa tietueessa.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d50dbb161fca0b0bfda18a258e5cef03e43fbeb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561095"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="18693-103">Tietuemallin luonti helpottamaan tietojen kirjaamista</span><span class="sxs-lookup"><span data-stu-id="18693-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18693-104">Tässä ohjeessa kerrotaan, miten voit luoda tietuemallin, jolloin usein käytettyjen kenttien arvoja ei tarvitse lisätä erikseen kussakin uudessa tietueessa.</span><span class="sxs-lookup"><span data-stu-id="18693-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="18693-105">Tässä menettelyssä luodaan uusi tietue uusille käyttöomaisuuteen lisättäville kannettaville.</span><span class="sxs-lookup"><span data-stu-id="18693-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="18693-106">Tässä menettelyssä käytetään USMF-malliyritystä.</span><span class="sxs-lookup"><span data-stu-id="18693-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="18693-107">Siirry siirtymisruudussa kohtaan **Moduulit > Käyttöomaisuuserät > Käyttöomaisuuserät > Käyttöomaisuuserät**.</span><span class="sxs-lookup"><span data-stu-id="18693-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="18693-108">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="18693-108">Select **New**.</span></span>
3. <span data-ttu-id="18693-109">Syötä tai valitse arvo **Käyttöomaisuusryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="18693-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="18693-110">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18693-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="18693-111">Kirjoita esimerkiksi **Yritysliidi, kannettava**.</span><span class="sxs-lookup"><span data-stu-id="18693-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="18693-112">Kirjoita arvo **Hakunimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18693-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="18693-113">Kirjoita esimerkiksi **kannettava**.</span><span class="sxs-lookup"><span data-stu-id="18693-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="18693-114">Laajenna **Teknistä tietoa** -osa.</span><span class="sxs-lookup"><span data-stu-id="18693-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="18693-115">Kirjoita arvot kenttiin **Valmistaja**, **Malli** ja **Mallin vuosi**.</span><span class="sxs-lookup"><span data-stu-id="18693-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="18693-116">Valitse toimintoruudussa **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="18693-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="18693-117">Valitse **Tietueen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="18693-117">Select **Record info**.</span></span>
10. <span data-ttu-id="18693-118">Valitse **Käyttäjämalli**.</span><span class="sxs-lookup"><span data-stu-id="18693-118">Select **User template**.</span></span>
11. <span data-ttu-id="18693-119">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="18693-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="18693-120">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="18693-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="18693-121">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="18693-121">Select **OK**.</span></span>
14. <span data-ttu-id="18693-122">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="18693-122">Select **Close**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]