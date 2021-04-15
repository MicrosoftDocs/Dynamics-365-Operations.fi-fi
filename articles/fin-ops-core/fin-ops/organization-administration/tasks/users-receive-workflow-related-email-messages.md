---
title: Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä
description: Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä.
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3207727c8deba97eebfd7516e9600238e5e79b3d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747246"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="356de-103">Anna käyttäjille mahdollisuus vastaanottaa työnkulkuun liittyviä sähköpostiviestejä</span><span class="sxs-lookup"><span data-stu-id="356de-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="356de-104">Voit määrittää järjestelmän lähettämään sähköpostiviestejä käyttäjille työnkulkuun liittyvien tapahtumien yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="356de-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="356de-105">Käyttäjille voidaan lähettää esimerkiksi sähköpostiviestejä, kun asiakirjat määritetään heille hyväksyntää varten.</span><span class="sxs-lookup"><span data-stu-id="356de-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="356de-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="356de-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="356de-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="356de-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="356de-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="356de-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="356de-109">Valitse **toimintoruudussa** **Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="356de-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="356de-110">Valitse **Työnkulku**-väli lehti. Varmista, että **Ilmoitukset**-osa on laajennettu.</span><span class="sxs-lookup"><span data-stu-id="356de-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="356de-111">Voit määrittää **Ilmoitukset**-osassa, miten haluat käyttäjän saavan ilmoituksen työnkulkuun liittyvistä tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="356de-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="356de-112">Valitse vaihtoehto **Rivinimiketyönkulkutyyppi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="356de-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="356de-113">Ryhmitelty – nimikkeiden ilmoitukset ryhmitellään yksittäiseen sähköpostiviestiin.</span><span class="sxs-lookup"><span data-stu-id="356de-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="356de-114">Yksilöllinen – sähköpostiviesti lähetetään kullekin rivinimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="356de-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="356de-115">Jos haluat käyttäjän saavan ilmoituksia asiakasohjelmassa, valitse **Lähetä ilmoitukset sähköpostitse** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="356de-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="356de-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="356de-116">Click **Save**.</span></span>
7. <span data-ttu-id="356de-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="356de-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="356de-118">Työnkulun sähköpostimallit ovat peräisin joko järjestelmän sähköpostimalleista tai organisaation sähköpostimalleista sen mukaan, onko työnkulku järjestelmätason (ei yrityskohtainen) vai organisaatiotason (yrityskohtainen) työnkulku.</span><span class="sxs-lookup"><span data-stu-id="356de-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]