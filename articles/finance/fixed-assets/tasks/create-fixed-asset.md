---
title: Luo käyttöomaisuuserä
description: Tässä ohjeaiheessa käsitellään uuden käyttöomaisuustietueen luontia käyttöomaisuuden luettelosivulta.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbbafb1732a9628cb90ad284fce224e3d8172afd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227037"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="a53e3-103">Luo käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="a53e3-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a53e3-104">Tässä ohjeaiheessa käsitellään uuden käyttöomaisuustietueen luontia **Käyttöomaisuus**-luettelosivulta.</span><span class="sxs-lookup"><span data-stu-id="a53e3-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="a53e3-105">Järjestelmä määrittää käyttöomaisuuserän numeron käyttöomaisuusryhmällä määritetyn numerosarjan perusteella.</span><span class="sxs-lookup"><span data-stu-id="a53e3-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="a53e3-106">Jos käyttöomaisuuseriä tuodaan Microsoft Excel -apuohjelman avulla käyttöomaisuusmalleja käyttämällä tai jos käytössä on toinen tuontityö, järjestelmä luo automaattisesti käyttöomaisuustietueet ja kasvattaa käyttöomaisuuserän numeroa.</span><span class="sxs-lookup"><span data-stu-id="a53e3-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="a53e3-107">Käyttöomaisuustietue luodaan manuaalisesti seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="a53e3-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="a53e3-108">Valitse **Siirtymisruutu \> Moduulit \> Käyttöomaisuuserät \> Käyttöomaisuuserät \> Käyttöomaisuuserät**.</span><span class="sxs-lookup"><span data-stu-id="a53e3-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="a53e3-109">Valitse **toimintoruudussa** **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a53e3-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="a53e3-110">Syötä tai valitse arvo **Käyttöomaisuusryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a53e3-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="a53e3-111">**Numero**-kenttään määritetään oletusarvo, jos **käyttöomaisuusparametrien** ja **käyttöomaisuusryhmän** **Käyttöomaisuuserien automaattinen numerointi** -toiminto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="a53e3-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="a53e3-112">Jos se ei ole käytössä, syötä käyttöomaisuuden yksilöivä numero.</span><span class="sxs-lookup"><span data-stu-id="a53e3-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="a53e3-113">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a53e3-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="a53e3-114">Syötä käyttöomaisuuserää koskevat lisätiedot, joita yritys tarvitsee.</span><span class="sxs-lookup"><span data-stu-id="a53e3-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="a53e3-115">Valitse **toimintoruudussa** **Kirjat**.</span><span class="sxs-lookup"><span data-stu-id="a53e3-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="a53e3-116">Kirjoita päivämäärä **Hankintapäivämäärä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a53e3-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="a53e3-117">Syötä **Hankintahinta**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="a53e3-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="a53e3-118">Anna käyttöomaisuuserää koskevat lisätiedot, joita kirja tarvitsee.</span><span class="sxs-lookup"><span data-stu-id="a53e3-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="a53e3-119">Anna poistokirjoja koskevat lisätiedot, joita jäljellä olevat kirjat tarvitsevat.</span><span class="sxs-lookup"><span data-stu-id="a53e3-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="a53e3-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a53e3-120">Close the page.</span></span>

<span data-ttu-id="a53e3-121">Käyttöomaisuuseriä voi luoda myös Excel-apuohjelmalla tai suorittamalla tuontityön **Tiedonhallinta**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="a53e3-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="a53e3-122">Annan arvot mallin pakollisiin kenttiin ennen tuonnin suorittamista.</span><span class="sxs-lookup"><span data-stu-id="a53e3-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="a53e3-123">Jos Excel-apuohjelman mallissa tai tiedonhallinnassa ei määritetty käyttöomaisuuserän numeroa, järjestelmä luo käyttöomaisuuserän numeron kullekin tuodulle käyttöomaisuudelle ja kasvattaa numerosarjaa automaattisesti kunkin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="a53e3-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="a53e3-124">Jos käyttöomaisuuserät tuodaan ja niiden numerot määritetään mallissa, järjestelmä **ei** kasvata numerosarjaa automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a53e3-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="a53e3-125">Siinä tapauksessa järjestelmänvalvojan on ehkä päivitettävä numerosarja manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="a53e3-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="a53e3-126">Jos määritit käyttöomaisuuserän numero Excel-apuohjelman mallissa, järjestelmä käyttää määritettyä käyttöomaisuuserän numero ja kasvattaa numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="a53e3-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="a53e3-127">Poiston kirjaamisen jälkeen **Käyttöönotto**- ja **Poiston suorituspäivä** -kentät lukitaan **Kirja**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a53e3-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="a53e3-128">Kumpaakaan kenttää ei myöskään päivitetä tietoentiteetistä.</span><span class="sxs-lookup"><span data-stu-id="a53e3-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="a53e3-129">Käyttöomaisuustietuetta ei poisteta, jos tapahtumat kirjattiin siihen liittyvään kirjaan tai jos juuri luotu käyttöomaisuuserä syötetään kirjauskansioriville, mutta sitä ei kirjata.</span><span class="sxs-lookup"><span data-stu-id="a53e3-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]