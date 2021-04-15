---
title: Sovelluksen metatietojen valmisteleminen RCS:ssä käytettäviksi
description: Tässä aiheessa käsitellään sovelluksen metatiedot sisältävän uuden raportointimäärityksen luontia.
author: NickSelin
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5fe475bd0fceea7e1e8edf7c375d34a4be6d92a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751031"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="ca9d9-103">Sovelluksen metatietojen valmisteleminen RCS:ssä käytettäviksi</span><span class="sxs-lookup"><span data-stu-id="ca9d9-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca9d9-104">Seuraavat vaiheet selittävät, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi luoda uuden sähköisen raportoinnin (ER) konfiguraation. Tämä konfiguraatio sisältää sovelluksen metatiedot ER-mallin yhdistämismääritysten suunnittelemiseen Regulatory Configuration Servicessä (RCS).</span><span class="sxs-lookup"><span data-stu-id="ca9d9-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="ca9d9-105">Tätä konfiguraatiota käytetään sen ER-näytemallin yhdistämismäärityksen suunnittelemiseen, jolla käytetään ulkomaankauppatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="ca9d9-106">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="ca9d9-107">Näitä vaiheita varten on ensin suoritettava ohjeaiheessa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ca9d9-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="ca9d9-108">Prerequisites</span></span>
1.    <span data-ttu-id="ca9d9-109">Valitse **Organisaation hallinto** > **Työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="ca9d9-110">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ca9d9-111">Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="ca9d9-112">Valitse **Metatietojen konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="ca9d9-113">Oletetaan, että RCS:ää käytetään suunnittelemaan sellainen Finance and Operations -sovelluksen ER-ratkaisu, jolla luodaan ulkomaankaupan liiketoimintatoimialueen tietoja sisältäviä sähköisiä asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="ca9d9-114">Jos haluat määrittää ER-tietomallin ja tarvittavien tietojen lähteiden välisen määrityksen, RCS:ssä on oltava Finance and Operations -sovelluksen metatietojen käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="ca9d9-115">Tämän vuoksi ER-ratkaisun suunnittelun osana on määritettävä uusi ER-metatietokonfiguraatio, joka sisältää kaikki valitun liiketoimintatoimialueen ER-raporttien luontiin tällä hetkellä tarvittavat metatiedot.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="ca9d9-116">Metatietojen konfiguroinnin lisääminen</span><span class="sxs-lookup"><span data-stu-id="ca9d9-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="ca9d9-117">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="ca9d9-118">Kirjoita **Nimi**-kenttään Ulkomaankaupan yhdistäminen.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="ca9d9-119">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="ca9d9-120">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="ca9d9-121">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ca9d9-122">Voit valita joko koko sovelluksen tai valittujen mallien tai moduulien kaikki metatiedot.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="ca9d9-123">Muista kuitenkin, että tässä tapauksessa seuraavat metatiedot lisätään automaattisesti: tietue-, luettelo- ja laajennetut tietotyyppitaulukot.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="ca9d9-124">Jos muita metatietoja tarvitaan, ne on lisättävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="ca9d9-125">Ulkomaankauppatapahtumiin liittyvät metatiedot saadaan valitsemalla metatietonimikkeet manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="ca9d9-126">Valitse **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="ca9d9-127">Valitse **Taulukon tietueet**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="ca9d9-128">Voit suodattaa pikasuodattimella **Nimi**-kenttää arvolla Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="ca9d9-129">Valitse **Intrastat**-taulukkotietue.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="ca9d9-130">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-130">Click **OK**.</span></span>
  
<span data-ttu-id="ca9d9-131">Intrastat-taulukkotietueen metatiedot on lisätty.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="ca9d9-132">Laajenna puussa **Taulukkotietueet Intrastat**\>**Suhteet**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="ca9d9-133">Valitse puussa **Taulukkotietueet Intrastat**\>**Suhteet\IntrastatCommodity (Taulukkotietueet EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="ca9d9-134">Valitse **Lisää metatiedot**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ca9d9-135">Valitun taulukkotietueen pakollisten suhteiden metatiedot on lisättävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="ca9d9-136">Valitse **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="ca9d9-137">Valitse **Luettelointi**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="ca9d9-138">Voit suodattaa pikasuodattimella **Nimi**-kenttää arvolla IntrastatDirection.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="ca9d9-139">Valitse **IntrastatDirection-luettelointi**-tietue.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="ca9d9-140">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="ca9d9-141">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="ca9d9-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="ca9d9-143">Metatietokonfiguraation luonnosversion suorittaminen</span><span class="sxs-lookup"><span data-stu-id="ca9d9-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="ca9d9-144">Valitse **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="ca9d9-145">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="ca9d9-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="ca9d9-147">Valitse valmis versio **1**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="ca9d9-148">Metatietokonfiguraation valmiin version vienti sovelluksesta XML-tiedostona</span><span class="sxs-lookup"><span data-stu-id="ca9d9-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="ca9d9-149">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="ca9d9-150">Valitse **Vie XML-tiedostona**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="ca9d9-151">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-151">Click **OK**.</span></span> 
    
<span data-ttu-id="ca9d9-152">Luotu ER-metatietokonfiguraatio on tallennettu XML-tiedostona, joka voidaan tuoda RCS:ään ja jota voidaan käyttää ulkomaankaupan liiketoimintatoimialueen metatietojen tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="ca9d9-153">Näiden tietojen perusteella voidaan määrittää sovelluksen metatietojen ja ER-tietomallin välisen yhdistämismäärityksen.</span><span class="sxs-lookup"><span data-stu-id="ca9d9-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]