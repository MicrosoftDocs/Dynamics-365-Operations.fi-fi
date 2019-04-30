---
title: Palkanlaskennan Talent and Dayforce -integroinnin määrittäminen
description: Tässä ohjeaiheessa kerrotaan, että kuinka konfiguroida integrointeja Microsoft Dynamics 365 for Talentin ja Ceridian Dayforcen välillä voidaksesi käsitellä palkka-ajoa.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/26/2019
ms.locfileid: "898441"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="bf76e-103">Talentin ja Dayforcen välisen palkanlaskennan integroinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bf76e-104">Microsoft Dynamics 365 for Talentin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="bf76e-105">Sekä Talentin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="bf76e-106">Käytettäessä jotakin palvelua, kuten Dayforcea palkka-ajojen suorittamiseen, on otettava käyttöön integrointi Talentissa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="bf76e-107">Integrointi edellyttää tiettyjä tietoja Talentista.</span><span class="sxs-lookup"><span data-stu-id="bf76e-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="bf76e-108">Sinun on varmistettava, että Dayforceen yhdistetyt tiedot on konfiguroitu Talentissa siten, että ne tukevat integrointia.</span><span class="sxs-lookup"><span data-stu-id="bf76e-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="bf76e-109">Integraatio käyttää seuraavanlaisia laajoja tietoryhmiä:</span><span class="sxs-lookup"><span data-stu-id="bf76e-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="bf76e-110">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-110">Human resources data</span></span>
- <span data-ttu-id="bf76e-111">Kompensaatiotiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-111">Compensation data</span></span>
- <span data-ttu-id="bf76e-112">Palkanlaskentatietoja, kuten maksujaksot, maksukaudet ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="bf76e-113">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-113">Worker data</span></span>

<span data-ttu-id="bf76e-114">Tässä ohjeaiheessa kuvataan vaiheita, joita sinun on noudatettava ottaaksesi integroinnin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="bf76e-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="bf76e-115">Lisäksi kerrotaan minkä tyyppisiä tietoja ja konfigurointitietoja integrointi edellyttää.</span><span class="sxs-lookup"><span data-stu-id="bf76e-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="bf76e-116">Ota integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="bf76e-116">Enable the integration</span></span>

<span data-ttu-id="bf76e-117">Ota integraatio käyttöön Talentissa ja lisää konfiguraatiotiedot muodostaaksesi yhteyden Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="bf76e-118">Mikäli haluat kirjanpitotapahtuman, joka valmistetaan ja tuodaan Microsoft Dynamics 365 for Finance and Operationsiin, sinun on perustettava myös Microsoft Azure -tallennustili ja kirjoitettava Azure-tallennuksen yhteyden muodostuskomento Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="bf76e-119">Ota integrointi käyttöön Talentissa seuraavien vaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="bf76e-120">Valitse **Järjestelmänvalvoja**-sivulla **konfiguroinnin integrointi**.</span><span class="sxs-lookup"><span data-stu-id="bf76e-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="bf76e-121">Lisää File Transfer Protocol (FTP) -päätepiste ja suojattu FTP-kansiopolku.</span><span class="sxs-lookup"><span data-stu-id="bf76e-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="bf76e-122">Kirjoita sen käyttäjän käyttäjänimi ja salasana, joka voi käyttää suojattua FTP-päätepistettä ja kansiopolkua.</span><span class="sxs-lookup"><span data-stu-id="bf76e-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="bf76e-123">Testaa yhteys kuten vaadittu ja määritä **Ota käyttöön palkanmaksun integrointi** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="bf76e-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="bf76e-124">Kun integrointi otetaan käyttöön, tietojen viennin paketti ja tiedostot luodaan ja taajuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="bf76e-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="bf76e-125">Voit muuttaa tätä taajuutta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="bf76e-126">Lisätietoja Azure-tallennustilien ja Azure-tallennusyhteyden yhteysmerkkijonoista seuraavissa Azure-aiheissa:</span><span class="sxs-lookup"><span data-stu-id="bf76e-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="bf76e-127">Lisätietoja Azure-tallennustileistä</span><span class="sxs-lookup"><span data-stu-id="bf76e-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="bf76e-128">Määritä Azure-tallennustilan yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="bf76e-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="bf76e-129">Määritä tietosi</span><span class="sxs-lookup"><span data-stu-id="bf76e-129">Configure your data</span></span> 

<span data-ttu-id="bf76e-130">Voidaksesi käsitellä palkanlaskentaa, sinun on määritettävä henkilöstöhallinnon tiedot Talentissa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="bf76e-131">On määritettävä organisaation tiedot, kuten työt ja toimet sekä edut ja kompensaatiotiedot.</span><span class="sxs-lookup"><span data-stu-id="bf76e-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="bf76e-132">Nämä tiedot sisältävät työllisyys-, palkka- ja vähennystiedot, jotka vaaditaan, jotta voidaan luoda työntekijän palkka.</span><span class="sxs-lookup"><span data-stu-id="bf76e-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="bf76e-133">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="bf76e-134">Edut</span><span class="sxs-lookup"><span data-stu-id="bf76e-134">Benefits</span></span> 

<span data-ttu-id="bf76e-135">Henkilöstöhallinto sisältää työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="bf76e-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="bf76e-136">Luodessasi etuja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="bf76e-137">Etusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="bf76e-137">Benefit plans</span></span>

- <span data-ttu-id="bf76e-138">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-138">Plan (required)</span></span>
- <span data-ttu-id="bf76e-139">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-139">Type (required)</span></span>
- <span data-ttu-id="bf76e-140">Palkanlaskennan vaikutus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-140">Payroll impact (required)</span></span>
- <span data-ttu-id="bf76e-141">Palauta velvoitteet</span><span class="sxs-lookup"><span data-stu-id="bf76e-141">Recover arrears</span></span>
- <span data-ttu-id="bf76e-142">Vähennysmenetelmä</span><span class="sxs-lookup"><span data-stu-id="bf76e-142">Deduction method</span></span>
- <span data-ttu-id="bf76e-143">Vähennyksen prioriteetti</span><span class="sxs-lookup"><span data-stu-id="bf76e-143">Deduction priority</span></span>
- <span data-ttu-id="bf76e-144">Rajaa kausi</span><span class="sxs-lookup"><span data-stu-id="bf76e-144">Limit period</span></span>
- <span data-ttu-id="bf76e-145">Rajasumma</span><span class="sxs-lookup"><span data-stu-id="bf76e-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="bf76e-146">Edut</span><span class="sxs-lookup"><span data-stu-id="bf76e-146">Benefits</span></span>

- <span data-ttu-id="bf76e-147">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-147">Plan (required)</span></span>
- <span data-ttu-id="bf76e-148">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-148">Type (required)</span></span>
- <span data-ttu-id="bf76e-149">Vaihtoehto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-149">Option (required)</span></span>
- <span data-ttu-id="bf76e-150">Edun tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-150">Benefit ID (required)</span></span>
- <span data-ttu-id="bf76e-151">Tiheys</span><span class="sxs-lookup"><span data-stu-id="bf76e-151">Frequency</span></span>
- <span data-ttu-id="bf76e-152">Peruste</span><span class="sxs-lookup"><span data-stu-id="bf76e-152">Basis</span></span>
- <span data-ttu-id="bf76e-153">Summa tai hinta</span><span class="sxs-lookup"><span data-stu-id="bf76e-153">Amount or rate</span></span>
- <span data-ttu-id="bf76e-154">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="bf76e-155">Tuetut maksutiheydet</span><span class="sxs-lookup"><span data-stu-id="bf76e-155">Supported frequencies</span></span> 

- <span data-ttu-id="bf76e-156">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="bf76e-156">Weekly</span></span>
- <span data-ttu-id="bf76e-157">Kahden viikon välein</span><span class="sxs-lookup"><span data-stu-id="bf76e-157">Bi-weekly</span></span>
- <span data-ttu-id="bf76e-158">Joka toinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="bf76e-158">Semi-monthly</span></span>
- <span data-ttu-id="bf76e-159">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="bf76e-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="bf76e-160">Tuetut pohjat</span><span class="sxs-lookup"><span data-stu-id="bf76e-160">Supported bases</span></span> 

- <span data-ttu-id="bf76e-161">Kiinteä summa</span><span class="sxs-lookup"><span data-stu-id="bf76e-161">Fixed amount</span></span>
- <span data-ttu-id="bf76e-162">Ansioiden prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="bf76e-162">Percent of earnings</span></span>
- <span data-ttu-id="bf76e-163">Tuottavat tunnit</span><span class="sxs-lookup"><span data-stu-id="bf76e-163">Productive hours</span></span>

<span data-ttu-id="bf76e-164">Dayforce luo seuraavat vähennykset, jotka perustuvat palkanlaskennan vaikutukseen, joka on määritelty etusuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="bf76e-165">Talentin valinta</span><span class="sxs-lookup"><span data-stu-id="bf76e-165">Selection in Talent</span></span>        | <span data-ttu-id="bf76e-166">Tulos Dayforcessa</span><span class="sxs-lookup"><span data-stu-id="bf76e-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="bf76e-167">None</span><span class="sxs-lookup"><span data-stu-id="bf76e-167">None</span></span>                       | <span data-ttu-id="bf76e-168">Vähennyksiä ei luoda.</span><span class="sxs-lookup"><span data-stu-id="bf76e-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="bf76e-169">Vain vähennys</span><span class="sxs-lookup"><span data-stu-id="bf76e-169">Deduction only</span></span>             | <span data-ttu-id="bf76e-170">Työntekijävähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="bf76e-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="bf76e-171">Vain osuus</span><span class="sxs-lookup"><span data-stu-id="bf76e-171">Contribution only</span></span>          | <span data-ttu-id="bf76e-172">Työnantajavähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="bf76e-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="bf76e-173">Vähennys ja osuus</span><span class="sxs-lookup"><span data-stu-id="bf76e-173">Deduction and contribution</span></span> | <span data-ttu-id="bf76e-174">Työntekijän ja työnantajan vähennykset luodaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="bf76e-175">Lisätietoja etuohjelman määrittämisestä ja hallitsemisesta seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="bf76e-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="bf76e-176">Työsuhde-etuohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="bf76e-177">Luo uusi etu</span><span class="sxs-lookup"><span data-stu-id="bf76e-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="bf76e-178">Määritä edun oikeutussäännöt ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="bf76e-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="bf76e-179">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="bf76e-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="bf76e-180">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="bf76e-180">Compensation</span></span> 

<span data-ttu-id="bf76e-181">Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista.</span><span class="sxs-lookup"><span data-stu-id="bf76e-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="bf76e-182">Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="bf76e-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="bf76e-183">Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="bf76e-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="bf76e-184">Dayforce käyttää kompensaatiotietoja laskeakseen työntekijän tunti- tai vuosihinnan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="bf76e-185">Kiinteät kompensaatiosuunnitelmat ja palkkojen muunnokset vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="bf76e-186">Työntekijöiden täytyy olla liitettynä kiinteään kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="bf76e-187">Katso lisätietoja kompensaatiosuunnitelmista seuraavista ohjeaiheista:</span><span class="sxs-lookup"><span data-stu-id="bf76e-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="bf76e-188">Kiinteiden kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="bf76e-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="bf76e-189">Muuttuvien kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="bf76e-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="bf76e-190">Palkka- ja kompensaatiorakenteen ja -suunnitelmien kehittäminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="bf76e-191">Kompensaation käsittely</span><span class="sxs-lookup"><span data-stu-id="bf76e-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="bf76e-192">Kompensaatioprosessin määrittäminen ja tulosten laskeminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="bf76e-193">Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="bf76e-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="bf76e-194">Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="bf76e-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="bf76e-195">Työt</span><span class="sxs-lookup"><span data-stu-id="bf76e-195">Jobs</span></span> 

<span data-ttu-id="bf76e-196">Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään.</span><span class="sxs-lookup"><span data-stu-id="bf76e-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="bf76e-197">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="bf76e-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="bf76e-198">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="bf76e-199">Määritä uudet työt</span><span class="sxs-lookup"><span data-stu-id="bf76e-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="bf76e-200">Toimet</span><span class="sxs-lookup"><span data-stu-id="bf76e-200">Positions</span></span>

<span data-ttu-id="bf76e-201">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="bf76e-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="bf76e-202">Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="bf76e-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="bf76e-203">Osastolla on toimi.</span><span class="sxs-lookup"><span data-stu-id="bf76e-203">A position exists in a department.</span></span> <span data-ttu-id="bf76e-204">Vain yksi työntekijä voidaan liittää yhteen toimeen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="bf76e-205">Muista seuraavat tiedot ja määritykset, kun määrität toimia:</span><span class="sxs-lookup"><span data-stu-id="bf76e-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="bf76e-206">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-206">Position (required)</span></span>
- <span data-ttu-id="bf76e-207">Kuvaus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-207">Description (required)</span></span>
- <span data-ttu-id="bf76e-208">Työ (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-208">Job (required)</span></span>
- <span data-ttu-id="bf76e-209">Osasto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-209">Department (required)</span></span>
- <span data-ttu-id="bf76e-210">Toimen tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-210">Position type (required)</span></span>
- <span data-ttu-id="bf76e-211">Kokopäiväinen (FTE)</span><span class="sxs-lookup"><span data-stu-id="bf76e-211">Full-time equivalent</span></span>
- <span data-ttu-id="bf76e-212">Vuosittaiset vakiotunnit (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="bf76e-213">Yrityksen maksama (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="bf76e-214">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-214">Pay cycle (required)</span></span>
- <span data-ttu-id="bf76e-215">Oletusarvo taloushallinnon dimensio – kustannuspaikka (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="bf76e-216">Työntekijän määritys – työntekijä, tehtävän alkamisaika, tehtävän lopetusaika, syykoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="bf76e-217">Mikäli useita toimia samalla osastolla liittyy samaan työhön, ne yhdistetään yhteen toimeen Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="bf76e-218">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="bf76e-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="bf76e-219">Työvoiman järjestäminen osastojen, töiden ja toimien avulla</span><span class="sxs-lookup"><span data-stu-id="bf76e-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="bf76e-220">Toimien määritys</span><span class="sxs-lookup"><span data-stu-id="bf76e-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="bf76e-221">Osastot</span><span class="sxs-lookup"><span data-stu-id="bf76e-221">Departments</span></span>

<span data-ttu-id="bf76e-222">Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="bf76e-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="bf76e-223">Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.</span><span class="sxs-lookup"><span data-stu-id="bf76e-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="bf76e-224">Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="bf76e-225">Osastot voivat olla tulosvastuullisia.</span><span class="sxs-lookup"><span data-stu-id="bf76e-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="bf76e-226">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="bf76e-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="bf76e-227">Osaston luominen ja liittäminen osastohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="bf76e-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="bf76e-228">Määritä uudet osastot</span><span class="sxs-lookup"><span data-stu-id="bf76e-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="bf76e-229">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="bf76e-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="bf76e-230">Palkkajakso määrittää kuinka usein palkkalistoja käytetään, ja minä tiettyinä päivinä työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="bf76e-231">Esimerkiksi palkkajakso voi olla kuukausittainen ja työntekijöille voidaan maksaa kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="bf76e-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="bf76e-232">Vaihtoehtoisesti palkkajakso voi olla viikoittainen ja työntekijöille voidaan maksaa tiistaina palkkajakson päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="bf76e-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="bf76e-233">Palkkajaksot on osoitettu toimiin, jotta voidaan valvoa milloin näissä tehtävissä oleville työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="bf76e-234">Luotuasi palkkajaksoja, voit luoda maksukausia kullekin jaksolle.</span><span class="sxs-lookup"><span data-stu-id="bf76e-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="bf76e-235">Jokaisella palkkakaudella on maksun oletuspäivämäärä, joka perustuu antamiisi tietoihin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="bf76e-236">Voit kuitenkin muokata maksun oletuspäivämäärää salliaksesi poikkeuksia, kuten kun maksupäivämäärä osuu vapaapäivälle.</span><span class="sxs-lookup"><span data-stu-id="bf76e-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="bf76e-237">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="bf76e-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="bf76e-238">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-238">Pay cycle (required)</span></span>
- <span data-ttu-id="bf76e-239">Maksujakson tiheys (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="bf76e-240">Kauden alkamispäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="bf76e-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="bf76e-241">Oletusmaksupäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="bf76e-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="bf76e-242">Nämä tiedot on integroitu Dayforce-palkkaryhmien kanssa ja eriteltynä eriteltyinä maittain tai alueittain kullekin maksujaksolle.</span><span class="sxs-lookup"><span data-stu-id="bf76e-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="bf76e-243">Ennen integraatiota on luotava vähintään yksi palkkakausi.</span><span class="sxs-lookup"><span data-stu-id="bf76e-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="bf76e-244">Dayforce luo maksuryhmäkalentereita ja maksupäiviä, jotka perustuvat ensimmäisen palkkakauden alkamispäivämäärään ja määritetty oletusmaksupäivä on asetettu Talentissa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="bf76e-245">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-245">Earning codes</span></span>

<span data-ttu-id="bf76e-246">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="bf76e-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="bf76e-247">Tunnuksissa on erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="bf76e-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="bf76e-248">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="bf76e-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="bf76e-249">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-249">Earning Code (required)</span></span>
- <span data-ttu-id="bf76e-250">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-250">Description</span></span>
- <span data-ttu-id="bf76e-251">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="bf76e-251">Unit of measure</span></span>
- <span data-ttu-id="bf76e-252">Tuottava</span><span class="sxs-lookup"><span data-stu-id="bf76e-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="bf76e-253">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-253">Worker data</span></span>

<span data-ttu-id="bf76e-254">Tietueet eri työntekijöille, joita sinulla on ovat tärkeitä henkilöstöhallinnossa ja palkanlaskentajärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="bf76e-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="bf76e-255">Tietueisiin lisättäviä tietoja käytetään työntekijöiden ja henkilökohtaisten tietojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="bf76e-256">Voit ylläpitää työntekijöille seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="bf76e-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="bf76e-257">**Perustiedot** – Ylläpidä työntekijän perustietoja, kuten yhteystiedot, demografiatiedot, tunnistetiedot, perheen tiedot, asevelvollisuuden tila, ekspatriaatin tiedot ja omat yhteyshenkilöt ja hätäyhteyshenkilöt.</span><span class="sxs-lookup"><span data-stu-id="bf76e-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="bf76e-258">**Työsuhde** – Ylläpidä tietoja työntekijän työsuhteesta, kuten yrityksen tai organisaation kytköksistä, toimen määrityksestä, aloitus- ja päättymispäivämääristä, työkelpoisuudesta, työehdoista, eläkkestä, lomista ja uudelleensijoittumisesta.</span><span class="sxs-lookup"><span data-stu-id="bf76e-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="bf76e-259">**Lomat ja poissaolot** –Ylläpidä tietoa työntekijän poissaoloista, kuten työaikakalentereista, poissaolotapahtumista ja poissaoloasetuksista.</span><span class="sxs-lookup"><span data-stu-id="bf76e-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="bf76e-260">**Kompensaatio ja palkanlaskenta** – Ylläpidä työntekijän kompensaatiosuunnitelmien tietoja ja palkanlaskentatietoja, kuten suunnitelmien toteutuminen, palkkiot, suorituskyky, provisio, verotiedot, eläkkeelle jääminen ja palkan vähennykset.</span><span class="sxs-lookup"><span data-stu-id="bf76e-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="bf76e-261">Kirjoittaessasi työntekijätietoja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="bf76e-262">Yleistiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-262">General information</span></span>

- <span data-ttu-id="bf76e-263">Henkilönumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-263">Personnel number (required)</span></span>
- <span data-ttu-id="bf76e-264">Etunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-264">First name (required)</span></span>
- <span data-ttu-id="bf76e-265">Sukunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-265">Last name (required)</span></span>
- <span data-ttu-id="bf76e-266">Toinen nimi</span><span class="sxs-lookup"><span data-stu-id="bf76e-266">Middle name</span></span>
- <span data-ttu-id="bf76e-267">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="bf76e-267">Seniority date</span></span>
- <span data-ttu-id="bf76e-268">Tunnetaan nimellä</span><span class="sxs-lookup"><span data-stu-id="bf76e-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="bf76e-269">Henkilökohtaiset tiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-269">Personal information</span></span>

- <span data-ttu-id="bf76e-270">Siviilisääty (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-270">Marital status (required)</span></span>
- <span data-ttu-id="bf76e-271">Syntymäpäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-271">Birth date (required)</span></span>
- <span data-ttu-id="bf76e-272">Sukupuoli (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-272">Gender (required)</span></span>
- <span data-ttu-id="bf76e-273">Henkilö on invalidi</span><span class="sxs-lookup"><span data-stu-id="bf76e-273">Person with disabilities</span></span>
- <span data-ttu-id="bf76e-274">Kansalaisuus, maa, alue (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="bf76e-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="bf76e-275">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-275">Address information</span></span>

- <span data-ttu-id="bf76e-276">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-276">Primary (required)</span></span>
- <span data-ttu-id="bf76e-277">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-277">Country/region (required)</span></span>
- <span data-ttu-id="bf76e-278">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-278">Postal code (required)</span></span>
- <span data-ttu-id="bf76e-279">Kadunnumero (pakollinen) (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="bf76e-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="bf76e-280">Rakennusta koskeva lisätieto (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="bf76e-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="bf76e-281">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-281">City (required)</span></span>
- <span data-ttu-id="bf76e-282">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-282">State (required)</span></span>
- <span data-ttu-id="bf76e-283">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="bf76e-284">Yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-284">Contact information</span></span> 

- <span data-ttu-id="bf76e-285">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-285">Primary (required)</span></span>
- <span data-ttu-id="bf76e-286">Yhteystiedon numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-286">Contact number (required)</span></span>
- <span data-ttu-id="bf76e-287">Alanumero</span><span class="sxs-lookup"><span data-stu-id="bf76e-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="bf76e-288">Palkanlaskentatiedot ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-288">Payroll information and earning codes</span></span>

<span data-ttu-id="bf76e-289">Työntekijöille voidaan antaa erityisiä tuloja tietyllä maksutaajuudella ja toivotulla maksutavalla.</span><span class="sxs-lookup"><span data-stu-id="bf76e-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="bf76e-290">Seuraavia kenttiä käytetään Dayforcessa sen varmistamiseksi, että näitä määrityksiä ja asetuksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="bf76e-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="bf76e-291">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-291">Earning codes</span></span>

- <span data-ttu-id="bf76e-292">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-292">Position (required)</span></span>
- <span data-ttu-id="bf76e-293">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-293">Earning Code (required)</span></span>
- <span data-ttu-id="bf76e-294">Taajuus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-294">Frequency (required)</span></span>
- <span data-ttu-id="bf76e-295">Summa (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="bf76e-296">Palkanlaskentatiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-296">Payroll information</span></span>

- <span data-ttu-id="bf76e-297">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="bf76e-297">Payment Method</span></span>
- <span data-ttu-id="bf76e-298">Talousalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-298">Economic Region (required)</span></span>
- <span data-ttu-id="bf76e-299">Työsuhde-etujen tunnus</span><span class="sxs-lookup"><span data-stu-id="bf76e-299">Employee Benefits ID</span></span>
- <span data-ttu-id="bf76e-300">Kansallinen/alueellinen tunnusnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-300">National ID Number (required)</span></span>
- <span data-ttu-id="bf76e-301">Sotilaspalveluksen numero</span><span class="sxs-lookup"><span data-stu-id="bf76e-301">Military Service Number</span></span>
- <span data-ttu-id="bf76e-302">Vuoron tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-302">Shift ID (required)</span></span>
- <span data-ttu-id="bf76e-303">Veronumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-303">Tax Number (required)</span></span>
- <span data-ttu-id="bf76e-304">Ammattijärjestön tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-304">Union ID (required)</span></span>
- <span data-ttu-id="bf76e-305">Työpäivän tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-305">Work Day ID (required)</span></span>
- <span data-ttu-id="bf76e-306">Työluvan numero</span><span class="sxs-lookup"><span data-stu-id="bf76e-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="bf76e-307">Maksutavoista Meksiko tukee seuraavia: **Käteinen**, **shekki** (yrityksen fyysinen shekki) ja **sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="bf76e-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="bf76e-308">Mikäli maksutapaa ei ole määritetty, **shekki** on oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="bf76e-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="bf76e-309">Työsuhteen tiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-309">Employment details</span></span>

<span data-ttu-id="bf76e-310">Työntekijöiden yksityiskohtaista historiaa käytetään keskeisenä informaationa, jolla saadaan työntekijän palkkaus, irtisanominen ja rekrytointitilastot Dayforcesta.</span><span class="sxs-lookup"><span data-stu-id="bf76e-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="bf76e-311">Dayforce tukee kerrallaan vain yhtä aktiivisen työntekijän tietuetta.</span><span class="sxs-lookup"><span data-stu-id="bf76e-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="bf76e-312">Työsuhteen alkamispäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-312">Employment start date (required)</span></span>
- <span data-ttu-id="bf76e-313">Työsuhteen päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-313">Employment end date</span></span>
- <span data-ttu-id="bf76e-314">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-314">Start date</span></span>
- <span data-ttu-id="bf76e-315">Muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-315">Adjusted start date</span></span>
- <span data-ttu-id="bf76e-316">Työsuhteen päättymispäivä (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="bf76e-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="bf76e-317">Työsuhteen päättymissyy (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="bf76e-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="bf76e-318">Seuraavien tietojen avulla lasketaan työntekijän tärkeimmät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="bf76e-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="bf76e-319">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-319">Talent</span></span>                | <span data-ttu-id="bf76e-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf76e-321">Viimeisimmän työhönoton päivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-321">Most recent hire date</span></span> | <span data-ttu-id="bf76e-322">Työntekijän työsuhteen alku voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="bf76e-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="bf76e-323">Työsuhteen loppumispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-323">Termination date</span></span>      | <span data-ttu-id="bf76e-324">Työntekijän työsuhteen loppu voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="bf76e-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="bf76e-325">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-325">Start date</span></span>            | <span data-ttu-id="bf76e-326">Muutettu alkamispäivämäärä, alkamispäivämäärä tai työsuhteen alku ei-aktiivisessa työsuhteen historiatietueessa</span><span class="sxs-lookup"><span data-stu-id="bf76e-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="bf76e-327">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-327">Original hire date</span></span>    | <span data-ttu-id="bf76e-328">Varhaisin työhistoriatietueen työsuhteen alku</span><span class="sxs-lookup"><span data-stu-id="bf76e-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="bf76e-329">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="bf76e-329">Compensation</span></span>

<span data-ttu-id="bf76e-330">Kiinteän kompensaatiosuunnitelmaan tulee liittää jokaisen työntekijän ensisijainen toimi koko työsuhteen ajalla.</span><span class="sxs-lookup"><span data-stu-id="bf76e-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="bf76e-331">Ajanjakso alkaa siitä päivämäärästä, jona työntekijä palkattiin (tai työsuhteen alkamispäivämäärä) ja jatkuu, kunnes työsuhde loppuu.</span><span class="sxs-lookup"><span data-stu-id="bf76e-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="bf76e-332">Voimaantulopäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-332">Effective Date (required)</span></span>
- <span data-ttu-id="bf76e-333">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="bf76e-333">Expiration date</span></span>
- <span data-ttu-id="bf76e-334">Palkkio (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-334">Pay Rate (required)</span></span>
- <span data-ttu-id="bf76e-335">Palkkion muunnokset (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="bf76e-336">Vuosittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="bf76e-337">Tunnittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="bf76e-338">Mikäli tuntityöntekijällä on useita toimia, ensisijaisen toimen kiinteä kompensaation tuodaan Dayforceen työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="bf76e-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="bf76e-339">Ei-ensisijaisten toimien tuntihinta tallennetaan Dayforcen vastaavaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="bf76e-340">Mikäli palkallisella työntekijällä on useita toimia, kumulatiivinen tuntihinta ja vuosittainen palkka kaikista aktiivisista toimista johdetaan ja käytetään työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="bf76e-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="bf76e-341">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="bf76e-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="bf76e-342">Sosiaaliturvan tunniste</span><span class="sxs-lookup"><span data-stu-id="bf76e-342">Social Security identifier</span></span> 

<span data-ttu-id="bf76e-343">Jokaisella työntekijä on oltava yksi ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="bf76e-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="bf76e-344">Tunnuksen on oltava **SSN**-tunnus.</span><span class="sxs-lookup"><span data-stu-id="bf76e-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="bf76e-345">Dayforcessa se johdetaan automaattisesti työntekijän sosiaaliturvatunnuksesta, jota tarvitaan työsuhdetta solmittaessa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="bf76e-346">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-346">Primary (required)</span></span>
- <span data-ttu-id="bf76e-347">Tunnuksen tyyppi = "Henkilötunnus"</span><span class="sxs-lookup"><span data-stu-id="bf76e-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="bf76e-348">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-348">Issued Date</span></span>
- <span data-ttu-id="bf76e-349">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="bf76e-349">Expiration Date</span></span>

<span data-ttu-id="bf76e-350">Työntekijät voi määrittää useita tunnistenumeroita **SSN**-tunnuksesta (henkilötunnus).</span><span class="sxs-lookup"><span data-stu-id="bf76e-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="bf76e-351">Tietue, joka on merkitty **Ensisijainen** on integroitu Dayforceen, riippumatta siitä, onko numero aktiivinen tai vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="bf76e-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="bf76e-352">Pankkitilit ja suoritukset</span><span class="sxs-lookup"><span data-stu-id="bf76e-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="bf76e-353">Voimassa olevat pankkitilitiedot on kirjattava kaikille työntekijöille, jotka haluavat, että hänelle maksetaan pankkisiirtona.</span><span class="sxs-lookup"><span data-stu-id="bf76e-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="bf76e-354">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-354">Talent</span></span>                         | <span data-ttu-id="bf76e-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf76e-356">Pankkitilin numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="bf76e-357">SWIFT-koodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-357">SWIFT code (required)</span></span>          | <span data-ttu-id="bf76e-358">**Pankkitunnus**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="bf76e-359">Sivuliikkeen numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="bf76e-360">Pankkitilin tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-360">Bank account type (required)</span></span>   | <span data-ttu-id="bf76e-361">**Tilityyppi**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="bf76e-362">Tuetut arvot sisältävät kohdat **Tarkistus** ja **Palkanlaskenta**.</span><span class="sxs-lookup"><span data-stu-id="bf76e-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="bf76e-363">Työntekijät, jotka haluavat, että heille maksetaan pankkisiirtona, on toimitettava linkki jäännöstilille, joka kuuluu oikeushenkilölle, jolla on ensisijainen osoite Meksikossa ja jolla on voimassa oleva tili meksikolaisessa pankissa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="bf76e-364">Kaikki muut jäljellä olevat tilit jätetään huomiotta.</span><span class="sxs-lookup"><span data-stu-id="bf76e-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="bf76e-365">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="bf76e-365">Address information</span></span>

<span data-ttu-id="bf76e-366">Jokaisella työntekijällä on oltava yksi ensisijainen toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="bf76e-366">Every employee must have one primary location.</span></span> <span data-ttu-id="bf76e-367">Dayforcessa tätä sijaintia käytetään määrittämään työntekijän ensisijainen oleskelulupa verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="bf76e-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="bf76e-368">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-368">Primary (required)</span></span>
- <span data-ttu-id="bf76e-369">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-369">Country/region (required)</span></span>
- <span data-ttu-id="bf76e-370">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="bf76e-371">Katuosoite (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-371">Street (required)</span></span>
- <span data-ttu-id="bf76e-372">Kadunnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-372">Street Number (required)</span></span>
- <span data-ttu-id="bf76e-373">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="bf76e-373">Building Complement</span></span>
- <span data-ttu-id="bf76e-374">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-374">City (required)</span></span>
- <span data-ttu-id="bf76e-375">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-375">State (required)</span></span>
- <span data-ttu-id="bf76e-376">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="bf76e-377">Määritä tiedot luodaksesi palkkalistoja Yhdysvalloissa ja Kanadassa</span><span class="sxs-lookup"><span data-stu-id="bf76e-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="bf76e-378">Jos luot maksuja työntekijöille, jotka ovat Yhdysvalloissa ja Kanadassa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="bf76e-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="bf76e-379">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="bf76e-379">Departments are required on positions.</span></span>
- <span data-ttu-id="bf76e-380">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="bf76e-381">Voit määrittää Talentin edellyttämään, että toimet määrittävät osaston.</span><span class="sxs-lookup"><span data-stu-id="bf76e-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="bf76e-382">Tehdäksesi tämän valitse **Henkilöstöhallinnon jaetut toimet > Toimet > Edellytä osastoja toimissa**.</span><span class="sxs-lookup"><span data-stu-id="bf76e-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="bf76e-383">Suosittelemme, että tämä asetus otetaan käyttöön integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="bf76e-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="bf76e-384">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="bf76e-384">Job types</span></span>

<span data-ttu-id="bf76e-385">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="bf76e-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="bf76e-386">Työlajit ovat pakollisia palkanlaskennan käsittelemiseksi Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="bf76e-387">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="bf76e-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="bf76e-388">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="bf76e-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="bf76e-389">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="bf76e-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="bf76e-390">Työlaji</span><span class="sxs-lookup"><span data-stu-id="bf76e-390">Job type</span></span>   | <span data-ttu-id="bf76e-391">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="bf76e-392">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="bf76e-392">Hourly</span></span>     | <span data-ttu-id="bf76e-393">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="bf76e-393">Hourly</span></span>      |
| <span data-ttu-id="bf76e-394">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="bf76e-394">Salaried</span></span>   | <span data-ttu-id="bf76e-395">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="bf76e-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="bf76e-396">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="bf76e-396">Position types</span></span> 

<span data-ttu-id="bf76e-397">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="bf76e-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="bf76e-398">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="bf76e-399">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="bf76e-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="bf76e-400">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="bf76e-400">Position type</span></span>   | <span data-ttu-id="bf76e-401">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="bf76e-402">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-402">Full-time</span></span>       | <span data-ttu-id="bf76e-403">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-403">Full time employee</span></span> |
| <span data-ttu-id="bf76e-404">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-404">Part-time</span></span>       | <span data-ttu-id="bf76e-405">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="bf76e-406">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-406">Reason codes</span></span>

<span data-ttu-id="bf76e-407">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="bf76e-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="bf76e-408">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="bf76e-409">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="bf76e-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="bf76e-410">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-410">Reason code</span></span>    | <span data-ttu-id="bf76e-411">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-411">Description</span></span>      | <span data-ttu-id="bf76e-412">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="bf76e-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="bf76e-413">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="bf76e-413">RESIGNATION</span></span>    | <span data-ttu-id="bf76e-414">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-414">Resignation</span></span>      | <span data-ttu-id="bf76e-415">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-415">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-416">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="bf76e-416">TERMINATION</span></span>    | <span data-ttu-id="bf76e-417">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="bf76e-417">Termination</span></span>      | <span data-ttu-id="bf76e-418">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-418">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-419">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="bf76e-419">RETIREMENT</span></span>     | <span data-ttu-id="bf76e-420">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-420">Retirement</span></span>       | <span data-ttu-id="bf76e-421">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-421">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-422">MUU</span><span class="sxs-lookup"><span data-stu-id="bf76e-422">OTHER</span></span>          | <span data-ttu-id="bf76e-423">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="bf76e-423">Other Reasons</span></span>    | <span data-ttu-id="bf76e-424">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-424">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-425">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="bf76e-425">DEATH</span></span>          | <span data-ttu-id="bf76e-426">Kuolema</span><span class="sxs-lookup"><span data-stu-id="bf76e-426">Death</span></span>            | <span data-ttu-id="bf76e-427">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-427">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="bf76e-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="bf76e-429">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="bf76e-429">Leave of Absence</span></span> | <span data-ttu-id="bf76e-430">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-430">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="bf76e-431">CONTRACTEND</span></span>    | <span data-ttu-id="bf76e-432">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-432">End of Contract</span></span>  | <span data-ttu-id="bf76e-433">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-433">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="bf76e-434">SALARYCHANGE</span></span>   | <span data-ttu-id="bf76e-435">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="bf76e-435">Change of Salary</span></span> | <span data-ttu-id="bf76e-436">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="bf76e-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="bf76e-437">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="bf76e-437">Marital status</span></span>

<span data-ttu-id="bf76e-438">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="bf76e-439">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="bf76e-440">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-440">Talent</span></span>                 | <span data-ttu-id="bf76e-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="bf76e-442">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="bf76e-442">Married</span></span>                | <span data-ttu-id="bf76e-443">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="bf76e-443">Married</span></span>              |
| <span data-ttu-id="bf76e-444">Yksi</span><span class="sxs-lookup"><span data-stu-id="bf76e-444">Single</span></span>                 | <span data-ttu-id="bf76e-445">Yksi</span><span class="sxs-lookup"><span data-stu-id="bf76e-445">Single</span></span>               |
| <span data-ttu-id="bf76e-446">Leski</span><span class="sxs-lookup"><span data-stu-id="bf76e-446">Widowed</span></span>                | <span data-ttu-id="bf76e-447">Leski</span><span class="sxs-lookup"><span data-stu-id="bf76e-447">Widowed</span></span>              |
| <span data-ttu-id="bf76e-448">Eronnut</span><span class="sxs-lookup"><span data-stu-id="bf76e-448">Divorced</span></span>               | <span data-ttu-id="bf76e-449">Eronnut</span><span class="sxs-lookup"><span data-stu-id="bf76e-449">Divorced</span></span>             |
| <span data-ttu-id="bf76e-450">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="bf76e-450">Registered Partnership</span></span> | <span data-ttu-id="bf76e-451">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="bf76e-451">Domestic Partnership</span></span> |
| <span data-ttu-id="bf76e-452">None</span><span class="sxs-lookup"><span data-stu-id="bf76e-452">None</span></span>                   | <span data-ttu-id="bf76e-453">None</span><span class="sxs-lookup"><span data-stu-id="bf76e-453">None</span></span>                 |
| <span data-ttu-id="bf76e-454">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="bf76e-454">Cohabiting</span></span>             | <span data-ttu-id="bf76e-455">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="bf76e-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="bf76e-456">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="bf76e-456">Gender</span></span>

<span data-ttu-id="bf76e-457">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="bf76e-458">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="bf76e-459">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-459">Talent</span></span>       | <span data-ttu-id="bf76e-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="bf76e-461">Mies</span><span class="sxs-lookup"><span data-stu-id="bf76e-461">Male</span></span>         | <span data-ttu-id="bf76e-462">Mies</span><span class="sxs-lookup"><span data-stu-id="bf76e-462">Male</span></span>            |
| <span data-ttu-id="bf76e-463">Nainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-463">Female</span></span>       | <span data-ttu-id="bf76e-464">Nainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-464">Female</span></span>          |
| <span data-ttu-id="bf76e-465">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="bf76e-465">Non-specific</span></span> | <span data-ttu-id="bf76e-466">*Ei tueta*</span><span class="sxs-lookup"><span data-stu-id="bf76e-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="bf76e-467">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-467">Earning codes</span></span>

<span data-ttu-id="bf76e-468">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="bf76e-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="bf76e-469">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="bf76e-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="bf76e-470">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="bf76e-471">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="bf76e-471">Supported frequencies</span></span>

- <span data-ttu-id="bf76e-472">Kaikki</span><span class="sxs-lookup"><span data-stu-id="bf76e-472">All</span></span>
- <span data-ttu-id="bf76e-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="bf76e-473">EVERYPAY</span></span>
- <span data-ttu-id="bf76e-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="bf76e-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="bf76e-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="bf76e-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="bf76e-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="bf76e-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="bf76e-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-477">1OFMTH</span></span>
- <span data-ttu-id="bf76e-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-478">LASTOFMTH</span></span>
- <span data-ttu-id="bf76e-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-479">2OFMTH</span></span>
- <span data-ttu-id="bf76e-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-480">3OFMTH</span></span>
- <span data-ttu-id="bf76e-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-481">4OFMTH</span></span>
- <span data-ttu-id="bf76e-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-482">5OFMTH</span></span>
- <span data-ttu-id="bf76e-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-483">1N2OFMTH</span></span>
- <span data-ttu-id="bf76e-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-484">3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-485">1N3OFMTH</span></span>
- <span data-ttu-id="bf76e-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-486">1N4OFMTH</span></span>
- <span data-ttu-id="bf76e-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-487">2N3OFMTH</span></span>
- <span data-ttu-id="bf76e-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-488">2N4OFMTH</span></span>
- <span data-ttu-id="bf76e-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="bf76e-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="bf76e-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="bf76e-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="bf76e-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="bf76e-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="bf76e-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="bf76e-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="bf76e-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="bf76e-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="bf76e-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="bf76e-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="bf76e-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="bf76e-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="bf76e-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="bf76e-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="bf76e-501">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="bf76e-501">Addresses</span></span>

<span data-ttu-id="bf76e-502">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="bf76e-503">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="bf76e-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="bf76e-504">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-504">Talent</span></span>          | <span data-ttu-id="bf76e-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="bf76e-506">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="bf76e-506">Country/Region</span></span>  | <span data-ttu-id="bf76e-507">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-507">Country Code</span></span>          |
| <span data-ttu-id="bf76e-508">Postinumero</span><span class="sxs-lookup"><span data-stu-id="bf76e-508">Zip/Postal Code</span></span> | <span data-ttu-id="bf76e-509">Postinumero</span><span class="sxs-lookup"><span data-stu-id="bf76e-509">Postal Code</span></span>           |
| <span data-ttu-id="bf76e-510">Alue</span><span class="sxs-lookup"><span data-stu-id="bf76e-510">State</span></span>           | <span data-ttu-id="bf76e-511">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-511">State Code</span></span>            |
| <span data-ttu-id="bf76e-512">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="bf76e-512">City</span></span>            | <span data-ttu-id="bf76e-513">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="bf76e-513">City</span></span>                  |
| <span data-ttu-id="bf76e-514">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="bf76e-514">County</span></span>          | <span data-ttu-id="bf76e-515">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="bf76e-515">County (Municipality)</span></span> |
| <span data-ttu-id="bf76e-516">Katu</span><span class="sxs-lookup"><span data-stu-id="bf76e-516">Street</span></span>          | <span data-ttu-id="bf76e-517">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="bf76e-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="bf76e-518">Verotusalueet</span><span class="sxs-lookup"><span data-stu-id="bf76e-518">Tax regions</span></span>

<span data-ttu-id="bf76e-519">Verotusalueita käytetään palkanlaskennan muodostamisessa käytettävän veron määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="bf76e-520">ALV-alueet yhdistetään Dayforceen toimipaikan osoitteina.</span><span class="sxs-lookup"><span data-stu-id="bf76e-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="bf76e-521">Oletusarvoinen verotusalue on liitettävä työntekijän aktiiviseen toimeen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="bf76e-522">Verotusalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-522">Tax region (required)</span></span>
- <span data-ttu-id="bf76e-523">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-523">Country/Region (required)</span></span>
- <span data-ttu-id="bf76e-524">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-524">State (required)</span></span>
- <span data-ttu-id="bf76e-525">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="bf76e-525">County</span></span> 
- <span data-ttu-id="bf76e-526">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="bf76e-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="bf76e-527">Määritä tietosi tuottaaksesi palkkalistoja Meksikossa</span><span class="sxs-lookup"><span data-stu-id="bf76e-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="bf76e-528">Jos luot maksuja työntekijöille, jotka ovat Meksikossa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="bf76e-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="bf76e-529">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="bf76e-529">Departments are required on positions.</span></span>
- <span data-ttu-id="bf76e-530">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="bf76e-531">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="bf76e-531">Job types</span></span>

<span data-ttu-id="bf76e-532">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="bf76e-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="bf76e-533">Työlajit ovat pakollisia palkkalistojen käsittelemiseen Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="bf76e-534">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="bf76e-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="bf76e-535">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="bf76e-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="bf76e-536">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="bf76e-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="bf76e-537">Työlaji</span><span class="sxs-lookup"><span data-stu-id="bf76e-537">Job type</span></span>   | <span data-ttu-id="bf76e-538">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="bf76e-539">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="bf76e-539">Hourly</span></span>     | <span data-ttu-id="bf76e-540">MX tunneittain</span><span class="sxs-lookup"><span data-stu-id="bf76e-540">MX Hourly</span></span>   |
| <span data-ttu-id="bf76e-541">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="bf76e-541">Salaried</span></span>   | <span data-ttu-id="bf76e-542">MX kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="bf76e-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="bf76e-543">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="bf76e-543">Position types</span></span> 

<span data-ttu-id="bf76e-544">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="bf76e-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="bf76e-545">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="bf76e-546">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="bf76e-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="bf76e-547">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="bf76e-547">Position type</span></span>   | <span data-ttu-id="bf76e-548">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="bf76e-549">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-549">Full-time</span></span>       | <span data-ttu-id="bf76e-550">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-550">Full time employee</span></span> |
| <span data-ttu-id="bf76e-551">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-551">Part-time</span></span>       | <span data-ttu-id="bf76e-552">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="bf76e-553">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-553">Reason codes</span></span>

<span data-ttu-id="bf76e-554">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="bf76e-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="bf76e-555">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="bf76e-556">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="bf76e-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="bf76e-557">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-557">Reason code</span></span>            | <span data-ttu-id="bf76e-558">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-558">Description</span></span>                    | <span data-ttu-id="bf76e-559">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="bf76e-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="bf76e-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="bf76e-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="bf76e-561">Lähtö ennen ensimmäistä palkanlaskentaa</span><span class="sxs-lookup"><span data-stu-id="bf76e-561">Departure before first payroll</span></span> | <span data-ttu-id="bf76e-562">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-562">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-563">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="bf76e-563">RESIGNATION</span></span>            | <span data-ttu-id="bf76e-564">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-564">Resignation</span></span>                    | <span data-ttu-id="bf76e-565">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-565">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-566">ELÄKE</span><span class="sxs-lookup"><span data-stu-id="bf76e-566">PENSION</span></span>                | <span data-ttu-id="bf76e-567">Eläke</span><span class="sxs-lookup"><span data-stu-id="bf76e-567">Pension</span></span>                        | <span data-ttu-id="bf76e-568">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-568">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-569">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="bf76e-569">TERMINATION</span></span>            | <span data-ttu-id="bf76e-570">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="bf76e-570">Termination</span></span>                    | <span data-ttu-id="bf76e-571">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-571">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-572">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="bf76e-572">RETIREMENT</span></span>             | <span data-ttu-id="bf76e-573">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-573">Retirement</span></span>                     | <span data-ttu-id="bf76e-574">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-574">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="bf76e-575">ABSENTEE</span></span>               | <span data-ttu-id="bf76e-576">Absentee</span><span class="sxs-lookup"><span data-stu-id="bf76e-576">Absentee</span></span>                       | <span data-ttu-id="bf76e-577">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-577">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-578">MUU</span><span class="sxs-lookup"><span data-stu-id="bf76e-578">OTHER</span></span>                  | <span data-ttu-id="bf76e-579">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="bf76e-579">Other Reasons</span></span>                  | <span data-ttu-id="bf76e-580">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-580">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-581">SULKEMINEN</span><span class="sxs-lookup"><span data-stu-id="bf76e-581">CLOSURE</span></span>                | <span data-ttu-id="bf76e-582">Liiketoiminnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-582">Business Closure</span></span>               | <span data-ttu-id="bf76e-583">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-583">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-584">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="bf76e-584">DEATH</span></span>                  | <span data-ttu-id="bf76e-585">Kuolema</span><span class="sxs-lookup"><span data-stu-id="bf76e-585">Death</span></span>                          | <span data-ttu-id="bf76e-586">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-586">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="bf76e-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="bf76e-588">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="bf76e-588">Leave of Absence</span></span>               | <span data-ttu-id="bf76e-589">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-589">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="bf76e-590">CONTRACTEND</span></span>            | <span data-ttu-id="bf76e-591">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="bf76e-591">End of Contract</span></span>                | <span data-ttu-id="bf76e-592">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="bf76e-592">Terminate worker</span></span>     |
| <span data-ttu-id="bf76e-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="bf76e-593">SALARYCHANGE</span></span>           | <span data-ttu-id="bf76e-594">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="bf76e-594">Change of Salary</span></span>               | <span data-ttu-id="bf76e-595">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="bf76e-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="bf76e-596">Työehdot</span><span class="sxs-lookup"><span data-stu-id="bf76e-596">Terms of employment</span></span>

<span data-ttu-id="bf76e-597">Työehtoja voidaan käyttää, kun luodaan työehtoluokkia.</span><span class="sxs-lookup"><span data-stu-id="bf76e-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="bf76e-598">Ehdot määritetään Dayforceen työsuhteen mittarin arvoina.</span><span class="sxs-lookup"><span data-stu-id="bf76e-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="bf76e-599">Seuraavat työsuhteen ja kuvaukset termit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="bf76e-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="bf76e-600">Työehdot</span><span class="sxs-lookup"><span data-stu-id="bf76e-600">Terms of employment</span></span>   | <span data-ttu-id="bf76e-601">kuvaus</span><span class="sxs-lookup"><span data-stu-id="bf76e-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="bf76e-602">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="bf76e-602">Regular</span></span>               | <span data-ttu-id="bf76e-603">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="bf76e-603">Regular</span></span>     |
| <span data-ttu-id="bf76e-604">Suora</span><span class="sxs-lookup"><span data-stu-id="bf76e-604">Direct</span></span>                | <span data-ttu-id="bf76e-605">Suora</span><span class="sxs-lookup"><span data-stu-id="bf76e-605">Direct</span></span>      |
| <span data-ttu-id="bf76e-606">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="bf76e-606">Internship</span></span>            | <span data-ttu-id="bf76e-607">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="bf76e-607">Internship</span></span>  |
| <span data-ttu-id="bf76e-608">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="bf76e-608">Permanent</span></span>             | <span data-ttu-id="bf76e-609">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="bf76e-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="bf76e-610">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="bf76e-610">Marital status</span></span>

<span data-ttu-id="bf76e-611">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="bf76e-612">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="bf76e-613">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-613">Talent</span></span>                 | <span data-ttu-id="bf76e-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="bf76e-615">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="bf76e-615">Married</span></span>                | <span data-ttu-id="bf76e-616">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="bf76e-616">Married</span></span>                   |
| <span data-ttu-id="bf76e-617">Yksi</span><span class="sxs-lookup"><span data-stu-id="bf76e-617">Single</span></span>                 | <span data-ttu-id="bf76e-618">Yksi</span><span class="sxs-lookup"><span data-stu-id="bf76e-618">Single</span></span>                    |
| <span data-ttu-id="bf76e-619">Leski</span><span class="sxs-lookup"><span data-stu-id="bf76e-619">Widowed</span></span>                | <span data-ttu-id="bf76e-620">Leski</span><span class="sxs-lookup"><span data-stu-id="bf76e-620">Widowed</span></span>                   |
| <span data-ttu-id="bf76e-621">Eronnut</span><span class="sxs-lookup"><span data-stu-id="bf76e-621">Divorced</span></span>               | <span data-ttu-id="bf76e-622">Eronnut</span><span class="sxs-lookup"><span data-stu-id="bf76e-622">Divorced</span></span>                  |
| <span data-ttu-id="bf76e-623">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="bf76e-623">Registered Partnership</span></span> | <span data-ttu-id="bf76e-624">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="bf76e-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="bf76e-625">None</span><span class="sxs-lookup"><span data-stu-id="bf76e-625">None</span></span>                   | <span data-ttu-id="bf76e-626">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="bf76e-627">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="bf76e-627">Cohabiting</span></span>             | <span data-ttu-id="bf76e-628">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="bf76e-629">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="bf76e-629">Gender</span></span>

<span data-ttu-id="bf76e-630">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="bf76e-631">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="bf76e-632">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-632">Talent</span></span>       | <span data-ttu-id="bf76e-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="bf76e-634">Mies</span><span class="sxs-lookup"><span data-stu-id="bf76e-634">Male</span></span>         | <span data-ttu-id="bf76e-635">Mies</span><span class="sxs-lookup"><span data-stu-id="bf76e-635">Male</span></span>                      |
| <span data-ttu-id="bf76e-636">Nainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-636">Female</span></span>       | <span data-ttu-id="bf76e-637">Nainen</span><span class="sxs-lookup"><span data-stu-id="bf76e-637">Female</span></span>                    |
| <span data-ttu-id="bf76e-638">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="bf76e-638">Non-specific</span></span> | <span data-ttu-id="bf76e-639">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="bf76e-640">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="bf76e-640">Payment method</span></span>

<span data-ttu-id="bf76e-641">Maksutavat antavat työntekijälle ja yritykselle keinon kuvata, miten työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="bf76e-642">Maksutavat on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="bf76e-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="bf76e-643">Seuraavassa taulukossa kuvataan, miten maksutavat liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="bf76e-644">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-644">Talent</span></span>             | <span data-ttu-id="bf76e-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="bf76e-646">Maksu</span><span class="sxs-lookup"><span data-stu-id="bf76e-646">Cash</span></span>               | <span data-ttu-id="bf76e-647">Maksu</span><span class="sxs-lookup"><span data-stu-id="bf76e-647">Cash</span></span>                      |
| <span data-ttu-id="bf76e-648">Sähköinen maksu</span><span class="sxs-lookup"><span data-stu-id="bf76e-648">Electronic Payment</span></span> | <span data-ttu-id="bf76e-649">Tapahtumien siirto</span><span class="sxs-lookup"><span data-stu-id="bf76e-649">Transfer</span></span>                  |
| <span data-ttu-id="bf76e-650">Tarkistus</span><span class="sxs-lookup"><span data-stu-id="bf76e-650">Check</span></span>              | <span data-ttu-id="bf76e-651">Sekki</span><span class="sxs-lookup"><span data-stu-id="bf76e-651">Cheque</span></span>                    |
| <span data-ttu-id="bf76e-652">Pankkivekseli</span><span class="sxs-lookup"><span data-stu-id="bf76e-652">Bank Draft</span></span>         | <span data-ttu-id="bf76e-653">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="bf76e-654">Muu</span><span class="sxs-lookup"><span data-stu-id="bf76e-654">Other</span></span>              | <span data-ttu-id="bf76e-655">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="bf76e-656">Pankkitilin tyyppi</span><span class="sxs-lookup"><span data-stu-id="bf76e-656">Bank account type</span></span>

<span data-ttu-id="bf76e-657">Pankkitilin tyyppejä käytetään sähköisissä maksuissa työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="bf76e-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="bf76e-658">Pankin tilityypit yhdistetään Dayforceen tilinsiirtämisen tietoina.</span><span class="sxs-lookup"><span data-stu-id="bf76e-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="bf76e-659">Pankkitilin tyypit ovat tarvittaessa käännettyjä ja hyväksytty arvoiksi sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="bf76e-660">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-660">Talent</span></span>            | <span data-ttu-id="bf76e-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="bf76e-662">Käyttötili</span><span class="sxs-lookup"><span data-stu-id="bf76e-662">Checking Account</span></span>  | <span data-ttu-id="bf76e-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="bf76e-663">CheckingAccount</span></span>           |
| <span data-ttu-id="bf76e-664">Palkanlaskennan tili</span><span class="sxs-lookup"><span data-stu-id="bf76e-664">Payroll Account</span></span>   | <span data-ttu-id="bf76e-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="bf76e-665">PayrollAccount</span></span>            |
| <span data-ttu-id="bf76e-666">Säästötili</span><span class="sxs-lookup"><span data-stu-id="bf76e-666">Savings Account</span></span>   | <span data-ttu-id="bf76e-667">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="bf76e-668">BankGirot-tili</span><span class="sxs-lookup"><span data-stu-id="bf76e-668">BankGirot account</span></span> | <span data-ttu-id="bf76e-669">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="bf76e-670">PlusGirot-tili</span><span class="sxs-lookup"><span data-stu-id="bf76e-670">PlusGirot account</span></span> | <span data-ttu-id="bf76e-671">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="bf76e-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="bf76e-672">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="bf76e-672">Earning codes</span></span>

<span data-ttu-id="bf76e-673">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="bf76e-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="bf76e-674">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="bf76e-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="bf76e-675">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="bf76e-676">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="bf76e-676">Supported frequencies</span></span>

- <span data-ttu-id="bf76e-677">Kaikki</span><span class="sxs-lookup"><span data-stu-id="bf76e-677">All</span></span>
- <span data-ttu-id="bf76e-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="bf76e-678">EVERYPAY</span></span>
- <span data-ttu-id="bf76e-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="bf76e-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="bf76e-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="bf76e-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="bf76e-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="bf76e-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="bf76e-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-682">1OFMTH</span></span>
- <span data-ttu-id="bf76e-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-683">LASTOFMTH</span></span>
- <span data-ttu-id="bf76e-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-684">2OFMTH</span></span>
- <span data-ttu-id="bf76e-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-685">3OFMTH</span></span>
- <span data-ttu-id="bf76e-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-686">4OFMTH</span></span>
- <span data-ttu-id="bf76e-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-687">5OFMTH</span></span>
- <span data-ttu-id="bf76e-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-688">1N2OFMTH</span></span>
- <span data-ttu-id="bf76e-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-689">3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-690">1N3OFMTH</span></span>
- <span data-ttu-id="bf76e-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-691">1N4OFMTH</span></span>
- <span data-ttu-id="bf76e-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-692">2N3OFMTH</span></span>
- <span data-ttu-id="bf76e-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-693">2N4OFMTH</span></span>
- <span data-ttu-id="bf76e-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="bf76e-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="bf76e-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="bf76e-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="bf76e-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="bf76e-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="bf76e-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="bf76e-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="bf76e-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="bf76e-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="bf76e-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="bf76e-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="bf76e-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="bf76e-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="bf76e-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="bf76e-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="bf76e-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="bf76e-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="bf76e-706">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="bf76e-706">Addresses</span></span>

<span data-ttu-id="bf76e-707">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="bf76e-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="bf76e-708">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="bf76e-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="bf76e-709">Talent</span><span class="sxs-lookup"><span data-stu-id="bf76e-709">Talent</span></span>              | <span data-ttu-id="bf76e-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="bf76e-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="bf76e-711">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="bf76e-711">Country/Region</span></span>      | <span data-ttu-id="bf76e-712">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-712">Country Code</span></span>          |
| <span data-ttu-id="bf76e-713">Postinumero</span><span class="sxs-lookup"><span data-stu-id="bf76e-713">Zip/Postal Code</span></span>     | <span data-ttu-id="bf76e-714">Postinumero</span><span class="sxs-lookup"><span data-stu-id="bf76e-714">Postal Code</span></span>           |
| <span data-ttu-id="bf76e-715">Alue</span><span class="sxs-lookup"><span data-stu-id="bf76e-715">State</span></span>               | <span data-ttu-id="bf76e-716">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="bf76e-716">State Code</span></span>            |
| <span data-ttu-id="bf76e-717">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="bf76e-717">City</span></span>                | <span data-ttu-id="bf76e-718">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="bf76e-718">City</span></span>                  |
| <span data-ttu-id="bf76e-719">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="bf76e-719">County</span></span>              | <span data-ttu-id="bf76e-720">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="bf76e-720">County (Municipality)</span></span> |
| <span data-ttu-id="bf76e-721">Katu</span><span class="sxs-lookup"><span data-stu-id="bf76e-721">Street</span></span>              | <span data-ttu-id="bf76e-722">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="bf76e-722">Address Line 1</span></span>        |
| <span data-ttu-id="bf76e-723">Kadunnumero</span><span class="sxs-lookup"><span data-stu-id="bf76e-723">Street Number</span></span>       | <span data-ttu-id="bf76e-724">Osoiterivi 2</span><span class="sxs-lookup"><span data-stu-id="bf76e-724">Address Line 2</span></span>        |
| <span data-ttu-id="bf76e-725">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="bf76e-725">Building Complement</span></span> | <span data-ttu-id="bf76e-726">Osoiterivi 5</span><span class="sxs-lookup"><span data-stu-id="bf76e-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="bf76e-727">Passin numero</span><span class="sxs-lookup"><span data-stu-id="bf76e-727">Passport number</span></span>

<span data-ttu-id="bf76e-728">Työntekijät voivat ilmoittaa passin tiedot.</span><span class="sxs-lookup"><span data-stu-id="bf76e-728">Employees can declare passport information.</span></span> <span data-ttu-id="bf76e-729">Tämä tietoa on **Passi**-tunnustyyppiä ja se on integroitu Dayforceen osaksi työntekijän Meksikon liittyvää tietoa.</span><span class="sxs-lookup"><span data-stu-id="bf76e-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="bf76e-730">Tunnustyyppi = "Passi"</span><span class="sxs-lookup"><span data-stu-id="bf76e-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="bf76e-731">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="bf76e-731">Issued Date</span></span>
- <span data-ttu-id="bf76e-732">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="bf76e-732">Expiration Date</span></span>

<span data-ttu-id="bf76e-733">Työntekijät voi määrittää useita tunnistenumeroita **Passi**-tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="bf76e-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="bf76e-734">Vain nykyiset aktiiviset passitapahtumat integroidaan Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="bf76e-735">Mikäli kaikki passitapahtumat ovat vanhentuneet, passi, joka on viimeksi myönnetty on integroitu Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="bf76e-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
