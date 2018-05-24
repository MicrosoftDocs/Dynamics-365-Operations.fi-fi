---
title: Korjausten hallinta
description: "Voit ryhmittää ongelmat systemaattisesti. Se auttaa aiemmin onnistuneiden ratkaisujen ehdottamisessa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 937571968c6956ce3dba1427082b298983540f59
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="repair-management"></a><span data-ttu-id="9419a-103">Korjausten hallinta</span><span class="sxs-lookup"><span data-stu-id="9419a-103">Repair management</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9419a-104">Korjausten hallinnassa voit ryhmittää ongelmat systemaattisesti.</span><span class="sxs-lookup"><span data-stu-id="9419a-104">For repair management you can group problems systematically.</span></span> <span data-ttu-id="9419a-105">Se auttaa aiemmin onnistuneiden ratkaisujen ehdottamisessa.</span><span class="sxs-lookup"><span data-stu-id="9419a-105">This is to help with the suggestion of solutions that have been successful in the past.</span></span>

<span data-ttu-id="9419a-106">Voit määrittää oireiden, vianmäärityksen ja ratkaisun asetukset.</span><span class="sxs-lookup"><span data-stu-id="9419a-106">You set up symptoms, diagnosis, and resolution settings.</span></span> <span data-ttu-id="9419a-107">Kaikkia näitä voidaan käyttää myöhemmin vastaanotettaessa samanlaisia korjattavia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="9419a-107">All these can later be applied when you receive a similar item for repair.</span></span> <span data-ttu-id="9419a-108">Voit myös määrittää korjauksen vaiheet, joiden avulla korjausta voi seurata.</span><span class="sxs-lookup"><span data-stu-id="9419a-108">You can also set up repair stages that can follow the progress of a repair issue.</span></span>

## <a name="setting-up-repair-management"></a><span data-ttu-id="9419a-109">Korjausten hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9419a-109">Setting up repair management</span></span>

<span data-ttu-id="9419a-110">Käytä seuraavia määrityslomakkeita syöttääksesi tiedot, joita käytetään korjauksen oireiden, vianmäärityksen ja ratkaisun määritykseen.</span><span class="sxs-lookup"><span data-stu-id="9419a-110">Use the following setup forms to enter information that will be used to specify the symptoms, the diagnosis, and the resolution, of the repair.</span></span>

1.  <span data-ttu-id="9419a-111">Valitse **Huollon hallinta** \> **Määritys** \> **Korjaus** \> **Olosuhteet**.</span><span class="sxs-lookup"><span data-stu-id="9419a-111">Click **Service management** \> **Setup** \> **Repair** \> **Conditions**.</span></span>

2.  <span data-ttu-id="9419a-112">Valitse **Huollon hallinta** \> **Määritys** \> **Korjaus** \> **Oirealueet**.</span><span class="sxs-lookup"><span data-stu-id="9419a-112">Click **Service management** \> **Setup** \> **Repair** \> **Symptom areas**.</span></span>

3.  <span data-ttu-id="9419a-113">Valitse **Huollon hallinta** \> **Määritys** \> **Korjaus** \> **Vianmääritysalueet**.</span><span class="sxs-lookup"><span data-stu-id="9419a-113">Click **Service management** \> **Setup** \> **Repair** \> **Diagnosis areas**.</span></span>

4.  <span data-ttu-id="9419a-114">Valitse **Huollon hallinta** \> **Määritys** \> **Korjaus** \> **Ratkaisut**.</span><span class="sxs-lookup"><span data-stu-id="9419a-114">Click **Service management** \> **Setup** \> **Repair** \> **Resolutions**.</span></span>

5.  <span data-ttu-id="9419a-115">Valitse **Huollon hallinta** \> **Määritys** \> **Korjaus** \> **Korjauksen vaiheet**.</span><span class="sxs-lookup"><span data-stu-id="9419a-115">Click **Service management** \> **Setup** \> **Repair** \> **Repair stages**.</span></span>

## <a name="symptoms-and-conditions"></a><span data-ttu-id="9419a-116">Oireet ja olosuhteet</span><span class="sxs-lookup"><span data-stu-id="9419a-116">Symptoms and conditions</span></span>

<span data-ttu-id="9419a-117">Oireet ovat asiakkaan kuvaus siitä, miten ongelma ilmenee.</span><span class="sxs-lookup"><span data-stu-id="9419a-117">Symptoms are how the customer characterizes the problem.</span></span> <span data-ttu-id="9419a-118">Oireet sisältävät asiakkaan havainnot korjaustarpeesta.</span><span class="sxs-lookup"><span data-stu-id="9419a-118">Symptoms include the customer observations that indicate the need for repair.</span></span>

<span data-ttu-id="9419a-119">Voit määrittää oirealueita, oirekoodeja ja olosuhteita.</span><span class="sxs-lookup"><span data-stu-id="9419a-119">You can set up symptom areas, symptom codes, and conditions.</span></span> <span data-ttu-id="9419a-120">Oirealue kattaa toimintahäiriön alueen ja oirekoodi kattaa toimintahäiriön oireen.</span><span class="sxs-lookup"><span data-stu-id="9419a-120">The symptom area covers the area of malfunction, and the symptom code covers the malfunction symptom.</span></span> <span data-ttu-id="9419a-121">Olosuhde kuvaa tilannetta tai ympäristöä, jossa ongelma ilmenee.</span><span class="sxs-lookup"><span data-stu-id="9419a-121">The condition describes the situation or environment that is present when the problem occurs.</span></span>

<span data-ttu-id="9419a-122">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="9419a-122">**Example**</span></span>

<span data-ttu-id="9419a-123">Tietokone tuodaan korjattavaksi, koska kiintolevy vikaantuu pitkän käyttöjakson jälkeen.</span><span class="sxs-lookup"><span data-stu-id="9419a-123">A computer is brought in for repair because the hard drive fails after an extended period of use.</span></span> <span data-ttu-id="9419a-124">Kiintolevyn vika aiheuttaa sinisen virhenäytön.</span><span class="sxs-lookup"><span data-stu-id="9419a-124">The hard drive failure causes a blue screen error.</span></span> <span data-ttu-id="9419a-125">Tietokoneen vastaanottava huoltoteknikko syöttää seuraavat oireet ja olosuhteet:</span><span class="sxs-lookup"><span data-stu-id="9419a-125">The technician who receives the computer enters the following symptoms and conditions:</span></span>

1.  <span data-ttu-id="9419a-126">Oirealue on kiintolevy</span><span class="sxs-lookup"><span data-stu-id="9419a-126">The symptom area is the hard drive</span></span>

2.  <span data-ttu-id="9419a-127">Oirekoodi on sininen virhenäyttö</span><span class="sxs-lookup"><span data-stu-id="9419a-127">The symptom code is the blue screen error</span></span>

3.  <span data-ttu-id="9419a-128">Olosuhde on, että kiintolevy on vikaantunut pitkän käyttöjakson jälkeen</span><span class="sxs-lookup"><span data-stu-id="9419a-128">The condition is that the hard drive fails after extended use</span></span>

## <a name="diagnosis-and-resolutions"></a><span data-ttu-id="9419a-129">Vianmääritys ja ratkaisut</span><span class="sxs-lookup"><span data-stu-id="9419a-129">Diagnosis and resolutions</span></span>

<span data-ttu-id="9419a-130">Vianmääritys- ja ratkaisukentät ovat tiedotteita korjauksen näkökulmasta.</span><span class="sxs-lookup"><span data-stu-id="9419a-130">The diagnosis and resolution fields are statements from the repair perspective.</span></span> <span data-ttu-id="9419a-131">Nämä ovat vaiheita, jotka tekninen asiantuntija suoritti tutkiessaan ongelmaa.</span><span class="sxs-lookup"><span data-stu-id="9419a-131">These are the steps that a technician went through to investigate the problem.</span></span>

<span data-ttu-id="9419a-132">Vianmääritysalue sisältää ongelman ratkaisuksi suoritettavan toiminnon.</span><span class="sxs-lookup"><span data-stu-id="9419a-132">The diagnosis area covers the operation that must occur to solve the issue.</span></span> <span data-ttu-id="9419a-133">Vianmäärityskoodi kertoo, miten ongelma hoidettiin, ja ratkaisu voi olla se, että nimike korjattiin, korvattiin tai asiakas peruutti tilauksen.</span><span class="sxs-lookup"><span data-stu-id="9419a-133">The diagnosis code is how the problem was handled, and the resolution could be that the item was repaired, replaced, or the order was canceled by the customer.</span></span> <span data-ttu-id="9419a-134">Jos esimerkiksi tietokone korjataan, vianmääritysalue voi olla "viallinen osa", vianmäärityskoodi "asennettiin uusi näytönohjain" ja ratkaisu "korvattu".</span><span class="sxs-lookup"><span data-stu-id="9419a-134">For example, if the computer is repaired, the diagnosis area could be "defective part," the diagnosis code could be "new video card installed," and the resolution could be "replaced."</span></span>

## <a name="repair-stages"></a><span data-ttu-id="9419a-135">Korjauksen vaiheet</span><span class="sxs-lookup"><span data-stu-id="9419a-135">Repair stages</span></span>

<span data-ttu-id="9419a-136">Korjauksen vaiheet osoittavat korjausprosessin etenemisen.</span><span class="sxs-lookup"><span data-stu-id="9419a-136">Repair stages state the progress of the repair process.</span></span> <span data-ttu-id="9419a-137">Korjauksen vaiheella on **Valmis**-valmistumisparametri, joka osoittaa korjausrivin valmistumisen ja lopetuspäivämäärän ja ajan tallennuksen.</span><span class="sxs-lookup"><span data-stu-id="9419a-137">The repair stage has a **Finished** sign-off parameter that indicates that the repair line has been completed, and the finishing date and time has been recorded.</span></span>

## <a name="applying-repair-management"></a><span data-ttu-id="9419a-138">Korjausten hallinnan kohdistaminen</span><span class="sxs-lookup"><span data-stu-id="9419a-138">Applying repair management</span></span>

<span data-ttu-id="9419a-139">Nimikkeelle on määritettävä huoltotilauksessa huoltokohdesuhde, jotta korjauksen hallinnan voi kohdistaa nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="9419a-139">To apply repair management to an item, the item must be set up with a service object relation on a service order.</span></span> <span data-ttu-id="9419a-140">Huoltotilauksesta voi tämän jälkeen luoda korjausrivin, joka sisältää nykyisen ongelman tiedot.</span><span class="sxs-lookup"><span data-stu-id="9419a-140">From the service order you can then create a repair line with information about the current issue.</span></span> <span data-ttu-id="9419a-141">Korjausrivillä määritetään korjattavana oleva huoltokohde ja oireiden, vianmäärityksen ja suorituksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="9419a-141">On the repair line you define the service object that is in repair and information about symptoms, diagnosis, and execution.</span></span> <span data-ttu-id="9419a-142">Korjausriville voi luoda myös huomautuksen.</span><span class="sxs-lookup"><span data-stu-id="9419a-142">You can also create a note for the repair line.</span></span>

<span data-ttu-id="9419a-143">Voit luoda korjausrivejä jokaisessa korjausprosessin vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="9419a-143">You can create repair lines for each step in the repair process.</span></span>

## <a name="create-a-repair-line-on-a-service-order"></a><span data-ttu-id="9419a-144">Korjausrivin luominen huoltotilaukseen</span><span class="sxs-lookup"><span data-stu-id="9419a-144">Create a repair line on a service order</span></span>

1.  <span data-ttu-id="9419a-145">Valitse **Huoltohallinta** \> **Yleinen** \> **Huoltotilaukset** \> **Huoltotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="9419a-145">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="9419a-146">Valitse huoltotilaus, jossa korjausta kaipaava huoltokohde on.</span><span class="sxs-lookup"><span data-stu-id="9419a-146">Select the service order with the service object that needs repair.</span></span>

3.  <span data-ttu-id="9419a-147">Valitse **Korjaus** \> **Korjausrivit** avataksesi **Korjausrivit**-lomakkeen.</span><span class="sxs-lookup"><span data-stu-id="9419a-147">Click **Repair** \> **Repair lines** to open the **Repair lines** form.</span></span>

4.  <span data-ttu-id="9419a-148">Luo uusi rivi CTRL+N-näppäinyhdistelmällä.</span><span class="sxs-lookup"><span data-stu-id="9419a-148">Press CTRL+N to create a new line.</span></span>

5.  <span data-ttu-id="9419a-149">Valitse huoltokohde.</span><span class="sxs-lookup"><span data-stu-id="9419a-149">Select a service object.</span></span> <span data-ttu-id="9419a-150">Voit valita minkä tahansa huoltokohteen, jolle on määritetty kohteen suhde huoltotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="9419a-150">You can select any service object that has been set up with an object relation on the service order.</span></span>

6.  <span data-ttu-id="9419a-151">Valitse mitkä tahansa korjausriville haluamasi esiintyvien oireiden, vianmäärityksen ja suorituksen arvot. Luo tarvittaessa huomautus korjausriville valitsemalla **Huomautus**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="9419a-151">Select any of the preset symptoms, diagnosis, and execution values that are relevant in the repair line and then click the **Note** tab to create a note on the repair line, if needed.</span></span>

7.  <span data-ttu-id="9419a-152">Tallenna uusi korjausrivi painamalla näppäinyhdistelmää CTRL+S.</span><span class="sxs-lookup"><span data-stu-id="9419a-152">Press CTRL+S to save the new repair line.</span></span> <span data-ttu-id="9419a-153">**Luonnin päivämäärä ja aika** -kenttä **Yleinen**-välilehdellä **Korjausrivit**-lomakkeessa päivitetään tallennusajalla.</span><span class="sxs-lookup"><span data-stu-id="9419a-153">The **Created date and time** field in the **General** tab of the **Repair lines** form is updated with the time of saving.</span></span>

## <a name="tracking-progress-and-resolving-a-repair-issue"></a><span data-ttu-id="9419a-154">Edistymisen seuranta ja korjausongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="9419a-154">Tracking progress and resolving a repair issue</span></span>

<span data-ttu-id="9419a-155">Voit määrittää korjausriville korjauksen vaiheet, joiden avulla korjauksen edistymistä voi jäljittää.</span><span class="sxs-lookup"><span data-stu-id="9419a-155">You can set the repair stages of a repair line to track the progress of the repair.</span></span>

<span data-ttu-id="9419a-156">Kun korjausongelma on ratkaistu, voit sulkea korjausrivin.</span><span class="sxs-lookup"><span data-stu-id="9419a-156">When a repair issue is resolved, you can close the repair line.</span></span> <span data-ttu-id="9419a-157">Määritä korjauksen vaiheeksi vaihe, jossa on käytössä **Valmis**-ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="9419a-157">Set the repair stage to a stage with a **Finished** property enabled.</span></span> <span data-ttu-id="9419a-158">Nykyinen päivämäärä ja aika rekisteröidään rivin lopetusajaksi.</span><span class="sxs-lookup"><span data-stu-id="9419a-158">The current date and time is registered as the finish time on the line.</span></span>

## <a name="close-a-repair-line-for-a-resolved-issue"></a><span data-ttu-id="9419a-159">Ratkaistun tapauksen korjausrivin sulkeminen</span><span class="sxs-lookup"><span data-stu-id="9419a-159">Close a repair line for a resolved issue</span></span>

1.  <span data-ttu-id="9419a-160">Avaa **Korjausrivit**-lomake.</span><span class="sxs-lookup"><span data-stu-id="9419a-160">Open the **Repair lines** form.</span></span> <span data-ttu-id="9419a-161">Luo korjausrivi avaamalla seuraamalla aiemmin tässä aiheessa kerrottua menettelytapaa.</span><span class="sxs-lookup"><span data-stu-id="9419a-161">Follow the procedure earlier in this topic to create a repair line.</span></span>

2.  <span data-ttu-id="9419a-162">Valitse se korjausrivi, jossa suljettava korjaustapaus sijaitsee.</span><span class="sxs-lookup"><span data-stu-id="9419a-162">Select the repair line with the repair issue that you want to close.</span></span>

3.  <span data-ttu-id="9419a-163">Valitse **Korjauksen vaihe** -kentässä vaihe, jossa **Valmis**-ominaisuus on käytössä.</span><span class="sxs-lookup"><span data-stu-id="9419a-163">In the **Repair stage** field, select a stage with the **Finished** property enabled.</span></span>

  



