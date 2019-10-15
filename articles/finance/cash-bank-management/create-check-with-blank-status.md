---
title: Sellaisten sekkien luominen, joiden tila on tyhjä
description: Tässä ohjeaiheessa selitetään, miten pankkitilille luodaan tyhjiä sekkejä sekkisivulla.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175913"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="26916-103">Sellaisten sekkien luominen, joiden tila on tyhjä</span><span class="sxs-lookup"><span data-stu-id="26916-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="26916-104">Tässä ohjeaiheessa selitetään tyhjien sekkien luominen.</span><span class="sxs-lookup"><span data-stu-id="26916-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="26916-105">Tyhjää sekkiä voi käyttää esimerkiksi sellaisen sekin kirjaamiseen, joka on vaurioitunut ja jota ei voi käyttää maksamiseen.</span><span class="sxs-lookup"><span data-stu-id="26916-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="26916-106">**Sekit**-sivulla suoritetaan sekkien ylläpitotehtäviä.</span><span class="sxs-lookup"><span data-stu-id="26916-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="26916-107">Siellä voidaan esimerkiksi luoda uusia sekkinumeroita ja poistaa sekkejä.</span><span class="sxs-lookup"><span data-stu-id="26916-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="26916-108">Voit myös luoda sekkejä, joiden tila on **Tyhjä**.</span><span class="sxs-lookup"><span data-stu-id="26916-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="26916-109">Kun tyhjiä sekkejä on luotu, niitä ei voi poistaa tai käyttää uudelleen järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="26916-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="26916-110">Tämä toiminto on käytössä **Sekit**-sivulla vain, jos **Luo sekkisivulla sekkejä, joilla on tyhjä tila** -toiminto otetaan käyttöön **Toimintojen hallinta** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="26916-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="26916-111">Jos toiminto ei ole käytössä, sekkejä, joiden tila on **Tyhjä**, voidaan luoda vain **Maksu sekillä** -valintaikkunassa ostoreskontran maksunluontiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="26916-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="26916-112">Avaa **Sekit**-sivu siirtymällä kohtaan **Kassan ja pankkitoiminnan hallinta \> Pankkitilit \> Pankkitilit** ja valitse sitten **Aiheeseen liittyviä tietoja** -ryhmän **Maksujen hallinta**-välilehdellä kohta **Sekit**.</span><span class="sxs-lookup"><span data-stu-id="26916-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="26916-113">Vaihtoehtoisesti voit siirtyä kohtaan **Kassa- ja pankkitoiminnan hallinta \> Kyselyt ja raportit \> Sekit**.</span><span class="sxs-lookup"><span data-stu-id="26916-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="26916-114">Tämän jälkeen sekkejä, joiden tila on **Tyhjä**, voidaan luoda valitsemalla toimintoruudussa **Luo tyhjiä sekkejä**.</span><span class="sxs-lookup"><span data-stu-id="26916-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="26916-115">Kun järjestelmä luo tyhjiä sekkejä, niihin liittyvä pankkitili on väliaikaisesti pois käytöstä.</span><span class="sxs-lookup"><span data-stu-id="26916-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="26916-116">Tämä toimintatapa vähentää riskiä siitä, että maksuja luodaan samaan aikaan, kun luodaan tyhjiä sekkejä.</span><span class="sxs-lookup"><span data-stu-id="26916-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="26916-117">Kun käsittely on valmis, asianosainen pankkitili aktivoidaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="26916-117">When the processing is completed, the associated bank account is reactivated.</span></span>
