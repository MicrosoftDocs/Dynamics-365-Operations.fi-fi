---
title: Loma- ja poissaoloparametrien määrittäminen
description: Määritä henkilöstöhallinnon parametrit lomaa ja poissaoloa varten Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008865"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="2f687-103">Loma- ja poissaoloparametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2f687-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="2f687-104">Ennen kuin määrität loma- ja poissaolosuunnitelmat Dynamics 365 Human Resources -ohjelmassa, kannattaa tarkistaa kaikkien liittyvien henkilöstöparametrien asetukset, kuten esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="2f687-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="2f687-105">Lomapyyntöjen numerosarja</span><span class="sxs-lookup"><span data-stu-id="2f687-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="2f687-106">Perhe- ja sairauspoissaolon säädös (FMLA) -asetukset</span><span class="sxs-lookup"><span data-stu-id="2f687-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="2f687-107">Työntekijän itsepalvelun asetukset loma- ja poissaolopyynnöille</span><span class="sxs-lookup"><span data-stu-id="2f687-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="2f687-108">Loman ja poissaolon parametrit</span><span class="sxs-lookup"><span data-stu-id="2f687-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="2f687-109">Tarkastele ja muuta henkilöstöparametreja</span><span class="sxs-lookup"><span data-stu-id="2f687-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="2f687-110">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2f687-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2f687-111">Valitse **Määritys**-kohdasta **Henkilöstöparametrit**.</span><span class="sxs-lookup"><span data-stu-id="2f687-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="2f687-112">Tarkista **Numerosarjat**-välilehdessä **Numerosarjakoodi** **Lomapyynnön tunnusta** varten ja muuta tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2f687-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="2f687-113">Tämä asetus määrittää järjestyksen, jota käytetään automaattisesti, kun tunnuksia annetaan lomapyyntöjä varten.</span><span class="sxs-lookup"><span data-stu-id="2f687-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="2f687-114">Tarkista **FMLA**-välilehdessä FMLA-asetukset ja muuta niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2f687-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="2f687-115">Määritä **Työntekijän itsepalvelu** -välilehdessä, voivatko esimiehet kirjoittaa loma- ja poissaolopyyntöjä työntekijöidensä puolesta.</span><span class="sxs-lookup"><span data-stu-id="2f687-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="2f687-116">Tarkista **Loma ja poissaolo** -välilehdessä asetukset ja muuta niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2f687-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="2f687-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2f687-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="2f687-118">Määritä kalenteriparametrit</span><span class="sxs-lookup"><span data-stu-id="2f687-118">Configure calendar parameters</span></span>

<span data-ttu-id="2f687-119">Jos olet ottanut loma- ja poissaolokalenterin esikatselutoiminnon käyttöön, sinun on määritettävä lisäparametrit.</span><span class="sxs-lookup"><span data-stu-id="2f687-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="2f687-120">Helmikuun 3. 2020 -versiossa vain **Odottavat lomapyynnöt** ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="2f687-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="2f687-121">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2f687-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2f687-122">Valitse **Määritys**-kohdasta **Henkilöstöparametrit**.</span><span class="sxs-lookup"><span data-stu-id="2f687-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="2f687-123">Muuta **Kalenteri**-välilehdessä asetukset tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2f687-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="2f687-124">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2f687-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f687-125">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="2f687-125">See also</span></span>

- [<span data-ttu-id="2f687-126">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="2f687-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
