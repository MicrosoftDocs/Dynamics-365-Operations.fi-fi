---
title: Hälytysten yleiskuvaus
description: Tämä ohjeaihe sisältää yleisiä tietoja hälytyksistä. Saat hälytysten avulla tietoja tapahtumista, joita haluat seurata työpäivän aikana.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a42e836c0b72798de3375c169e45b121debd55ec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191267"
---
# <a name="alerts-overview"></a><span data-ttu-id="bd41f-104">Hälytysten yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="bd41f-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="bd41f-105">Tietoja hälytyksistä</span><span class="sxs-lookup"><span data-stu-id="bd41f-105">About alerts</span></span>
<span data-ttu-id="bd41f-106">Hälytykset muodostavat kriittisten tapahtumien ilmoitusjärjestelmän järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="bd41f-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="bd41f-107">Saat hälytysten avulla tietoja tapahtumista, joita haluat seurata työpäivän aikana.</span><span class="sxs-lookup"><span data-stu-id="bd41f-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="bd41f-108">Voit luoda kätevästi oman hälytyssääntöjoukon, joilla saat hälytyksen myöhässä olevista lähetyksistä, poistetuista tilauksista, hintojen muutoksista ja muista reagointia vaativista tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="bd41f-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="bd41f-109">Toiminnanohjausratkaisussa (ERP) on useita tyypillisiä skenaarioita, joissa hälytystoimintoa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="bd41f-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="bd41f-110">Seuraavassa on muutamia esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="bd41f-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="bd41f-111">Skenaario 1: Hälytyssäännön luonti uusia myyntitilauksia varten</span><span class="sxs-lookup"><span data-stu-id="bd41f-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="bd41f-112">Avaa **Kaikki myyntitilaukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="bd41f-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="bd41f-113">Valitse **Asetukset**-välilehden **Jaa**-ryhmän toimintoruudussa **Luo mukautettu hälytys**.</span><span class="sxs-lookup"><span data-stu-id="bd41f-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="bd41f-114">Valitse **Hälytä seuraavissa tilanteissa** -pikavälilehden **Luo hälytyssääntö** -valintaikkunan **Tapahtuma**-kentässä **Tietue on luotu**.</span><span class="sxs-lookup"><span data-stu-id="bd41f-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="bd41f-115">Tilanne 2: Hälytyssäännön luonti toimituspäivän lykkäystä varten</span><span class="sxs-lookup"><span data-stu-id="bd41f-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="bd41f-116">Avaa **Kaikki ostotilaukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="bd41f-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="bd41f-117">Pääset käyttämään ostotilauksen tietoja valitsemalla ostotilauksen tunnuksen.</span><span class="sxs-lookup"><span data-stu-id="bd41f-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="bd41f-118">Laajenna **Ostotilauksen otsikko** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="bd41f-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="bd41f-119">Valitse **Asetukset**-välilehden **Jaa**-ryhmän toimintoruudussa **Luo mukautettu hälytys**.</span><span class="sxs-lookup"><span data-stu-id="bd41f-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="bd41f-120">Valitse **Hälytä seuraavissa tilanteissa** -pikavälilehden **Luo hälytyssääntö** -valintaikkunan **Kenttä**-kentässä **Toimituspäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="bd41f-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="bd41f-121">Valitse **Tapahtuma**-kentässä **on siirretty**.</span><span class="sxs-lookup"><span data-stu-id="bd41f-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="bd41f-122">Kun **Luo hälytyssääntö** -valintaikkuna suljetaan, sääntö näkyy **Ylläpidä hälytyssääntöjä** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="bd41f-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="bd41f-123">Voit päivittää aiemmin luotuja hälytyssääntöjä **Ylläpidä hälytyssääntöjä** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="bd41f-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="bd41f-124">Voit esimerkiksi muokata tapahtuman käynnistimiä, päivittää ilmoituksia ja päivittää voimassaolon päättymispäivät.</span><span class="sxs-lookup"><span data-stu-id="bd41f-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="bd41f-125">Voit avata **Ylläpidä hälytyssääntöjä** -sivun toimintoruudun **Asetukset**-välilehden **Hälytys**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="bd41f-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="bd41f-126">Mitä tapahtuu, kun luodaan hälytyssääntö?</span><span class="sxs-lookup"><span data-stu-id="bd41f-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="bd41f-127">Kun luot hälytyssääntöjä, voit liittää ennalta määritetyn tapahtuman tiettyyn kenttään.</span><span class="sxs-lookup"><span data-stu-id="bd41f-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="bd41f-128">Esimerkiksi kentässä määritetty päivämäärä saavutetaan tai kentän sisältöä muutetaan.</span><span class="sxs-lookup"><span data-stu-id="bd41f-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="bd41f-129">Vaihtoehtoisesti voit liittää tapahtuman tietyn sivun tietueisiin.</span><span class="sxs-lookup"><span data-stu-id="bd41f-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="bd41f-130">Esimerkiksi tietue on luotu tai tietue on poistettu.</span><span class="sxs-lookup"><span data-stu-id="bd41f-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="bd41f-131">Kun valittu tapahtuma tapahtuu sivun kentässä tai tietueessa, sinulle lähetetään hälytys.</span><span class="sxs-lookup"><span data-stu-id="bd41f-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="bd41f-132">Kun luot esimerkiksi säännön, jossa tietyn ostotilausrivin **Toimituspäivämäärä**-kenttä liitetään **erääntymisestä on aikaa** -tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="bd41f-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="bd41f-133">Määritit aikavälin viideksi päiväksi.</span><span class="sxs-lookup"><span data-stu-id="bd41f-133">You set the time frame to five days.</span></span> <span data-ttu-id="bd41f-134">Tässä tapauksessa hälytys lähetetään viisi päivää ostotilausrivin toimituspäivän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bd41f-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="bd41f-135">Voit myös tarkentaa hälytyssääntöjä määrittämällä ehdot.</span><span class="sxs-lookup"><span data-stu-id="bd41f-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="bd41f-136">Voit saada hälytyksiä esimerkiksi ostotilauksista, jotka luodaan tietyille toimittajatileille.</span><span class="sxs-lookup"><span data-stu-id="bd41f-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="bd41f-137">Valmistellaan hälytystä</span><span class="sxs-lookup"><span data-stu-id="bd41f-137">Preparing for an alert</span></span>

<span data-ttu-id="bd41f-138">Ennen hälytyssäännön luomista on päätettävä, milloin ja missä tilanteissa haluat vastaanottaa hälytyksiä.</span><span class="sxs-lookup"><span data-stu-id="bd41f-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="bd41f-139">Kun tiedät, mistä tapahtumasta haluat ilmoituksen, voit etsiä sivun, jossa kyseisen tapahtuman aiheuttavat tiedot näkyvät.</span><span class="sxs-lookup"><span data-stu-id="bd41f-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="bd41f-140">Tapahtuma voi olla tietty päivämäärä tai tapahtuva muutos.</span><span class="sxs-lookup"><span data-stu-id="bd41f-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="bd41f-141">Sinun onkin etsittävä sivu, jossa päivämäärä on määritetty tai jossa muuttuva kenttä tai luotu uusi tietue tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="bd41f-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="bd41f-142">Kun nämä tiedot ovat valmiina, voit luoda hälytyssäännön.</span><span class="sxs-lookup"><span data-stu-id="bd41f-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="bd41f-143">Hälytyssäännön osat</span><span class="sxs-lookup"><span data-stu-id="bd41f-143">Components of an alert rule</span></span>

<span data-ttu-id="bd41f-144">Hälytyssäännöllä on viisi osaa:</span><span class="sxs-lookup"><span data-stu-id="bd41f-144">An alert rule has five components:</span></span>

- <span data-ttu-id="bd41f-145">**Tapahtuma** – Tapahtuma, joka käynnistää hälytyssäännön, voi olla tietty päivämäärä tai tapahtuva muutos.</span><span class="sxs-lookup"><span data-stu-id="bd41f-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="bd41f-146">Voit määrittää tapahtumia **Luo hälytyssääntö** -valintaikkunan **Lähetä sähköpostihälytykset työn tilan muutoksista** -pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="bd41f-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="bd41f-147">**Ehto** – Voit valita **Luo hälytyssääntö** -valintaikkunan **Hälytä seuraavasta:** -pikavälilehdessä ehtojen laajuuden. Näin voit määrittää, milloin saat tapahtumista hälytyksen.</span><span class="sxs-lookup"><span data-stu-id="bd41f-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="bd41f-148">Voit käyttää sääntöä joko vain nykyisessä tietueessa tai kaikissa sivulla näkyvissä tietueissa.</span><span class="sxs-lookup"><span data-stu-id="bd41f-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="bd41f-149">Jos sääntö koskee kaikkia yrityksiä, voit määrittää **Organisaationlaajuinen**-asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bd41f-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="bd41f-150">**Päättymissääntö** – **Luo hälytyssääntö** -valintaikkunan **Hälytä tähän asti** -pikavälilehdessä voit määrittää, miten kauan hälytyssääntö on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="bd41f-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="bd41f-151">**Sisältö** – Voit määrittää **Luo hälytyssääntö** -valintaikkunan **Hälytystapa**-pikavälilehdessä hälytykselle aihe- ja sanomatekstin.</span><span class="sxs-lookup"><span data-stu-id="bd41f-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="bd41f-152">**Käyttäjä** – Määritä **Luo hälytyssääntö** -valintaikkunan **Hälytys - kuka** -pikavälilehdessä käyttäjä, joka vastaanottaa hälytyssanoman.</span><span class="sxs-lookup"><span data-stu-id="bd41f-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="bd41f-153">Käyttäjätunnus valitaan oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="bd41f-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bd41f-154">Tämä asetus on rajoitettu organisaation järjestelmänvalvojien käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bd41f-154">This option is restricted to organization administrators.</span></span>

## <a name="email-notifications-from-alerts"></a><span data-ttu-id="bd41f-155">Sähköposti-ilmoitukset hälytyksistä</span><span class="sxs-lookup"><span data-stu-id="bd41f-155">Email notifications from alerts</span></span>

<span data-ttu-id="bd41f-156">Sähköposti-ilmoituksia hälytyksistä ei ole vielä otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bd41f-156">Email notifications from alerts are not yet enabled.</span></span> <span data-ttu-id="bd41f-157">Se otetaan käyttöön myöhemmässä päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="bd41f-157">This will be enabled in a future update.</span></span>

## <a name="videos"></a><span data-ttu-id="bd41f-158">Videot</span><span class="sxs-lookup"><span data-stu-id="bd41f-158">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="bd41f-159">Suodatettujen tietojen valvonta hälytysten avulla</span><span class="sxs-lookup"><span data-stu-id="bd41f-159">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="bd41f-160">[Suodatettujen tietojen valvonta hälytysten avulla](https://youtu.be/ZYKMcv6kl9s) -video (mainittu edellä) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on katsottavissa YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="bd41f-160">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="bd41f-161">Hälytyssääntövaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="bd41f-161">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3E4PV]

<span data-ttu-id="bd41f-162">[Hälytyssääntövaihtoehdot](https://youtu.be/cpzimwOjicM) -video (edellä mainittu) sisältyy [Finance and Operations -toistoluetteloon](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on katsottavissa YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="bd41f-162">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

