---
title: Asiakasohjelman hälytysilmoitukset sähköpostitse
description: Tässä ohjeaiheessa käsitellään sellaisten sääntöjen määrittämistä, jolla lähetetään sähköposti-ilmoituksia ennaltamääritettyjen tapahtumien sattuessa.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2019
ms.locfileid: "373764"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="92dff-103">Asiakasohjelman hälytysilmoitukset sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="92dff-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="92dff-104">Voit määrittää Microsoft Dynamics 365 for Finance and Operationsissa mukautetut hälytyssäännöt, jotka seuraavat tietojen suodatettuja näkyviä ja lähettävät automaattisesti sähköposti-ilmoituksia, kun ennaltamääritetyt tapahtumat tapahtuvat.</span><span class="sxs-lookup"><span data-stu-id="92dff-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="92dff-105">Sähköposti-ilmoitusten lähetysasetus on käytettävissä kaikissa tuetuissa hälytystyypeissä, ja se voidaan käyttöön myös aiemmin luoduille hälytyssäännöille.</span><span class="sxs-lookup"><span data-stu-id="92dff-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="92dff-106">Voit käyttää valmiita ohjausobjektia ja luoda niiden avulla järjestelmän erätöiden suodatusnäkyviä seuraavia hälytyssääntöjä.</span><span class="sxs-lookup"><span data-stu-id="92dff-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="92dff-107">**Tila**-kentän arvoa seuraamalla on mahdollista määrittää hälytyssääntöjä, jotka lähettävät sähköpostin, kun erätyö epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="92dff-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="92dff-108">Näiden hälytyssääntöjen luonnin jälkeen sinun ei enää tarvitse tarkistaa liiketoimintatietojen muutoksia raporteista.</span><span class="sxs-lookup"><span data-stu-id="92dff-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="92dff-109">Finance and Operationsin älykäs palvelu nimittäin havaitsee nämä muutokset ja seuraa niitä puolestasi.</span><span class="sxs-lookup"><span data-stu-id="92dff-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="92dff-110">Asiakasohjelman hälytykset määräytyvät Microsoft Office -integroinnin kautta saatavasta sähköpostin alijärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="92dff-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="92dff-111">Suosituksena on SMTP (Simple Mail Transfer Protocol) -palvelun käyttö, jotta sähköpostin jakelu ei perustu paikalliseen sähköpostiohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="92dff-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="92dff-112">Sähköpostitse lähetettävät ilmoitukset edellyttävät, että asiakkaat määrittävät integroidut sähköpostipalvelut.</span><span class="sxs-lookup"><span data-stu-id="92dff-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="92dff-113">Sähköposti-ilmoitukset lähetetään vastaanottajille hälytyksen omistajien puolesta.</span><span class="sxs-lookup"><span data-stu-id="92dff-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="92dff-114">Lisätietoja sähköpostin määrittämisestä Finance and Operationsissa on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="92dff-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="92dff-115">Seuraavassa kuvassa on **Luo hälytyssääntö** -valintaikkuna, jossa on nyt myös **Lähetä sähköposti** -asetus.</span><span class="sxs-lookup"><span data-stu-id="92dff-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="92dff-116">[![Luo hälytyssääntö -valintaikkuna, jos Lähetä sähköposti -asetukseksi on valittu Kyllä](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="92dff-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="92dff-117">Kun **Lähetä sähköposti** -asetukseksi on valittu **Kyllä**, hälytysilmoitusten toimittamista jatketaan toimintokeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="92dff-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="92dff-118">Hälytysilmoitusten sähköpostimallit</span><span class="sxs-lookup"><span data-stu-id="92dff-118">Alert notification email templates</span></span>

<span data-ttu-id="92dff-119">Palvelu lähettää sähköposti-ilmoituksia käyttämällä valmiita sähköpostimalleja, jotka toimittavat hälytysilmoituksen perustiedot.</span><span class="sxs-lookup"><span data-stu-id="92dff-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span> <span data-ttu-id="92dff-120">Näihin tietoihin sisältyy suora linkki sivulle, jossa hälytyssääntö on määritetty.</span><span class="sxs-lookup"><span data-stu-id="92dff-120">These details include a direct link to the page where the alert rule was defined.</span></span>

<span data-ttu-id="92dff-121">Seuraavassa kuvassa on sähköpostitse toimitettujen hälytysilmoitusten rakenne.</span><span class="sxs-lookup"><span data-stu-id="92dff-121">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="92dff-122">[![Tietueen luontia, kentän muutoksia ja mallin poistoa koskevat mallipohjaiset hälytysilmoitukset](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="92dff-122">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
