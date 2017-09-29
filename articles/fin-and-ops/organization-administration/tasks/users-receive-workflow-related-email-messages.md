--- 
title: "Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä"
description: "Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1ff7de584631563939104c87b00fdc26bdb1a3cb
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="a8d00-103">Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä</span><span class="sxs-lookup"><span data-stu-id="a8d00-103">Enable users to receive workflow-related email messages</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8d00-104">Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a8d00-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="a8d00-105">Käyttäjille voidaan lähettää esimerkiksi sähköpostiviestejä, kun asiakirjat määritetään heille hyväksyntää varten.</span><span class="sxs-lookup"><span data-stu-id="a8d00-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="a8d00-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a8d00-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a8d00-107">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="a8d00-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="a8d00-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a8d00-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a8d00-109">Napsauta Käyttäjän asetukset.</span><span class="sxs-lookup"><span data-stu-id="a8d00-109">Click User options.</span></span>
4. <span data-ttu-id="a8d00-110">Valitse Työnkulku-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a8d00-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="a8d00-111">Varmista, että Ilmoitukset-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="a8d00-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="a8d00-112">Voit määrittää Ilmoitukset-osassa, miten haluat käyttäjän saavan ilmoituksen työnkulkuun liittyvistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="a8d00-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="a8d00-113">Valitse vaihtoehto Rivinimiketyönkulkutyyppi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a8d00-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="a8d00-114">Ryhmitelty – nimikkeiden ilmoitukset ryhmitellään yksittäiseen sähköpostiviestiin.</span><span class="sxs-lookup"><span data-stu-id="a8d00-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="a8d00-115">Yksilöllinen – sähköpostiviesti lähetetään kullekin rivinimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="a8d00-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="a8d00-116">Jos haluat käyttäjän saavan ilmoituksia asiakasohjelmassa, valitse Lähetä ilmoitukset sähköpostitse -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a8d00-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="a8d00-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a8d00-117">Click Save.</span></span>
7. <span data-ttu-id="a8d00-118">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a8d00-118">Close the page.</span></span>


