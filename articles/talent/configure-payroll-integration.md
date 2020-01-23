---
title: Palkanlaskennan Talent and Dayforce -integroinnin määrittäminen
description: Tässä ohjeaiheessa kerrotaan, että kuinka konfiguroida integrointeja Microsoft Dynamics 365 Talentin ja Ceridian Dayforcen välillä voidaksesi käsitellä palkka-ajoa.
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
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898528"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="600da-103">Talentin ja Dayforcen välisen palkanlaskennan integroinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="600da-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="600da-104">Microsoft Dynamics 365 Talentin ja Ceridian Dayforcen välinen integrointi käyttää useita konfiguraation vaiheita, jotka on kuvattu tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="600da-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="600da-105">Sekä Talentin että Dayforcen integrointi on määritettävä ennen kuin voit käsitellä palkka-ajoa.</span><span class="sxs-lookup"><span data-stu-id="600da-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="600da-106">Käytettäessä jotakin palvelua, kuten Dayforcea palkka-ajojen suorittamiseen, on otettava käyttöön integrointi Talentissa.</span><span class="sxs-lookup"><span data-stu-id="600da-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="600da-107">Integrointi edellyttää tiettyjä tietoja Talentista.</span><span class="sxs-lookup"><span data-stu-id="600da-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="600da-108">Sinun on varmistettava, että Dayforceen yhdistetyt tiedot on konfiguroitu Talentissa siten, että ne tukevat integrointia.</span><span class="sxs-lookup"><span data-stu-id="600da-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="600da-109">Integraatio käyttää seuraavanlaisia laajoja tietoryhmiä:</span><span class="sxs-lookup"><span data-stu-id="600da-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="600da-110">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="600da-110">Human resources data</span></span>
- <span data-ttu-id="600da-111">Kompensaatiotiedot</span><span class="sxs-lookup"><span data-stu-id="600da-111">Compensation data</span></span>
- <span data-ttu-id="600da-112">Palkanlaskentatietoja, kuten maksujaksot, maksukaudet ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="600da-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="600da-113">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="600da-113">Worker data</span></span>

<span data-ttu-id="600da-114">Tässä ohjeaiheessa kuvataan vaiheita, joita sinun on noudatettava ottaaksesi integroinnin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="600da-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="600da-115">Lisäksi kerrotaan minkä tyyppisiä tietoja ja konfigurointitietoja integrointi edellyttää.</span><span class="sxs-lookup"><span data-stu-id="600da-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="600da-116">Ota integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="600da-116">Enable the integration</span></span>

<span data-ttu-id="600da-117">Ota integraatio käyttöön Talentissa ja lisää konfiguraatiotiedot muodostaaksesi yhteyden Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="600da-118">Mikäli haluat kirjanpitotapahtuman, joka valmistetaan ja tuodaan Microsoft Dynamics 365 Financeen, sinun on määritettävä myös Microsoft Azure -tallennustili ja kirjoitettava Azure-tallennuksen yhteyden muodostuskomento Financeen.</span><span class="sxs-lookup"><span data-stu-id="600da-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="600da-119">Ota integrointi käyttöön Talentissa seuraavien vaiheiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="600da-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="600da-120">Valitse **Järjestelmänvalvoja**-sivulla **konfiguroinnin integrointi**.</span><span class="sxs-lookup"><span data-stu-id="600da-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="600da-121">Lisää File Transfer Protocol (FTP) -päätepiste ja suojattu FTP-kansiopolku.</span><span class="sxs-lookup"><span data-stu-id="600da-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="600da-122">Kirjoita sen käyttäjän käyttäjänimi ja salasana, joka voi käyttää suojattua FTP-päätepistettä ja kansiopolkua.</span><span class="sxs-lookup"><span data-stu-id="600da-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="600da-123">Testaa yhteys kuten vaadittu ja määritä **Ota käyttöön palkanmaksun integrointi** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="600da-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="600da-124">Kun integrointi otetaan käyttöön, tietojen viennin paketti ja tiedostot luodaan ja taajuus määritetään.</span><span class="sxs-lookup"><span data-stu-id="600da-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="600da-125">Voit muuttaa tätä taajuutta tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="600da-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="600da-126">Lisätietoja Azure-tallennustilien ja Azure-tallennusyhteyden yhteysmerkkijonoista seuraavissa Azure-aiheissa:</span><span class="sxs-lookup"><span data-stu-id="600da-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="600da-127">Lisätietoja Azure-tallennustileistä</span><span class="sxs-lookup"><span data-stu-id="600da-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="600da-128">Määritä Azure-tallennustilan yhteysmerkkijonot</span><span class="sxs-lookup"><span data-stu-id="600da-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="600da-129">Tekniset tiedot, kun palkanlaskennan integrointi on otettu käyttöön</span><span class="sxs-lookup"><span data-stu-id="600da-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="600da-130">Palkanlaskennan integroinnin käytöstäpoistamisella on kaksi pääasiallista vaikutusta:</span><span class="sxs-lookup"><span data-stu-id="600da-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="600da-131">Palkanlaskennan integroinnin vienti -niminen tietojen vientiprojekti luodaan.</span><span class="sxs-lookup"><span data-stu-id="600da-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="600da-132">Tämä projekti sisältää palkanhallinnan integrointiin tarvittavat yksiköt ja kentät.</span><span class="sxs-lookup"><span data-stu-id="600da-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="600da-133">Voit tutustua projektiin valitsemalla ensin **Järjestelmän hallinta**, sitten **Tietojen hallinta** -ruudun ja avaamalla lopuksi tietoprojektin projektiluettelosta.</span><span class="sxs-lookup"><span data-stu-id="600da-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="600da-134">Tämä erätyö suorittaa tietojen vientiprojektin, salaa tuloksena olevan tietopaketin ja siirtää tietopakettitiedoston SFTP-päätepisteeseen, joka on määritetty **Integroinnin määritys** -näytössä.</span><span class="sxs-lookup"><span data-stu-id="600da-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="600da-135">SFTP-päätepisteeseen siirretty tietopaketti salataan paketin yksilöllisellä avaimella.</span><span class="sxs-lookup"><span data-stu-id="600da-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="600da-136">Avain on Azure Key Vaultissa, jota vain Ceridian voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="600da-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="600da-137">Tietopaketin sisällön salausta ei voi purkaa eikä sisältöä tutkia.</span><span class="sxs-lookup"><span data-stu-id="600da-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="600da-138">Jos tietopaketin sisältöä on tarkasteltava, Palkanlaskennan integroinnin vienti -tietoprojekti on vietävä manuaalisesti, jonka jälkeen on ladattava ja avattava.</span><span class="sxs-lookup"><span data-stu-id="600da-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="600da-139">Manuaalisessa viennissä ei käytetä salausta eikä pakettia siirretä.</span><span class="sxs-lookup"><span data-stu-id="600da-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="600da-140">Määritä tietosi</span><span class="sxs-lookup"><span data-stu-id="600da-140">Configure your data</span></span> 

<span data-ttu-id="600da-141">Voidaksesi käsitellä palkanlaskentaa, sinun on määritettävä henkilöstöhallinnon tiedot Talentissa.</span><span class="sxs-lookup"><span data-stu-id="600da-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="600da-142">On määritettävä organisaation tiedot, kuten työt ja toimet sekä edut ja kompensaatiotiedot.</span><span class="sxs-lookup"><span data-stu-id="600da-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="600da-143">Nämä tiedot sisältävät työllisyys-, palkka- ja vähennystiedot, jotka vaaditaan, jotta voidaan luoda työntekijän palkka.</span><span class="sxs-lookup"><span data-stu-id="600da-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="600da-144">Henkilöstöhallintotiedot</span><span class="sxs-lookup"><span data-stu-id="600da-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="600da-145">Edut</span><span class="sxs-lookup"><span data-stu-id="600da-145">Benefits</span></span> 

<span data-ttu-id="600da-146">Henkilöstöhallinto sisältää työkaluja, joiden avulla organisaation tarjoamia tai työntekijöitä varten käsittelemiä etuja, vähennyksiä ja työntekijöiden kompensaatiosuunnitelmia voi määrittää ja ylläpitää.</span><span class="sxs-lookup"><span data-stu-id="600da-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="600da-147">Luodessasi etuja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="600da-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="600da-148">Etusuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="600da-148">Benefit plans</span></span>

- <span data-ttu-id="600da-149">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-149">Plan (required)</span></span>
- <span data-ttu-id="600da-150">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-150">Type (required)</span></span>
- <span data-ttu-id="600da-151">Palkanlaskennan vaikutus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-151">Payroll impact (required)</span></span>
- <span data-ttu-id="600da-152">Palauta velvoitteet</span><span class="sxs-lookup"><span data-stu-id="600da-152">Recover arrears</span></span>
- <span data-ttu-id="600da-153">Vähennysmenetelmä</span><span class="sxs-lookup"><span data-stu-id="600da-153">Deduction method</span></span>
- <span data-ttu-id="600da-154">Vähennyksen prioriteetti</span><span class="sxs-lookup"><span data-stu-id="600da-154">Deduction priority</span></span>
- <span data-ttu-id="600da-155">Rajaa kausi</span><span class="sxs-lookup"><span data-stu-id="600da-155">Limit period</span></span>
- <span data-ttu-id="600da-156">Rajasumma</span><span class="sxs-lookup"><span data-stu-id="600da-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="600da-157">Edut</span><span class="sxs-lookup"><span data-stu-id="600da-157">Benefits</span></span>

- <span data-ttu-id="600da-158">Suunnitelma (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-158">Plan (required)</span></span>
- <span data-ttu-id="600da-159">Tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-159">Type (required)</span></span>
- <span data-ttu-id="600da-160">Vaihtoehto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-160">Option (required)</span></span>
- <span data-ttu-id="600da-161">Edun tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-161">Benefit ID (required)</span></span>
- <span data-ttu-id="600da-162">Tiheys</span><span class="sxs-lookup"><span data-stu-id="600da-162">Frequency</span></span>
- <span data-ttu-id="600da-163">Peruste</span><span class="sxs-lookup"><span data-stu-id="600da-163">Basis</span></span>
- <span data-ttu-id="600da-164">Summa tai hinta</span><span class="sxs-lookup"><span data-stu-id="600da-164">Amount or rate</span></span>
- <span data-ttu-id="600da-165">Ansiokoodi</span><span class="sxs-lookup"><span data-stu-id="600da-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="600da-166">Tuetut maksutiheydet</span><span class="sxs-lookup"><span data-stu-id="600da-166">Supported frequencies</span></span> 

- <span data-ttu-id="600da-167">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="600da-167">Weekly</span></span>
- <span data-ttu-id="600da-168">Kahden viikon välein</span><span class="sxs-lookup"><span data-stu-id="600da-168">Bi-weekly</span></span>
- <span data-ttu-id="600da-169">Joka toinen kuukausi</span><span class="sxs-lookup"><span data-stu-id="600da-169">Semi-monthly</span></span>
- <span data-ttu-id="600da-170">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="600da-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="600da-171">Tuetut pohjat</span><span class="sxs-lookup"><span data-stu-id="600da-171">Supported bases</span></span> 

- <span data-ttu-id="600da-172">Kiinteä summa</span><span class="sxs-lookup"><span data-stu-id="600da-172">Fixed amount</span></span>
- <span data-ttu-id="600da-173">Ansioiden prosenttiosuus</span><span class="sxs-lookup"><span data-stu-id="600da-173">Percent of earnings</span></span>
- <span data-ttu-id="600da-174">Tuottavat tunnit</span><span class="sxs-lookup"><span data-stu-id="600da-174">Productive hours</span></span>

<span data-ttu-id="600da-175">Dayforce luo seuraavat vähennykset, jotka perustuvat palkanlaskennan vaikutukseen, joka on määritelty etusuunnitelmassa.</span><span class="sxs-lookup"><span data-stu-id="600da-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="600da-176">Talentin valinta</span><span class="sxs-lookup"><span data-stu-id="600da-176">Selection in Talent</span></span>        | <span data-ttu-id="600da-177">Tulos Dayforcessa</span><span class="sxs-lookup"><span data-stu-id="600da-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="600da-178">None</span><span class="sxs-lookup"><span data-stu-id="600da-178">None</span></span>                       | <span data-ttu-id="600da-179">Vähennyksiä ei luoda.</span><span class="sxs-lookup"><span data-stu-id="600da-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="600da-180">Vain vähennys</span><span class="sxs-lookup"><span data-stu-id="600da-180">Deduction only</span></span>             | <span data-ttu-id="600da-181">Työntekijävähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="600da-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="600da-182">Vain osuus</span><span class="sxs-lookup"><span data-stu-id="600da-182">Contribution only</span></span>          | <span data-ttu-id="600da-183">Työnantajavähennys on luotu.</span><span class="sxs-lookup"><span data-stu-id="600da-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="600da-184">Vähennys ja osuus</span><span class="sxs-lookup"><span data-stu-id="600da-184">Deduction and contribution</span></span> | <span data-ttu-id="600da-185">Työntekijän ja työnantajan vähennykset luodaan.</span><span class="sxs-lookup"><span data-stu-id="600da-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="600da-186">Lisätietoja etuohjelman määrittämisestä ja hallitsemisesta seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="600da-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="600da-187">Työsuhde-etuohjelman toteuttaminen</span><span class="sxs-lookup"><span data-stu-id="600da-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="600da-188">Luo uusi etu</span><span class="sxs-lookup"><span data-stu-id="600da-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="600da-189">Määritä edun oikeutussäännöt ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="600da-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="600da-190">Rekisteröi etuja työntekijöille ja poista niitä</span><span class="sxs-lookup"><span data-stu-id="600da-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="600da-191">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="600da-191">Compensation</span></span> 

<span data-ttu-id="600da-192">Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista.</span><span class="sxs-lookup"><span data-stu-id="600da-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="600da-193">Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="600da-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="600da-194">Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="600da-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="600da-195">Dayforce käyttää kompensaatiotietoja laskeakseen työntekijän tunti- tai vuosihinnan.</span><span class="sxs-lookup"><span data-stu-id="600da-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="600da-196">Kiinteät kompensaatiosuunnitelmat ja palkkojen muunnokset vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="600da-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="600da-197">Työntekijöiden täytyy olla liitettynä kiinteään kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="600da-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="600da-198">Katso lisätietoja kompensaatiosuunnitelmista seuraavista ohjeaiheista:</span><span class="sxs-lookup"><span data-stu-id="600da-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="600da-199">Kiinteiden kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="600da-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="600da-200">Muuttuvien kompensaatiosuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="600da-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="600da-201">Palkka- ja kompensaatiorakenteen ja -suunnitelmien kehittäminen</span><span class="sxs-lookup"><span data-stu-id="600da-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="600da-202">Kompensaation käsittely</span><span class="sxs-lookup"><span data-stu-id="600da-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="600da-203">Kompensaatioprosessin määrittäminen ja tulosten laskeminen</span><span class="sxs-lookup"><span data-stu-id="600da-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="600da-204">Työntekijän rekisteröiminen kiinteän kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="600da-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="600da-205">Työntekijän rekisteröiminen muuttuvan kompensaation suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="600da-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="600da-206">Työt</span><span class="sxs-lookup"><span data-stu-id="600da-206">Jobs</span></span> 

<span data-ttu-id="600da-207">Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään.</span><span class="sxs-lookup"><span data-stu-id="600da-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="600da-208">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="600da-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="600da-209">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="600da-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="600da-210">Määritä uudet työt</span><span class="sxs-lookup"><span data-stu-id="600da-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="600da-211">Toimet</span><span class="sxs-lookup"><span data-stu-id="600da-211">Positions</span></span>

<span data-ttu-id="600da-212">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="600da-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="600da-213">Esimerkiksi toimi Myyntipäällikkö (Itä) on yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="600da-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="600da-214">Osastolla on toimi.</span><span class="sxs-lookup"><span data-stu-id="600da-214">A position exists in a department.</span></span> <span data-ttu-id="600da-215">Vain yksi työntekijä voidaan liittää yhteen toimeen.</span><span class="sxs-lookup"><span data-stu-id="600da-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="600da-216">Muista seuraavat tiedot ja määritykset, kun määrität toimia:</span><span class="sxs-lookup"><span data-stu-id="600da-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="600da-217">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-217">Position (required)</span></span>
- <span data-ttu-id="600da-218">Kuvaus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-218">Description (required)</span></span>
- <span data-ttu-id="600da-219">Työ (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-219">Job (required)</span></span>
- <span data-ttu-id="600da-220">Osasto (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-220">Department (required)</span></span>
- <span data-ttu-id="600da-221">Toimen tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-221">Position type (required)</span></span>
- <span data-ttu-id="600da-222">Kokopäiväinen (FTE)</span><span class="sxs-lookup"><span data-stu-id="600da-222">Full-time equivalent</span></span>
- <span data-ttu-id="600da-223">Vuosittaiset vakiotunnit (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="600da-224">Yrityksen maksama (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="600da-225">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-225">Pay cycle (required)</span></span>
- <span data-ttu-id="600da-226">Oletusarvo taloushallinnon dimensio – kustannuspaikka (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="600da-227">Työntekijän määritys – työntekijä, tehtävän alkamisaika, tehtävän lopetusaika, syykoodi</span><span class="sxs-lookup"><span data-stu-id="600da-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="600da-228">Mikäli useita toimia samalla osastolla liittyy samaan työhön, ne yhdistetään yhteen toimeen Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="600da-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="600da-229">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="600da-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="600da-230">Työvoiman järjestäminen osastojen, töiden ja toimien avulla</span><span class="sxs-lookup"><span data-stu-id="600da-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="600da-231">Toimien määritys</span><span class="sxs-lookup"><span data-stu-id="600da-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="600da-232">Osastot</span><span class="sxs-lookup"><span data-stu-id="600da-232">Departments</span></span>

<span data-ttu-id="600da-233">Osasto on toimintayksikkö, joka vastaa organisaation luokkaa tai liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="600da-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="600da-234">Osasto on vastuussa määrätystä organisaation alueesta, kuten myynnistä, kirjanpidosta tai henkilöstöhallinnosta.</span><span class="sxs-lookup"><span data-stu-id="600da-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="600da-235">Voit käyttää osastoja toiminnallisia alueita koskevaan raportointiin.</span><span class="sxs-lookup"><span data-stu-id="600da-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="600da-236">Osastot voivat olla tulosvastuullisia.</span><span class="sxs-lookup"><span data-stu-id="600da-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="600da-237">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="600da-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="600da-238">Osaston luominen ja liittäminen osastohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="600da-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="600da-239">Määritä uudet osastot</span><span class="sxs-lookup"><span data-stu-id="600da-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="600da-240">Maksujaksot ja maksukaudet</span><span class="sxs-lookup"><span data-stu-id="600da-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="600da-241">Palkkajakso määrittää kuinka usein palkkalistoja käytetään, ja minä tiettyinä päivinä työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="600da-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="600da-242">Esimerkiksi palkkajakso voi olla kuukausittainen ja työntekijöille voidaan maksaa kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="600da-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="600da-243">Vaihtoehtoisesti palkkajakso voi olla viikoittainen ja työntekijöille voidaan maksaa tiistaina palkkajakson päätyttyä.</span><span class="sxs-lookup"><span data-stu-id="600da-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="600da-244">Palkkajaksot on osoitettu toimiin, jotta voidaan valvoa milloin näissä tehtävissä oleville työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="600da-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="600da-245">Luotuasi palkkajaksoja, voit luoda maksukausia kullekin jaksolle.</span><span class="sxs-lookup"><span data-stu-id="600da-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="600da-246">Jokaisella palkkakaudella on maksun oletuspäivämäärä, joka perustuu antamiisi tietoihin.</span><span class="sxs-lookup"><span data-stu-id="600da-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="600da-247">Voit kuitenkin muokata maksun oletuspäivämäärää salliaksesi poikkeuksia, kuten kun maksupäivämäärä osuu vapaapäivälle.</span><span class="sxs-lookup"><span data-stu-id="600da-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="600da-248">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="600da-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="600da-249">Maksujakson (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-249">Pay cycle (required)</span></span>
- <span data-ttu-id="600da-250">Maksujakson tiheys (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="600da-251">Kauden alkamispäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="600da-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="600da-252">Oletusmaksupäivä (ensimmäinen palkkakausi vaaditaan)</span><span class="sxs-lookup"><span data-stu-id="600da-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="600da-253">Nämä tiedot on integroitu Dayforce-palkkaryhmien kanssa ja eriteltynä eriteltyinä maittain tai alueittain kullekin maksujaksolle.</span><span class="sxs-lookup"><span data-stu-id="600da-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="600da-254">Ennen integraatiota on luotava vähintään yksi palkkakausi.</span><span class="sxs-lookup"><span data-stu-id="600da-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="600da-255">Dayforce luo maksuryhmäkalentereita ja maksupäiviä, jotka perustuvat ensimmäisen palkkakauden alkamispäivämäärään ja määritetty oletusmaksupäivä on asetettu Talentissa.</span><span class="sxs-lookup"><span data-stu-id="600da-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="600da-256">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="600da-256">Earning codes</span></span>

<span data-ttu-id="600da-257">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="600da-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="600da-258">Tunnuksissa on erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="600da-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="600da-259">Dayforcessa käytetään seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="600da-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="600da-260">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-260">Earning Code (required)</span></span>
- <span data-ttu-id="600da-261">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-261">Description</span></span>
- <span data-ttu-id="600da-262">Mittayksikkö</span><span class="sxs-lookup"><span data-stu-id="600da-262">Unit of measure</span></span>
- <span data-ttu-id="600da-263">Tuottava</span><span class="sxs-lookup"><span data-stu-id="600da-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="600da-264">Työntekijän tiedot</span><span class="sxs-lookup"><span data-stu-id="600da-264">Worker data</span></span>

<span data-ttu-id="600da-265">Tietueet eri työntekijöille, joita sinulla on ovat tärkeitä henkilöstöhallinnossa ja palkanlaskentajärjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="600da-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="600da-266">Tietueisiin lisättäviä tietoja käytetään työntekijöiden ja henkilökohtaisten tietojen seurannassa.</span><span class="sxs-lookup"><span data-stu-id="600da-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="600da-267">Voit ylläpitää työntekijöille seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="600da-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="600da-268">**Perustiedot** – Ylläpidä työntekijän perustietoja, kuten yhteystiedot, demografiatiedot, tunnistetiedot, perheen tiedot, asevelvollisuuden tila, ekspatriaatin tiedot ja omat yhteyshenkilöt ja hätäyhteyshenkilöt.</span><span class="sxs-lookup"><span data-stu-id="600da-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="600da-269">**Työsuhde** – Ylläpidä tietoja työntekijän työsuhteesta, kuten yrityksen tai organisaation kytköksistä, toimen määrityksestä, aloitus- ja päättymispäivämääristä, työkelpoisuudesta, työehdoista, eläkkestä, lomista ja uudelleensijoittumisesta.</span><span class="sxs-lookup"><span data-stu-id="600da-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="600da-270">**Lomat ja poissaolot** –Ylläpidä tietoa työntekijän poissaoloista, kuten työaikakalentereista, poissaolotapahtumista ja poissaoloasetuksista.</span><span class="sxs-lookup"><span data-stu-id="600da-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="600da-271">**Kompensaatio ja palkanlaskenta** – Ylläpidä työntekijän kompensaatiosuunnitelmien tietoja ja palkanlaskentatietoja, kuten suunnitelmien toteutuminen, palkkiot, suorituskyky, provisio, verotiedot, eläkkeelle jääminen ja palkan vähennykset.</span><span class="sxs-lookup"><span data-stu-id="600da-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="600da-272">Kirjoittaessasi työntekijätietoja, pidä mielessä seuraavat tiedot ja konfiguraatiot, joita käytetään Dayforcessa.</span><span class="sxs-lookup"><span data-stu-id="600da-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="600da-273">Yleistiedot</span><span class="sxs-lookup"><span data-stu-id="600da-273">General information</span></span>

- <span data-ttu-id="600da-274">Henkilönumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-274">Personnel number (required)</span></span>
- <span data-ttu-id="600da-275">Etunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-275">First name (required)</span></span>
- <span data-ttu-id="600da-276">Sukunimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-276">Last name (required)</span></span>
- <span data-ttu-id="600da-277">Toinen nimi</span><span class="sxs-lookup"><span data-stu-id="600da-277">Middle name</span></span>
- <span data-ttu-id="600da-278">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="600da-278">Seniority date</span></span>
- <span data-ttu-id="600da-279">Tunnetaan nimellä</span><span class="sxs-lookup"><span data-stu-id="600da-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="600da-280">Henkilökohtaiset tiedot</span><span class="sxs-lookup"><span data-stu-id="600da-280">Personal information</span></span>

- <span data-ttu-id="600da-281">Siviilisääty (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-281">Marital status (required)</span></span>
- <span data-ttu-id="600da-282">Syntymäpäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-282">Birth date (required)</span></span>
- <span data-ttu-id="600da-283">Sukupuoli (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-283">Gender (required)</span></span>
- <span data-ttu-id="600da-284">Henkilö on invalidi</span><span class="sxs-lookup"><span data-stu-id="600da-284">Person with disabilities</span></span>
- <span data-ttu-id="600da-285">Kansalaisuus, maa, alue (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="600da-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="600da-286">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="600da-286">Address information</span></span>

- <span data-ttu-id="600da-287">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-287">Primary (required)</span></span>
- <span data-ttu-id="600da-288">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-288">Country/region (required)</span></span>
- <span data-ttu-id="600da-289">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-289">Postal code (required)</span></span>
- <span data-ttu-id="600da-290">Kadunnumero (pakollinen) (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="600da-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="600da-291">Rakennusta koskeva lisätieto (vain Meksikossa)</span><span class="sxs-lookup"><span data-stu-id="600da-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="600da-292">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-292">City (required)</span></span>
- <span data-ttu-id="600da-293">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-293">State (required)</span></span>
- <span data-ttu-id="600da-294">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="600da-295">Yhteystiedot</span><span class="sxs-lookup"><span data-stu-id="600da-295">Contact information</span></span> 

- <span data-ttu-id="600da-296">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-296">Primary (required)</span></span>
- <span data-ttu-id="600da-297">Yhteystiedon numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-297">Contact number (required)</span></span>
- <span data-ttu-id="600da-298">Alanumero</span><span class="sxs-lookup"><span data-stu-id="600da-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="600da-299">Palkanlaskentatiedot ja ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="600da-299">Payroll information and earning codes</span></span>

<span data-ttu-id="600da-300">Työntekijöille voidaan antaa erityisiä tuloja tietyllä maksutaajuudella ja toivotulla maksutavalla.</span><span class="sxs-lookup"><span data-stu-id="600da-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="600da-301">Seuraavia kenttiä käytetään Dayforcessa sen varmistamiseksi, että näitä määrityksiä ja asetuksia käytetään.</span><span class="sxs-lookup"><span data-stu-id="600da-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="600da-302">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="600da-302">Earning codes</span></span>

- <span data-ttu-id="600da-303">Toimi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-303">Position (required)</span></span>
- <span data-ttu-id="600da-304">Ansiokoodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-304">Earning Code (required)</span></span>
- <span data-ttu-id="600da-305">Taajuus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-305">Frequency (required)</span></span>
- <span data-ttu-id="600da-306">Summa (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="600da-307">Palkanlaskentatiedot</span><span class="sxs-lookup"><span data-stu-id="600da-307">Payroll information</span></span>

- <span data-ttu-id="600da-308">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="600da-308">Payment Method</span></span>
- <span data-ttu-id="600da-309">Talousalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-309">Economic Region (required)</span></span>
- <span data-ttu-id="600da-310">Työsuhde-etujen tunnus</span><span class="sxs-lookup"><span data-stu-id="600da-310">Employee Benefits ID</span></span>
- <span data-ttu-id="600da-311">Kansallinen/alueellinen tunnusnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-311">National ID Number (required)</span></span>
- <span data-ttu-id="600da-312">Sotilaspalveluksen numero</span><span class="sxs-lookup"><span data-stu-id="600da-312">Military Service Number</span></span>
- <span data-ttu-id="600da-313">Vuoron tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-313">Shift ID (required)</span></span>
- <span data-ttu-id="600da-314">Veronumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-314">Tax Number (required)</span></span>
- <span data-ttu-id="600da-315">Ammattijärjestön tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-315">Union ID (required)</span></span>
- <span data-ttu-id="600da-316">Työpäivän tunnus (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-316">Work Day ID (required)</span></span>
- <span data-ttu-id="600da-317">Työluvan numero</span><span class="sxs-lookup"><span data-stu-id="600da-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="600da-318">Maksutavoista Meksiko tukee seuraavia: **Käteinen**, **shekki** (yrityksen fyysinen shekki) ja **sähköinen maksu**.</span><span class="sxs-lookup"><span data-stu-id="600da-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="600da-319">Mikäli maksutapaa ei ole määritetty, **shekki** on oletusarvo.</span><span class="sxs-lookup"><span data-stu-id="600da-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="600da-320">Työsuhteen tiedot</span><span class="sxs-lookup"><span data-stu-id="600da-320">Employment details</span></span>

<span data-ttu-id="600da-321">Työntekijöiden yksityiskohtaista historiaa käytetään keskeisenä informaationa, jolla saadaan työntekijän palkkaus, irtisanominen ja rekrytointitilastot Dayforcesta.</span><span class="sxs-lookup"><span data-stu-id="600da-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="600da-322">Dayforce tukee kerrallaan vain yhtä aktiivisen työntekijän tietuetta.</span><span class="sxs-lookup"><span data-stu-id="600da-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="600da-323">Työsuhteen alkamispäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-323">Employment start date (required)</span></span>
- <span data-ttu-id="600da-324">Työsuhteen päättymispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-324">Employment end date</span></span>
- <span data-ttu-id="600da-325">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-325">Start date</span></span>
- <span data-ttu-id="600da-326">Muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-326">Adjusted start date</span></span>
- <span data-ttu-id="600da-327">Työsuhteen päättymispäivä (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="600da-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="600da-328">Työsuhteen päättymissyy (pakollinen päättyessä)</span><span class="sxs-lookup"><span data-stu-id="600da-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="600da-329">Seuraavien tietojen avulla lasketaan työntekijän tärkeimmät päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="600da-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="600da-330">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-330">Talent</span></span>                | <span data-ttu-id="600da-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600da-332">Viimeisimmän työhönoton päivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-332">Most recent hire date</span></span> | <span data-ttu-id="600da-333">Työntekijän työsuhteen alku voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="600da-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="600da-334">Työsuhteen loppumispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-334">Termination date</span></span>      | <span data-ttu-id="600da-335">Työntekijän työsuhteen loppu voimassa olevassa työhistoriatietueessa</span><span class="sxs-lookup"><span data-stu-id="600da-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="600da-336">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-336">Start date</span></span>            | <span data-ttu-id="600da-337">Muutettu alkamispäivämäärä, alkamispäivämäärä tai työsuhteen alku ei-aktiivisessa työsuhteen historiatietueessa</span><span class="sxs-lookup"><span data-stu-id="600da-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="600da-338">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-338">Original hire date</span></span>    | <span data-ttu-id="600da-339">Varhaisin työhistoriatietueen työsuhteen alku</span><span class="sxs-lookup"><span data-stu-id="600da-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="600da-340">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="600da-340">Compensation</span></span>

<span data-ttu-id="600da-341">Kiinteän kompensaatiosuunnitelmaan tulee liittää jokaisen työntekijän ensisijainen toimi koko työsuhteen ajalla.</span><span class="sxs-lookup"><span data-stu-id="600da-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="600da-342">Ajanjakso alkaa siitä päivämäärästä, jona työntekijä palkattiin (tai työsuhteen alkamispäivämäärä) ja jatkuu, kunnes työsuhde loppuu.</span><span class="sxs-lookup"><span data-stu-id="600da-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="600da-343">Voimaantulopäivä (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-343">Effective Date (required)</span></span>
- <span data-ttu-id="600da-344">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="600da-344">Expiration date</span></span>
- <span data-ttu-id="600da-345">Palkkio (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-345">Pay Rate (required)</span></span>
- <span data-ttu-id="600da-346">Palkkion muunnokset (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="600da-347">Vuosittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="600da-348">Tunnittainen arvo (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="600da-349">Mikäli tuntityöntekijällä on useita toimia, ensisijaisen toimen kiinteä kompensaation tuodaan Dayforceen työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="600da-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="600da-350">Ei-ensisijaisten toimien tuntihinta tallennetaan Dayforcen vastaavaan sijaintiin.</span><span class="sxs-lookup"><span data-stu-id="600da-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="600da-351">Mikäli palkallisella työntekijällä on useita toimia, kumulatiivinen tuntihinta ja vuosittainen palkka kaikista aktiivisista toimista johdetaan ja käytetään työntekijätason hinta-/peruspalkkana.</span><span class="sxs-lookup"><span data-stu-id="600da-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="600da-352">Tunnusnumerot</span><span class="sxs-lookup"><span data-stu-id="600da-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="600da-353">Sosiaaliturvan tunniste</span><span class="sxs-lookup"><span data-stu-id="600da-353">Social Security identifier</span></span> 

<span data-ttu-id="600da-354">Jokaisella työntekijä on oltava yksi ensisijainen tunnus.</span><span class="sxs-lookup"><span data-stu-id="600da-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="600da-355">Tunnuksen on oltava **SSN**-tunnus.</span><span class="sxs-lookup"><span data-stu-id="600da-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="600da-356">Dayforcessa se johdetaan automaattisesti työntekijän sosiaaliturvatunnuksesta, jota tarvitaan työsuhdetta solmittaessa.</span><span class="sxs-lookup"><span data-stu-id="600da-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="600da-357">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-357">Primary (required)</span></span>
- <span data-ttu-id="600da-358">Tunnuksen tyyppi = "Henkilötunnus"</span><span class="sxs-lookup"><span data-stu-id="600da-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="600da-359">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-359">Issued Date</span></span>
- <span data-ttu-id="600da-360">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="600da-360">Expiration Date</span></span>

<span data-ttu-id="600da-361">Työntekijät voi määrittää useita tunnistenumeroita **SSN**-tunnuksesta (henkilötunnus).</span><span class="sxs-lookup"><span data-stu-id="600da-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="600da-362">Tietue, joka on merkitty **Ensisijainen** on integroitu Dayforceen, riippumatta siitä, onko numero aktiivinen tai vanhentunut.</span><span class="sxs-lookup"><span data-stu-id="600da-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="600da-363">Pankkitilit ja suoritukset</span><span class="sxs-lookup"><span data-stu-id="600da-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="600da-364">Voimassa olevat pankkitilitiedot on kirjattava kaikille työntekijöille, jotka haluavat, että hänelle maksetaan pankkisiirtona.</span><span class="sxs-lookup"><span data-stu-id="600da-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="600da-365">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-365">Talent</span></span>                         | <span data-ttu-id="600da-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="600da-367">Pankkitilin numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="600da-368">SWIFT-koodi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-368">SWIFT code (required)</span></span>          | <span data-ttu-id="600da-369">**Pankkitunnus**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="600da-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="600da-370">Sivuliikkeen numero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="600da-371">Pankkitilin tyyppi (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-371">Bank account type (required)</span></span>   | <span data-ttu-id="600da-372">**Tilityyppi**-kenttä, jota käytetään, kun käsitellään palkkalistoja Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="600da-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="600da-373">Tuetut arvot sisältävät kohdat **Tarkistus** ja **Palkanlaskenta**.</span><span class="sxs-lookup"><span data-stu-id="600da-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="600da-374">Työntekijät, jotka haluavat, että heille maksetaan pankkisiirtona, on toimitettava linkki jäännöstilille, joka kuuluu oikeushenkilölle, jolla on ensisijainen osoite Meksikossa ja jolla on voimassa oleva tili meksikolaisessa pankissa.</span><span class="sxs-lookup"><span data-stu-id="600da-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="600da-375">Kaikki muut jäljellä olevat tilit jätetään huomiotta.</span><span class="sxs-lookup"><span data-stu-id="600da-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="600da-376">Osoitetiedot</span><span class="sxs-lookup"><span data-stu-id="600da-376">Address information</span></span>

<span data-ttu-id="600da-377">Jokaisella työntekijällä on oltava yksi ensisijainen toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="600da-377">Every employee must have one primary location.</span></span> <span data-ttu-id="600da-378">Dayforcessa tätä sijaintia käytetään määrittämään työntekijän ensisijainen oleskelulupa verotusta varten.</span><span class="sxs-lookup"><span data-stu-id="600da-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="600da-379">Ensisijainen (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-379">Primary (required)</span></span>
- <span data-ttu-id="600da-380">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-380">Country/region (required)</span></span>
- <span data-ttu-id="600da-381">Postinumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="600da-382">Katuosoite (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-382">Street (required)</span></span>
- <span data-ttu-id="600da-383">Kadunnumero (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-383">Street Number (required)</span></span>
- <span data-ttu-id="600da-384">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="600da-384">Building Complement</span></span>
- <span data-ttu-id="600da-385">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-385">City (required)</span></span>
- <span data-ttu-id="600da-386">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-386">State (required)</span></span>
- <span data-ttu-id="600da-387">Lääni (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="600da-388">Määritä tiedot luodaksesi palkkalistoja Yhdysvalloissa ja Kanadassa</span><span class="sxs-lookup"><span data-stu-id="600da-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="600da-389">Jos luot maksuja työntekijöille, jotka ovat Yhdysvalloissa ja Kanadassa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="600da-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="600da-390">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="600da-390">Departments are required on positions.</span></span>
- <span data-ttu-id="600da-391">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="600da-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="600da-392">Voit määrittää Talentin edellyttämään, että toimet määrittävät osaston.</span><span class="sxs-lookup"><span data-stu-id="600da-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="600da-393">Tehdäksesi tämän valitse **Henkilöstöhallinnon jaetut toimet > Toimet > Edellytä osastoja toimissa**.</span><span class="sxs-lookup"><span data-stu-id="600da-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="600da-394">Suosittelemme, että tämä asetus otetaan käyttöön integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="600da-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="600da-395">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="600da-395">Job types</span></span>

<span data-ttu-id="600da-396">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="600da-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="600da-397">Työlajit ovat pakollisia palkanlaskennan käsittelemiseksi Yhdysvalloissa ja Kanadassa.</span><span class="sxs-lookup"><span data-stu-id="600da-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="600da-398">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="600da-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="600da-399">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="600da-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="600da-400">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="600da-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="600da-401">Työlaji</span><span class="sxs-lookup"><span data-stu-id="600da-401">Job type</span></span>   | <span data-ttu-id="600da-402">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="600da-403">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="600da-403">Hourly</span></span>     | <span data-ttu-id="600da-404">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="600da-404">Hourly</span></span>      |
| <span data-ttu-id="600da-405">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="600da-405">Salaried</span></span>   | <span data-ttu-id="600da-406">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="600da-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="600da-407">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="600da-407">Position types</span></span> 

<span data-ttu-id="600da-408">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="600da-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="600da-409">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="600da-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="600da-410">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="600da-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="600da-411">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="600da-411">Position type</span></span>   | <span data-ttu-id="600da-412">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="600da-413">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="600da-413">Full-time</span></span>       | <span data-ttu-id="600da-414">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-414">Full time employee</span></span> |
| <span data-ttu-id="600da-415">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="600da-415">Part-time</span></span>       | <span data-ttu-id="600da-416">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="600da-417">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="600da-417">Reason codes</span></span>

<span data-ttu-id="600da-418">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="600da-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="600da-419">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="600da-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="600da-420">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="600da-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="600da-421">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="600da-421">Reason code</span></span>    | <span data-ttu-id="600da-422">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-422">Description</span></span>      | <span data-ttu-id="600da-423">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="600da-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="600da-424">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="600da-424">RESIGNATION</span></span>    | <span data-ttu-id="600da-425">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="600da-425">Resignation</span></span>      | <span data-ttu-id="600da-426">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-426">Terminate worker</span></span>     |
| <span data-ttu-id="600da-427">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="600da-427">TERMINATION</span></span>    | <span data-ttu-id="600da-428">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="600da-428">Termination</span></span>      | <span data-ttu-id="600da-429">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-429">Terminate worker</span></span>     |
| <span data-ttu-id="600da-430">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="600da-430">RETIREMENT</span></span>     | <span data-ttu-id="600da-431">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="600da-431">Retirement</span></span>       | <span data-ttu-id="600da-432">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-432">Terminate worker</span></span>     |
| <span data-ttu-id="600da-433">MUU</span><span class="sxs-lookup"><span data-stu-id="600da-433">OTHER</span></span>          | <span data-ttu-id="600da-434">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="600da-434">Other Reasons</span></span>    | <span data-ttu-id="600da-435">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-435">Terminate worker</span></span>     |
| <span data-ttu-id="600da-436">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="600da-436">DEATH</span></span>          | <span data-ttu-id="600da-437">Kuolema</span><span class="sxs-lookup"><span data-stu-id="600da-437">Death</span></span>            | <span data-ttu-id="600da-438">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-438">Terminate worker</span></span>     |
| <span data-ttu-id="600da-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="600da-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="600da-440">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="600da-440">Leave of Absence</span></span> | <span data-ttu-id="600da-441">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-441">Terminate worker</span></span>     |
| <span data-ttu-id="600da-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="600da-442">CONTRACTEND</span></span>    | <span data-ttu-id="600da-443">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="600da-443">End of Contract</span></span>  | <span data-ttu-id="600da-444">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-444">Terminate worker</span></span>     |
| <span data-ttu-id="600da-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="600da-445">SALARYCHANGE</span></span>   | <span data-ttu-id="600da-446">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="600da-446">Change of Salary</span></span> | <span data-ttu-id="600da-447">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="600da-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="600da-448">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="600da-448">Marital status</span></span>

<span data-ttu-id="600da-449">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="600da-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="600da-450">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="600da-451">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-451">Talent</span></span>                 | <span data-ttu-id="600da-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="600da-453">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="600da-453">Married</span></span>                | <span data-ttu-id="600da-454">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="600da-454">Married</span></span>              |
| <span data-ttu-id="600da-455">Yksi</span><span class="sxs-lookup"><span data-stu-id="600da-455">Single</span></span>                 | <span data-ttu-id="600da-456">Yksi</span><span class="sxs-lookup"><span data-stu-id="600da-456">Single</span></span>               |
| <span data-ttu-id="600da-457">Leski</span><span class="sxs-lookup"><span data-stu-id="600da-457">Widowed</span></span>                | <span data-ttu-id="600da-458">Leski</span><span class="sxs-lookup"><span data-stu-id="600da-458">Widowed</span></span>              |
| <span data-ttu-id="600da-459">Eronnut</span><span class="sxs-lookup"><span data-stu-id="600da-459">Divorced</span></span>               | <span data-ttu-id="600da-460">Eronnut</span><span class="sxs-lookup"><span data-stu-id="600da-460">Divorced</span></span>             |
| <span data-ttu-id="600da-461">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="600da-461">Registered Partnership</span></span> | <span data-ttu-id="600da-462">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="600da-462">Domestic Partnership</span></span> |
| <span data-ttu-id="600da-463">None</span><span class="sxs-lookup"><span data-stu-id="600da-463">None</span></span>                   | <span data-ttu-id="600da-464">None</span><span class="sxs-lookup"><span data-stu-id="600da-464">None</span></span>                 |
| <span data-ttu-id="600da-465">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="600da-465">Cohabiting</span></span>             | <span data-ttu-id="600da-466">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="600da-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="600da-467">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="600da-467">Gender</span></span>

<span data-ttu-id="600da-468">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="600da-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="600da-469">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="600da-470">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-470">Talent</span></span>       | <span data-ttu-id="600da-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="600da-472">Mies</span><span class="sxs-lookup"><span data-stu-id="600da-472">Male</span></span>         | <span data-ttu-id="600da-473">Mies</span><span class="sxs-lookup"><span data-stu-id="600da-473">Male</span></span>            |
| <span data-ttu-id="600da-474">Nainen</span><span class="sxs-lookup"><span data-stu-id="600da-474">Female</span></span>       | <span data-ttu-id="600da-475">Nainen</span><span class="sxs-lookup"><span data-stu-id="600da-475">Female</span></span>          |
| <span data-ttu-id="600da-476">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="600da-476">Non-specific</span></span> | <span data-ttu-id="600da-477">*Ei tueta*</span><span class="sxs-lookup"><span data-stu-id="600da-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="600da-478">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="600da-478">Earning codes</span></span>

<span data-ttu-id="600da-479">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="600da-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="600da-480">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="600da-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="600da-481">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="600da-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="600da-482">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="600da-482">Supported frequencies</span></span>

- <span data-ttu-id="600da-483">Kaikki</span><span class="sxs-lookup"><span data-stu-id="600da-483">All</span></span>
- <span data-ttu-id="600da-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="600da-484">EVERYPAY</span></span>
- <span data-ttu-id="600da-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="600da-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="600da-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="600da-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="600da-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="600da-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="600da-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-488">1OFMTH</span></span>
- <span data-ttu-id="600da-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-489">LASTOFMTH</span></span>
- <span data-ttu-id="600da-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-490">2OFMTH</span></span>
- <span data-ttu-id="600da-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-491">3OFMTH</span></span>
- <span data-ttu-id="600da-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-492">4OFMTH</span></span>
- <span data-ttu-id="600da-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-493">5OFMTH</span></span>
- <span data-ttu-id="600da-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-494">1N2OFMTH</span></span>
- <span data-ttu-id="600da-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-495">3N4OFMTH</span></span>
- <span data-ttu-id="600da-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-496">1N3OFMTH</span></span>
- <span data-ttu-id="600da-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-497">1N4OFMTH</span></span>
- <span data-ttu-id="600da-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-498">2N3OFMTH</span></span>
- <span data-ttu-id="600da-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-499">2N4OFMTH</span></span>
- <span data-ttu-id="600da-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="600da-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="600da-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="600da-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="600da-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="600da-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="600da-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="600da-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="600da-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="600da-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="600da-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="600da-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="600da-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="600da-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="600da-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="600da-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="600da-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="600da-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="600da-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="600da-512">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="600da-512">Addresses</span></span>

<span data-ttu-id="600da-513">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="600da-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="600da-514">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="600da-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="600da-515">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-515">Talent</span></span>          | <span data-ttu-id="600da-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="600da-517">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="600da-517">Country/Region</span></span>  | <span data-ttu-id="600da-518">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="600da-518">Country Code</span></span>          |
| <span data-ttu-id="600da-519">Postinumero</span><span class="sxs-lookup"><span data-stu-id="600da-519">Zip/Postal Code</span></span> | <span data-ttu-id="600da-520">Postinumero</span><span class="sxs-lookup"><span data-stu-id="600da-520">Postal Code</span></span>           |
| <span data-ttu-id="600da-521">Alue</span><span class="sxs-lookup"><span data-stu-id="600da-521">State</span></span>           | <span data-ttu-id="600da-522">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="600da-522">State Code</span></span>            |
| <span data-ttu-id="600da-523">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="600da-523">City</span></span>            | <span data-ttu-id="600da-524">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="600da-524">City</span></span>                  |
| <span data-ttu-id="600da-525">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="600da-525">County</span></span>          | <span data-ttu-id="600da-526">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="600da-526">County (Municipality)</span></span> |
| <span data-ttu-id="600da-527">Katu</span><span class="sxs-lookup"><span data-stu-id="600da-527">Street</span></span>          | <span data-ttu-id="600da-528">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="600da-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="600da-529">Verotusalueet</span><span class="sxs-lookup"><span data-stu-id="600da-529">Tax regions</span></span>

<span data-ttu-id="600da-530">Verotusalueita käytetään palkanlaskennan muodostamisessa käytettävän veron määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="600da-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="600da-531">ALV-alueet yhdistetään Dayforceen toimipaikan osoitteina.</span><span class="sxs-lookup"><span data-stu-id="600da-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="600da-532">Oletusarvoinen verotusalue on liitettävä työntekijän aktiiviseen toimeen.</span><span class="sxs-lookup"><span data-stu-id="600da-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="600da-533">Verotusalue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-533">Tax region (required)</span></span>
- <span data-ttu-id="600da-534">Maa/alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-534">Country/Region (required)</span></span>
- <span data-ttu-id="600da-535">Alue (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-535">State (required)</span></span>
- <span data-ttu-id="600da-536">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="600da-536">County</span></span> 
- <span data-ttu-id="600da-537">Kaupunki (pakollinen)</span><span class="sxs-lookup"><span data-stu-id="600da-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="600da-538">Määritä tietosi tuottaaksesi palkkalistoja Meksikossa</span><span class="sxs-lookup"><span data-stu-id="600da-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="600da-539">Jos luot maksuja työntekijöille, jotka ovat Meksikossa, seuraavat seikat on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="600da-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="600da-540">Toimia varten vaaditaan osastot.</span><span class="sxs-lookup"><span data-stu-id="600da-540">Departments are required on positions.</span></span>
- <span data-ttu-id="600da-541">Kustannuspaikat on määritettävä taloushallinnon dimensioina ja niiden pitää olla ensimmäisenä osana merkkijonoa oletusarvoisessa taloushallinnon dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="600da-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="600da-542">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="600da-542">Job types</span></span>

<span data-ttu-id="600da-543">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="600da-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="600da-544">Työlajit ovat pakollisia palkkalistojen käsittelemiseen Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="600da-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="600da-545">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="600da-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="600da-546">Työlajit on yhdistetty Dayforceen maksulajeina, jotka ilmaisevat, onko työntekijällä tuntipalkka vai kuukausipalkka.</span><span class="sxs-lookup"><span data-stu-id="600da-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="600da-547">Tarvitaan seuraavat työlajit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="600da-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="600da-548">Työlaji</span><span class="sxs-lookup"><span data-stu-id="600da-548">Job type</span></span>   | <span data-ttu-id="600da-549">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="600da-550">Tunneittain</span><span class="sxs-lookup"><span data-stu-id="600da-550">Hourly</span></span>     | <span data-ttu-id="600da-551">MX tunneittain</span><span class="sxs-lookup"><span data-stu-id="600da-551">MX Hourly</span></span>   |
| <span data-ttu-id="600da-552">Kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="600da-552">Salaried</span></span>   | <span data-ttu-id="600da-553">MX kuukausipalkka</span><span class="sxs-lookup"><span data-stu-id="600da-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="600da-554">Toimityypit</span><span class="sxs-lookup"><span data-stu-id="600da-554">Position types</span></span> 

<span data-ttu-id="600da-555">Voit käyttää toimityyppejä kuvaamaan, onko toimi kokoaikainen, osa-aikainen vai jokin muu.</span><span class="sxs-lookup"><span data-stu-id="600da-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="600da-556">Toimityypit on yhdistetty Dayforceen maksuluokkina, jotka ilmaisevat, onko työntekijä koko- vai osa-aikainen.</span><span class="sxs-lookup"><span data-stu-id="600da-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="600da-557">Tarvitaan seuraavat toimityypit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="600da-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="600da-558">Toimityyppi</span><span class="sxs-lookup"><span data-stu-id="600da-558">Position type</span></span>   | <span data-ttu-id="600da-559">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="600da-560">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="600da-560">Full-time</span></span>       | <span data-ttu-id="600da-561">Kokopäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-561">Full time employee</span></span> |
| <span data-ttu-id="600da-562">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="600da-562">Part-time</span></span>       | <span data-ttu-id="600da-563">Osapäiväinen työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="600da-564">Syykoodit</span><span class="sxs-lookup"><span data-stu-id="600da-564">Reason codes</span></span>

<span data-ttu-id="600da-565">Syykoodit antavat tietoja työntekijän tilasta</span><span class="sxs-lookup"><span data-stu-id="600da-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="600da-566">Syykoodit määritetään Dayforceen tilan syinä, jotka ilmaisevat muutokset työntekijän toimessa tai työsuhteessa.</span><span class="sxs-lookup"><span data-stu-id="600da-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="600da-567">Tarvitaan seuraavat syykoodit ja kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="600da-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="600da-568">Syykoodi</span><span class="sxs-lookup"><span data-stu-id="600da-568">Reason code</span></span>            | <span data-ttu-id="600da-569">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-569">Description</span></span>                    | <span data-ttu-id="600da-570">Soveltuvat skenaariot</span><span class="sxs-lookup"><span data-stu-id="600da-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="600da-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="600da-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="600da-572">Lähtö ennen ensimmäistä palkanlaskentaa</span><span class="sxs-lookup"><span data-stu-id="600da-572">Departure before first payroll</span></span> | <span data-ttu-id="600da-573">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-573">Terminate worker</span></span>     |
| <span data-ttu-id="600da-574">EROAMINEN</span><span class="sxs-lookup"><span data-stu-id="600da-574">RESIGNATION</span></span>            | <span data-ttu-id="600da-575">Eroaminen</span><span class="sxs-lookup"><span data-stu-id="600da-575">Resignation</span></span>                    | <span data-ttu-id="600da-576">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-576">Terminate worker</span></span>     |
| <span data-ttu-id="600da-577">ELÄKE</span><span class="sxs-lookup"><span data-stu-id="600da-577">PENSION</span></span>                | <span data-ttu-id="600da-578">Eläke</span><span class="sxs-lookup"><span data-stu-id="600da-578">Pension</span></span>                        | <span data-ttu-id="600da-579">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-579">Terminate worker</span></span>     |
| <span data-ttu-id="600da-580">IRTISANOMINEN</span><span class="sxs-lookup"><span data-stu-id="600da-580">TERMINATION</span></span>            | <span data-ttu-id="600da-581">Irtisanominen</span><span class="sxs-lookup"><span data-stu-id="600da-581">Termination</span></span>                    | <span data-ttu-id="600da-582">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-582">Terminate worker</span></span>     |
| <span data-ttu-id="600da-583">ELÄKKEELLE SIIRTYMINEN</span><span class="sxs-lookup"><span data-stu-id="600da-583">RETIREMENT</span></span>             | <span data-ttu-id="600da-584">Eläkkeelle siirtyminen</span><span class="sxs-lookup"><span data-stu-id="600da-584">Retirement</span></span>                     | <span data-ttu-id="600da-585">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-585">Terminate worker</span></span>     |
| <span data-ttu-id="600da-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="600da-586">ABSENTEE</span></span>               | <span data-ttu-id="600da-587">Absentee</span><span class="sxs-lookup"><span data-stu-id="600da-587">Absentee</span></span>                       | <span data-ttu-id="600da-588">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-588">Terminate worker</span></span>     |
| <span data-ttu-id="600da-589">MUU</span><span class="sxs-lookup"><span data-stu-id="600da-589">OTHER</span></span>                  | <span data-ttu-id="600da-590">Muut syyt</span><span class="sxs-lookup"><span data-stu-id="600da-590">Other Reasons</span></span>                  | <span data-ttu-id="600da-591">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-591">Terminate worker</span></span>     |
| <span data-ttu-id="600da-592">SULKEMINEN</span><span class="sxs-lookup"><span data-stu-id="600da-592">CLOSURE</span></span>                | <span data-ttu-id="600da-593">Liiketoiminnan sulkeminen</span><span class="sxs-lookup"><span data-stu-id="600da-593">Business Closure</span></span>               | <span data-ttu-id="600da-594">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-594">Terminate worker</span></span>     |
| <span data-ttu-id="600da-595">KUOLEMA</span><span class="sxs-lookup"><span data-stu-id="600da-595">DEATH</span></span>                  | <span data-ttu-id="600da-596">Kuolema</span><span class="sxs-lookup"><span data-stu-id="600da-596">Death</span></span>                          | <span data-ttu-id="600da-597">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-597">Terminate worker</span></span>     |
| <span data-ttu-id="600da-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="600da-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="600da-599">Virkavapaa</span><span class="sxs-lookup"><span data-stu-id="600da-599">Leave of Absence</span></span>               | <span data-ttu-id="600da-600">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-600">Terminate worker</span></span>     |
| <span data-ttu-id="600da-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="600da-601">CONTRACTEND</span></span>            | <span data-ttu-id="600da-602">Sopimuksen päättyminen</span><span class="sxs-lookup"><span data-stu-id="600da-602">End of Contract</span></span>                | <span data-ttu-id="600da-603">Irtisano työntekijä</span><span class="sxs-lookup"><span data-stu-id="600da-603">Terminate worker</span></span>     |
| <span data-ttu-id="600da-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="600da-604">SALARYCHANGE</span></span>           | <span data-ttu-id="600da-605">Palkan muutos</span><span class="sxs-lookup"><span data-stu-id="600da-605">Change of Salary</span></span>               | <span data-ttu-id="600da-606">Kompensaatio</span><span class="sxs-lookup"><span data-stu-id="600da-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="600da-607">Työehdot</span><span class="sxs-lookup"><span data-stu-id="600da-607">Terms of employment</span></span>

<span data-ttu-id="600da-608">Työehtoja voidaan käyttää, kun luodaan työehtoluokkia.</span><span class="sxs-lookup"><span data-stu-id="600da-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="600da-609">Ehdot määritetään Dayforceen työsuhteen mittarin arvoina.</span><span class="sxs-lookup"><span data-stu-id="600da-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="600da-610">Seuraavat työsuhteen ja kuvaukset termit ovat pakollisia.</span><span class="sxs-lookup"><span data-stu-id="600da-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="600da-611">Työehdot</span><span class="sxs-lookup"><span data-stu-id="600da-611">Terms of employment</span></span>   | <span data-ttu-id="600da-612">kuvaus</span><span class="sxs-lookup"><span data-stu-id="600da-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="600da-613">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="600da-613">Regular</span></span>               | <span data-ttu-id="600da-614">Säännöllinen</span><span class="sxs-lookup"><span data-stu-id="600da-614">Regular</span></span>     |
| <span data-ttu-id="600da-615">Suora</span><span class="sxs-lookup"><span data-stu-id="600da-615">Direct</span></span>                | <span data-ttu-id="600da-616">Suora</span><span class="sxs-lookup"><span data-stu-id="600da-616">Direct</span></span>      |
| <span data-ttu-id="600da-617">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="600da-617">Internship</span></span>            | <span data-ttu-id="600da-618">Harjoittelujakso</span><span class="sxs-lookup"><span data-stu-id="600da-618">Internship</span></span>  |
| <span data-ttu-id="600da-619">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="600da-619">Permanent</span></span>             | <span data-ttu-id="600da-620">Pysyvä</span><span class="sxs-lookup"><span data-stu-id="600da-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="600da-621">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="600da-621">Marital status</span></span>

<span data-ttu-id="600da-622">Siviilisääty on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="600da-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="600da-623">Seuraavassa taulukossa kuvataan, miten siviilisääty liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="600da-624">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-624">Talent</span></span>                 | <span data-ttu-id="600da-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="600da-626">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="600da-626">Married</span></span>                | <span data-ttu-id="600da-627">Naimisissa</span><span class="sxs-lookup"><span data-stu-id="600da-627">Married</span></span>                   |
| <span data-ttu-id="600da-628">Yksi</span><span class="sxs-lookup"><span data-stu-id="600da-628">Single</span></span>                 | <span data-ttu-id="600da-629">Yksi</span><span class="sxs-lookup"><span data-stu-id="600da-629">Single</span></span>                    |
| <span data-ttu-id="600da-630">Leski</span><span class="sxs-lookup"><span data-stu-id="600da-630">Widowed</span></span>                | <span data-ttu-id="600da-631">Leski</span><span class="sxs-lookup"><span data-stu-id="600da-631">Widowed</span></span>                   |
| <span data-ttu-id="600da-632">Eronnut</span><span class="sxs-lookup"><span data-stu-id="600da-632">Divorced</span></span>               | <span data-ttu-id="600da-633">Eronnut</span><span class="sxs-lookup"><span data-stu-id="600da-633">Divorced</span></span>                  |
| <span data-ttu-id="600da-634">Rekisteröity suhde</span><span class="sxs-lookup"><span data-stu-id="600da-634">Registered Partnership</span></span> | <span data-ttu-id="600da-635">Kotimainen kumppanuus</span><span class="sxs-lookup"><span data-stu-id="600da-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="600da-636">None</span><span class="sxs-lookup"><span data-stu-id="600da-636">None</span></span>                   | <span data-ttu-id="600da-637">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="600da-638">Avoliitossa</span><span class="sxs-lookup"><span data-stu-id="600da-638">Cohabiting</span></span>             | <span data-ttu-id="600da-639">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="600da-640">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="600da-640">Gender</span></span>

<span data-ttu-id="600da-641">Sukupuolinimitykset on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="600da-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="600da-642">Seuraavassa taulukossa kuvataan, miten sukupuolinimitykset liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="600da-643">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-643">Talent</span></span>       | <span data-ttu-id="600da-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="600da-645">Mies</span><span class="sxs-lookup"><span data-stu-id="600da-645">Male</span></span>         | <span data-ttu-id="600da-646">Mies</span><span class="sxs-lookup"><span data-stu-id="600da-646">Male</span></span>                      |
| <span data-ttu-id="600da-647">Nainen</span><span class="sxs-lookup"><span data-stu-id="600da-647">Female</span></span>       | <span data-ttu-id="600da-648">Nainen</span><span class="sxs-lookup"><span data-stu-id="600da-648">Female</span></span>                    |
| <span data-ttu-id="600da-649">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="600da-649">Non-specific</span></span> | <span data-ttu-id="600da-650">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="600da-651">Maksutapa</span><span class="sxs-lookup"><span data-stu-id="600da-651">Payment method</span></span>

<span data-ttu-id="600da-652">Maksutavat antavat työntekijälle ja yritykselle keinon kuvata, miten työntekijöille maksetaan.</span><span class="sxs-lookup"><span data-stu-id="600da-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="600da-653">Maksutavat on liitetty Dayforceen ja käännetty tarvittaessa integraatiolle hyväksyttyihin arvoihin.</span><span class="sxs-lookup"><span data-stu-id="600da-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="600da-654">Seuraavassa taulukossa kuvataan, miten maksutavat liitetään Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="600da-655">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-655">Talent</span></span>             | <span data-ttu-id="600da-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="600da-657">Maksu</span><span class="sxs-lookup"><span data-stu-id="600da-657">Cash</span></span>               | <span data-ttu-id="600da-658">Maksu</span><span class="sxs-lookup"><span data-stu-id="600da-658">Cash</span></span>                      |
| <span data-ttu-id="600da-659">Sähköinen maksu</span><span class="sxs-lookup"><span data-stu-id="600da-659">Electronic Payment</span></span> | <span data-ttu-id="600da-660">Tapahtumien siirto</span><span class="sxs-lookup"><span data-stu-id="600da-660">Transfer</span></span>                  |
| <span data-ttu-id="600da-661">Tarkistus</span><span class="sxs-lookup"><span data-stu-id="600da-661">Check</span></span>              | <span data-ttu-id="600da-662">Sekki</span><span class="sxs-lookup"><span data-stu-id="600da-662">Cheque</span></span>                    |
| <span data-ttu-id="600da-663">Pankkivekseli</span><span class="sxs-lookup"><span data-stu-id="600da-663">Bank Draft</span></span>         | <span data-ttu-id="600da-664">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="600da-665">Muu</span><span class="sxs-lookup"><span data-stu-id="600da-665">Other</span></span>              | <span data-ttu-id="600da-666">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="600da-667">Pankkitilin tyyppi</span><span class="sxs-lookup"><span data-stu-id="600da-667">Bank account type</span></span>

<span data-ttu-id="600da-668">Pankkitilin tyyppejä käytetään sähköisissä maksuissa työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="600da-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="600da-669">Pankin tilityypit yhdistetään Dayforceen tilinsiirtämisen tietoina.</span><span class="sxs-lookup"><span data-stu-id="600da-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="600da-670">Pankkitilin tyypit ovat tarvittaessa käännettyjä ja hyväksytty arvoiksi sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="600da-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="600da-671">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-671">Talent</span></span>            | <span data-ttu-id="600da-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="600da-673">Käyttötili</span><span class="sxs-lookup"><span data-stu-id="600da-673">Checking Account</span></span>  | <span data-ttu-id="600da-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="600da-674">CheckingAccount</span></span>           |
| <span data-ttu-id="600da-675">Palkanlaskennan tili</span><span class="sxs-lookup"><span data-stu-id="600da-675">Payroll Account</span></span>   | <span data-ttu-id="600da-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="600da-676">PayrollAccount</span></span>            |
| <span data-ttu-id="600da-677">Säästötili</span><span class="sxs-lookup"><span data-stu-id="600da-677">Savings Account</span></span>   | <span data-ttu-id="600da-678">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="600da-679">BankGirot-tili</span><span class="sxs-lookup"><span data-stu-id="600da-679">BankGirot account</span></span> | <span data-ttu-id="600da-680">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="600da-681">PlusGirot-tili</span><span class="sxs-lookup"><span data-stu-id="600da-681">PlusGirot account</span></span> | <span data-ttu-id="600da-682">*Meksiko ei tue tyyppiä*</span><span class="sxs-lookup"><span data-stu-id="600da-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="600da-683">Ansiokoodit</span><span class="sxs-lookup"><span data-stu-id="600da-683">Earning codes</span></span>

<span data-ttu-id="600da-684">Ansiokoodit tunnistavat yksilöllisesti kaikentyyppiset ansiot, joita työntekijät saavat.</span><span class="sxs-lookup"><span data-stu-id="600da-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="600da-685">Tunnukset kattavat erilaisia parametreja, jotka liittyvät tuloihin, kuten kirjanpitosäännöt, verolait, raportointivaatimukset ja ylöspäin bruttotehokkuus.</span><span class="sxs-lookup"><span data-stu-id="600da-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="600da-686">Mikäli käytetään ei-tuettua taajuutta **Jokainen palkka** -taajuutta käytetään oletusarvon mukaan laskelmissa.</span><span class="sxs-lookup"><span data-stu-id="600da-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="600da-687">Tuetut maksutaajuudet</span><span class="sxs-lookup"><span data-stu-id="600da-687">Supported frequencies</span></span>

- <span data-ttu-id="600da-688">Kaikki</span><span class="sxs-lookup"><span data-stu-id="600da-688">All</span></span>
- <span data-ttu-id="600da-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="600da-689">EVERYPAY</span></span>
- <span data-ttu-id="600da-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="600da-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="600da-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="600da-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="600da-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="600da-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="600da-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-693">1OFMTH</span></span>
- <span data-ttu-id="600da-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-694">LASTOFMTH</span></span>
- <span data-ttu-id="600da-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-695">2OFMTH</span></span>
- <span data-ttu-id="600da-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-696">3OFMTH</span></span>
- <span data-ttu-id="600da-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-697">4OFMTH</span></span>
- <span data-ttu-id="600da-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-698">5OFMTH</span></span>
- <span data-ttu-id="600da-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-699">1N2OFMTH</span></span>
- <span data-ttu-id="600da-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-700">3N4OFMTH</span></span>
- <span data-ttu-id="600da-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-701">1N3OFMTH</span></span>
- <span data-ttu-id="600da-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-702">1N4OFMTH</span></span>
- <span data-ttu-id="600da-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-703">2N3OFMTH</span></span>
- <span data-ttu-id="600da-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-704">2N4OFMTH</span></span>
- <span data-ttu-id="600da-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="600da-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="600da-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="600da-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="600da-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="600da-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="600da-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="600da-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="600da-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="600da-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="600da-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="600da-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="600da-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="600da-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="600da-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="600da-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="600da-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="600da-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="600da-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="600da-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="600da-717">Osoitteet</span><span class="sxs-lookup"><span data-stu-id="600da-717">Addresses</span></span>

<span data-ttu-id="600da-718">Määriteltyjen maiden tai alueiden, valtioiden ja läänin (kuntien) koodien tunnistaminen edellyttää tiettyjä muotoja, joita Dayforce ja maassa tai alueella olevat toimijat pystyvät tunnistamaan.</span><span class="sxs-lookup"><span data-stu-id="600da-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="600da-719">Vaikka kaupunkien muoto on joustava, jokainen paikkakunta täytyy liittää osavaltioon.</span><span class="sxs-lookup"><span data-stu-id="600da-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="600da-720">Talent</span><span class="sxs-lookup"><span data-stu-id="600da-720">Talent</span></span>              | <span data-ttu-id="600da-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="600da-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="600da-722">Maa/alue</span><span class="sxs-lookup"><span data-stu-id="600da-722">Country/Region</span></span>      | <span data-ttu-id="600da-723">Maakoodi</span><span class="sxs-lookup"><span data-stu-id="600da-723">Country Code</span></span>          |
| <span data-ttu-id="600da-724">Postinumero</span><span class="sxs-lookup"><span data-stu-id="600da-724">Zip/Postal Code</span></span>     | <span data-ttu-id="600da-725">Postinumero</span><span class="sxs-lookup"><span data-stu-id="600da-725">Postal Code</span></span>           |
| <span data-ttu-id="600da-726">Alue</span><span class="sxs-lookup"><span data-stu-id="600da-726">State</span></span>               | <span data-ttu-id="600da-727">Aluekoodi</span><span class="sxs-lookup"><span data-stu-id="600da-727">State Code</span></span>            |
| <span data-ttu-id="600da-728">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="600da-728">City</span></span>                | <span data-ttu-id="600da-729">Paikkakunta</span><span class="sxs-lookup"><span data-stu-id="600da-729">City</span></span>                  |
| <span data-ttu-id="600da-730">Piirikunta</span><span class="sxs-lookup"><span data-stu-id="600da-730">County</span></span>              | <span data-ttu-id="600da-731">Lääni (kunta)</span><span class="sxs-lookup"><span data-stu-id="600da-731">County (Municipality)</span></span> |
| <span data-ttu-id="600da-732">Katu</span><span class="sxs-lookup"><span data-stu-id="600da-732">Street</span></span>              | <span data-ttu-id="600da-733">Osoiterivi 1</span><span class="sxs-lookup"><span data-stu-id="600da-733">Address Line 1</span></span>        |
| <span data-ttu-id="600da-734">Kadunnumero</span><span class="sxs-lookup"><span data-stu-id="600da-734">Street Number</span></span>       | <span data-ttu-id="600da-735">Osoiterivi 2</span><span class="sxs-lookup"><span data-stu-id="600da-735">Address Line 2</span></span>        |
| <span data-ttu-id="600da-736">Rakennusta koskeva lisätieto</span><span class="sxs-lookup"><span data-stu-id="600da-736">Building Complement</span></span> | <span data-ttu-id="600da-737">Osoiterivi 5</span><span class="sxs-lookup"><span data-stu-id="600da-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="600da-738">Passin numero</span><span class="sxs-lookup"><span data-stu-id="600da-738">Passport number</span></span>

<span data-ttu-id="600da-739">Työntekijät voivat ilmoittaa passin tiedot.</span><span class="sxs-lookup"><span data-stu-id="600da-739">Employees can declare passport information.</span></span> <span data-ttu-id="600da-740">Tämä tietoa on **Passi**-tunnustyyppiä ja se on integroitu Dayforceen osaksi työntekijän Meksikon liittyvää tietoa.</span><span class="sxs-lookup"><span data-stu-id="600da-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="600da-741">Tunnustyyppi = "Passi"</span><span class="sxs-lookup"><span data-stu-id="600da-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="600da-742">Myöntämispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="600da-742">Issued Date</span></span>
- <span data-ttu-id="600da-743">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="600da-743">Expiration Date</span></span>

<span data-ttu-id="600da-744">Työntekijät voi määrittää useita tunnistenumeroita **Passi**-tunnuksesta.</span><span class="sxs-lookup"><span data-stu-id="600da-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="600da-745">Vain nykyiset aktiiviset passitapahtumat integroidaan Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="600da-746">Mikäli kaikki passitapahtumat ovat vanhentuneet, passi, joka on viimeksi myönnetty on integroitu Dayforceen.</span><span class="sxs-lookup"><span data-stu-id="600da-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
