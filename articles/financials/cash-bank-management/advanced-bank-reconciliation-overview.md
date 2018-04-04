---
title: "Pankkitilin täsmäytyksen lisätoimintojen yhteenveto"
description: "Tässä artikkelissa kuvataan pankkitilin täsmäytysprosessin lisätoimintojen työnkulku. Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda tiliotteet, jotka voidaan täsmäyttää automaattisesti pankkitapahtumista."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ff59250b836a73986848109ce48f843fed1d71a9
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="c9f7b-104">Pankkitilin täsmäytyksen lisätoimintojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="c9f7b-104">Advanced bank reconciliation overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c9f7b-105">Tässä artikkelissa kuvataan pankkitilin täsmäytysprosessin lisätoimintojen työnkulku.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="c9f7b-106">Pankkitilin täsmäytyksen lisätoimintojen avulla voit tuoda tiliotteet, jotka voidaan täsmäyttää automaattisesti pankkitapahtumista.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="c9f7b-107">Pankkitilin täsmäytyksen lisätoimintojen avulla tuodaan tiliotteita.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="c9f7b-108">Tuotu tiliote voidaan tämän jälkeen täsmäyttää automaattisesti pankkitapahtumista.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="c9f7b-109">Pankkitilin täsmäytyksen lisätoimintojen työnkulun vaiheet ovat seuraavat.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="c9f7b-110">Määritä tiliotteen tuonti.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="c9f7b-111">Tuo tiliotteet tietoyksikön ympäristön kautta.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="c9f7b-112">Muodostetaan kolme tavallista tiliotteen muotoa: ISO20022, BAI2 ja MT940.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="c9f7b-113">Toimintoja voidaan käyttää missä tahansa muodossa.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="c9f7b-114">Määritä numerosarja pankin täsmäytyksen lisätoimintoja varten. Määritä myös pankin täsmäytyssäännöt.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="c9f7b-115">Täsmäytyssääntö on ehtojoukko, jonka avulla tiliotteen ja Microsoft Dynamics 365 for Finance and Operations -sovelluksen pankkitapahtuman rivejä suodatetaan täsmäytysprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="c9f7b-116">Liiketoimintakäytäntöjesi mukaan voit määrittää useita vastaavia sääntöjä automatisoidaksesi ja optimoidaksesi täsmäytysprosessin.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="c9f7b-117">Täsmäytä tiliotteet Microsoft Dynamics 365 for Finance and Operationsin pankkitapahtumien kanssa.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="c9f7b-118">Suorita täsmäytyksen kirjauskansioille automaattinen täsmäytys ja luonti.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="c9f7b-119">Tarkastele rinnakkain tiliotteita ja Dynamics 365 for Finance and Operationsin pankkitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="c9f7b-120">Kirjaa Dynamics 365 for Finance and Operationsin pankkitapahtumat automaattisesti, jos ne näkyvät tiliotteella, mutta eivät Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="c9f7b-121">Luo täsmäytystiliote.</span><span class="sxs-lookup"><span data-stu-id="c9f7b-121">Generate a reconciliation statement.</span></span>






