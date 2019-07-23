---
title: Palkanlaskennan Talent and Dayforce -integroinnin määrittäminen
description: Tässä ohjeaiheessa kerrotaan, että kuinka konfiguroida integrointeja Microsoft Dynamics 365 for Talentin ja Ceridian Dayforcen välillä voidaksesi käsitellä palkka-ajoa.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 59234ef44ad22383ae5daf71d4b663c6183e6c05
ms.sourcegitcommit: d599bc1fc60a010c2753ca547219ae21456b1df9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/25/2019
ms.locfileid: "1702815"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="d4622-103">Talentin ja Dayforcen välisen palkanlaskennan integroinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d4622-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4622-104">Microsoft Dynamics 365 for Talentin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="d4622-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="d4622-105">Sekä Talentin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.</span><span class="sxs-lookup"><span data-stu-id="d4622-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d4622-106">Käytettäessä jotakin palvelua, kuten Dayforcea palkka-ajojen suorittamiseen, on otettava käyttöön integrointi Talentissa.</span><span class="sxs-lookup"><span data-stu-id="d4622-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="d4622-107">Integrointi edellyttää tiettyjä tietoja Talentista.</span><span class="sxs-lookup"><span data-stu-id="d4622-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="d4622-108">Sinun on varmistettava, että Dayforceen yhdistetyt tiedot on konfiguroitu Talentissa siten, että ne tukevat integrointia.</span><span class="sxs-lookup"><span data-stu-id="d4622-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="d4622-109">Integraatio käyttää seuraavanlaisia laajoja tietoryhmiä:</span><span class="sxs-lookup"><span data-stu-id="d4622-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d4622-110">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-110">Human resources data</span></span>
- <span data-ttu-id="d4622-111">Kompensaatiotiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-111">Compensation data</span></span>
- <span data-ttu-id="d4622-112">Palkanlaskentatietoja, kuten maksujaksot, maksukaudet ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d4622-113">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-113">Worker data</span></span>

<span data-ttu-id="d4622-114">Tässä ohjeaiheessa kuvataan vaiheita, joita sinun on noudatettava ottaaksesi integroinnin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="d4622-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d4622-115">Lisäksi kerrotaan minkä tyyppisiä tietoja ja konfigurointitietoja integrointi edellyttää.</span><span class="sxs-lookup"><span data-stu-id="d4622-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d4622-116">Ota integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="d4622-116">Enable the integration</span></span>

<span data-ttu-id="d4622-117">Ota integraatio käyttöön Talentissa ja lisää konfiguraatiotiedot muodostaaksesi yhteyden Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d4622-118">Mikäli haluat kirjanpitotapahtuman, joka valmistetaan ja tuodaan Microsoft Dynamics 365 for Finance and Operationsiin, sinun on perustettava myös Microsoft Azure -tallennustili ja kirjoitettava Azure-tallennuksen yhteyden muodostuskomento Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="d4622-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="d4622-119">Ota integrointi käyttöön Talentissa seuraavien vaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="d4622-120">Valitse **Järjestelmänvalvoja**-sivulla **konfiguroinnin integrointi**.</span><span class="sxs-lookup"><span data-stu-id="d4622-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d4622-121">Lisää File Transfer Protocol (FTP) -päätepiste ja suojattu FTP-kansiopolku.</span><span class="sxs-lookup"><span data-stu-id="d4622-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d4622-122">Kirjoita sen käyttäjän käyttäjänimi ja salasana, joka voi käyttää suojattua FTP-päätepistettä ja kansiopolkua.</span><span class="sxs-lookup"><span data-stu-id="d4622-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d4622-123">Testaa yhteys kuten vaadittu ja määritä **Ota käyttöön palkanmaksun integrointi** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="d4622-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d4622-124">Kun integrointi otetaan käyttöön, tietojen viennin paketti ja tiedostot luodaan ja taajuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="d4622-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d4622-125">Voit muuttaa tätä taajuutta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="d4622-126">Lisätietoja Azure-tallennustilien ja Azure-tallennusyhteyden yhteysmerkkijonoista seuraavissa Azure-aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d4622-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="d4622-127">Lisätietoja Azure-tallennustileistä</span><span class="sxs-lookup"><span data-stu-id="d4622-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d4622-128">Määritä Azure-tallennustilan yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="d4622-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="d4622-129">Tekniset tiedot, kun palkanlaskennan integrointi on otettu käyttöön</span><span class="sxs-lookup"><span data-stu-id="d4622-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="d4622-130">Palkanlaskennan integroinnin käytöstäpoistamisella on kaksi pääasiallista vaikutusta:</span><span class="sxs-lookup"><span data-stu-id="d4622-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="d4622-131">Palkanlaskennan integroinnin vienti -niminen tietojen vientiprojekti luodaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="d4622-132">Tämä projekti sisältää palkanhallinnan integrointiin tarvittavat yksiköt ja kentät.</span><span class="sxs-lookup"><span data-stu-id="d4622-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="d4622-133">Voit tutustua projektiin valitsemalla ensin **Järjestelmän hallinta**, sitten **Tietojen hallinta** -ruudun ja avaamalla lopuksi tietoprojektin projektiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="d4622-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="d4622-134">Tämä erätyö suorittaa tietojen vientiprojektin, salaa tuloksena olevan tietopaketin ja siirtää tietopakettitiedoston SFTP-päätepisteeseen, joka on määritetty **Integroinnin määritys** -näytössä.</span><span class="sxs-lookup"><span data-stu-id="d4622-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="d4622-135">SFTP-päätepisteeseen siirretty tietopaketti salataan paketin yksilöllisellä avaimella.</span><span class="sxs-lookup"><span data-stu-id="d4622-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="d4622-136">Avain on Azure Key Vaultissa, jota vain Ceridian voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="d4622-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="d4622-137">Tietopaketin sisällön salausta ei voi purkaa eikä sisältöä tutkia.</span><span class="sxs-lookup"><span data-stu-id="d4622-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="d4622-138">Jos tietopaketin sisältöä on tarkasteltava, Palkanlaskennan integroinnin vienti -tietoprojekti on vietävä manuaalisesti, jonka jälkeen on ladattava ja avattava.</span><span class="sxs-lookup"><span data-stu-id="d4622-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="d4622-139">Manuaalisessa viennissä ei käytetä salausta eikä pakettia siirretä.</span><span class="sxs-lookup"><span data-stu-id="d4622-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="d4622-140">Määritä tietosi</span><span class="sxs-lookup"><span data-stu-id="d4622-140">Configure your data</span></span> 

<span data-ttu-id="d4622-141">Voidaksesi käsitellä palkanlaskentaa, sinun on määritettävä henkilöstöhallinnon tiedot Talentissa.</span><span class="sxs-lookup"><span data-stu-id="d4622-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="d4622-142">On määritettävä organisaation tiedot, kuten työt ja toimet sekä edut ja kompensaatiotiedot.</span><span class="sxs-lookup"><span data-stu-id="d4622-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d4622-143">Nämä tiedot sisältävät työllisyys-, palkka- ja vähennystiedot, jotka vaaditaan, jotta voidaan luoda työntekijän palkka.</span><span class="sxs-lookup"><span data-stu-id="d4622-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d4622-144">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d4622-145">Edut</span><span class="sxs-lookup"><span data-stu-id="d4622-145">Benefits</span></span> 

<span data-ttu-id="d4622-146">Henkilöstöhallinto sisältää työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="d4622-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d4622-147">Luodessasi etuja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="d4622-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d4622-148">Etusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="d4622-148">Benefit plans</span></span>

- <span data-ttu-id="d4622-149">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-149">Plan (required)</span></span>
- <span data-ttu-id="d4622-150">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-150">Type (required)</span></span>
- <span data-ttu-id="d4622-151">Palkanlaskennan vaikutus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-151">Payroll impact (required)</span></span>
- <span data-ttu-id="d4622-152">Palauta velvoitteet</span><span class="sxs-lookup"><span data-stu-id="d4622-152">Recover arrears</span></span>
- <span data-ttu-id="d4622-153">Vähennysmenetelmä</span><span class="sxs-lookup"><span data-stu-id="d4622-153">Deduction method</span></span>
- <span data-ttu-id="d4622-154">Vähennyksen prioriteetti</span><span class="sxs-lookup"><span data-stu-id="d4622-154">Deduction priority</span></span>
- <span data-ttu-id="d4622-155">Rajaa kausi</span><span class="sxs-lookup"><span data-stu-id="d4622-155">Limit period</span></span>
- <span data-ttu-id="d4622-156">Rajasumma</span><span class="sxs-lookup"><span data-stu-id="d4622-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d4622-157">Edut</span><span class="sxs-lookup"><span data-stu-id="d4622-157">Benefits</span></span>

- <span data-ttu-id="d4622-158">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-158">Plan (required)</span></span>
- <span data-ttu-id="d4622-159">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-159">Type (required)</span></span>
- <span data-ttu-id="d4622-160">Vaihtoehto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-160">Option (required)</span></span>
- <span data-ttu-id="d4622-161">Edun tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-161">Benefit ID (required)</span></span>
- <span data-ttu-id="d4622-162">Tiheys</span><span class="sxs-lookup"><span data-stu-id="d4622-162">Frequency</span></span>
- <span data-ttu-id="d4622-163">Peruste</span><span class="sxs-lookup"><span data-stu-id="d4622-163">Basis</span></span>
- <span data-ttu-id="d4622-164">Summa tai hinta</span><span class="sxs-lookup"><span data-stu-id="d4622-164">Amount or rate</span></span>
- <span data-ttu-id="d4622-165">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d4622-166">Tuetut maksutiheydet</span><span class="sxs-lookup"><span data-stu-id="d4622-166">Supported frequencies</span></span> 

- <span data-ttu-id="d4622-167">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="d4622-167">Weekly</span></span>
- <span data-ttu-id="d4622-168">Kahden viikon välein</span><span class="sxs-lookup"><span data-stu-id="d4622-168">Bi-weekly</span></span>
- <span data-ttu-id="d4622-169">Joka toinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="d4622-169">Semi-monthly</span></span>
- <span data-ttu-id="d4622-170">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="d4622-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d4622-171">Tuetut pohjat</span><span class="sxs-lookup"><span data-stu-id="d4622-171">Supported bases</span></span> 

- <span data-ttu-id="d4622-172">Kiinteä summa</span><span class="sxs-lookup"><span data-stu-id="d4622-172">Fixed amount</span></span>
- <span data-ttu-id="d4622-173">Ansioiden prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="d4622-173">Percent of earnings</span></span>
- <span data-ttu-id="d4622-174">Tuottavat tunnit</span><span class="sxs-lookup"><span data-stu-id="d4622-174">Productive hours</span></span>

<span data-ttu-id="d4622-175">Dayforce luo seuraavat vähennykset, jotka perustuvat palkanlaskennan vaikutukseen, joka on määritelty etusuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="d4622-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d4622-176">Talentin valinta</span><span class="sxs-lookup"><span data-stu-id="d4622-176">Selection in Talent</span></span>        | <span data-ttu-id="d4622-177">Tulos Dayforcessa</span><span class="sxs-lookup"><span data-stu-id="d4622-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d4622-178">None</span><span class="sxs-lookup"><span data-stu-id="d4622-178">None</span></span>                       | <span data-ttu-id="d4622-179">Vähennyksiä ei luoda.</span><span class="sxs-lookup"><span data-stu-id="d4622-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="d4622-180">Vain vähennys</span><span class="sxs-lookup"><span data-stu-id="d4622-180">Deduction only</span></span>             | <span data-ttu-id="d4622-181">Työntekijävähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="d4622-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d4622-182">Vain osuus</span><span class="sxs-lookup"><span data-stu-id="d4622-182">Contribution only</span></span>          | <span data-ttu-id="d4622-183">Työnantajavähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="d4622-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d4622-184">Vähennys ja osuus</span><span class="sxs-lookup"><span data-stu-id="d4622-184">Deduction and contribution</span></span> | <span data-ttu-id="d4622-185">Työntekijän ja työnantajan vähennykset luodaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d4622-186">Lisätietoja etuohjelman määrittämisestä ja hallitsemisesta seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d4622-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="d4622-187">Työsuhde-etuohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="d4622-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d4622-188">Luo uusi etu</span><span class="sxs-lookup"><span data-stu-id="d4622-188">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d4622-189">Määritä edun oikeutussäännöt ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="d4622-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d4622-190">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="d4622-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d4622-191">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="d4622-191">Compensation</span></span> 

<span data-ttu-id="d4622-192">Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista.</span><span class="sxs-lookup"><span data-stu-id="d4622-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d4622-193">Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="d4622-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d4622-194">Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="d4622-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d4622-195">Dayforce käyttää kompensaatiotietoja laskeakseen työntekijän tunti- tai vuosihinnan.</span><span class="sxs-lookup"><span data-stu-id="d4622-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d4622-196">Kiinteät kompensaatiosuunnitelmat ja palkkojen muunnokset vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d4622-197">Työntekijöiden täytyy olla liitettynä kiinteään kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d4622-198">Katso lisätietoja kompensaatiosuunnitelmista seuraavista ohjeaiheista:</span><span class="sxs-lookup"><span data-stu-id="d4622-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="d4622-199">Kiinteiden kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="d4622-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d4622-200">Muuttuvien kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="d4622-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d4622-201">Palkka- ja kompensaatiorakenteen ja -suunnitelmien kehittäminen</span><span class="sxs-lookup"><span data-stu-id="d4622-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d4622-202">Kompensaation käsittely</span><span class="sxs-lookup"><span data-stu-id="d4622-202">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d4622-203">Kompensaatioprosessin määrittäminen ja tulosten laskeminen</span><span class="sxs-lookup"><span data-stu-id="d4622-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d4622-204">Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="d4622-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d4622-205">Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="d4622-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d4622-206">Työt</span><span class="sxs-lookup"><span data-stu-id="d4622-206">Jobs</span></span> 

<span data-ttu-id="d4622-207">Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään.</span><span class="sxs-lookup"><span data-stu-id="d4622-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d4622-208">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d4622-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d4622-209">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="d4622-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d4622-210">Määritä uudet työt</span><span class="sxs-lookup"><span data-stu-id="d4622-210">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d4622-211">Toimet</span><span class="sxs-lookup"><span data-stu-id="d4622-211">Positions</span></span>

<span data-ttu-id="d4622-212">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="d4622-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="d4622-213">Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="d4622-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d4622-214">Osastolla on toimi.</span><span class="sxs-lookup"><span data-stu-id="d4622-214">A position exists in a department.</span></span> <span data-ttu-id="d4622-215">Vain yksi työntekijä voidaan liittää yhteen toimeen.</span><span class="sxs-lookup"><span data-stu-id="d4622-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d4622-216">Muista seuraavat tiedot ja määritykset, kun määrität toimia:</span><span class="sxs-lookup"><span data-stu-id="d4622-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d4622-217">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-217">Position (required)</span></span>
- <span data-ttu-id="d4622-218">Kuvaus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-218">Description (required)</span></span>
- <span data-ttu-id="d4622-219">Työ (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-219">Job (required)</span></span>
- <span data-ttu-id="d4622-220">Osasto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-220">Department (required)</span></span>
- <span data-ttu-id="d4622-221">Toimen tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-221">Position type (required)</span></span>
- <span data-ttu-id="d4622-222">Kokopäiväinen (FTE)</span><span class="sxs-lookup"><span data-stu-id="d4622-222">Full-time equivalent</span></span>
- <span data-ttu-id="d4622-223">Vuosittaiset vakiotunnit (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="d4622-224">Yrityksen maksama (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d4622-225">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-225">Pay cycle (required)</span></span>
- <span data-ttu-id="d4622-226">Oletusarvo taloushallinnon dimensio – kustannuspaikka (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d4622-227">Työntekijän määritys – työntekijä, tehtävän alkamisaika, tehtävän lopetusaika, syykoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d4622-228">Mikäli useita toimia samalla osastolla liittyy samaan työhön, ne yhdistetään yhteen toimeen Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="d4622-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d4622-229">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d4622-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d4622-230">Työvoiman järjestäminen osastojen, töiden ja toimien avulla</span><span class="sxs-lookup"><span data-stu-id="d4622-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d4622-231">Toimien määritys</span><span class="sxs-lookup"><span data-stu-id="d4622-231">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d4622-232">Osastot</span><span class="sxs-lookup"><span data-stu-id="d4622-232">Departments</span></span>

<span data-ttu-id="d4622-233">Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="d4622-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d4622-234">Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.</span><span class="sxs-lookup"><span data-stu-id="d4622-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d4622-235">Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin.</span><span class="sxs-lookup"><span data-stu-id="d4622-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d4622-236">Osastot voivat olla tulosvastuullisia.</span><span class="sxs-lookup"><span data-stu-id="d4622-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d4622-237">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="d4622-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d4622-238">Osaston luominen ja liittäminen osastohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="d4622-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d4622-239">Määritä uudet osastot</span><span class="sxs-lookup"><span data-stu-id="d4622-239">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d4622-240">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="d4622-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="d4622-241">Palkkajakso määrittää kuinka usein palkkalistoja käytetään, ja minä tiettyinä päivinä työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d4622-242">Esimerkiksi palkkajakso voi olla kuukausittainen ja työntekijöille voidaan maksaa kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="d4622-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d4622-243">Vaihtoehtoisesti palkkajakso voi olla viikoittainen ja työntekijöille voidaan maksaa tiistaina palkkajakson päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="d4622-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d4622-244">Palkkajaksot on osoitettu toimiin, jotta voidaan valvoa milloin näissä tehtävissä oleville työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d4622-245">Luotuasi palkkajaksoja, voit luoda maksukausia kullekin jaksolle.</span><span class="sxs-lookup"><span data-stu-id="d4622-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d4622-246">Jokaisella palkkakaudella on maksun oletuspäivämäärä, joka perustuu antamiisi tietoihin.</span><span class="sxs-lookup"><span data-stu-id="d4622-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d4622-247">Voit kuitenkin muokata maksun oletuspäivämäärää salliaksesi poikkeuksia, kuten kun maksupäivämäärä osuu vapaapäivälle.</span><span class="sxs-lookup"><span data-stu-id="d4622-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d4622-248">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="d4622-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d4622-249">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-249">Pay cycle (required)</span></span>
- <span data-ttu-id="d4622-250">Maksujakson tiheys (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d4622-251">Kauden alkamispäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="d4622-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d4622-252">Oletusmaksupäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="d4622-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d4622-253">Nämä tiedot on integroitu Dayforce-palkkaryhmien kanssa ja eriteltynä eriteltyinä maittain tai alueittain kullekin maksujaksolle.</span><span class="sxs-lookup"><span data-stu-id="d4622-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d4622-254">Ennen integraatiota on luotava vähintään yksi palkkakausi.</span><span class="sxs-lookup"><span data-stu-id="d4622-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d4622-255">Dayforce luo maksuryhmäkalentereita ja maksupäiviä, jotka perustuvat ensimmäisen palkkakauden alkamispäivämäärään ja määritetty oletusmaksupäivä on asetettu Talentissa.</span><span class="sxs-lookup"><span data-stu-id="d4622-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d4622-256">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-256">Earning codes</span></span>

<span data-ttu-id="d4622-257">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="d4622-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d4622-258">Tunnuksissa on erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="d4622-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d4622-259">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="d4622-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d4622-260">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-260">Earning Code (required)</span></span>
- <span data-ttu-id="d4622-261">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-261">Description</span></span>
- <span data-ttu-id="d4622-262">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="d4622-262">Unit of measure</span></span>
- <span data-ttu-id="d4622-263">Tuottava</span><span class="sxs-lookup"><span data-stu-id="d4622-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d4622-264">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-264">Worker data</span></span>

<span data-ttu-id="d4622-265">Tietueet eri työntekijöille, joita sinulla on ovat tärkeitä henkilöstöhallinnossa ja palkanlaskentajärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="d4622-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d4622-266">Tietueisiin lisättäviä tietoja käytetään työntekijöiden ja henkilökohtaisten tietojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="d4622-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d4622-267">Voit ylläpitää työntekijöille seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="d4622-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d4622-268">**Perustiedot** – Ylläpidä työntekijän perustietoja, kuten yhteystiedot, demografiatiedot, tunnistetiedot, perheen tiedot, asevelvollisuuden tila, ekspatriaatin tiedot ja omat yhteyshenkilöt ja hätäyhteyshenkilöt.</span><span class="sxs-lookup"><span data-stu-id="d4622-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d4622-269">**Työsuhde** – Ylläpidä tietoja työntekijän työsuhteesta, kuten yrityksen tai organisaation kytköksistä, toimen määrityksestä, aloitus- ja päättymispäivämääristä, työkelpoisuudesta, työehdoista, eläkkestä, lomista ja uudelleensijoittumisesta.</span><span class="sxs-lookup"><span data-stu-id="d4622-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d4622-270">**Lomat ja poissaolot** –Ylläpidä tietoa työntekijän poissaoloista, kuten työaikakalentereista, poissaolotapahtumista ja poissaoloasetuksista.</span><span class="sxs-lookup"><span data-stu-id="d4622-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d4622-271">**Kompensaatio ja palkanlaskenta** – Ylläpidä työntekijän kompensaatiosuunnitelmien tietoja ja palkanlaskentatietoja, kuten suunnitelmien toteutuminen, palkkiot, suorituskyky, provisio, verotiedot, eläkkeelle jääminen ja palkan vähennykset.</span><span class="sxs-lookup"><span data-stu-id="d4622-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d4622-272">Kirjoittaessasi työntekijätietoja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="d4622-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d4622-273">Yleistiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-273">General information</span></span>

- <span data-ttu-id="d4622-274">Henkilönumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-274">Personnel number (required)</span></span>
- <span data-ttu-id="d4622-275">Etunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-275">First name (required)</span></span>
- <span data-ttu-id="d4622-276">Sukunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-276">Last name (required)</span></span>
- <span data-ttu-id="d4622-277">Toinen nimi</span><span class="sxs-lookup"><span data-stu-id="d4622-277">Middle name</span></span>
- <span data-ttu-id="d4622-278">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="d4622-278">Seniority date</span></span>
- <span data-ttu-id="d4622-279">Tunnetaan nimellä</span><span class="sxs-lookup"><span data-stu-id="d4622-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d4622-280">Henkilökohtaiset tiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-280">Personal information</span></span>

- <span data-ttu-id="d4622-281">Siviilisääty (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-281">Marital status (required)</span></span>
- <span data-ttu-id="d4622-282">Syntymäpäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-282">Birth date (required)</span></span>
- <span data-ttu-id="d4622-283">Sukupuoli (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-283">Gender (required)</span></span>
- <span data-ttu-id="d4622-284">Henkilö on invalidi</span><span class="sxs-lookup"><span data-stu-id="d4622-284">Person with disabilities</span></span>
- <span data-ttu-id="d4622-285">Kansalaisuus, maa, alue (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="d4622-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d4622-286">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-286">Address information</span></span>

- <span data-ttu-id="d4622-287">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-287">Primary (required)</span></span>
- <span data-ttu-id="d4622-288">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-288">Country/region (required)</span></span>
- <span data-ttu-id="d4622-289">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-289">Postal code (required)</span></span>
- <span data-ttu-id="d4622-290">Kadunnumero (pakollinen) (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="d4622-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d4622-291">Rakennusta koskeva lisätieto (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="d4622-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d4622-292">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-292">City (required)</span></span>
- <span data-ttu-id="d4622-293">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-293">State (required)</span></span>
- <span data-ttu-id="d4622-294">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d4622-295">Yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-295">Contact information</span></span> 

- <span data-ttu-id="d4622-296">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-296">Primary (required)</span></span>
- <span data-ttu-id="d4622-297">Yhteystiedon numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-297">Contact number (required)</span></span>
- <span data-ttu-id="d4622-298">Alanumero</span><span class="sxs-lookup"><span data-stu-id="d4622-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d4622-299">Palkanlaskentatiedot ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-299">Payroll information and earning codes</span></span>

<span data-ttu-id="d4622-300">Työntekijöille voidaan antaa erityisiä tuloja tietyllä maksutaajuudella ja toivotulla maksutavalla.</span><span class="sxs-lookup"><span data-stu-id="d4622-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d4622-301">Seuraavia kenttiä käytetään Dayforcessa sen varmistamiseksi, että näitä määrityksiä ja asetuksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="d4622-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d4622-302">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-302">Earning codes</span></span>

- <span data-ttu-id="d4622-303">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-303">Position (required)</span></span>
- <span data-ttu-id="d4622-304">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-304">Earning Code (required)</span></span>
- <span data-ttu-id="d4622-305">Taajuus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-305">Frequency (required)</span></span>
- <span data-ttu-id="d4622-306">Summa (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d4622-307">Palkanlaskentatiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-307">Payroll information</span></span>

- <span data-ttu-id="d4622-308">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="d4622-308">Payment Method</span></span>
- <span data-ttu-id="d4622-309">Talousalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-309">Economic Region (required)</span></span>
- <span data-ttu-id="d4622-310">Työsuhde-etujen tunnus</span><span class="sxs-lookup"><span data-stu-id="d4622-310">Employee Benefits ID</span></span>
- <span data-ttu-id="d4622-311">Kansallinen/alueellinen tunnusnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-311">National ID Number (required)</span></span>
- <span data-ttu-id="d4622-312">Sotilaspalveluksen numero</span><span class="sxs-lookup"><span data-stu-id="d4622-312">Military Service Number</span></span>
- <span data-ttu-id="d4622-313">Vuoron tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-313">Shift ID (required)</span></span>
- <span data-ttu-id="d4622-314">Veronumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-314">Tax Number (required)</span></span>
- <span data-ttu-id="d4622-315">Ammattijärjestön tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-315">Union ID (required)</span></span>
- <span data-ttu-id="d4622-316">Työpäivän tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-316">Work Day ID (required)</span></span>
- <span data-ttu-id="d4622-317">Työluvan numero</span><span class="sxs-lookup"><span data-stu-id="d4622-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d4622-318">Maksutavoista Meksiko tukee seuraavia: **Käteinen**, **shekki** (yrityksen fyysinen shekki) ja **sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="d4622-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d4622-319">Mikäli maksutapaa ei ole määritetty, **shekki** on oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="d4622-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d4622-320">Työsuhteen tiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-320">Employment details</span></span>

<span data-ttu-id="d4622-321">Työntekijöiden yksityiskohtaista historiaa käytetään keskeisenä informaationa, jolla saadaan työntekijän palkkaus, irtisanominen ja rekrytointitilastot Dayforcesta.</span><span class="sxs-lookup"><span data-stu-id="d4622-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d4622-322">Dayforce tukee kerrallaan vain yhtä aktiivisen työntekijän tietuetta.</span><span class="sxs-lookup"><span data-stu-id="d4622-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d4622-323">Työsuhteen alkamispäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-323">Employment start date (required)</span></span>
- <span data-ttu-id="d4622-324">Työsuhteen päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-324">Employment end date</span></span>
- <span data-ttu-id="d4622-325">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-325">Start date</span></span>
- <span data-ttu-id="d4622-326">Muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-326">Adjusted start date</span></span>
- <span data-ttu-id="d4622-327">Työsuhteen päättymispäivä (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="d4622-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d4622-328">Työsuhteen päättymissyy (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="d4622-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d4622-329">Seuraavien tietojen avulla lasketaan työntekijän tärkeimmät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="d4622-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d4622-330">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-330">Talent</span></span>                | <span data-ttu-id="d4622-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4622-332">Viimeisimmän työhönoton päivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-332">Most recent hire date</span></span> | <span data-ttu-id="d4622-333">Työntekijän työsuhteen alku voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="d4622-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d4622-334">Työsuhteen loppumispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-334">Termination date</span></span>      | <span data-ttu-id="d4622-335">Työntekijän työsuhteen loppu voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="d4622-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d4622-336">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-336">Start date</span></span>            | <span data-ttu-id="d4622-337">Muutettu alkamispäivämäärä, alkamispäivämäärä tai työsuhteen alku ei-aktiivisessa työsuhteen historiatietueessa</span><span class="sxs-lookup"><span data-stu-id="d4622-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d4622-338">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-338">Original hire date</span></span>    | <span data-ttu-id="d4622-339">Varhaisin työhistoriatietueen työsuhteen alku</span><span class="sxs-lookup"><span data-stu-id="d4622-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d4622-340">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="d4622-340">Compensation</span></span>

<span data-ttu-id="d4622-341">Kiinteän kompensaatiosuunnitelmaan tulee liittää jokaisen työntekijän ensisijainen toimi koko työsuhteen ajalla.</span><span class="sxs-lookup"><span data-stu-id="d4622-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d4622-342">Ajanjakso alkaa siitä päivämäärästä, jona työntekijä palkattiin (tai työsuhteen alkamispäivämäärä) ja jatkuu, kunnes työsuhde loppuu.</span><span class="sxs-lookup"><span data-stu-id="d4622-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d4622-343">Voimaantulopäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-343">Effective Date (required)</span></span>
- <span data-ttu-id="d4622-344">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="d4622-344">Expiration date</span></span>
- <span data-ttu-id="d4622-345">Palkkio (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-345">Pay Rate (required)</span></span>
- <span data-ttu-id="d4622-346">Palkkion muunnokset (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d4622-347">Vuosittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="d4622-348">Tunnittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="d4622-349">Mikäli tuntityöntekijällä on useita toimia, ensisijaisen toimen kiinteä kompensaation tuodaan Dayforceen työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="d4622-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d4622-350">Ei-ensisijaisten toimien tuntihinta tallennetaan Dayforcen vastaavaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="d4622-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d4622-351">Mikäli palkallisella työntekijällä on useita toimia, kumulatiivinen tuntihinta ja vuosittainen palkka kaikista aktiivisista toimista johdetaan ja käytetään työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="d4622-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d4622-352">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="d4622-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d4622-353">Sosiaaliturvan tunniste</span><span class="sxs-lookup"><span data-stu-id="d4622-353">Social Security identifier</span></span> 

<span data-ttu-id="d4622-354">Jokaisella työntekijä on oltava yksi ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="d4622-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d4622-355">Tunnuksen on oltava **SSN**-tunnus.</span><span class="sxs-lookup"><span data-stu-id="d4622-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d4622-356">Dayforcessa se johdetaan automaattisesti työntekijän sosiaaliturvatunnuksesta, jota tarvitaan työsuhdetta solmittaessa.</span><span class="sxs-lookup"><span data-stu-id="d4622-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d4622-357">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-357">Primary (required)</span></span>
- <span data-ttu-id="d4622-358">Tunnuksen tyyppi = "Henkilötunnus"</span><span class="sxs-lookup"><span data-stu-id="d4622-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d4622-359">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-359">Issued Date</span></span>
- <span data-ttu-id="d4622-360">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="d4622-360">Expiration Date</span></span>

<span data-ttu-id="d4622-361">Työntekijät voi määrittää useita tunnistenumeroita **SSN**-tunnuksesta (henkilötunnus).</span><span class="sxs-lookup"><span data-stu-id="d4622-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d4622-362">Tietue, joka on merkitty **Ensisijainen** on integroitu Dayforceen, riippumatta siitä, onko numero aktiivinen tai vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="d4622-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d4622-363">Pankkitilit ja suoritukset</span><span class="sxs-lookup"><span data-stu-id="d4622-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="d4622-364">Voimassa olevat pankkitilitiedot on kirjattava kaikille työntekijöille, jotka haluavat, että hänelle maksetaan pankkisiirtona.</span><span class="sxs-lookup"><span data-stu-id="d4622-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d4622-365">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-365">Talent</span></span>                         | <span data-ttu-id="d4622-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4622-367">Pankkitilin numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d4622-368">SWIFT-koodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-368">SWIFT code (required)</span></span>          | <span data-ttu-id="d4622-369">**Pankkitunnus**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="d4622-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d4622-370">Sivuliikkeen numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d4622-371">Pankkitilin tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-371">Bank account type (required)</span></span>   | <span data-ttu-id="d4622-372">**Tilityyppi**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="d4622-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d4622-373">Tuetut arvot sisältävät kohdat **Tarkistus** ja **Palkanlaskenta**.</span><span class="sxs-lookup"><span data-stu-id="d4622-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d4622-374">Työntekijät, jotka haluavat, että heille maksetaan pankkisiirtona, on toimitettava linkki jäännöstilille, joka kuuluu oikeushenkilölle, jolla on ensisijainen osoite Meksikossa ja jolla on voimassa oleva tili meksikolaisessa pankissa.</span><span class="sxs-lookup"><span data-stu-id="d4622-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d4622-375">Kaikki muut jäljellä olevat tilit jätetään huomiotta.</span><span class="sxs-lookup"><span data-stu-id="d4622-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d4622-376">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="d4622-376">Address information</span></span>

<span data-ttu-id="d4622-377">Jokaisella työntekijällä on oltava yksi ensisijainen toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="d4622-377">Every employee must have one primary location.</span></span> <span data-ttu-id="d4622-378">Dayforcessa tätä sijaintia käytetään määrittämään työntekijän ensisijainen oleskelulupa verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="d4622-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d4622-379">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-379">Primary (required)</span></span>
- <span data-ttu-id="d4622-380">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-380">Country/region (required)</span></span>
- <span data-ttu-id="d4622-381">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="d4622-382">Katuosoite (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-382">Street (required)</span></span>
- <span data-ttu-id="d4622-383">Kadunnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-383">Street Number (required)</span></span>
- <span data-ttu-id="d4622-384">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="d4622-384">Building Complement</span></span>
- <span data-ttu-id="d4622-385">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-385">City (required)</span></span>
- <span data-ttu-id="d4622-386">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-386">State (required)</span></span>
- <span data-ttu-id="d4622-387">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d4622-388">Määritä tiedot luodaksesi palkkalistoja Yhdysvalloissa ja Kanadassa</span><span class="sxs-lookup"><span data-stu-id="d4622-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d4622-389">Jos luot maksuja työntekijöille, jotka ovat Yhdysvalloissa ja Kanadassa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="d4622-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d4622-390">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="d4622-390">Departments are required on positions.</span></span>
- <span data-ttu-id="d4622-391">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="d4622-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d4622-392">Voit määrittää Talentin edellyttämään, että toimet määrittävät osaston.</span><span class="sxs-lookup"><span data-stu-id="d4622-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="d4622-393">Tehdäksesi tämän valitse **Henkilöstöhallinnon jaetut toimet > Toimet > Edellytä osastoja toimissa**.</span><span class="sxs-lookup"><span data-stu-id="d4622-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d4622-394">Suosittelemme, että tämä asetus otetaan käyttöön integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="d4622-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d4622-395">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="d4622-395">Job types</span></span>

<span data-ttu-id="d4622-396">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="d4622-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d4622-397">Työlajit ovat pakollisia palkanlaskennan käsittelemiseksi Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="d4622-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d4622-398">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="d4622-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d4622-399">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="d4622-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d4622-400">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="d4622-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d4622-401">Työlaji</span><span class="sxs-lookup"><span data-stu-id="d4622-401">Job type</span></span>   | <span data-ttu-id="d4622-402">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d4622-403">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="d4622-403">Hourly</span></span>     | <span data-ttu-id="d4622-404">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="d4622-404">Hourly</span></span>      |
| <span data-ttu-id="d4622-405">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="d4622-405">Salaried</span></span>   | <span data-ttu-id="d4622-406">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="d4622-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d4622-407">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="d4622-407">Position types</span></span> 

<span data-ttu-id="d4622-408">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="d4622-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d4622-409">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="d4622-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d4622-410">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="d4622-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d4622-411">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="d4622-411">Position type</span></span>   | <span data-ttu-id="d4622-412">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d4622-413">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="d4622-413">Full-time</span></span>       | <span data-ttu-id="d4622-414">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-414">Full time employee</span></span> |
| <span data-ttu-id="d4622-415">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="d4622-415">Part-time</span></span>       | <span data-ttu-id="d4622-416">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d4622-417">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-417">Reason codes</span></span>

<span data-ttu-id="d4622-418">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="d4622-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d4622-419">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="d4622-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d4622-420">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="d4622-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d4622-421">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-421">Reason code</span></span>    | <span data-ttu-id="d4622-422">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-422">Description</span></span>      | <span data-ttu-id="d4622-423">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="d4622-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d4622-424">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="d4622-424">RESIGNATION</span></span>    | <span data-ttu-id="d4622-425">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="d4622-425">Resignation</span></span>      | <span data-ttu-id="d4622-426">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-426">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-427">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="d4622-427">TERMINATION</span></span>    | <span data-ttu-id="d4622-428">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="d4622-428">Termination</span></span>      | <span data-ttu-id="d4622-429">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-429">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-430">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="d4622-430">RETIREMENT</span></span>     | <span data-ttu-id="d4622-431">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="d4622-431">Retirement</span></span>       | <span data-ttu-id="d4622-432">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-432">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-433">MUU</span><span class="sxs-lookup"><span data-stu-id="d4622-433">OTHER</span></span>          | <span data-ttu-id="d4622-434">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="d4622-434">Other Reasons</span></span>    | <span data-ttu-id="d4622-435">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-435">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-436">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="d4622-436">DEATH</span></span>          | <span data-ttu-id="d4622-437">Kuolema</span><span class="sxs-lookup"><span data-stu-id="d4622-437">Death</span></span>            | <span data-ttu-id="d4622-438">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-438">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d4622-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d4622-440">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="d4622-440">Leave of Absence</span></span> | <span data-ttu-id="d4622-441">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-441">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d4622-442">CONTRACTEND</span></span>    | <span data-ttu-id="d4622-443">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="d4622-443">End of Contract</span></span>  | <span data-ttu-id="d4622-444">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-444">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d4622-445">SALARYCHANGE</span></span>   | <span data-ttu-id="d4622-446">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="d4622-446">Change of Salary</span></span> | <span data-ttu-id="d4622-447">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="d4622-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d4622-448">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="d4622-448">Marital status</span></span>

<span data-ttu-id="d4622-449">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="d4622-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4622-450">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4622-451">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-451">Talent</span></span>                 | <span data-ttu-id="d4622-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d4622-453">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="d4622-453">Married</span></span>                | <span data-ttu-id="d4622-454">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="d4622-454">Married</span></span>              |
| <span data-ttu-id="d4622-455">Yksi</span><span class="sxs-lookup"><span data-stu-id="d4622-455">Single</span></span>                 | <span data-ttu-id="d4622-456">Yksi</span><span class="sxs-lookup"><span data-stu-id="d4622-456">Single</span></span>               |
| <span data-ttu-id="d4622-457">Leski</span><span class="sxs-lookup"><span data-stu-id="d4622-457">Widowed</span></span>                | <span data-ttu-id="d4622-458">Leski</span><span class="sxs-lookup"><span data-stu-id="d4622-458">Widowed</span></span>              |
| <span data-ttu-id="d4622-459">Eronnut</span><span class="sxs-lookup"><span data-stu-id="d4622-459">Divorced</span></span>               | <span data-ttu-id="d4622-460">Eronnut</span><span class="sxs-lookup"><span data-stu-id="d4622-460">Divorced</span></span>             |
| <span data-ttu-id="d4622-461">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="d4622-461">Registered Partnership</span></span> | <span data-ttu-id="d4622-462">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="d4622-462">Domestic Partnership</span></span> |
| <span data-ttu-id="d4622-463">None</span><span class="sxs-lookup"><span data-stu-id="d4622-463">None</span></span>                   | <span data-ttu-id="d4622-464">None</span><span class="sxs-lookup"><span data-stu-id="d4622-464">None</span></span>                 |
| <span data-ttu-id="d4622-465">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="d4622-465">Cohabiting</span></span>             | <span data-ttu-id="d4622-466">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="d4622-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d4622-467">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="d4622-467">Gender</span></span>

<span data-ttu-id="d4622-468">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="d4622-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4622-469">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4622-470">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-470">Talent</span></span>       | <span data-ttu-id="d4622-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d4622-472">Mies</span><span class="sxs-lookup"><span data-stu-id="d4622-472">Male</span></span>         | <span data-ttu-id="d4622-473">Mies</span><span class="sxs-lookup"><span data-stu-id="d4622-473">Male</span></span>            |
| <span data-ttu-id="d4622-474">Nainen</span><span class="sxs-lookup"><span data-stu-id="d4622-474">Female</span></span>       | <span data-ttu-id="d4622-475">Nainen</span><span class="sxs-lookup"><span data-stu-id="d4622-475">Female</span></span>          |
| <span data-ttu-id="d4622-476">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="d4622-476">Non-specific</span></span> | <span data-ttu-id="d4622-477">*Ei tueta*</span><span class="sxs-lookup"><span data-stu-id="d4622-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d4622-478">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-478">Earning codes</span></span>

<span data-ttu-id="d4622-479">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="d4622-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d4622-480">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="d4622-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d4622-481">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="d4622-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d4622-482">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="d4622-482">Supported frequencies</span></span>

- <span data-ttu-id="d4622-483">Kaikki</span><span class="sxs-lookup"><span data-stu-id="d4622-483">All</span></span>
- <span data-ttu-id="d4622-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d4622-484">EVERYPAY</span></span>
- <span data-ttu-id="d4622-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d4622-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d4622-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d4622-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d4622-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d4622-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d4622-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-488">1OFMTH</span></span>
- <span data-ttu-id="d4622-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-489">LASTOFMTH</span></span>
- <span data-ttu-id="d4622-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-490">2OFMTH</span></span>
- <span data-ttu-id="d4622-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-491">3OFMTH</span></span>
- <span data-ttu-id="d4622-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-492">4OFMTH</span></span>
- <span data-ttu-id="d4622-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-493">5OFMTH</span></span>
- <span data-ttu-id="d4622-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-494">1N2OFMTH</span></span>
- <span data-ttu-id="d4622-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-495">3N4OFMTH</span></span>
- <span data-ttu-id="d4622-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-496">1N3OFMTH</span></span>
- <span data-ttu-id="d4622-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-497">1N4OFMTH</span></span>
- <span data-ttu-id="d4622-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-498">2N3OFMTH</span></span>
- <span data-ttu-id="d4622-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-499">2N4OFMTH</span></span>
- <span data-ttu-id="d4622-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="d4622-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="d4622-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="d4622-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="d4622-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d4622-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d4622-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d4622-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d4622-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d4622-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4622-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d4622-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4622-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d4622-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4622-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d4622-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4622-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d4622-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4622-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d4622-512">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="d4622-512">Addresses</span></span>

<span data-ttu-id="d4622-513">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d4622-514">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="d4622-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d4622-515">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-515">Talent</span></span>          | <span data-ttu-id="d4622-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d4622-517">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="d4622-517">Country/Region</span></span>  | <span data-ttu-id="d4622-518">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-518">Country Code</span></span>          |
| <span data-ttu-id="d4622-519">Postinumero</span><span class="sxs-lookup"><span data-stu-id="d4622-519">Zip/Postal Code</span></span> | <span data-ttu-id="d4622-520">Postinumero</span><span class="sxs-lookup"><span data-stu-id="d4622-520">Postal Code</span></span>           |
| <span data-ttu-id="d4622-521">Alue</span><span class="sxs-lookup"><span data-stu-id="d4622-521">State</span></span>           | <span data-ttu-id="d4622-522">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-522">State Code</span></span>            |
| <span data-ttu-id="d4622-523">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="d4622-523">City</span></span>            | <span data-ttu-id="d4622-524">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="d4622-524">City</span></span>                  |
| <span data-ttu-id="d4622-525">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="d4622-525">County</span></span>          | <span data-ttu-id="d4622-526">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="d4622-526">County (Municipality)</span></span> |
| <span data-ttu-id="d4622-527">Katu</span><span class="sxs-lookup"><span data-stu-id="d4622-527">Street</span></span>          | <span data-ttu-id="d4622-528">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="d4622-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d4622-529">Verotusalueet</span><span class="sxs-lookup"><span data-stu-id="d4622-529">Tax regions</span></span>

<span data-ttu-id="d4622-530">Verotusalueita käytetään palkanlaskennan muodostamisessa käytettävän veron määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="d4622-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d4622-531">ALV-alueet yhdistetään Dayforceen toimipaikan osoitteina.</span><span class="sxs-lookup"><span data-stu-id="d4622-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d4622-532">Oletusarvoinen verotusalue on liitettävä työntekijän aktiiviseen toimeen.</span><span class="sxs-lookup"><span data-stu-id="d4622-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d4622-533">Verotusalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-533">Tax region (required)</span></span>
- <span data-ttu-id="d4622-534">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-534">Country/Region (required)</span></span>
- <span data-ttu-id="d4622-535">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-535">State (required)</span></span>
- <span data-ttu-id="d4622-536">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="d4622-536">County</span></span> 
- <span data-ttu-id="d4622-537">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="d4622-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d4622-538">Määritä tietosi tuottaaksesi palkkalistoja Meksikossa</span><span class="sxs-lookup"><span data-stu-id="d4622-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d4622-539">Jos luot maksuja työntekijöille, jotka ovat Meksikossa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="d4622-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d4622-540">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="d4622-540">Departments are required on positions.</span></span>
- <span data-ttu-id="d4622-541">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="d4622-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d4622-542">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="d4622-542">Job types</span></span>

<span data-ttu-id="d4622-543">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="d4622-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d4622-544">Työlajit ovat pakollisia palkkalistojen käsittelemiseen Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="d4622-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d4622-545">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="d4622-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d4622-546">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="d4622-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d4622-547">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="d4622-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d4622-548">Työlaji</span><span class="sxs-lookup"><span data-stu-id="d4622-548">Job type</span></span>   | <span data-ttu-id="d4622-549">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d4622-550">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="d4622-550">Hourly</span></span>     | <span data-ttu-id="d4622-551">MX tunneittain</span><span class="sxs-lookup"><span data-stu-id="d4622-551">MX Hourly</span></span>   |
| <span data-ttu-id="d4622-552">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="d4622-552">Salaried</span></span>   | <span data-ttu-id="d4622-553">MX kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="d4622-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d4622-554">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="d4622-554">Position types</span></span> 

<span data-ttu-id="d4622-555">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="d4622-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d4622-556">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="d4622-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d4622-557">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="d4622-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d4622-558">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="d4622-558">Position type</span></span>   | <span data-ttu-id="d4622-559">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d4622-560">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="d4622-560">Full-time</span></span>       | <span data-ttu-id="d4622-561">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-561">Full time employee</span></span> |
| <span data-ttu-id="d4622-562">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="d4622-562">Part-time</span></span>       | <span data-ttu-id="d4622-563">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d4622-564">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-564">Reason codes</span></span>

<span data-ttu-id="d4622-565">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="d4622-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d4622-566">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="d4622-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d4622-567">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="d4622-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d4622-568">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-568">Reason code</span></span>            | <span data-ttu-id="d4622-569">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-569">Description</span></span>                    | <span data-ttu-id="d4622-570">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="d4622-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d4622-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="d4622-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d4622-572">Lähtö ennen ensimmäistä palkanlaskentaa</span><span class="sxs-lookup"><span data-stu-id="d4622-572">Departure before first payroll</span></span> | <span data-ttu-id="d4622-573">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-573">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-574">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="d4622-574">RESIGNATION</span></span>            | <span data-ttu-id="d4622-575">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="d4622-575">Resignation</span></span>                    | <span data-ttu-id="d4622-576">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-576">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-577">ELÄKE</span><span class="sxs-lookup"><span data-stu-id="d4622-577">PENSION</span></span>                | <span data-ttu-id="d4622-578">Eläke</span><span class="sxs-lookup"><span data-stu-id="d4622-578">Pension</span></span>                        | <span data-ttu-id="d4622-579">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-579">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-580">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="d4622-580">TERMINATION</span></span>            | <span data-ttu-id="d4622-581">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="d4622-581">Termination</span></span>                    | <span data-ttu-id="d4622-582">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-582">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-583">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="d4622-583">RETIREMENT</span></span>             | <span data-ttu-id="d4622-584">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="d4622-584">Retirement</span></span>                     | <span data-ttu-id="d4622-585">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-585">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="d4622-586">ABSENTEE</span></span>               | <span data-ttu-id="d4622-587">Absentee</span><span class="sxs-lookup"><span data-stu-id="d4622-587">Absentee</span></span>                       | <span data-ttu-id="d4622-588">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-588">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-589">MUU</span><span class="sxs-lookup"><span data-stu-id="d4622-589">OTHER</span></span>                  | <span data-ttu-id="d4622-590">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="d4622-590">Other Reasons</span></span>                  | <span data-ttu-id="d4622-591">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-591">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-592">SULKEMINEN</span><span class="sxs-lookup"><span data-stu-id="d4622-592">CLOSURE</span></span>                | <span data-ttu-id="d4622-593">Liiketoiminnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="d4622-593">Business Closure</span></span>               | <span data-ttu-id="d4622-594">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-594">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-595">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="d4622-595">DEATH</span></span>                  | <span data-ttu-id="d4622-596">Kuolema</span><span class="sxs-lookup"><span data-stu-id="d4622-596">Death</span></span>                          | <span data-ttu-id="d4622-597">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-597">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d4622-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d4622-599">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="d4622-599">Leave of Absence</span></span>               | <span data-ttu-id="d4622-600">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-600">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d4622-601">CONTRACTEND</span></span>            | <span data-ttu-id="d4622-602">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="d4622-602">End of Contract</span></span>                | <span data-ttu-id="d4622-603">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="d4622-603">Terminate worker</span></span>     |
| <span data-ttu-id="d4622-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d4622-604">SALARYCHANGE</span></span>           | <span data-ttu-id="d4622-605">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="d4622-605">Change of Salary</span></span>               | <span data-ttu-id="d4622-606">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="d4622-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d4622-607">Työehdot</span><span class="sxs-lookup"><span data-stu-id="d4622-607">Terms of employment</span></span>

<span data-ttu-id="d4622-608">Työehtoja voidaan käyttää, kun luodaan työehtoluokkia.</span><span class="sxs-lookup"><span data-stu-id="d4622-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d4622-609">Ehdot määritetään Dayforceen työsuhteen mittarin arvoina.</span><span class="sxs-lookup"><span data-stu-id="d4622-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d4622-610">Seuraavat työsuhteen ja kuvaukset termit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="d4622-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d4622-611">Työehdot</span><span class="sxs-lookup"><span data-stu-id="d4622-611">Terms of employment</span></span>   | <span data-ttu-id="d4622-612">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d4622-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d4622-613">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="d4622-613">Regular</span></span>               | <span data-ttu-id="d4622-614">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="d4622-614">Regular</span></span>     |
| <span data-ttu-id="d4622-615">Suora</span><span class="sxs-lookup"><span data-stu-id="d4622-615">Direct</span></span>                | <span data-ttu-id="d4622-616">Suora</span><span class="sxs-lookup"><span data-stu-id="d4622-616">Direct</span></span>      |
| <span data-ttu-id="d4622-617">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="d4622-617">Internship</span></span>            | <span data-ttu-id="d4622-618">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="d4622-618">Internship</span></span>  |
| <span data-ttu-id="d4622-619">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="d4622-619">Permanent</span></span>             | <span data-ttu-id="d4622-620">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="d4622-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d4622-621">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="d4622-621">Marital status</span></span>

<span data-ttu-id="d4622-622">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="d4622-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4622-623">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4622-624">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-624">Talent</span></span>                 | <span data-ttu-id="d4622-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d4622-626">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="d4622-626">Married</span></span>                | <span data-ttu-id="d4622-627">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="d4622-627">Married</span></span>                   |
| <span data-ttu-id="d4622-628">Yksi</span><span class="sxs-lookup"><span data-stu-id="d4622-628">Single</span></span>                 | <span data-ttu-id="d4622-629">Yksi</span><span class="sxs-lookup"><span data-stu-id="d4622-629">Single</span></span>                    |
| <span data-ttu-id="d4622-630">Leski</span><span class="sxs-lookup"><span data-stu-id="d4622-630">Widowed</span></span>                | <span data-ttu-id="d4622-631">Leski</span><span class="sxs-lookup"><span data-stu-id="d4622-631">Widowed</span></span>                   |
| <span data-ttu-id="d4622-632">Eronnut</span><span class="sxs-lookup"><span data-stu-id="d4622-632">Divorced</span></span>               | <span data-ttu-id="d4622-633">Eronnut</span><span class="sxs-lookup"><span data-stu-id="d4622-633">Divorced</span></span>                  |
| <span data-ttu-id="d4622-634">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="d4622-634">Registered Partnership</span></span> | <span data-ttu-id="d4622-635">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="d4622-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="d4622-636">None</span><span class="sxs-lookup"><span data-stu-id="d4622-636">None</span></span>                   | <span data-ttu-id="d4622-637">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4622-638">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="d4622-638">Cohabiting</span></span>             | <span data-ttu-id="d4622-639">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d4622-640">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="d4622-640">Gender</span></span>

<span data-ttu-id="d4622-641">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="d4622-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4622-642">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4622-643">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-643">Talent</span></span>       | <span data-ttu-id="d4622-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d4622-645">Mies</span><span class="sxs-lookup"><span data-stu-id="d4622-645">Male</span></span>         | <span data-ttu-id="d4622-646">Mies</span><span class="sxs-lookup"><span data-stu-id="d4622-646">Male</span></span>                      |
| <span data-ttu-id="d4622-647">Nainen</span><span class="sxs-lookup"><span data-stu-id="d4622-647">Female</span></span>       | <span data-ttu-id="d4622-648">Nainen</span><span class="sxs-lookup"><span data-stu-id="d4622-648">Female</span></span>                    |
| <span data-ttu-id="d4622-649">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="d4622-649">Non-specific</span></span> | <span data-ttu-id="d4622-650">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d4622-651">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="d4622-651">Payment method</span></span>

<span data-ttu-id="d4622-652">Maksutavat antavat työntekijälle ja yritykselle keinon kuvata, miten työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d4622-653">Maksutavat on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="d4622-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d4622-654">Seuraavassa taulukossa kuvataan, miten maksutavat liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d4622-655">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-655">Talent</span></span>             | <span data-ttu-id="d4622-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d4622-657">Maksu</span><span class="sxs-lookup"><span data-stu-id="d4622-657">Cash</span></span>               | <span data-ttu-id="d4622-658">Maksu</span><span class="sxs-lookup"><span data-stu-id="d4622-658">Cash</span></span>                      |
| <span data-ttu-id="d4622-659">Sähköinen maksu</span><span class="sxs-lookup"><span data-stu-id="d4622-659">Electronic Payment</span></span> | <span data-ttu-id="d4622-660">Tapahtumien siirto</span><span class="sxs-lookup"><span data-stu-id="d4622-660">Transfer</span></span>                  |
| <span data-ttu-id="d4622-661">Tarkistus</span><span class="sxs-lookup"><span data-stu-id="d4622-661">Check</span></span>              | <span data-ttu-id="d4622-662">Sekki</span><span class="sxs-lookup"><span data-stu-id="d4622-662">Cheque</span></span>                    |
| <span data-ttu-id="d4622-663">Pankkivekseli</span><span class="sxs-lookup"><span data-stu-id="d4622-663">Bank Draft</span></span>         | <span data-ttu-id="d4622-664">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4622-665">Muu</span><span class="sxs-lookup"><span data-stu-id="d4622-665">Other</span></span>              | <span data-ttu-id="d4622-666">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d4622-667">Pankkitilin tyyppi</span><span class="sxs-lookup"><span data-stu-id="d4622-667">Bank account type</span></span>

<span data-ttu-id="d4622-668">Pankkitilin tyyppejä käytetään sähköisissä maksuissa työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="d4622-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d4622-669">Pankin tilityypit yhdistetään Dayforceen tilinsiirtämisen tietoina.</span><span class="sxs-lookup"><span data-stu-id="d4622-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d4622-670">Pankkitilin tyypit ovat tarvittaessa käännettyjä ja hyväksytty arvoiksi sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d4622-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d4622-671">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-671">Talent</span></span>            | <span data-ttu-id="d4622-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d4622-673">Käyttötili</span><span class="sxs-lookup"><span data-stu-id="d4622-673">Checking Account</span></span>  | <span data-ttu-id="d4622-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="d4622-674">CheckingAccount</span></span>           |
| <span data-ttu-id="d4622-675">Palkanlaskennan tili</span><span class="sxs-lookup"><span data-stu-id="d4622-675">Payroll Account</span></span>   | <span data-ttu-id="d4622-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="d4622-676">PayrollAccount</span></span>            |
| <span data-ttu-id="d4622-677">Säästötili</span><span class="sxs-lookup"><span data-stu-id="d4622-677">Savings Account</span></span>   | <span data-ttu-id="d4622-678">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4622-679">BankGirot-tili</span><span class="sxs-lookup"><span data-stu-id="d4622-679">BankGirot account</span></span> | <span data-ttu-id="d4622-680">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d4622-681">PlusGirot-tili</span><span class="sxs-lookup"><span data-stu-id="d4622-681">PlusGirot account</span></span> | <span data-ttu-id="d4622-682">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="d4622-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d4622-683">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="d4622-683">Earning codes</span></span>

<span data-ttu-id="d4622-684">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="d4622-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d4622-685">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="d4622-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d4622-686">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="d4622-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d4622-687">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="d4622-687">Supported frequencies</span></span>

- <span data-ttu-id="d4622-688">Kaikki</span><span class="sxs-lookup"><span data-stu-id="d4622-688">All</span></span>
- <span data-ttu-id="d4622-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d4622-689">EVERYPAY</span></span>
- <span data-ttu-id="d4622-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d4622-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d4622-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d4622-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d4622-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d4622-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d4622-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-693">1OFMTH</span></span>
- <span data-ttu-id="d4622-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-694">LASTOFMTH</span></span>
- <span data-ttu-id="d4622-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-695">2OFMTH</span></span>
- <span data-ttu-id="d4622-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-696">3OFMTH</span></span>
- <span data-ttu-id="d4622-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-697">4OFMTH</span></span>
- <span data-ttu-id="d4622-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-698">5OFMTH</span></span>
- <span data-ttu-id="d4622-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-699">1N2OFMTH</span></span>
- <span data-ttu-id="d4622-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-700">3N4OFMTH</span></span>
- <span data-ttu-id="d4622-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-701">1N3OFMTH</span></span>
- <span data-ttu-id="d4622-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-702">1N4OFMTH</span></span>
- <span data-ttu-id="d4622-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-703">2N3OFMTH</span></span>
- <span data-ttu-id="d4622-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-704">2N4OFMTH</span></span>
- <span data-ttu-id="d4622-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="d4622-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="d4622-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="d4622-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="d4622-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d4622-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d4622-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d4622-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d4622-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d4622-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d4622-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4622-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d4622-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d4622-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d4622-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4622-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d4622-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4622-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d4622-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d4622-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d4622-717">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="d4622-717">Addresses</span></span>

<span data-ttu-id="d4622-718">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="d4622-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d4622-719">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="d4622-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d4622-720">Talent</span><span class="sxs-lookup"><span data-stu-id="d4622-720">Talent</span></span>              | <span data-ttu-id="d4622-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d4622-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d4622-722">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="d4622-722">Country/Region</span></span>      | <span data-ttu-id="d4622-723">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-723">Country Code</span></span>          |
| <span data-ttu-id="d4622-724">Postinumero</span><span class="sxs-lookup"><span data-stu-id="d4622-724">Zip/Postal Code</span></span>     | <span data-ttu-id="d4622-725">Postinumero</span><span class="sxs-lookup"><span data-stu-id="d4622-725">Postal Code</span></span>           |
| <span data-ttu-id="d4622-726">Alue</span><span class="sxs-lookup"><span data-stu-id="d4622-726">State</span></span>               | <span data-ttu-id="d4622-727">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="d4622-727">State Code</span></span>            |
| <span data-ttu-id="d4622-728">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="d4622-728">City</span></span>                | <span data-ttu-id="d4622-729">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="d4622-729">City</span></span>                  |
| <span data-ttu-id="d4622-730">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="d4622-730">County</span></span>              | <span data-ttu-id="d4622-731">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="d4622-731">County (Municipality)</span></span> |
| <span data-ttu-id="d4622-732">Katu</span><span class="sxs-lookup"><span data-stu-id="d4622-732">Street</span></span>              | <span data-ttu-id="d4622-733">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="d4622-733">Address Line 1</span></span>        |
| <span data-ttu-id="d4622-734">Kadunnumero</span><span class="sxs-lookup"><span data-stu-id="d4622-734">Street Number</span></span>       | <span data-ttu-id="d4622-735">Osoiterivi 2</span><span class="sxs-lookup"><span data-stu-id="d4622-735">Address Line 2</span></span>        |
| <span data-ttu-id="d4622-736">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="d4622-736">Building Complement</span></span> | <span data-ttu-id="d4622-737">Osoiterivi 5</span><span class="sxs-lookup"><span data-stu-id="d4622-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d4622-738">Passin numero</span><span class="sxs-lookup"><span data-stu-id="d4622-738">Passport number</span></span>

<span data-ttu-id="d4622-739">Työntekijät voivat ilmoittaa passin tiedot.</span><span class="sxs-lookup"><span data-stu-id="d4622-739">Employees can declare passport information.</span></span> <span data-ttu-id="d4622-740">Tämä tietoa on **Passi**-tunnustyyppiä ja se on integroitu Dayforceen osaksi työntekijän Meksikon liittyvää tietoa.</span><span class="sxs-lookup"><span data-stu-id="d4622-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d4622-741">Tunnustyyppi = "Passi"</span><span class="sxs-lookup"><span data-stu-id="d4622-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d4622-742">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="d4622-742">Issued Date</span></span>
- <span data-ttu-id="d4622-743">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="d4622-743">Expiration Date</span></span>

<span data-ttu-id="d4622-744">Työntekijät voi määrittää useita tunnistenumeroita **Passi**-tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="d4622-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d4622-745">Vain nykyiset aktiiviset passitapahtumat integroidaan Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d4622-746">Mikäli kaikki passitapahtumat ovat vanhentuneet, passi, joka on viimeksi myönnetty on integroitu Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="d4622-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
