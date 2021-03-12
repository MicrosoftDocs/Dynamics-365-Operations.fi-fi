---
title: Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä
description: Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 221e38cbe31e2ad24a56cb2e71206a1ebcdd619e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2020
ms.locfileid: "4799001"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="fd571-103">Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä</span><span class="sxs-lookup"><span data-stu-id="fd571-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fd571-104">Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="fd571-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="fd571-105">Käyttäjille voidaan lähettää esimerkiksi sähköpostiviestejä, kun asiakirjat määritetään heille hyväksyntää varten.</span><span class="sxs-lookup"><span data-stu-id="fd571-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="fd571-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="fd571-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="fd571-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="fd571-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="fd571-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="fd571-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fd571-109">Valitse **toimintoruudussa** **Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="fd571-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="fd571-110">Valitse **Työnkulku**-väli lehti. Varmista, että **Ilmoitukset**-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="fd571-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="fd571-111">Voit määrittää **Ilmoitukset**-osassa, miten haluat käyttäjän saavan ilmoituksen työnkulkuun liittyvistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="fd571-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="fd571-112">Valitse vaihtoehto **Rivinimiketyönkulkutyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="fd571-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="fd571-113">Ryhmitelty – nimikkeiden ilmoitukset ryhmitellään yksittäiseen sähköpostiviestiin.</span><span class="sxs-lookup"><span data-stu-id="fd571-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="fd571-114">Yksilöllinen – sähköpostiviesti lähetetään kullekin rivinimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="fd571-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="fd571-115">Jos haluat käyttäjän saavan ilmoituksia asiakasohjelmassa, valitse **Lähetä ilmoitukset sähköpostitse** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="fd571-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="fd571-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="fd571-116">Click **Save**.</span></span>
7. <span data-ttu-id="fd571-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fd571-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="fd571-118">Työnkulun sähköpostimallit ovat peräisin joko järjestelmän sähköpostimalleista tai organisaation sähköpostimalleista sen mukaan, onko työnkulku järjestelmätason (ei yrityskohtainen) vai organisaatiotason (yrityskohtainen) työnkulku.</span><span class="sxs-lookup"><span data-stu-id="fd571-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>
