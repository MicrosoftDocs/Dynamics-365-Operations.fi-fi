---
title: Huoltotuoterakenteen muokkaaminen
description: Huoltotuoterakenteen muokkaaminen.
author: YuyuScheller
manager: AnnBe
ms.date: 05/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5ebbcf3865d176c713d96bf90b819b8252e8087f
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---


# <a name="modify-a-service-bom"></a><span data-ttu-id="af27d-103">Huoltotuoterakenteen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="af27d-103">Modify a Service BOM</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="af27d-104">Voit kirjata elementin historian huollon tuoterakenteen sisällä.</span><span class="sxs-lookup"><span data-stu-id="af27d-104">You can record the history of an element in a service BOM.</span></span> <span data-ttu-id="af27d-105">Aina, kun päivität tuoterakenneriviä, **Historia**-ruutuun syntyy historiarivi.</span><span class="sxs-lookup"><span data-stu-id="af27d-105">Every time that you update a BOM line, a history line is created in the **History** pane.</span></span> <span data-ttu-id="af27d-106">Historiarivillä näkyy tuoterakennerivin nykyinen tila.</span><span class="sxs-lookup"><span data-stu-id="af27d-106">The history line shows the current state of the BOM line.</span></span>

## <a name="update-a-service-bom-element"></a><span data-ttu-id="af27d-107">Huollon tuoterakenteen elementin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="af27d-107">Update a service BOM element</span></span>

1.  <span data-ttu-id="af27d-108">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="af27d-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="af27d-109">Napsauta **Muokkaa** avataksesi **Huoltosopimukset**-tietolomakkeen.</span><span class="sxs-lookup"><span data-stu-id="af27d-109">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="af27d-110">Napsauta **toimintoruudussa** **Huoltokohteet** avataksesi **Huoltokohteet**-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="af27d-110">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="af27d-111">Valitse päivitettävän kohteen tuoterakennerivi ja valitse sitten **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="af27d-111">Select the object to update a BOM line for, and then click **Designer**.</span></span>

5.  <span data-ttu-id="af27d-112">Valitse päivitettävä tuoterakennerivi **Suunnittelija**-lomakkeessa ja valitse sitten **Muokkaa tuoterakenneriviä**.</span><span class="sxs-lookup"><span data-stu-id="af27d-112">In the **Designer** form, select the BOM line to update, and then click **Edit BOM line**.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="af27d-113">Valitse <STRONG>Määritys</STRONG>-välilehdellä <STRONG>Muokkaa lisättäessä</STRONG> -valintaruutu, jos haluat <STRONG>Muokkaa tuoterakenneriviä</STRONG> -lomakkeen avautuvan, kun vedät rivin huollon tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="af27d-113">On the <STRONG>Setup</STRONG> tab, select the <STRONG>Edit when adding</STRONG> check box if you want the <STRONG>Edit BOM line</STRONG> form to open when you drag a line into the service BOM.</span></span></P>

6.  <span data-ttu-id="af27d-114">Anna määrä **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="af27d-114">In the **Quantity** field, enter the quantity.</span></span>

7.  <span data-ttu-id="af27d-115">Valitse **Luo huoltotilausrivi**-valintaruutu, jos haluat luoda huoltotilausrivin korvaavalle nimikkeelle, jonka voi sitten laskuttaa.</span><span class="sxs-lookup"><span data-stu-id="af27d-115">If you want to create a service order line for the replacement item, which can then be invoiced, select the **Create service order line** check box.</span></span>

8.  <span data-ttu-id="af27d-116">Sulje lomake valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="af27d-116">Click **OK** to close the form.</span></span>

## <a name="delete-a-service-bom-line"></a><span data-ttu-id="af27d-117">Huollon tuoterakenteen poistaminen</span><span class="sxs-lookup"><span data-stu-id="af27d-117">Delete a service BOM line</span></span>

1.  <span data-ttu-id="af27d-118">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="af27d-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="af27d-119">Napsauta **Muokkaa** avataksesi **Huoltosopimukset**-tietolomakkeen.</span><span class="sxs-lookup"><span data-stu-id="af27d-119">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="af27d-120">Napsauta **toimintoruudussa** **Huoltokohteet** avataksesi **Huoltokohteet**-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="af27d-120">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="af27d-121">Valitse objekti, josta huollon tuoterakennerivi poistetaan ja napsauta sitten **Suunnittelija**.</span><span class="sxs-lookup"><span data-stu-id="af27d-121">Select the object to delete a service BOM line from, and then click **Designer**.</span></span>

5.  <span data-ttu-id="af27d-122">Valitse poistettava tuoterakennerivi **Suunnittelija**-lomakkeessa ja valitse sitten **Poista tuoterakennerivi**.</span><span class="sxs-lookup"><span data-stu-id="af27d-122">In the **Designer** form, select the BOM line to delete, and then click **Delete BOM line**.</span></span>

## <a name="see-also"></a><span data-ttu-id="af27d-123">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="af27d-123">See also</span></span>

[<span data-ttu-id="af27d-124">Mallituoterakenteet </span><span class="sxs-lookup"><span data-stu-id="af27d-124">Template BOMs</span></span>](template-boms.md)

  



