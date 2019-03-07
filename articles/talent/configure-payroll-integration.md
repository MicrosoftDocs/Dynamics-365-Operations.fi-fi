---
title: Palkanlaskennan Talent and Dayforce -integroinnin määrittäminen
description: Tässä ohjeaiheessa kerrotaan, että kuinka konfiguroida integrointeja Microsoft Dynamics 365 for Talentin ja Ceridian Dayforcen välillä voidaksesi käsitellä palkka-ajoa.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304183"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="00e45-103">Talentin ja Dayforcen välisen palkanlaskennan integroinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00e45-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="00e45-104">Microsoft Dynamics 365 for Talentin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="00e45-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="00e45-105">Sekä Talentin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.</span><span class="sxs-lookup"><span data-stu-id="00e45-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="00e45-106">Käytettäessä jotakin palvelua, kuten Dayforcea palkka-ajojen suorittamiseen, on otettava käyttöön integrointi Talentissa.</span><span class="sxs-lookup"><span data-stu-id="00e45-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="00e45-107">Integrointi edellyttää tiettyjä tietoja Talentista.</span><span class="sxs-lookup"><span data-stu-id="00e45-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="00e45-108">Sinun on varmistettava, että Dayforceen yhdistetyt tiedot on konfiguroitu Talentissa siten, että ne tukevat integrointia.</span><span class="sxs-lookup"><span data-stu-id="00e45-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="00e45-109">Integraatio käyttää seuraavanlaisia laajoja tietoryhmiä:</span><span class="sxs-lookup"><span data-stu-id="00e45-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="00e45-110">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-110">Human resources data</span></span>
- <span data-ttu-id="00e45-111">Kompensaatiotiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-111">Compensation data</span></span>
- <span data-ttu-id="00e45-112">Palkanlaskentatietoja, kuten maksujaksot, maksukaudet ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="00e45-113">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-113">Worker data</span></span>

<span data-ttu-id="00e45-114">Tässä ohjeaiheessa kuvataan vaiheita, joita sinun on noudatettava ottaaksesi integroinnin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="00e45-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="00e45-115">Lisäksi kerrotaan minkä tyyppisiä tietoja ja konfigurointitietoja integrointi edellyttää.</span><span class="sxs-lookup"><span data-stu-id="00e45-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="00e45-116">Ota integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="00e45-116">Enable the integration</span></span>

<span data-ttu-id="00e45-117">Ota integraatio käyttöön Talentissa ja lisää konfiguraatiotiedot muodostaaksesi yhteyden Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="00e45-118">Mikäli haluat kirjanpitotapahtuman, joka valmistetaan ja tuodaan Microsoft Dynamics 365 for Finance and Operationsiin, sinun on perustettava myös Microsoft Azure -tallennustili ja kirjoitettava Azure-tallennuksen yhteyden muodostuskomento Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="00e45-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="00e45-119">Ota integrointi käyttöön Talentissa seuraavien vaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="00e45-120">Valitse **Järjestelmänvalvoja**-sivulla **konfiguroinnin integrointi**.</span><span class="sxs-lookup"><span data-stu-id="00e45-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="00e45-121">Lisää File Transfer Protocol (FTP) -päätepiste ja suojattu FTP-kansiopolku.</span><span class="sxs-lookup"><span data-stu-id="00e45-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="00e45-122">Kirjoita sen käyttäjän käyttäjänimi ja salasana, joka voi käyttää suojattua FTP-päätepistettä ja kansiopolkua.</span><span class="sxs-lookup"><span data-stu-id="00e45-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="00e45-123">Testaa yhteys kuten vaadittu ja määritä **Ota käyttöön palkanmaksun integrointi** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="00e45-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="00e45-124">Kun integrointi otetaan käyttöön, tietojen viennin paketti ja tiedostot luodaan ja taajuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="00e45-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="00e45-125">Voit muuttaa tätä taajuutta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="00e45-126">Lisätietoja Azure-tallennustilien ja Azure-tallennusyhteyden yhteysmerkkijonoista seuraavissa Azure-aiheissa:</span><span class="sxs-lookup"><span data-stu-id="00e45-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="00e45-127">Lisätietoja Azure-tallennustileistä</span><span class="sxs-lookup"><span data-stu-id="00e45-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="00e45-128">Määritä Azure-tallennustilan yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="00e45-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="00e45-129">Määritä tietosi</span><span class="sxs-lookup"><span data-stu-id="00e45-129">Configure your data</span></span> 

<span data-ttu-id="00e45-130">Voidaksesi käsitellä palkanlaskentaa, sinun on määritettävä henkilöstöhallinnon tiedot Talentissa.</span><span class="sxs-lookup"><span data-stu-id="00e45-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="00e45-131">On määritettävä organisaation tiedot, kuten työt ja toimet sekä edut ja kompensaatiotiedot.</span><span class="sxs-lookup"><span data-stu-id="00e45-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="00e45-132">Nämä tiedot sisältävät työllisyys-, palkka- ja vähennystiedot, jotka vaaditaan, jotta voidaan luoda työntekijän palkka.</span><span class="sxs-lookup"><span data-stu-id="00e45-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="00e45-133">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="00e45-134">Edut</span><span class="sxs-lookup"><span data-stu-id="00e45-134">Benefits</span></span> 

<span data-ttu-id="00e45-135">Henkilöstöhallinto sisältää työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="00e45-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="00e45-136">Luodessasi etuja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="00e45-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="00e45-137">Etusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="00e45-137">Benefit plans</span></span>

- <span data-ttu-id="00e45-138">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-138">Plan (required)</span></span>
- <span data-ttu-id="00e45-139">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-139">Type (required)</span></span>
- <span data-ttu-id="00e45-140">Palkanlaskennan vaikutus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-140">Payroll impact (required)</span></span>
- <span data-ttu-id="00e45-141">Palauta velvoitteet</span><span class="sxs-lookup"><span data-stu-id="00e45-141">Recover arrears</span></span>
- <span data-ttu-id="00e45-142">Vähennysmenetelmä</span><span class="sxs-lookup"><span data-stu-id="00e45-142">Deduction method</span></span>
- <span data-ttu-id="00e45-143">Vähennyksen prioriteetti</span><span class="sxs-lookup"><span data-stu-id="00e45-143">Deduction priority</span></span>
- <span data-ttu-id="00e45-144">Rajaa kausi</span><span class="sxs-lookup"><span data-stu-id="00e45-144">Limit period</span></span>
- <span data-ttu-id="00e45-145">Rajasumma</span><span class="sxs-lookup"><span data-stu-id="00e45-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="00e45-146">Edut</span><span class="sxs-lookup"><span data-stu-id="00e45-146">Benefits</span></span>

- <span data-ttu-id="00e45-147">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-147">Plan (required)</span></span>
- <span data-ttu-id="00e45-148">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-148">Type (required)</span></span>
- <span data-ttu-id="00e45-149">Vaihtoehto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-149">Option (required)</span></span>
- <span data-ttu-id="00e45-150">Edun tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-150">Benefit ID (required)</span></span>
- <span data-ttu-id="00e45-151">Tiheys</span><span class="sxs-lookup"><span data-stu-id="00e45-151">Frequency</span></span>
- <span data-ttu-id="00e45-152">Peruste</span><span class="sxs-lookup"><span data-stu-id="00e45-152">Basis</span></span>
- <span data-ttu-id="00e45-153">Summa tai hinta</span><span class="sxs-lookup"><span data-stu-id="00e45-153">Amount or rate</span></span>
- <span data-ttu-id="00e45-154">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="00e45-155">Tuetut maksutiheydet</span><span class="sxs-lookup"><span data-stu-id="00e45-155">Supported frequencies</span></span> 

- <span data-ttu-id="00e45-156">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="00e45-156">Weekly</span></span>
- <span data-ttu-id="00e45-157">Kahden viikon välein</span><span class="sxs-lookup"><span data-stu-id="00e45-157">Bi-weekly</span></span>
- <span data-ttu-id="00e45-158">Joka toinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="00e45-158">Semi-monthly</span></span>
- <span data-ttu-id="00e45-159">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="00e45-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="00e45-160">Tuetut pohjat</span><span class="sxs-lookup"><span data-stu-id="00e45-160">Supported bases</span></span> 

- <span data-ttu-id="00e45-161">Kiinteä summa</span><span class="sxs-lookup"><span data-stu-id="00e45-161">Fixed amount</span></span>
- <span data-ttu-id="00e45-162">Ansioiden prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="00e45-162">Percent of earnings</span></span>
- <span data-ttu-id="00e45-163">Tuottavat tunnit</span><span class="sxs-lookup"><span data-stu-id="00e45-163">Productive hours</span></span>

<span data-ttu-id="00e45-164">Dayforce luo seuraavat vähennykset, jotka perustuvat palkanlaskennan vaikutukseen, joka on määritelty etusuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="00e45-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="00e45-165">Talentin valinta</span><span class="sxs-lookup"><span data-stu-id="00e45-165">Selection in Talent</span></span>        | <span data-ttu-id="00e45-166">Tulos Dayforcessa</span><span class="sxs-lookup"><span data-stu-id="00e45-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="00e45-167">None</span><span class="sxs-lookup"><span data-stu-id="00e45-167">None</span></span>                       | <span data-ttu-id="00e45-168">Vähennyksiä ei luoda.</span><span class="sxs-lookup"><span data-stu-id="00e45-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="00e45-169">Vain vähennys</span><span class="sxs-lookup"><span data-stu-id="00e45-169">Deduction only</span></span>             | <span data-ttu-id="00e45-170">Työntekijävähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="00e45-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="00e45-171">Vain osuus</span><span class="sxs-lookup"><span data-stu-id="00e45-171">Contribution only</span></span>          | <span data-ttu-id="00e45-172">Työnantajavähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="00e45-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="00e45-173">Vähennys ja osuus</span><span class="sxs-lookup"><span data-stu-id="00e45-173">Deduction and contribution</span></span> | <span data-ttu-id="00e45-174">Työntekijän ja työnantajan vähennykset luodaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="00e45-175">Lisätietoja etuohjelman määrittämisestä ja hallitsemisesta seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="00e45-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="00e45-176">Työsuhde-etuohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="00e45-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="00e45-177">Luo uusi etu</span><span class="sxs-lookup"><span data-stu-id="00e45-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="00e45-178">Määritä edun oikeutussäännöt ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="00e45-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="00e45-179">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="00e45-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="00e45-180">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="00e45-180">Compensation</span></span> 

<span data-ttu-id="00e45-181">Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista.</span><span class="sxs-lookup"><span data-stu-id="00e45-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="00e45-182">Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="00e45-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="00e45-183">Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="00e45-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="00e45-184">Dayforce käyttää kompensaatiotietoja laskeakseen työntekijän tunti- tai vuosihinnan.</span><span class="sxs-lookup"><span data-stu-id="00e45-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="00e45-185">Kiinteät kompensaatiosuunnitelmat ja palkkojen muunnokset vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="00e45-186">Työntekijöiden täytyy olla liitettynä kiinteään kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="00e45-187">Katso lisätietoja kompensaatiosuunnitelmista seuraavista ohjeaiheista:</span><span class="sxs-lookup"><span data-stu-id="00e45-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="00e45-188">Kiinteiden kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="00e45-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="00e45-189">Muuttuvien kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="00e45-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="00e45-190">Palkka- ja kompensaatiorakenteen ja -suunnitelmien kehittäminen</span><span class="sxs-lookup"><span data-stu-id="00e45-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="00e45-191">Kompensaation käsittely</span><span class="sxs-lookup"><span data-stu-id="00e45-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="00e45-192">Kompensaatioprosessin määrittäminen ja tulosten laskeminen</span><span class="sxs-lookup"><span data-stu-id="00e45-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="00e45-193">Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="00e45-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="00e45-194">Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="00e45-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="00e45-195">Työt</span><span class="sxs-lookup"><span data-stu-id="00e45-195">Jobs</span></span> 

<span data-ttu-id="00e45-196">Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään.</span><span class="sxs-lookup"><span data-stu-id="00e45-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="00e45-197">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="00e45-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="00e45-198">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="00e45-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="00e45-199">Määritä uudet työt</span><span class="sxs-lookup"><span data-stu-id="00e45-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="00e45-200">Toimet</span><span class="sxs-lookup"><span data-stu-id="00e45-200">Positions</span></span>

<span data-ttu-id="00e45-201">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="00e45-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="00e45-202">Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="00e45-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="00e45-203">Osastolla on toimi.</span><span class="sxs-lookup"><span data-stu-id="00e45-203">A position exists in a department.</span></span> <span data-ttu-id="00e45-204">Vain yksi työntekijä voidaan liittää yhteen toimeen.</span><span class="sxs-lookup"><span data-stu-id="00e45-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="00e45-205">Muista seuraavat tiedot ja määritykset, kun määrität toimia:</span><span class="sxs-lookup"><span data-stu-id="00e45-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="00e45-206">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-206">Position (required)</span></span>
- <span data-ttu-id="00e45-207">Kuvaus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-207">Description (required)</span></span>
- <span data-ttu-id="00e45-208">Työ (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-208">Job (required)</span></span>
- <span data-ttu-id="00e45-209">Osasto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-209">Department (required)</span></span>
- <span data-ttu-id="00e45-210">Toimen tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-210">Position type (required)</span></span>
- <span data-ttu-id="00e45-211">Kokopäiväinen (FTE)</span><span class="sxs-lookup"><span data-stu-id="00e45-211">Full-time equivalent</span></span>
- <span data-ttu-id="00e45-212">Vuosittaiset vakiotunnit (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="00e45-213">Yrityksen maksama (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="00e45-214">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-214">Pay cycle (required)</span></span>
- <span data-ttu-id="00e45-215">Oletusarvo taloushallinnon dimensio – kustannuspaikka (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="00e45-216">Työntekijän määritys – työntekijä, tehtävän alkamisaika, tehtävän lopetusaika, syykoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="00e45-217">Mikäli useita toimia samalla osastolla liittyy samaan työhön, ne yhdistetään yhteen toimeen Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="00e45-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="00e45-218">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="00e45-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="00e45-219">Työvoiman järjestäminen osastojen, töiden ja toimien avulla</span><span class="sxs-lookup"><span data-stu-id="00e45-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="00e45-220">Toimien määritys</span><span class="sxs-lookup"><span data-stu-id="00e45-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="00e45-221">Osastot</span><span class="sxs-lookup"><span data-stu-id="00e45-221">Departments</span></span>

<span data-ttu-id="00e45-222">Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="00e45-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="00e45-223">Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.</span><span class="sxs-lookup"><span data-stu-id="00e45-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="00e45-224">Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin.</span><span class="sxs-lookup"><span data-stu-id="00e45-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="00e45-225">Osastot voivat olla tulosvastuullisia.</span><span class="sxs-lookup"><span data-stu-id="00e45-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="00e45-226">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="00e45-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="00e45-227">Osaston luominen ja liittäminen osastohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="00e45-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="00e45-228">Määritä uudet osastot</span><span class="sxs-lookup"><span data-stu-id="00e45-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="00e45-229">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="00e45-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="00e45-230">Palkkajakso määrittää kuinka usein palkkalistoja käytetään, ja minä tiettyinä päivinä työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="00e45-231">Esimerkiksi palkkajakso voi olla kuukausittainen ja työntekijöille voidaan maksaa kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="00e45-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="00e45-232">Vaihtoehtoisesti palkkajakso voi olla viikoittainen ja työntekijöille voidaan maksaa tiistaina palkkajakson päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="00e45-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="00e45-233">Palkkajaksot on osoitettu toimiin, jotta voidaan valvoa milloin näissä tehtävissä oleville työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="00e45-234">Luotuasi palkkajaksoja, voit luoda maksukausia kullekin jaksolle.</span><span class="sxs-lookup"><span data-stu-id="00e45-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="00e45-235">Jokaisella palkkakaudella on maksun oletuspäivämäärä, joka perustuu antamiisi tietoihin.</span><span class="sxs-lookup"><span data-stu-id="00e45-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="00e45-236">Voit kuitenkin muokata maksun oletuspäivämäärää salliaksesi poikkeuksia, kuten kun maksupäivämäärä osuu vapaapäivälle.</span><span class="sxs-lookup"><span data-stu-id="00e45-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="00e45-237">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="00e45-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="00e45-238">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-238">Pay cycle (required)</span></span>
- <span data-ttu-id="00e45-239">Maksujakson tiheys (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="00e45-240">Kauden alkamispäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="00e45-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="00e45-241">Oletusmaksupäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="00e45-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="00e45-242">Nämä tiedot on integroitu Dayforce-palkkaryhmien kanssa ja eriteltynä eriteltyinä maittain tai alueittain kullekin maksujaksolle.</span><span class="sxs-lookup"><span data-stu-id="00e45-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="00e45-243">Ennen integraatiota on luotava vähintään yksi palkkakausi.</span><span class="sxs-lookup"><span data-stu-id="00e45-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="00e45-244">Dayforce luo maksuryhmäkalentereita ja maksupäiviä, jotka perustuvat ensimmäisen palkkakauden alkamispäivämäärään ja määritetty oletusmaksupäivä on asetettu Talentissa.</span><span class="sxs-lookup"><span data-stu-id="00e45-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="00e45-245">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-245">Earning codes</span></span>

<span data-ttu-id="00e45-246">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="00e45-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="00e45-247">Tunnuksissa on erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="00e45-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="00e45-248">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="00e45-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="00e45-249">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-249">Earning Code (required)</span></span>
- <span data-ttu-id="00e45-250">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-250">Description</span></span>
- <span data-ttu-id="00e45-251">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="00e45-251">Unit of measure</span></span>
- <span data-ttu-id="00e45-252">Tuottava</span><span class="sxs-lookup"><span data-stu-id="00e45-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="00e45-253">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-253">Worker data</span></span>

<span data-ttu-id="00e45-254">Tietueet eri työntekijöille, joita sinulla on ovat tärkeitä henkilöstöhallinnossa ja palkanlaskentajärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="00e45-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="00e45-255">Tietueisiin lisättäviä tietoja käytetään työntekijöiden ja henkilökohtaisten tietojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="00e45-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="00e45-256">Voit ylläpitää työntekijöille seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="00e45-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="00e45-257">**Perustiedot** – Ylläpidä työntekijän perustietoja, kuten yhteystiedot, demografiatiedot, tunnistetiedot, perheen tiedot, asevelvollisuuden tila, ekspatriaatin tiedot ja omat yhteyshenkilöt ja hätäyhteyshenkilöt.</span><span class="sxs-lookup"><span data-stu-id="00e45-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="00e45-258">**Työsuhde** – Ylläpidä tietoja työntekijän työsuhteesta, kuten yrityksen tai organisaation kytköksistä, toimen määrityksestä, aloitus- ja päättymispäivämääristä, työkelpoisuudesta, työehdoista, eläkkestä, lomista ja uudelleensijoittumisesta.</span><span class="sxs-lookup"><span data-stu-id="00e45-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="00e45-259">**Lomat ja poissaolot** –Ylläpidä tietoa työntekijän poissaoloista, kuten työaikakalentereista, poissaolotapahtumista ja poissaoloasetuksista.</span><span class="sxs-lookup"><span data-stu-id="00e45-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="00e45-260">**Kompensaatio ja palkanlaskenta** – Ylläpidä työntekijän kompensaatiosuunnitelmien tietoja ja palkanlaskentatietoja, kuten suunnitelmien toteutuminen, palkkiot, suorituskyky, provisio, verotiedot, eläkkeelle jääminen ja palkan vähennykset.</span><span class="sxs-lookup"><span data-stu-id="00e45-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="00e45-261">Kirjoittaessasi työntekijätietoja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="00e45-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="00e45-262">Yleistiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-262">General information</span></span>

- <span data-ttu-id="00e45-263">Henkilönumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-263">Personnel number (required)</span></span>
- <span data-ttu-id="00e45-264">Etunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-264">First name (required)</span></span>
- <span data-ttu-id="00e45-265">Sukunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-265">Last name (required)</span></span>
- <span data-ttu-id="00e45-266">Toinen nimi</span><span class="sxs-lookup"><span data-stu-id="00e45-266">Middle name</span></span>
- <span data-ttu-id="00e45-267">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="00e45-267">Seniority date</span></span>
- <span data-ttu-id="00e45-268">Tunnetaan nimellä</span><span class="sxs-lookup"><span data-stu-id="00e45-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="00e45-269">Henkilökohtaiset tiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-269">Personal information</span></span>

- <span data-ttu-id="00e45-270">Siviilisääty (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-270">Marital status (required)</span></span>
- <span data-ttu-id="00e45-271">Syntymäpäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-271">Birth date (required)</span></span>
- <span data-ttu-id="00e45-272">Sukupuoli (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-272">Gender (required)</span></span>
- <span data-ttu-id="00e45-273">Henkilö on invalidi</span><span class="sxs-lookup"><span data-stu-id="00e45-273">Person with disabilities</span></span>
- <span data-ttu-id="00e45-274">Kansalaisuus, maa, alue (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="00e45-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="00e45-275">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-275">Address information</span></span>

- <span data-ttu-id="00e45-276">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-276">Primary (required)</span></span>
- <span data-ttu-id="00e45-277">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-277">Country/region (required)</span></span>
- <span data-ttu-id="00e45-278">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-278">Postal code (required)</span></span>
- <span data-ttu-id="00e45-279">Kadunnumero (pakollinen) (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="00e45-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="00e45-280">Rakennusta koskeva lisätieto (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="00e45-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="00e45-281">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-281">City (required)</span></span>
- <span data-ttu-id="00e45-282">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-282">State (required)</span></span>
- <span data-ttu-id="00e45-283">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="00e45-284">Yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-284">Contact information</span></span> 

- <span data-ttu-id="00e45-285">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-285">Primary (required)</span></span>
- <span data-ttu-id="00e45-286">Yhteystiedon numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-286">Contact number (required)</span></span>
- <span data-ttu-id="00e45-287">Alanumero</span><span class="sxs-lookup"><span data-stu-id="00e45-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="00e45-288">Palkanlaskentatiedot ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-288">Payroll information and earning codes</span></span>

<span data-ttu-id="00e45-289">Työntekijöille voidaan antaa erityisiä tuloja tietyllä maksutaajuudella ja toivotulla maksutavalla.</span><span class="sxs-lookup"><span data-stu-id="00e45-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="00e45-290">Seuraavia kenttiä käytetään Dayforcessa sen varmistamiseksi, että näitä määrityksiä ja asetuksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="00e45-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="00e45-291">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-291">Earning codes</span></span>

- <span data-ttu-id="00e45-292">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-292">Position (required)</span></span>
- <span data-ttu-id="00e45-293">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-293">Earning Code (required)</span></span>
- <span data-ttu-id="00e45-294">Taajuus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-294">Frequency (required)</span></span>
- <span data-ttu-id="00e45-295">Summa (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="00e45-296">Palkanlaskentatiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-296">Payroll information</span></span>

- <span data-ttu-id="00e45-297">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="00e45-297">Payment Method</span></span>
- <span data-ttu-id="00e45-298">Talousalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-298">Economic Region (required)</span></span>
- <span data-ttu-id="00e45-299">Työsuhde-etujen tunnus</span><span class="sxs-lookup"><span data-stu-id="00e45-299">Employee Benefits ID</span></span>
- <span data-ttu-id="00e45-300">Kansallinen/alueellinen tunnusnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-300">National ID Number (required)</span></span>
- <span data-ttu-id="00e45-301">Sotilaspalveluksen numero</span><span class="sxs-lookup"><span data-stu-id="00e45-301">Military Service Number</span></span>
- <span data-ttu-id="00e45-302">Vuoron tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-302">Shift ID (required)</span></span>
- <span data-ttu-id="00e45-303">Veronumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-303">Tax Number (required)</span></span>
- <span data-ttu-id="00e45-304">Ammattijärjestön tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-304">Union ID (required)</span></span>
- <span data-ttu-id="00e45-305">Työpäivän tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-305">Work Day ID (required)</span></span>
- <span data-ttu-id="00e45-306">Työluvan numero</span><span class="sxs-lookup"><span data-stu-id="00e45-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="00e45-307">Maksutavoista Meksiko tukee seuraavia: **Käteinen**, **shekki** (yrityksen fyysinen shekki) ja **sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="00e45-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="00e45-308">Mikäli maksutapaa ei ole määritetty, **shekki** on oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="00e45-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="00e45-309">Työsuhteen tiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-309">Employment details</span></span>

<span data-ttu-id="00e45-310">Työntekijöiden yksityiskohtaista historiaa käytetään keskeisenä informaationa, jolla saadaan työntekijän palkkaus, irtisanominen ja rekrytointitilastot Dayforcesta.</span><span class="sxs-lookup"><span data-stu-id="00e45-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="00e45-311">Dayforce tukee kerrallaan vain yhtä aktiivisen työntekijän tietuetta.</span><span class="sxs-lookup"><span data-stu-id="00e45-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="00e45-312">Työsuhteen alkamispäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-312">Employment start date (required)</span></span>
- <span data-ttu-id="00e45-313">Työsuhteen päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-313">Employment end date</span></span>
- <span data-ttu-id="00e45-314">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-314">Start date</span></span>
- <span data-ttu-id="00e45-315">Muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-315">Adjusted start date</span></span>
- <span data-ttu-id="00e45-316">Työsuhteen päättymispäivä (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="00e45-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="00e45-317">Työsuhteen päättymissyy (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="00e45-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="00e45-318">Seuraavien tietojen avulla lasketaan työntekijän tärkeimmät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="00e45-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="00e45-319">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-319">Talent</span></span>                | <span data-ttu-id="00e45-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e45-321">Viimeisimmän työhönoton päivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-321">Most recent hire date</span></span> | <span data-ttu-id="00e45-322">Työntekijän työsuhteen alku voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="00e45-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="00e45-323">Työsuhteen loppumispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-323">Termination date</span></span>      | <span data-ttu-id="00e45-324">Työntekijän työsuhteen loppu voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="00e45-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="00e45-325">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-325">Start date</span></span>            | <span data-ttu-id="00e45-326">Muutettu alkamispäivämäärä, alkamispäivämäärä tai työsuhteen alku ei-aktiivisessa työsuhteen historiatietueessa</span><span class="sxs-lookup"><span data-stu-id="00e45-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="00e45-327">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-327">Original hire date</span></span>    | <span data-ttu-id="00e45-328">Varhaisin työhistoriatietueen työsuhteen alku</span><span class="sxs-lookup"><span data-stu-id="00e45-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="00e45-329">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="00e45-329">Compensation</span></span>

<span data-ttu-id="00e45-330">Kiinteän kompensaatiosuunnitelmaan tulee liittää jokaisen työntekijän ensisijainen toimi koko työsuhteen ajalla.</span><span class="sxs-lookup"><span data-stu-id="00e45-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="00e45-331">Ajanjakso alkaa siitä päivämäärästä, jona työntekijä palkattiin (tai työsuhteen alkamispäivämäärä) ja jatkuu, kunnes työsuhde loppuu.</span><span class="sxs-lookup"><span data-stu-id="00e45-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="00e45-332">Voimaantulopäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-332">Effective Date (required)</span></span>
- <span data-ttu-id="00e45-333">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="00e45-333">Expiration date</span></span>
- <span data-ttu-id="00e45-334">Palkkio (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-334">Pay Rate (required)</span></span>
- <span data-ttu-id="00e45-335">Palkkion muunnokset (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="00e45-336">Vuosittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="00e45-337">Tunnittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="00e45-338">Mikäli tuntityöntekijällä on useita toimia, ensisijaisen toimen kiinteä kompensaation tuodaan Dayforceen työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="00e45-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="00e45-339">Ei-ensisijaisten toimien tuntihinta tallennetaan Dayforcen vastaavaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="00e45-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="00e45-340">Mikäli palkallisella työntekijällä on useita toimia, kumulatiivinen tuntihinta ja vuosittainen palkka kaikista aktiivisista toimista johdetaan ja käytetään työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="00e45-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="00e45-341">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="00e45-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="00e45-342">Sosiaaliturvan tunniste</span><span class="sxs-lookup"><span data-stu-id="00e45-342">Social Security identifier</span></span> 

<span data-ttu-id="00e45-343">Jokaisella työntekijä on oltava yksi ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="00e45-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="00e45-344">Tunnuksen on oltava **SSN**-tunnus.</span><span class="sxs-lookup"><span data-stu-id="00e45-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="00e45-345">Dayforcessa se johdetaan automaattisesti työntekijän sosiaaliturvatunnuksesta, jota tarvitaan työsuhdetta solmittaessa.</span><span class="sxs-lookup"><span data-stu-id="00e45-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="00e45-346">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-346">Primary (required)</span></span>
- <span data-ttu-id="00e45-347">Tunnuksen tyyppi = "Henkilötunnus"</span><span class="sxs-lookup"><span data-stu-id="00e45-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="00e45-348">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-348">Issued Date</span></span>
- <span data-ttu-id="00e45-349">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="00e45-349">Expiration Date</span></span>

<span data-ttu-id="00e45-350">Työntekijät voi määrittää useita tunnistenumeroita **SSN**-tunnuksesta (henkilötunnus).</span><span class="sxs-lookup"><span data-stu-id="00e45-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="00e45-351">Tietue, joka on merkitty **Ensisijainen** on integroitu Dayforceen, riippumatta siitä, onko numero aktiivinen tai vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="00e45-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="00e45-352">Pankkitilit ja suoritukset</span><span class="sxs-lookup"><span data-stu-id="00e45-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="00e45-353">Voimassa olevat pankkitilitiedot on kirjattava kaikille työntekijöille, jotka haluavat, että hänelle maksetaan pankkisiirtona.</span><span class="sxs-lookup"><span data-stu-id="00e45-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="00e45-354">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-354">Talent</span></span>                         | <span data-ttu-id="00e45-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e45-356">Pankkitilin numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="00e45-357">SWIFT-koodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-357">SWIFT code (required)</span></span>          | <span data-ttu-id="00e45-358">**Pankkitunnus**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="00e45-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="00e45-359">Sivuliikkeen numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="00e45-360">Pankkitilin tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-360">Bank account type (required)</span></span>   | <span data-ttu-id="00e45-361">**Tilityyppi**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="00e45-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="00e45-362">Tuetut arvot sisältävät kohdat **Tarkistus** ja **Palkanlaskenta**.</span><span class="sxs-lookup"><span data-stu-id="00e45-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="00e45-363">Työntekijät, jotka haluavat, että heille maksetaan pankkisiirtona, on toimitettava linkki jäännöstilille, joka kuuluu oikeushenkilölle, jolla on ensisijainen osoite Meksikossa ja jolla on voimassa oleva tili meksikolaisessa pankissa.</span><span class="sxs-lookup"><span data-stu-id="00e45-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="00e45-364">Kaikki muut jäljellä olevat tilit jätetään huomiotta.</span><span class="sxs-lookup"><span data-stu-id="00e45-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="00e45-365">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="00e45-365">Address information</span></span>

<span data-ttu-id="00e45-366">Jokaisella työntekijällä on oltava yksi ensisijainen toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="00e45-366">Every employee must have one primary location.</span></span> <span data-ttu-id="00e45-367">Dayforcessa tätä sijaintia käytetään määrittämään työntekijän ensisijainen oleskelulupa verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="00e45-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="00e45-368">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-368">Primary (required)</span></span>
- <span data-ttu-id="00e45-369">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-369">Country/region (required)</span></span>
- <span data-ttu-id="00e45-370">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="00e45-371">Katuosoite (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-371">Street (required)</span></span>
- <span data-ttu-id="00e45-372">Kadunnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-372">Street Number (required)</span></span>
- <span data-ttu-id="00e45-373">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="00e45-373">Building Complement</span></span>
- <span data-ttu-id="00e45-374">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-374">City (required)</span></span>
- <span data-ttu-id="00e45-375">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-375">State (required)</span></span>
- <span data-ttu-id="00e45-376">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="00e45-377">Määritä tiedot luodaksesi palkkalistoja Yhdysvalloissa ja Kanadassa</span><span class="sxs-lookup"><span data-stu-id="00e45-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="00e45-378">Jos luot maksuja työntekijöille, jotka ovat Yhdysvalloissa ja Kanadassa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="00e45-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="00e45-379">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="00e45-379">Departments are required on positions.</span></span>
- <span data-ttu-id="00e45-380">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="00e45-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="00e45-381">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="00e45-381">Job types</span></span>

<span data-ttu-id="00e45-382">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="00e45-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="00e45-383">Työlajit ovat pakollisia palkanlaskennan käsittelemiseksi Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="00e45-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="00e45-384">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="00e45-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="00e45-385">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="00e45-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="00e45-386">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="00e45-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="00e45-387">Työlaji</span><span class="sxs-lookup"><span data-stu-id="00e45-387">Job type</span></span>   | <span data-ttu-id="00e45-388">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="00e45-389">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="00e45-389">Hourly</span></span>     | <span data-ttu-id="00e45-390">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="00e45-390">Hourly</span></span>      |
| <span data-ttu-id="00e45-391">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="00e45-391">Salaried</span></span>   | <span data-ttu-id="00e45-392">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="00e45-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="00e45-393">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="00e45-393">Position types</span></span> 

<span data-ttu-id="00e45-394">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="00e45-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="00e45-395">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="00e45-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="00e45-396">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="00e45-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="00e45-397">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="00e45-397">Position type</span></span>   | <span data-ttu-id="00e45-398">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="00e45-399">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="00e45-399">Full-time</span></span>       | <span data-ttu-id="00e45-400">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-400">Full time employee</span></span> |
| <span data-ttu-id="00e45-401">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="00e45-401">Part-time</span></span>       | <span data-ttu-id="00e45-402">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="00e45-403">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-403">Reason codes</span></span>

<span data-ttu-id="00e45-404">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="00e45-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="00e45-405">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="00e45-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="00e45-406">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="00e45-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="00e45-407">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-407">Reason code</span></span>    | <span data-ttu-id="00e45-408">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-408">Description</span></span>      | <span data-ttu-id="00e45-409">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="00e45-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="00e45-410">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="00e45-410">RESIGNATION</span></span>    | <span data-ttu-id="00e45-411">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="00e45-411">Resignation</span></span>      | <span data-ttu-id="00e45-412">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-412">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-413">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="00e45-413">TERMINATION</span></span>    | <span data-ttu-id="00e45-414">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="00e45-414">Termination</span></span>      | <span data-ttu-id="00e45-415">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-415">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-416">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="00e45-416">RETIREMENT</span></span>     | <span data-ttu-id="00e45-417">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="00e45-417">Retirement</span></span>       | <span data-ttu-id="00e45-418">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-418">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-419">MUU</span><span class="sxs-lookup"><span data-stu-id="00e45-419">OTHER</span></span>          | <span data-ttu-id="00e45-420">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="00e45-420">Other Reasons</span></span>    | <span data-ttu-id="00e45-421">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-421">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-422">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="00e45-422">DEATH</span></span>          | <span data-ttu-id="00e45-423">Kuolema</span><span class="sxs-lookup"><span data-stu-id="00e45-423">Death</span></span>            | <span data-ttu-id="00e45-424">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-424">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="00e45-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="00e45-426">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="00e45-426">Leave of Absence</span></span> | <span data-ttu-id="00e45-427">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-427">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="00e45-428">CONTRACTEND</span></span>    | <span data-ttu-id="00e45-429">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="00e45-429">End of Contract</span></span>  | <span data-ttu-id="00e45-430">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-430">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="00e45-431">SALARYCHANGE</span></span>   | <span data-ttu-id="00e45-432">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="00e45-432">Change of Salary</span></span> | <span data-ttu-id="00e45-433">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="00e45-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="00e45-434">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="00e45-434">Marital status</span></span>

<span data-ttu-id="00e45-435">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="00e45-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="00e45-436">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="00e45-437">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-437">Talent</span></span>                 | <span data-ttu-id="00e45-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="00e45-439">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="00e45-439">Married</span></span>                | <span data-ttu-id="00e45-440">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="00e45-440">Married</span></span>              |
| <span data-ttu-id="00e45-441">Yksi</span><span class="sxs-lookup"><span data-stu-id="00e45-441">Single</span></span>                 | <span data-ttu-id="00e45-442">Yksi</span><span class="sxs-lookup"><span data-stu-id="00e45-442">Single</span></span>               |
| <span data-ttu-id="00e45-443">Leski</span><span class="sxs-lookup"><span data-stu-id="00e45-443">Widowed</span></span>                | <span data-ttu-id="00e45-444">Leski</span><span class="sxs-lookup"><span data-stu-id="00e45-444">Widowed</span></span>              |
| <span data-ttu-id="00e45-445">Eronnut</span><span class="sxs-lookup"><span data-stu-id="00e45-445">Divorced</span></span>               | <span data-ttu-id="00e45-446">Eronnut</span><span class="sxs-lookup"><span data-stu-id="00e45-446">Divorced</span></span>             |
| <span data-ttu-id="00e45-447">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="00e45-447">Registered Partnership</span></span> | <span data-ttu-id="00e45-448">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="00e45-448">Domestic Partnership</span></span> |
| <span data-ttu-id="00e45-449">None</span><span class="sxs-lookup"><span data-stu-id="00e45-449">None</span></span>                   | <span data-ttu-id="00e45-450">None</span><span class="sxs-lookup"><span data-stu-id="00e45-450">None</span></span>                 |
| <span data-ttu-id="00e45-451">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="00e45-451">Cohabiting</span></span>             | <span data-ttu-id="00e45-452">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="00e45-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="00e45-453">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="00e45-453">Gender</span></span>

<span data-ttu-id="00e45-454">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="00e45-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="00e45-455">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="00e45-456">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-456">Talent</span></span>       | <span data-ttu-id="00e45-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="00e45-458">Mies</span><span class="sxs-lookup"><span data-stu-id="00e45-458">Male</span></span>         | <span data-ttu-id="00e45-459">Mies</span><span class="sxs-lookup"><span data-stu-id="00e45-459">Male</span></span>            |
| <span data-ttu-id="00e45-460">Nainen</span><span class="sxs-lookup"><span data-stu-id="00e45-460">Female</span></span>       | <span data-ttu-id="00e45-461">Nainen</span><span class="sxs-lookup"><span data-stu-id="00e45-461">Female</span></span>          |
| <span data-ttu-id="00e45-462">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="00e45-462">Non-specific</span></span> | <span data-ttu-id="00e45-463">*Ei tueta*</span><span class="sxs-lookup"><span data-stu-id="00e45-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="00e45-464">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-464">Earning codes</span></span>

<span data-ttu-id="00e45-465">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="00e45-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="00e45-466">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="00e45-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="00e45-467">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="00e45-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="00e45-468">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="00e45-468">Supported frequencies</span></span>

- <span data-ttu-id="00e45-469">Kaikki</span><span class="sxs-lookup"><span data-stu-id="00e45-469">All</span></span>
- <span data-ttu-id="00e45-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="00e45-470">EVERYPAY</span></span>
- <span data-ttu-id="00e45-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="00e45-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="00e45-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="00e45-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="00e45-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="00e45-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="00e45-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-474">1OFMTH</span></span>
- <span data-ttu-id="00e45-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-475">LASTOFMTH</span></span>
- <span data-ttu-id="00e45-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-476">2OFMTH</span></span>
- <span data-ttu-id="00e45-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-477">3OFMTH</span></span>
- <span data-ttu-id="00e45-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-478">4OFMTH</span></span>
- <span data-ttu-id="00e45-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-479">5OFMTH</span></span>
- <span data-ttu-id="00e45-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-480">1N2OFMTH</span></span>
- <span data-ttu-id="00e45-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-481">3N4OFMTH</span></span>
- <span data-ttu-id="00e45-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-482">1N3OFMTH</span></span>
- <span data-ttu-id="00e45-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-483">1N4OFMTH</span></span>
- <span data-ttu-id="00e45-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-484">2N3OFMTH</span></span>
- <span data-ttu-id="00e45-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-485">2N4OFMTH</span></span>
- <span data-ttu-id="00e45-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="00e45-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="00e45-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="00e45-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="00e45-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="00e45-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="00e45-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="00e45-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="00e45-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="00e45-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="00e45-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="00e45-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="00e45-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="00e45-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="00e45-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="00e45-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="00e45-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="00e45-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="00e45-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="00e45-498">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="00e45-498">Addresses</span></span>

<span data-ttu-id="00e45-499">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="00e45-500">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="00e45-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="00e45-501">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-501">Talent</span></span>          | <span data-ttu-id="00e45-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="00e45-503">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="00e45-503">Country/Region</span></span>  | <span data-ttu-id="00e45-504">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-504">Country Code</span></span>          |
| <span data-ttu-id="00e45-505">Postinumero</span><span class="sxs-lookup"><span data-stu-id="00e45-505">Zip/Postal Code</span></span> | <span data-ttu-id="00e45-506">Postinumero</span><span class="sxs-lookup"><span data-stu-id="00e45-506">Postal Code</span></span>           |
| <span data-ttu-id="00e45-507">Alue</span><span class="sxs-lookup"><span data-stu-id="00e45-507">State</span></span>           | <span data-ttu-id="00e45-508">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-508">State Code</span></span>            |
| <span data-ttu-id="00e45-509">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="00e45-509">City</span></span>            | <span data-ttu-id="00e45-510">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="00e45-510">City</span></span>                  |
| <span data-ttu-id="00e45-511">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="00e45-511">County</span></span>          | <span data-ttu-id="00e45-512">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="00e45-512">County (Municipality)</span></span> |
| <span data-ttu-id="00e45-513">Katu</span><span class="sxs-lookup"><span data-stu-id="00e45-513">Street</span></span>          | <span data-ttu-id="00e45-514">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="00e45-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="00e45-515">Verotusalueet</span><span class="sxs-lookup"><span data-stu-id="00e45-515">Tax regions</span></span>

<span data-ttu-id="00e45-516">Verotusalueita käytetään palkanlaskennan muodostamisessa käytettävän veron määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="00e45-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="00e45-517">ALV-alueet yhdistetään Dayforceen toimipaikan osoitteina.</span><span class="sxs-lookup"><span data-stu-id="00e45-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="00e45-518">Oletusarvoinen verotusalue on liitettävä työntekijän aktiiviseen toimeen.</span><span class="sxs-lookup"><span data-stu-id="00e45-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="00e45-519">Verotusalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-519">Tax region (required)</span></span>
- <span data-ttu-id="00e45-520">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-520">Country/Region (required)</span></span>
- <span data-ttu-id="00e45-521">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-521">State (required)</span></span>
- <span data-ttu-id="00e45-522">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="00e45-522">County</span></span> 
- <span data-ttu-id="00e45-523">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="00e45-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="00e45-524">Määritä tietosi tuottaaksesi palkkalistoja Meksikossa</span><span class="sxs-lookup"><span data-stu-id="00e45-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="00e45-525">Jos luot maksuja työntekijöille, jotka ovat Meksikossa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="00e45-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="00e45-526">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="00e45-526">Departments are required on positions.</span></span>
- <span data-ttu-id="00e45-527">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="00e45-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="00e45-528">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="00e45-528">Job types</span></span>

<span data-ttu-id="00e45-529">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="00e45-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="00e45-530">Työlajit ovat pakollisia palkkalistojen käsittelemiseen Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="00e45-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="00e45-531">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="00e45-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="00e45-532">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="00e45-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="00e45-533">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="00e45-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="00e45-534">Työlaji</span><span class="sxs-lookup"><span data-stu-id="00e45-534">Job type</span></span>   | <span data-ttu-id="00e45-535">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="00e45-536">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="00e45-536">Hourly</span></span>     | <span data-ttu-id="00e45-537">MX tunneittain</span><span class="sxs-lookup"><span data-stu-id="00e45-537">MX Hourly</span></span>   |
| <span data-ttu-id="00e45-538">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="00e45-538">Salaried</span></span>   | <span data-ttu-id="00e45-539">MX kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="00e45-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="00e45-540">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="00e45-540">Position types</span></span> 

<span data-ttu-id="00e45-541">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="00e45-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="00e45-542">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="00e45-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="00e45-543">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="00e45-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="00e45-544">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="00e45-544">Position type</span></span>   | <span data-ttu-id="00e45-545">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="00e45-546">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="00e45-546">Full-time</span></span>       | <span data-ttu-id="00e45-547">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-547">Full time employee</span></span> |
| <span data-ttu-id="00e45-548">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="00e45-548">Part-time</span></span>       | <span data-ttu-id="00e45-549">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="00e45-550">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-550">Reason codes</span></span>

<span data-ttu-id="00e45-551">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="00e45-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="00e45-552">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="00e45-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="00e45-553">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="00e45-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="00e45-554">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-554">Reason code</span></span>            | <span data-ttu-id="00e45-555">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-555">Description</span></span>                    | <span data-ttu-id="00e45-556">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="00e45-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="00e45-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="00e45-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="00e45-558">Lähtö ennen ensimmäistä palkanlaskentaa</span><span class="sxs-lookup"><span data-stu-id="00e45-558">Departure before first payroll</span></span> | <span data-ttu-id="00e45-559">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-559">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-560">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="00e45-560">RESIGNATION</span></span>            | <span data-ttu-id="00e45-561">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="00e45-561">Resignation</span></span>                    | <span data-ttu-id="00e45-562">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-562">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-563">ELÄKE</span><span class="sxs-lookup"><span data-stu-id="00e45-563">PENSION</span></span>                | <span data-ttu-id="00e45-564">Eläke</span><span class="sxs-lookup"><span data-stu-id="00e45-564">Pension</span></span>                        | <span data-ttu-id="00e45-565">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-565">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-566">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="00e45-566">TERMINATION</span></span>            | <span data-ttu-id="00e45-567">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="00e45-567">Termination</span></span>                    | <span data-ttu-id="00e45-568">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-568">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-569">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="00e45-569">RETIREMENT</span></span>             | <span data-ttu-id="00e45-570">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="00e45-570">Retirement</span></span>                     | <span data-ttu-id="00e45-571">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-571">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="00e45-572">ABSENTEE</span></span>               | <span data-ttu-id="00e45-573">Absentee</span><span class="sxs-lookup"><span data-stu-id="00e45-573">Absentee</span></span>                       | <span data-ttu-id="00e45-574">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-574">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-575">MUU</span><span class="sxs-lookup"><span data-stu-id="00e45-575">OTHER</span></span>                  | <span data-ttu-id="00e45-576">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="00e45-576">Other Reasons</span></span>                  | <span data-ttu-id="00e45-577">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-577">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-578">SULKEMINEN</span><span class="sxs-lookup"><span data-stu-id="00e45-578">CLOSURE</span></span>                | <span data-ttu-id="00e45-579">Liiketoiminnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="00e45-579">Business Closure</span></span>               | <span data-ttu-id="00e45-580">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-580">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-581">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="00e45-581">DEATH</span></span>                  | <span data-ttu-id="00e45-582">Kuolema</span><span class="sxs-lookup"><span data-stu-id="00e45-582">Death</span></span>                          | <span data-ttu-id="00e45-583">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-583">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="00e45-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="00e45-585">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="00e45-585">Leave of Absence</span></span>               | <span data-ttu-id="00e45-586">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-586">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="00e45-587">CONTRACTEND</span></span>            | <span data-ttu-id="00e45-588">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="00e45-588">End of Contract</span></span>                | <span data-ttu-id="00e45-589">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="00e45-589">Terminate worker</span></span>     |
| <span data-ttu-id="00e45-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="00e45-590">SALARYCHANGE</span></span>           | <span data-ttu-id="00e45-591">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="00e45-591">Change of Salary</span></span>               | <span data-ttu-id="00e45-592">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="00e45-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="00e45-593">Työehdot</span><span class="sxs-lookup"><span data-stu-id="00e45-593">Terms of employment</span></span>

<span data-ttu-id="00e45-594">Työehtoja voidaan käyttää, kun luodaan työehtoluokkia.</span><span class="sxs-lookup"><span data-stu-id="00e45-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="00e45-595">Ehdot määritetään Dayforceen työsuhteen mittarin arvoina.</span><span class="sxs-lookup"><span data-stu-id="00e45-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="00e45-596">Seuraavat työsuhteen ja kuvaukset termit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="00e45-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="00e45-597">Työehdot</span><span class="sxs-lookup"><span data-stu-id="00e45-597">Terms of employment</span></span>   | <span data-ttu-id="00e45-598">kuvaus</span><span class="sxs-lookup"><span data-stu-id="00e45-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="00e45-599">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="00e45-599">Regular</span></span>               | <span data-ttu-id="00e45-600">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="00e45-600">Regular</span></span>     |
| <span data-ttu-id="00e45-601">Suora</span><span class="sxs-lookup"><span data-stu-id="00e45-601">Direct</span></span>                | <span data-ttu-id="00e45-602">Suora</span><span class="sxs-lookup"><span data-stu-id="00e45-602">Direct</span></span>      |
| <span data-ttu-id="00e45-603">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="00e45-603">Internship</span></span>            | <span data-ttu-id="00e45-604">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="00e45-604">Internship</span></span>  |
| <span data-ttu-id="00e45-605">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="00e45-605">Permanent</span></span>             | <span data-ttu-id="00e45-606">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="00e45-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="00e45-607">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="00e45-607">Marital status</span></span>

<span data-ttu-id="00e45-608">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="00e45-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="00e45-609">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="00e45-610">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-610">Talent</span></span>                 | <span data-ttu-id="00e45-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="00e45-612">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="00e45-612">Married</span></span>                | <span data-ttu-id="00e45-613">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="00e45-613">Married</span></span>                   |
| <span data-ttu-id="00e45-614">Yksi</span><span class="sxs-lookup"><span data-stu-id="00e45-614">Single</span></span>                 | <span data-ttu-id="00e45-615">Yksi</span><span class="sxs-lookup"><span data-stu-id="00e45-615">Single</span></span>                    |
| <span data-ttu-id="00e45-616">Leski</span><span class="sxs-lookup"><span data-stu-id="00e45-616">Widowed</span></span>                | <span data-ttu-id="00e45-617">Leski</span><span class="sxs-lookup"><span data-stu-id="00e45-617">Widowed</span></span>                   |
| <span data-ttu-id="00e45-618">Eronnut</span><span class="sxs-lookup"><span data-stu-id="00e45-618">Divorced</span></span>               | <span data-ttu-id="00e45-619">Eronnut</span><span class="sxs-lookup"><span data-stu-id="00e45-619">Divorced</span></span>                  |
| <span data-ttu-id="00e45-620">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="00e45-620">Registered Partnership</span></span> | <span data-ttu-id="00e45-621">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="00e45-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="00e45-622">None</span><span class="sxs-lookup"><span data-stu-id="00e45-622">None</span></span>                   | <span data-ttu-id="00e45-623">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="00e45-624">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="00e45-624">Cohabiting</span></span>             | <span data-ttu-id="00e45-625">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="00e45-626">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="00e45-626">Gender</span></span>

<span data-ttu-id="00e45-627">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="00e45-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="00e45-628">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="00e45-629">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-629">Talent</span></span>       | <span data-ttu-id="00e45-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="00e45-631">Mies</span><span class="sxs-lookup"><span data-stu-id="00e45-631">Male</span></span>         | <span data-ttu-id="00e45-632">Mies</span><span class="sxs-lookup"><span data-stu-id="00e45-632">Male</span></span>                      |
| <span data-ttu-id="00e45-633">Nainen</span><span class="sxs-lookup"><span data-stu-id="00e45-633">Female</span></span>       | <span data-ttu-id="00e45-634">Nainen</span><span class="sxs-lookup"><span data-stu-id="00e45-634">Female</span></span>                    |
| <span data-ttu-id="00e45-635">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="00e45-635">Non-specific</span></span> | <span data-ttu-id="00e45-636">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="00e45-637">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="00e45-637">Payment method</span></span>

<span data-ttu-id="00e45-638">Maksutavat antavat työntekijälle ja yritykselle keinon kuvata, miten työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="00e45-639">Maksutavat on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="00e45-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="00e45-640">Seuraavassa taulukossa kuvataan, miten maksutavat liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="00e45-641">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-641">Talent</span></span>             | <span data-ttu-id="00e45-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="00e45-643">Maksu</span><span class="sxs-lookup"><span data-stu-id="00e45-643">Cash</span></span>               | <span data-ttu-id="00e45-644">Maksu</span><span class="sxs-lookup"><span data-stu-id="00e45-644">Cash</span></span>                      |
| <span data-ttu-id="00e45-645">Sähköinen maksu</span><span class="sxs-lookup"><span data-stu-id="00e45-645">Electronic Payment</span></span> | <span data-ttu-id="00e45-646">Tapahtumien siirto</span><span class="sxs-lookup"><span data-stu-id="00e45-646">Transfer</span></span>                  |
| <span data-ttu-id="00e45-647">Tarkistus</span><span class="sxs-lookup"><span data-stu-id="00e45-647">Check</span></span>              | <span data-ttu-id="00e45-648">Sekki</span><span class="sxs-lookup"><span data-stu-id="00e45-648">Cheque</span></span>                    |
| <span data-ttu-id="00e45-649">Pankkivekseli</span><span class="sxs-lookup"><span data-stu-id="00e45-649">Bank Draft</span></span>         | <span data-ttu-id="00e45-650">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="00e45-651">Muu</span><span class="sxs-lookup"><span data-stu-id="00e45-651">Other</span></span>              | <span data-ttu-id="00e45-652">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="00e45-653">Pankkitilin tyyppi</span><span class="sxs-lookup"><span data-stu-id="00e45-653">Bank account type</span></span>

<span data-ttu-id="00e45-654">Pankkitilin tyyppejä käytetään sähköisissä maksuissa työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="00e45-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="00e45-655">Pankin tilityypit yhdistetään Dayforceen tilinsiirtämisen tietoina.</span><span class="sxs-lookup"><span data-stu-id="00e45-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="00e45-656">Pankkitilin tyypit ovat tarvittaessa käännettyjä ja hyväksytty arvoiksi sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="00e45-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="00e45-657">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-657">Talent</span></span>            | <span data-ttu-id="00e45-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="00e45-659">Käyttötili</span><span class="sxs-lookup"><span data-stu-id="00e45-659">Checking Account</span></span>  | <span data-ttu-id="00e45-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="00e45-660">CheckingAccount</span></span>           |
| <span data-ttu-id="00e45-661">Palkanlaskennan tili</span><span class="sxs-lookup"><span data-stu-id="00e45-661">Payroll Account</span></span>   | <span data-ttu-id="00e45-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="00e45-662">PayrollAccount</span></span>            |
| <span data-ttu-id="00e45-663">Säästötili</span><span class="sxs-lookup"><span data-stu-id="00e45-663">Savings Account</span></span>   | <span data-ttu-id="00e45-664">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="00e45-665">BankGirot-tili</span><span class="sxs-lookup"><span data-stu-id="00e45-665">BankGirot account</span></span> | <span data-ttu-id="00e45-666">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="00e45-667">PlusGirot-tili</span><span class="sxs-lookup"><span data-stu-id="00e45-667">PlusGirot account</span></span> | <span data-ttu-id="00e45-668">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="00e45-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="00e45-669">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="00e45-669">Earning codes</span></span>

<span data-ttu-id="00e45-670">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="00e45-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="00e45-671">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="00e45-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="00e45-672">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="00e45-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="00e45-673">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="00e45-673">Supported frequencies</span></span>

- <span data-ttu-id="00e45-674">Kaikki</span><span class="sxs-lookup"><span data-stu-id="00e45-674">All</span></span>
- <span data-ttu-id="00e45-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="00e45-675">EVERYPAY</span></span>
- <span data-ttu-id="00e45-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="00e45-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="00e45-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="00e45-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="00e45-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="00e45-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="00e45-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-679">1OFMTH</span></span>
- <span data-ttu-id="00e45-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-680">LASTOFMTH</span></span>
- <span data-ttu-id="00e45-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-681">2OFMTH</span></span>
- <span data-ttu-id="00e45-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-682">3OFMTH</span></span>
- <span data-ttu-id="00e45-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-683">4OFMTH</span></span>
- <span data-ttu-id="00e45-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-684">5OFMTH</span></span>
- <span data-ttu-id="00e45-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-685">1N2OFMTH</span></span>
- <span data-ttu-id="00e45-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-686">3N4OFMTH</span></span>
- <span data-ttu-id="00e45-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-687">1N3OFMTH</span></span>
- <span data-ttu-id="00e45-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-688">1N4OFMTH</span></span>
- <span data-ttu-id="00e45-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-689">2N3OFMTH</span></span>
- <span data-ttu-id="00e45-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-690">2N4OFMTH</span></span>
- <span data-ttu-id="00e45-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="00e45-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="00e45-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="00e45-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="00e45-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="00e45-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="00e45-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="00e45-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="00e45-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="00e45-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="00e45-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="00e45-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="00e45-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="00e45-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="00e45-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="00e45-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="00e45-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="00e45-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="00e45-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="00e45-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="00e45-703">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="00e45-703">Addresses</span></span>

<span data-ttu-id="00e45-704">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="00e45-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="00e45-705">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="00e45-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="00e45-706">Talent</span><span class="sxs-lookup"><span data-stu-id="00e45-706">Talent</span></span>              | <span data-ttu-id="00e45-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="00e45-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="00e45-708">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="00e45-708">Country/Region</span></span>      | <span data-ttu-id="00e45-709">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-709">Country Code</span></span>          |
| <span data-ttu-id="00e45-710">Postinumero</span><span class="sxs-lookup"><span data-stu-id="00e45-710">Zip/Postal Code</span></span>     | <span data-ttu-id="00e45-711">Postinumero</span><span class="sxs-lookup"><span data-stu-id="00e45-711">Postal Code</span></span>           |
| <span data-ttu-id="00e45-712">Alue</span><span class="sxs-lookup"><span data-stu-id="00e45-712">State</span></span>               | <span data-ttu-id="00e45-713">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="00e45-713">State Code</span></span>            |
| <span data-ttu-id="00e45-714">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="00e45-714">City</span></span>                | <span data-ttu-id="00e45-715">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="00e45-715">City</span></span>                  |
| <span data-ttu-id="00e45-716">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="00e45-716">County</span></span>              | <span data-ttu-id="00e45-717">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="00e45-717">County (Municipality)</span></span> |
| <span data-ttu-id="00e45-718">Katu</span><span class="sxs-lookup"><span data-stu-id="00e45-718">Street</span></span>              | <span data-ttu-id="00e45-719">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="00e45-719">Address Line 1</span></span>        |
| <span data-ttu-id="00e45-720">Kadunnumero</span><span class="sxs-lookup"><span data-stu-id="00e45-720">Street Number</span></span>       | <span data-ttu-id="00e45-721">Osoiterivi 2</span><span class="sxs-lookup"><span data-stu-id="00e45-721">Address Line 2</span></span>        |
| <span data-ttu-id="00e45-722">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="00e45-722">Building Complement</span></span> | <span data-ttu-id="00e45-723">Osoiterivi 5</span><span class="sxs-lookup"><span data-stu-id="00e45-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="00e45-724">Passin numero</span><span class="sxs-lookup"><span data-stu-id="00e45-724">Passport number</span></span>

<span data-ttu-id="00e45-725">Työntekijät voivat ilmoittaa passin tiedot.</span><span class="sxs-lookup"><span data-stu-id="00e45-725">Employees can declare passport information.</span></span> <span data-ttu-id="00e45-726">Tämä tietoa on **Passi**-tunnustyyppiä ja se on integroitu Dayforceen osaksi työntekijän Meksikon liittyvää tietoa.</span><span class="sxs-lookup"><span data-stu-id="00e45-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="00e45-727">Tunnustyyppi = "Passi"</span><span class="sxs-lookup"><span data-stu-id="00e45-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="00e45-728">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="00e45-728">Issued Date</span></span>
- <span data-ttu-id="00e45-729">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="00e45-729">Expiration Date</span></span>

<span data-ttu-id="00e45-730">Työntekijät voi määrittää useita tunnistenumeroita **Passi**-tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="00e45-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="00e45-731">Vain nykyiset aktiiviset passitapahtumat integroidaan Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="00e45-732">Mikäli kaikki passitapahtumat ovat vanhentuneet, passi, joka on viimeksi myönnetty on integroitu Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="00e45-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
