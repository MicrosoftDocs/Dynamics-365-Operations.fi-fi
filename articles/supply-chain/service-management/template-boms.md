---
title: Mallituoterakenteet
description: "Mallituoterakenteen avulla luodaan säännöllisesti huollettavien huoltokohteiden komponentit sisältävä vakioitu luettelo."
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/21/2018

---

# <a name="template-boms"></a><span data-ttu-id="ce937-103">Mallituoterakenteet</span><span class="sxs-lookup"><span data-stu-id="ce937-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ce937-104">Mallituoterakenteen avulla luodaan säännöllisesti huollettavien huoltokohteiden komponentit sisältävä vakioitu luettelo.</span><span class="sxs-lookup"><span data-stu-id="ce937-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="ce937-105">Mallituoterakenteessa luetteloidut komponentit edustavat huoltokohteen yksittäisiä alikomponentteja.</span><span class="sxs-lookup"><span data-stu-id="ce937-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="ce937-106">Kohdistamalla mallituoterakenteen huoltokohteeseen voit pitää kirjaa huoltokohteeseen vaihdetuista alikomponenteista.</span><span class="sxs-lookup"><span data-stu-id="ce937-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="ce937-107">Voit kohdistaa mallituoterakenteen huoltosopimukseen tai huoltotilaukseen liittämällä sen huoltokohteen suhteeseen.</span><span class="sxs-lookup"><span data-stu-id="ce937-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ce937-108">Voit liittää huoltokohteeseen vain yhden mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="ce937-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="ce937-109">Mallituoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="ce937-109">Create a template BOM</span></span>

<span data-ttu-id="ce937-110">Seuraavassa taulukossa on tietoja eri menetelmistä, joiden avulla voit luoda mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="ce937-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce937-111">Tapa</span><span class="sxs-lookup"><span data-stu-id="ce937-111">Method</span></span></p></th>
<th><p><span data-ttu-id="ce937-112">kuvaus</span><span class="sxs-lookup"><span data-stu-id="ce937-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce937-113">Tuotanto</span><span class="sxs-lookup"><span data-stu-id="ce937-113">Production</span></span></p></td>
<td><p><span data-ttu-id="ce937-114">Tuotannon mallituoterakenne perustuu tuotantotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="ce937-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="ce937-115">Tämä vaihtoehto on käytettävissä vain, jos käytössä on tuotantoympäristö.</span><span class="sxs-lookup"><span data-stu-id="ce937-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="ce937-116">Tämän vaihtoehdon etu on siinä, että sinulla on käytettävissä nimikkeen voimassa oleva ja yksityiskohtainen komponenttiluettelo.</span><span class="sxs-lookup"><span data-stu-id="ce937-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce937-117">Nimike BOM</span><span class="sxs-lookup"><span data-stu-id="ce937-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="ce937-118">Mallituoterakenne luodaan nimikkeen tuoterakenteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="ce937-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="ce937-119">Toisin kuin tuotannon tuoterakenne, nimikkeen tuoterakenne on staattinen luettelo komponenteista, joista nimike koostuu.</span><span class="sxs-lookup"><span data-stu-id="ce937-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce937-120">Aiemmin luotu malli</span><span class="sxs-lookup"><span data-stu-id="ce937-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="ce937-121">Malli luodaan aiemman mallituoterakenteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="ce937-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce937-122">Manuaalinen</span><span class="sxs-lookup"><span data-stu-id="ce937-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="ce937-123">Jos tiedät tarkalleen, mitä varaosia huoltokohteeseen yleensä vaihdetaan, saatat haluta luoda mallituoterakenteen manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ce937-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="ce937-124">Tämä tapa auttaa varmistamaan, että malliin sisällytettävät komponentit vastaavat työpaikan todellisia vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="ce937-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="ce937-125">Mallituoterakenteen kohdistaminen huoltosopimukseen tai huoltotilaukseen</span><span class="sxs-lookup"><span data-stu-id="ce937-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="ce937-126">Mallituoterakenne voidaan kohdistaa huoltosopimukseen, huoltotilaukseen tai niihin molempiin.</span><span class="sxs-lookup"><span data-stu-id="ce937-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="ce937-127">Huoltosopimus kattaa yleensä pitkäaikaisen asiakassuhteen.</span><span class="sxs-lookup"><span data-stu-id="ce937-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="ce937-128">Huollon tuoterakenteeseen tallennetut aiemmat korvaukset voidaan tallentaa huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="ce937-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="ce937-129">Mallituoterakenne voidaan kohdistaa myös huoltokohteeseen sen huoltohistorian kirjaamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ce937-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="ce937-130">Huollon tuoterakenteen aiempien tietojen kopioiminen</span><span class="sxs-lookup"><span data-stu-id="ce937-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="ce937-131">Voit kopioida huollon tuoterakennerivin historiatiedot yhdestä huoltosopimuksesta toiseen.</span><span class="sxs-lookup"><span data-stu-id="ce937-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="ce937-132">Kopioimalla huollon historiatiedot huoltosopimusten välillä voit säilyttää nimikkeen korvaustiedot.</span><span class="sxs-lookup"><span data-stu-id="ce937-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="ce937-133">**Esimerkki**</span><span class="sxs-lookup"><span data-stu-id="ce937-133">**Example**</span></span>

<span data-ttu-id="ce937-134">Olet määrittänyt asiakkaan autolle kolmen vuoden huoltosopimuksen.</span><span class="sxs-lookup"><span data-stu-id="ce937-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="ce937-135">Tänä aikana asiakas on tottunut hyvään palveluun, jota yritys tarjoaa.</span><span class="sxs-lookup"><span data-stu-id="ce937-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="ce937-136">Siksi sopimuksen päättyessä asiakas haluaa määrittää uuden.</span><span class="sxs-lookup"><span data-stu-id="ce937-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="ce937-137">Voit nyt neuvotella paremman sopimuksen yritykselle.</span><span class="sxs-lookup"><span data-stu-id="ce937-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="ce937-138">Kirjaukset vaihdetuista komponenteista voivat olla hyödyllisiä tulevaisuudessa, joten kopioit huollon tuoterakenteen historiatiedot uuteen sopimukseen.</span><span class="sxs-lookup"><span data-stu-id="ce937-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="ce937-139">Mallituoterakenteen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ce937-139">Modify the template BOM</span></span>

<span data-ttu-id="ce937-140">Jos huoltokohteeseen ei ole liitetty mallituoterakennetta, voit muokata tai poistaa mallituoterakenteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="ce937-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="ce937-141">Mallituoterakenteen huoltokohteeseen liittämisen jälkeen voit muokata vain tuoterakenteen paikallista versiota.</span><span class="sxs-lookup"><span data-stu-id="ce937-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="ce937-142">Jos haluat tehdä mallituoterakenteen paikallisesta versiosta kaksoiskappaleen, voit luoda uuden paikalliseen versioon perustuvan mallituoterakenteen.</span><span class="sxs-lookup"><span data-stu-id="ce937-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="ce937-143">Lisätietoja on kohdassa [Huoltotuoterakenteen muokkaaminen](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="ce937-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="ce937-144">Jos korvaat tuoterakenteen nimikkeen, voit rekisteröidä korvauksen tuoterakennerivillä tuoteraketeen suunnittelutyökalussa.</span><span class="sxs-lookup"><span data-stu-id="ce937-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="ce937-145">Voit halutessasi luoda korvauskohteelle huoltotilausrivin.</span><span class="sxs-lookup"><span data-stu-id="ce937-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="ce937-146">Jos luot huoltotilausrivin, voit laskuttaa korvausnimikkeen.</span><span class="sxs-lookup"><span data-stu-id="ce937-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="ce937-147">Jos et luo huoltotilausriviä korvaukselle, korvauksen rekisteröinti säilytetään huoltokohteen historian seuraamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ce937-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="ce937-148">Tuoterakennerivin tietojen näyttötavan muuttaminen</span><span class="sxs-lookup"><span data-stu-id="ce937-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="ce937-149">Voit muuttaa mallituoterakenteiden tai huollon tuoterakenteiden tietojen näyttötapaa.</span><span class="sxs-lookup"><span data-stu-id="ce937-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="ce937-150">Muutokset kohdistetaan kaikkiin mallituoterakenteisiin ja huollon tuoterakenteisiin.</span><span class="sxs-lookup"><span data-stu-id="ce937-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="ce937-151">Se sisältää myös huoltokohteisiin liitetyt tuoterakenteet.</span><span class="sxs-lookup"><span data-stu-id="ce937-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="ce937-152">Mallituoterakenteen numerosarjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ce937-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="ce937-153">Mallituoterakenteiden käyttämiseksi sinun on määritettävä kaksi numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="ce937-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="ce937-154">Määritä yksinumerosarja mallituoterakenteelle ja toinen tuoterakennehistorian rivinumerolle.</span><span class="sxs-lookup"><span data-stu-id="ce937-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ce937-155">Numerosarjoja käytetään tunnisteiden kohdistamiseksi tietueisiin, jotka edellyttävät niitä.</span><span class="sxs-lookup"><span data-stu-id="ce937-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="ce937-156">Ennen kuin voit liittää numerosarjan mallituoterakenteeseen tuoterakennehistorian rivinumeroon, numerosarjakoodit on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="ce937-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="ce937-157">Määritä numerosarjat</span><span class="sxs-lookup"><span data-stu-id="ce937-157">Set up number sequences</span></span>

1.  <span data-ttu-id="ce937-158">Valitse **Numerosarjat**-luettelosivu ja luo numerosarjat mallituoterakenteita ja tuoterakennehistorian rivinumeroa varten.</span><span class="sxs-lookup"><span data-stu-id="ce937-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="ce937-159">Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltohallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="ce937-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="ce937-160">Valitse **Numerosarjat**, ja valitse sitten numerosarjakoodi numerosarjaviitteille, jotka loit **Numerosarjat**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="ce937-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="ce937-161">Tallenna muutokset sulkemalla lomake.</span><span class="sxs-lookup"><span data-stu-id="ce937-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ce937-162">Järjestelmä käyttää tuoterakennehistorian rivinumeroa yhdistääkseen tuoterakenteen historian tapahtumat huoltosopimukseen tai huoltotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="ce937-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="ce937-163">Numeroa ei näytetä käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="ce937-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="ce937-164">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="ce937-164">See also</span></span>

[<span data-ttu-id="ce937-165">Mallituoterakenteen luominen</span><span class="sxs-lookup"><span data-stu-id="ce937-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="ce937-166">Mallituoterakenteiden hallitseminen kohteiden suhteissa</span><span class="sxs-lookup"><span data-stu-id="ce937-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="ce937-167">Huoltotuoterakenteen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ce937-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 



