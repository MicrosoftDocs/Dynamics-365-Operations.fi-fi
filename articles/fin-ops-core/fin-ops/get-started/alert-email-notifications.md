---
title: Asiakasohjelman hälytysilmoitukset sähköpostitse
description: Tässä ohjeaiheessa käsitellään sellaisten sääntöjen määrittämistä, jolla lähetetään sähköposti-ilmoituksia ennaltamääritettyjen tapahtumien sattuessa.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a1d520584e331631bb5a6a88ba6c9a8b50b3d29e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798620"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="5743f-103">Asiakasohjelman hälytysilmoitukset sähköpostitse</span><span class="sxs-lookup"><span data-stu-id="5743f-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5743f-104">Voit määrittää mukautetut hälytyssäännöt, jotka seuraavat tietojen suodatettuja näkymiä ja lähettävät automaattisesti sähköposti-ilmoituksia, kun ennaltamääritetyt tapahtumat tapahtuvat.</span><span class="sxs-lookup"><span data-stu-id="5743f-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="5743f-105">Sähköposti-ilmoitusten lähetysasetus on käytettävissä kaikissa tuetuissa hälytystyypeissä, ja se voidaan käyttöön myös aiemmin luoduille hälytyssäännöille.</span><span class="sxs-lookup"><span data-stu-id="5743f-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="5743f-106">Voit käyttää valmiita ohjausobjektia ja luoda niiden avulla järjestelmän erätöiden suodatusnäkyviä seuraavia hälytyssääntöjä.</span><span class="sxs-lookup"><span data-stu-id="5743f-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="5743f-107">**Tila**-kentän arvoa seuraamalla on mahdollista määrittää hälytyssääntöjä, jotka lähettävät sähköpostin, kun erätyö epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="5743f-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="5743f-108">Näiden hälytyssääntöjen luonnin jälkeen, liiketoimintatietojen muutoksia ei enää tarvitse tarkistaa raporteista.</span><span class="sxs-lookup"><span data-stu-id="5743f-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="5743f-109">Älykäs muutoksen havaintopalvelu voi seurata näitä muutoksia puolestasi.</span><span class="sxs-lookup"><span data-stu-id="5743f-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="5743f-110">Asiakasohjelman hälytykset määräytyvät Microsoft Office -integroinnin kautta saatavasta sähköpostin alijärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="5743f-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="5743f-111">Suosituksena on SMTP (Simple Mail Transfer Protocol) -palvelun käyttö, jotta sähköpostin jakelu ei perustu paikalliseen sähköpostiohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="5743f-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="5743f-112">Sähköpostitse lähetettävät ilmoitukset edellyttävät, että asiakkaat määrittävät integroidut sähköpostipalvelut.</span><span class="sxs-lookup"><span data-stu-id="5743f-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="5743f-113">Sähköposti-ilmoitukset lähetetään vastaanottajille hälytyksen omistajien puolesta.</span><span class="sxs-lookup"><span data-stu-id="5743f-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="5743f-114">Lisätietoja sähköpostin määrittämisestä on kohdassa [Sähköpostiviestin määrittäminen ja lähettäminen](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="5743f-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="5743f-115">Seuraavassa kuvassa on **Luo hälytyssääntö** -valintaikkuna, jossa on nyt myös **Lähetä sähköposti** -asetus.</span><span class="sxs-lookup"><span data-stu-id="5743f-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="5743f-116">[![Luo hälytyssääntö -valintaikkuna, jos Lähetä sähköposti -asetukseksi on valittu Kyllä](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="5743f-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5743f-117">Kun **Lähetä sähköposti** -asetukseksi on valittu **Kyllä**, hälytysilmoitusten toimittamista jatketaan toimintokeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="5743f-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="5743f-118">Hälytysilmoitusten sähköpostimallit</span><span class="sxs-lookup"><span data-stu-id="5743f-118">Alert notification email templates</span></span>

<span data-ttu-id="5743f-119">Palvelu lähettää sähköposti-ilmoituksia käyttämällä valmiita sähköpostimalleja, jotka toimittavat hälytysilmoituksen perustiedot.</span><span class="sxs-lookup"><span data-stu-id="5743f-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="5743f-120">Seuraavassa kuvassa on sähköpostitse toimitettujen hälytysilmoitusten rakenne.</span><span class="sxs-lookup"><span data-stu-id="5743f-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="5743f-121">[![Tietueen luontia, kentän muutoksia ja mallin poistoa koskevat mallipohjaiset hälytysilmoitukset](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="5743f-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
