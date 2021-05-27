---
title: Henkilökohtaisten tietojen muokkaamisen rajoittaminen
description: Estä työntekijöitä muokkaamasta yhteystietoja Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e3eeb66d4f32b1fea1a43fff9f5b09d87d1f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018706"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="1030b-103">Henkilökohtaisten tietojen muokkaamisen rajoittaminen</span><span class="sxs-lookup"><span data-stu-id="1030b-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="1030b-104">Tässä aiheessa kuvataan, kuinka työntekijöitä voi estää muokkaamasta yhteystietoja Dynamics 365 Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="1030b-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1030b-105">Saatat haluta estää työntekijöitä muokkaamasta tiettyjä yhteystietoja, kuten yrityksen sijaintia tai sähköpostiosoitetta.</span><span class="sxs-lookup"><span data-stu-id="1030b-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="1030b-106">Ennen kuin voit käyttää tätä ominaisuutta, sinun täytyy ottaa käyttöön **(Esikatselu) Estä työntekijöitä lisäämästä tai muokkaamasta osoite- ja yhteystietoja tiettyihin tarkoituksiin** -ominaisuus käyttöön ominaisuuksien hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="1030b-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="1030b-107">Lisätietoja esiversiotoimintojen käyttöönotosta on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="1030b-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="1030b-108">![Ota esikatselutoiminto käyttöön](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="1030b-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="1030b-109">Valitse tiedot, jotka työntekijä voi lisätä tai muokata</span><span class="sxs-lookup"><span data-stu-id="1030b-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="1030b-110">Valitse Human Resourcesissa ensin **Henkilöstön hallinta**, sitten **Linkit** ja lopuksi **Henkilöstöhallintoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="1030b-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Valitse Henkilöstöhallintoparametrit](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="1030b-112">Valitse **Henkilöstöhallintoparametrit** -sivulta **Työntekijän itsepalvelu** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="1030b-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Valitse Työntekijän itsepalvelu](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="1030b-114">Poista **Työntekijän itsepalvelu** -välilehden **Osoite- ja yhteystiedot** -osiosta kaikkien niiden tietojen valinta, joita et halua työntekijöiden lisäävän tai muokkaavan.</span><span class="sxs-lookup"><span data-stu-id="1030b-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="1030b-115">Tässä esimerkissä olemme poistaneet **yrityksen** yhteystietojen valinnan.</span><span class="sxs-lookup"><span data-stu-id="1030b-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![Yrityksen yhteystietojen muokkaamisen rajoittaminen](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="1030b-117">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="1030b-117">Select **Save**.</span></span>

   ![Tallenna muutokset](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="1030b-119">Työntekijäkokemus</span><span class="sxs-lookup"><span data-stu-id="1030b-119">Employee experience</span></span>

<span data-ttu-id="1030b-120">Kun olet estänyt työntekijöitä lisäämästä tai muokkaamasta yhteystietoja, he näkevät kyseiset tiedot, mutta eivät voi muuttaa niitä.</span><span class="sxs-lookup"><span data-stu-id="1030b-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="1030b-121">Tässä esimerkissä työntekijöitä on estetty muokkaamasta **yrityksen** yhteystietoja, mutta he voivat silti nähdä työntekijän itsepalvelun tiedot:</span><span class="sxs-lookup"><span data-stu-id="1030b-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![Yrityksen yhteystietojen tarkasteleminen](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="1030b-123">Kun työntekijät valitsevat yrityksen yhteystiedot, he näkevät **Muokkaa osoitetta** -ruudun Vain luku -tilassa eivätkä he voi muuttaa kenttiä.</span><span class="sxs-lookup"><span data-stu-id="1030b-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![Yrityksen yhteystiedot näytetään Vain luku -muodossa](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="1030b-125">Jos he lisäävät uuden osoitteen valitsemalla **Lisää**, he eivät voi valita **Yritys**-vaihtoehtoa **Tarkoitus**-pudotusvalikosta.</span><span class="sxs-lookup"><span data-stu-id="1030b-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Työntekijä ei voi lisätä yrityksen osoitetta](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="1030b-127">Työntekijöillä on sama kokemus, kun he valitsevat **Henkilökohtaiset tiedot** -sivulta **Yhteystiedot** ja lisäävät uuden osoitteen.</span><span class="sxs-lookup"><span data-stu-id="1030b-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="1030b-128">**Tarkoitus**-pudotusvalikossa näytetään vain sentyyppiset tiedot, joita he voivat lisätä.</span><span class="sxs-lookup"><span data-stu-id="1030b-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Työntekijä ei voi valita Yritys-vaihtoehtoa Tarkoitus-pudotusvalikosta](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="1030b-130">**Tarkoitus** näytetään nyt **Yhteystiedot**-ruudukossa.</span><span class="sxs-lookup"><span data-stu-id="1030b-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![Tarkoitus näytetään Yhteystiedot-ruudukossa](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="1030b-132">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="1030b-132">See also</span></span>

[<span data-ttu-id="1030b-133">Työntekijän ja esimiehen itsepalvelun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="1030b-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="1030b-134">Määritä Human Resourcesin parametrit</span><span class="sxs-lookup"><span data-stu-id="1030b-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="1030b-135">Muokkaa henkilökohtaisia tietoja</span><span class="sxs-lookup"><span data-stu-id="1030b-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)