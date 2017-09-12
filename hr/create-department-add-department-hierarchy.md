---
title: "Osaston luonti ja sen liittäminen osastohierarkiaan"
description: "Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta. Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta. Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin. Osastot voivat olla tulosvastuullisia."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: adf3dbf8b7ffa906c872a6b66d9cb43eb8e02805
ms.contentlocale: fi-fi
ms.lasthandoff: 06/29/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a><span data-ttu-id="d3f08-106">Osaston luonti ja sen liittäminen osastohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="d3f08-106">Create a department and associate it with the department hierarchy</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="d3f08-107">Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="d3f08-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d3f08-108">Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.</span><span class="sxs-lookup"><span data-stu-id="d3f08-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d3f08-109">Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin.</span><span class="sxs-lookup"><span data-stu-id="d3f08-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d3f08-110">Osastot voivat olla tulosvastuullisia.</span><span class="sxs-lookup"><span data-stu-id="d3f08-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d3f08-111">Osasto voi sisältää kustannuspaikkaryhmän.</span><span class="sxs-lookup"><span data-stu-id="d3f08-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="d3f08-112">Osastoille voidaan määrittää toimia.</span><span class="sxs-lookup"><span data-stu-id="d3f08-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="d3f08-113">Luo osasto valitsemalla **Henkilöstöhallinto** &gt; **Osastot** &gt; **Osasto**.</span><span class="sxs-lookup"><span data-stu-id="d3f08-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="d3f08-114">Seuraavassa taulukossa näkyvät valittavina olevat kentät.</span><span class="sxs-lookup"><span data-stu-id="d3f08-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="d3f08-115">Kenttä</span><span class="sxs-lookup"><span data-stu-id="d3f08-115">Field</span></span>               | <span data-ttu-id="d3f08-116">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d3f08-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f08-117">Nimi</span><span class="sxs-lookup"><span data-stu-id="d3f08-117">Name</span></span>                | <span data-ttu-id="d3f08-118">Kirjoita osaston nimi.</span><span class="sxs-lookup"><span data-stu-id="d3f08-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="d3f08-119">Osaston numero</span><span class="sxs-lookup"><span data-stu-id="d3f08-119">Department number</span></span>   | <span data-ttu-id="d3f08-120">Oletusarvo voidaan luoda automaattisesti, jos numerosarjakoodi on määritetty **Organisaatiotunnus**-viitteeseen **Numerojärjestykset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="d3f08-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="d3f08-121">Hakunimi</span><span class="sxs-lookup"><span data-stu-id="d3f08-121">Search name</span></span>         | <span data-ttu-id="d3f08-122">Kirjoita lyhyt nimi tai lyhenne, jota voidaan käyttää osaston haussa.</span><span class="sxs-lookup"><span data-stu-id="d3f08-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="d3f08-123">Muistio</span><span class="sxs-lookup"><span data-stu-id="d3f08-123">Memo</span></span>                | <span data-ttu-id="d3f08-124">Anna mahdolliset lisätiedot tässä.</span><span class="sxs-lookup"><span data-stu-id="d3f08-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="d3f08-125">Hierarkiassa</span><span class="sxs-lookup"><span data-stu-id="d3f08-125">In hierarchy</span></span>        | <span data-ttu-id="d3f08-126">Valittuna oleva valintaruutu ilmaisee, että osasto on mukana osastohierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="d3f08-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="d3f08-127">Jos haluat tietoja siitä, miten osasto lisätään osastohierarkiaan, ks. tässä artikkelissa myöhemmin annettavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="d3f08-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="d3f08-128">DUNS-numero</span><span class="sxs-lookup"><span data-stu-id="d3f08-128">DUNS number</span></span>         | <span data-ttu-id="d3f08-129">DUNS on lyhenne englanninkielisistä sanoista Data Universal Number System.</span><span class="sxs-lookup"><span data-stu-id="d3f08-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="d3f08-130">Tämä on yhdeksännumeroinen luku, jonka myöntää Dun & Bradstreet.</span><span class="sxs-lookup"><span data-stu-id="d3f08-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="d3f08-131">Esimies</span><span class="sxs-lookup"><span data-stu-id="d3f08-131">Manager</span></span>             | <span data-ttu-id="d3f08-132">Valitse henkilö, joka johtaa osastoa.</span><span class="sxs-lookup"><span data-stu-id="d3f08-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="d3f08-133">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="d3f08-133">Addresses</span></span>           | <span data-ttu-id="d3f08-134">Lisää osaston osoitetiedot.</span><span class="sxs-lookup"><span data-stu-id="d3f08-134">Add the address information for the department.</span></span> <span data-ttu-id="d3f08-135">Lisää esimerkiksi postitusosoite rakennukselle, jossa osasto sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="d3f08-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="d3f08-136">Yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="d3f08-136">Contact information</span></span> | <span data-ttu-id="d3f08-137">Lisää osaston yhteystiedot.</span><span class="sxs-lookup"><span data-stu-id="d3f08-137">Add contact information for the department.</span></span> <span data-ttu-id="d3f08-138">Lisää esimerkiksi osaston palvelupisteen puhelinnumero.</span><span class="sxs-lookup"><span data-stu-id="d3f08-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="d3f08-139">Voit lisätä osaston osastohierarkiaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d3f08-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="d3f08-140">Valitse **Henkilöstöhallinto** &gt; **Osastot** &gt; **Osastohierarkia**.</span><span class="sxs-lookup"><span data-stu-id="d3f08-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="d3f08-141">Valitse **Muokkaa**, ja valitse sitten organisaatio, jonka alle osasto kuuluu.</span><span class="sxs-lookup"><span data-stu-id="d3f08-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="d3f08-142">Napsauta **Lisää**, ja valitse luettelosta **Osasto**.</span><span class="sxs-lookup"><span data-stu-id="d3f08-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="d3f08-143">Valitse näkyviin tulevasta luettelosta hierarkiaan lisättävä osasto.</span><span class="sxs-lookup"><span data-stu-id="d3f08-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="d3f08-144">Tallenna muutokset.</span><span class="sxs-lookup"><span data-stu-id="d3f08-144">Save your changes.</span></span> <span data-ttu-id="d3f08-145">Saat sanoman, että hierarkiasta on luotu luonnosversio.</span><span class="sxs-lookup"><span data-stu-id="d3f08-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="d3f08-146">Kun olet valmis, valitse **Julkaise** hierarkian suunnittelutoiminnossa.</span><span class="sxs-lookup"><span data-stu-id="d3f08-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="d3f08-147">Voit syöttää voimassaolopäivämäärän, joka ilmaisee, milloin hierarkia tulisi julkaista.</span><span class="sxs-lookup"><span data-stu-id="d3f08-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="d3f08-148">Jos esimerkiksi haluat lisätä uuden osaston seuraavan vuoden alusta, aseta voimaantulopäiväksi 1.1. seuraavana kalenterivuonna.</span><span class="sxs-lookup"><span data-stu-id="d3f08-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="d3f08-149">Hierarkian muutokset tulevat voimaan tuona päivänä.</span><span class="sxs-lookup"><span data-stu-id="d3f08-149">The changes to the hierarchy will take effect on that date.</span></span>





