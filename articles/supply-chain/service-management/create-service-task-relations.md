---
title: Huoltotehtävän suhteiden luominen
description: Voi liittää huoltotehtäviä huoltosopimuksiin tai huoltotilauksiin kuvataksesi sopimuksen tai tilauksen huoltotehtävää.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b167714dc81cf0e4ee70d7092f2ec030043abe71
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202603"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="9c21a-103">Huoltotehtävän suhteiden luominen</span><span class="sxs-lookup"><span data-stu-id="9c21a-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c21a-104">Voi liittää huoltotehtäviä huoltosopimuksiin tai huoltotilauksiin kuvataksesi sopimuksen tai tilauksen huoltotehtävää.</span><span class="sxs-lookup"><span data-stu-id="9c21a-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="9c21a-105">Sekä teknikot että asiakkaat näkevät nämä tiedot.</span><span class="sxs-lookup"><span data-stu-id="9c21a-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="9c21a-106">Suhteen luominen huoltosopimukseen</span><span class="sxs-lookup"><span data-stu-id="9c21a-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="9c21a-107">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="9c21a-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="9c21a-108">Valitse nykyinen huoltosopimus tai luo uusi huoltosopimus.</span><span class="sxs-lookup"><span data-stu-id="9c21a-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="9c21a-109">Valitse toimintoruudussa **Huoltotehtävät**-painike.</span><span class="sxs-lookup"><span data-stu-id="9c21a-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="9c21a-110">Paina **Huoltotehtävät**-lomakkeessa CTRL + N luodaksesi uuden rivin, ja valitse sitten huoltosopimukseen liitettävä huoltotehtävä **Huoltotehtävä**-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="9c21a-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="9c21a-111">Lisää **Kuvaus** -välilehden vapaatekstikenttiin mahdolliset sisäisten tai ulkoisten huomautusten kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="9c21a-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="9c21a-112">Tallenna tietue sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="9c21a-112">Close the form to save the record.</span></span>

<span data-ttu-id="9c21a-113">Toista tämä toimenpide, kunnes olet luonut huoltosopimuksen kaikki tarvittavat huoltotehtäväsuhteet.</span><span class="sxs-lookup"><span data-stu-id="9c21a-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="9c21a-114">Voit nyt määrittää nämä huoltotehtävät liittyville huoltoriveille.</span><span class="sxs-lookup"><span data-stu-id="9c21a-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="9c21a-115">Huoltosopimukselle luotavat huoltotehtäväsuhteet ovat käytettävissä kaikissa huoltotilauksissa, jotka liittyvät huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="9c21a-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="9c21a-116">Suhteen luominen huoltotilaukseen</span><span class="sxs-lookup"><span data-stu-id="9c21a-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="9c21a-117">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="9c21a-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="9c21a-118">Valitse nykyinen huoltotilaus tai luo uusi huoltotilaus.</span><span class="sxs-lookup"><span data-stu-id="9c21a-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="9c21a-119">Valitse toimintoruudussa **Huoltotehtävät**-painike.</span><span class="sxs-lookup"><span data-stu-id="9c21a-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="9c21a-120">Paina **Huoltotehtävät**-lomakkeessa CTRL + N luodaksesi uuden rivin, ja valitse sitten huoltotilaukseen liitettävät huoltotehtävät **Huoltotehtävä**-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="9c21a-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="9c21a-121">Lisää **Kuvaus** -välilehden vapaatekstikenttiin mahdolliset sisäisten tai ulkoisten huomautusten kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="9c21a-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="9c21a-122">Tallenna tietue sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="9c21a-122">Close the form to save the record.</span></span>

<span data-ttu-id="9c21a-123">Toista tämä toimenpide, kunnes olet luonut huoltotilauksen kaikki tarvittavat huoltotehtäväsuhteet.</span><span class="sxs-lookup"><span data-stu-id="9c21a-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="9c21a-124">Kun luot huoltotilausrivejä, voit valita huoltotehtävän, jolle suhde luotiin.</span><span class="sxs-lookup"><span data-stu-id="9c21a-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="9c21a-125">Huoltotilaukselle luotavat huoltotehtäväsuhteet ovat käytettävissä kyseisessä huoltotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="9c21a-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c21a-126">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="9c21a-126">See also</span></span>

[<span data-ttu-id="9c21a-127">Huoltotehtävien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9c21a-127">Service tasks overview</span></span>](service-tasks.md)


  


