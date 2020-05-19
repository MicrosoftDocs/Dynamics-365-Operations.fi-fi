---
title: Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten
description: Tässä ohjeaiheessa kerrotaan, miten voit korjata suoritetun ER-muodon tietolähteet ja ymmärtää paremmin konfiguroidun tietovuon ja muunnoksen.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 5b51c4beac0ddf1e2b53fe300e10c0f608e5d1e1
ms.sourcegitcommit: 153bb33722c02501bf7bcfd56ac887602d5dfbd3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2020
ms.locfileid: "3318663"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="40575-103">Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten</span><span class="sxs-lookup"><span data-stu-id="40575-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="40575-104">Kun [määrität](tasks/er-format-configuration-2016-11.md) sähköisen raportointi (ER) -ratkaisun tuottamaan lähteviä asiakirjoja, määrität menetelmät, joita käytetään tietojen noutamiseen sovelluksesta ja kirjoitetaan se luotavaan tuotokseen.</span><span class="sxs-lookup"><span data-stu-id="40575-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="40575-105">Jotta ER-ratkaisun elinkaarituki olisi tehokkaampaa, ratkaisusi tulisi koostua ER-[tietomallista](general-electronic-reporting.md#DataModelComponent) ja sen [kartoitus](general-electronic-reporting.md#ModelMappingComponent)-komponenteista sekä ER-[formaatista](general-electronic-reporting.md#FormatComponentOutbound) ja sen kartoituskomponenteista, jotta mallikartoitus on sovelluskohtainen, kun taas muut komponentit ovat sovelluskohtaisia.</span><span class="sxs-lookup"><span data-stu-id="40575-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="40575-106">Tämän vuoksi useat ER-komponentit saattavat [vaikuttaa](general-electronic-reporting.md#FormatComponentOutbound) tietojen syöttämisen yhteydessä luotuun tulostukseen.</span><span class="sxs-lookup"><span data-stu-id="40575-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="40575-107">Joskus luodun tuotoksen tiedot näyttävät erilaisilta kuin samat tiedot sovellustietokannassa.</span><span class="sxs-lookup"><span data-stu-id="40575-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="40575-108">Tällöin haluat määrittää, mikä ER-komponentti on vastuussa tietojen muunnoksesta.</span><span class="sxs-lookup"><span data-stu-id="40575-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="40575-109">ER-tietolähteen virheenkorjaustoiminto vähentää merkittävästi tähän tutkimukseen liittyvää aikaa ja kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="40575-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="40575-110">Voit keskeyttää ER-muodon suorittamisen ja avata tietolähteen virheenkorjausliittymän.</span><span class="sxs-lookup"><span data-stu-id="40575-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="40575-111">Siellä voit selata käytettävissä olevia tietolähteitä ja valita yksittäisen tietolähteen suoritusta varten.</span><span class="sxs-lookup"><span data-stu-id="40575-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="40575-112">Tämä manuaalinen suorittaminen simuloi tietolähteen suorittamista ER-muodon todellisen suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="40575-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="40575-113">Tulos esitetään sivulla, jolla voit analysoida vastaanotettuja tietoja.</span><span class="sxs-lookup"><span data-stu-id="40575-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="40575-114">Voit ottaa tietolähteen virheenkorjaustoiminnon käyttöön määrittämällä **Ota tietojen virheenkorjaus käyttöön muodon suorituksen yhteydessä** -vaihtoehdon Suorita vaihtoehdon arvoksi **Kyllä** ER-käyttäjäparametreissa.</span><span class="sxs-lookup"><span data-stu-id="40575-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="40575-115">Tämän jälkeen voit käynnistää tietolähteen virheenkorjauksen, kun luot lähteviä asiakirjoja suorittamalla ER-muodon.</span><span class="sxs-lookup"><span data-stu-id="40575-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="40575-116">**Aloita virheenkorjaus** -vaihtoehdon avulla voit myös aloittaa tietolähteen virheenkorjaustoiminnon, joka on konfiguroitu [ER-työvaiheen suunnittelutoiminnossa](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="40575-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="40575-117">Tässä ohjeaiheessa on ohjeita tietolähteen virheenkorjauksen käynnistämiseen suoritettavissa ER-muodoissa.</span><span class="sxs-lookup"><span data-stu-id="40575-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="40575-118">Siinä selitetään, miten tiedot voivat auttaa tietovuon ja tietojen muunnosten ymmärtämiseksi.</span><span class="sxs-lookup"><span data-stu-id="40575-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="40575-119">Tämän ohjeaiheen esimerkeissä käytetään toimittajamaksukäsittelyn liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="40575-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="40575-120">Rajoitukset</span><span class="sxs-lookup"><span data-stu-id="40575-120">Limitations</span></span>

<span data-ttu-id="40575-121">Tietolähteen virheenkorjauksen avulla voidaan käyttää sellaisten tietolähteiden tietoja, joita käytetään lähtevien tiedostojen luomisessa suoritettaville eri muodoissa.</span><span class="sxs-lookup"><span data-stu-id="40575-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="40575-122">Sitä ei voi käyttää sellaisten ER-muotojen tietolähteiden vian korjaukseen, jotka on suunniteltu jäsentämään saapuvia tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="40575-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="40575-123">Seuraavat ER-muotojen asetukset eivät ole käytettävissä tietolähteen virheen korjausta varten:</span><span class="sxs-lookup"><span data-stu-id="40575-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="40575-124">Lomakkeen muunnokset</span><span class="sxs-lookup"><span data-stu-id="40575-124">Format transformations</span></span>
- <span data-ttu-id="40575-125">Oikeellisuustarkistussääntöjen muotoileminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="40575-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="40575-126">Lausekkeiden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="40575-126">Enabling expressions</span></span>
- <span data-ttu-id="40575-127">Muistissa olevan tiedonkeräyksen tiedot</span><span class="sxs-lookup"><span data-stu-id="40575-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="40575-128">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="40575-128">Prerequisites</span></span>

- <span data-ttu-id="40575-129">Tässä ohjeaiheessa olevien esimerkkien suorittaminen edellyttää käyttöoikeutta johonkin seuraavaan [rooliin](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="40575-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="40575-130">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="40575-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="40575-131">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="40575-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="40575-132">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="40575-132">System administrator</span></span>

- <span data-ttu-id="40575-133">Yritykselle on asetettava **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="40575-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="40575-134">Tämän ohjeaiheen [lisäyksen 1](#appendix1) vaiheiden mukaisesti voit ladata toimittajien maksuissa tarvittavien Microsoft er-ratkaisujen komponentit.</span><span class="sxs-lookup"><span data-stu-id="40575-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="40575-135">Tämän ohjeaiheen [Lisäyksessä 2](#appendix2) olevien ohjeiden avulla voit valmistella ostoreskontran toimittajamaksun käsittelyä varten käyttämällä ER-ratkaisua, jonka voit ladata.</span><span class="sxs-lookup"><span data-stu-id="40575-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="40575-136">Toimittajamaksun käsitteleminen siten, että se saa maksutiedoston</span><span class="sxs-lookup"><span data-stu-id="40575-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="40575-137">Käsittele toimittajamaksuja tämän ohjeaiheen [Lisäyksen 3](#appendix3) ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="40575-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Toimittajamaksujen käsittely käynnissä](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="40575-139">Lataa ja tallenna zip-tiedosto paikalliseen tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="40575-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="40575-140">Pura **ISO20022 Credit transfer.xml**-maksutiedosto zip-tiedostosta.</span><span class="sxs-lookup"><span data-stu-id="40575-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="40575-141">Avaa purettu maksutiedosto XML-tiedoston katseluohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="40575-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="40575-142">Toimittajan pankkitilin kansainvälinen pankkitilin numero (IBAN)-koodi ei sisällä välilyöntejä maksutiedostossa.</span><span class="sxs-lookup"><span data-stu-id="40575-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="40575-143">Siksi se eroaa **pankkitilit**-sivulla [syötetystä](#enteredIBANcode) arvosta.</span><span class="sxs-lookup"><span data-stu-id="40575-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![IBAN-koodi ilman välilyöntejä](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="40575-145">Voit käyttää ER-tietolähteen virheenkorjaustoimintoa, kun haluat tietää, mitä ER-ratkaisun osaa käytetään IBAN-koodin välien lyhentämiseen.</span><span class="sxs-lookup"><span data-stu-id="40575-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="40575-146">Tietolähteen virheenkorjauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="40575-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="40575-147">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="40575-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="40575-148">Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="40575-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="40575-149">Määritä **Ota tietojen virheenkorjaus käyttöön muodon suorituksen yhteydessä** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="40575-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="40575-150">Tämä parametri on käyttäjä- ja yrityskohtainen.</span><span class="sxs-lookup"><span data-stu-id="40575-150">This parameter is user-specific and company-specific.</span></span>

    ![Käyttäjän parametrit -valintaikkuna](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="40575-152">Toimittajan summan käsitteleminen virheen korjausta varten</span><span class="sxs-lookup"><span data-stu-id="40575-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="40575-153">Käsittele toimittajamaksuja tämän ohjeaiheen [Lisäyksen 3](#appendix3) ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="40575-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="40575-154">Vahvista, että haluat keskeyttää toimittajan maksujenkäsittelyn ja käynnistää sen sijaan tietolähteen **virheenkorjauksen tietolähteet** -sivulla, valitsemalla sanomaruudun vaihtoehdon **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="40575-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Vahvistussanomaruutu](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="40575-156">Virheenkorjauksen tietolähteet, joita käytetään maksukäsittelyssä</span><span class="sxs-lookup"><span data-stu-id="40575-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="40575-157">Mallimäärityksen virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="40575-157">Debug the model mapping</span></span>

1. <span data-ttu-id="40575-158">Valitse **Tietolähteiden virheenkorjaus** -sivun toimintoruudussa **Mallimääritys**, jonka avulla voit aloittaa virheenkorjauksen tästä ER-komponentista.</span><span class="sxs-lookup"><span data-stu-id="40575-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="40575-159">Valitse vasemmanpuoleisen tietolähderuudun **\$notSentTransactions**-tietolähde ja valitse sitten **Lue kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="40575-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="40575-160">Voit valita **Lue 1 tietue**, **lue 10 tietuetta**, **lue 100 tietuetta** tai **lue kaikki tietueet** pakottamaan valitun tietolähteen lukemiseen tarvittavan määrän tietueita.</span><span class="sxs-lookup"><span data-stu-id="40575-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="40575-161">Näin voit simuloida tietolähteen käyttöä käynnissä olevan ER-muodon avulla.</span><span class="sxs-lookup"><span data-stu-id="40575-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="40575-162">Valitse oikealla olevassa tietoruudussa **Laajenna kaikki**.</span><span class="sxs-lookup"><span data-stu-id="40575-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="40575-163">Voit nähdä, että **tietueluettelo**-tyypin valittu tietolähde sisältää yhden tietueen.</span><span class="sxs-lookup"><span data-stu-id="40575-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="40575-164">Laajenna **\$notSentTransactions**-tietolähde ja valitse sisäkkäinen **vendBankAccountInTransactionCompany()**-menetelmä.</span><span class="sxs-lookup"><span data-stu-id="40575-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="40575-165">Laajenna **vendBankAccountInTransactionCompany()**-menetelmä ja valitse sisäkkäinen **IBAN**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="40575-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="40575-166">Valitse **Hae arvo**.</span><span class="sxs-lookup"><span data-stu-id="40575-166">Select **Get value**.</span></span>

    <span data-ttu-id="40575-167">Valitsemalla **Hae arvo** voit pakottaa valitun tietolähteen valitun kentän arvon luettavaksi.</span><span class="sxs-lookup"><span data-stu-id="40575-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="40575-168">Näin voit simuloida tämän kentän käyttöä käynnissä olevan ER-muodon avulla.</span><span class="sxs-lookup"><span data-stu-id="40575-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="40575-169">Valitse **Laajenna kaikki**.</span><span class="sxs-lookup"><span data-stu-id="40575-169">Select **Expand all**.</span></span>

    ![Mallimäärityksen IBAN-kentän arvo](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="40575-171">Kuten näette, mallikartoitus ei ole vastuussa katkenneista välilyönneistä, sillä toimittajan pankkitilin palauttama IBAN-koodi sisältää välilyöntejä.</span><span class="sxs-lookup"><span data-stu-id="40575-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="40575-172">Tämän vuoksi tietolähteen virheenkorjausta on jatkettava.</span><span class="sxs-lookup"><span data-stu-id="40575-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="40575-173">Muodon yhdistämismäärityksen virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="40575-173">Debug the format mapping</span></span>

1. <span data-ttu-id="40575-174">Valitse **Tietolähteiden virheenkorjaus** -sivun toimintoruudussa **Muodon määritys**, jonka avulla voit jatkaa virheenkorjauksen tästä ER-komponentista.</span><span class="sxs-lookup"><span data-stu-id="40575-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="40575-175">Valitse **\$PaymentByDebtor**-tietolähde ja valitse sitten **Lue kaikki tietueet**.</span><span class="sxs-lookup"><span data-stu-id="40575-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="40575-176">Laajenna **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="40575-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="40575-177">Laajenna **\$PaymentByDebtor.Lines** ja valitse sitten **Lue kaikki tietueet**.</span><span class="sxs-lookup"><span data-stu-id="40575-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="40575-178">Laajenna **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="40575-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="40575-179">Laajenna **\$PaymentByDebtor.Lines.CreditorAccount.Identification**ja valitse sitten **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="40575-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="40575-180">Valitse **Hae arvo**.</span><span class="sxs-lookup"><span data-stu-id="40575-180">Select **Get value**.</span></span>
8. <span data-ttu-id="40575-181">Valitse **Laajenna kaikki**.</span><span class="sxs-lookup"><span data-stu-id="40575-181">Select **Expand all**.</span></span>

    ![Muodon määrityksen IBAN-kentän arvo](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="40575-183">Kuten näette, mallikartoituksen tietolähteet eivät ole vastuussa katkenneista välilyönneistä, sillä toimittajan pankkitilin palauttama IBAN-koodi sisältää välilyöntejä.</span><span class="sxs-lookup"><span data-stu-id="40575-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="40575-184">Tämän vuoksi tietolähteen virheenkorjausta on jatkettava.</span><span class="sxs-lookup"><span data-stu-id="40575-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="40575-185">Muodon virheenkorjaus</span><span class="sxs-lookup"><span data-stu-id="40575-185">Debug the format</span></span>

1. <span data-ttu-id="40575-186">Valitse **Tietolähteiden virheenkorjaus** -sivun toimintoruudussa **Muoto**, jonka avulla voit jatkaa virheenkorjauksen tästä ER-komponentista.</span><span class="sxs-lookup"><span data-stu-id="40575-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="40575-187">Laajenna muotoiluelementit ja valitse **ISO20022CTReports** \> **XMLHeader** \> **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** ja valitse sitten **Lue kaikki tietueet**.</span><span class="sxs-lookup"><span data-stu-id="40575-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="40575-188">Laajenna muotoiluelementit ja valitse **ISO20022CTReports** \> **XMLHeader** \> **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** ja valitse sitten **Lue kaikki tietueet**.</span><span class="sxs-lookup"><span data-stu-id="40575-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="40575-189">Laajenna muotoiluelementit ja valitse **ISO20022CTReports** \> **XMLHeader** \> **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Tunnus** \> **IBAN** \> **BankIBAN** ja valitse sitten **Hae arvo**.</span><span class="sxs-lookup"><span data-stu-id="40575-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="40575-190">Valitse **Laajenna kaikki**.</span><span class="sxs-lookup"><span data-stu-id="40575-190">Select **Expand all**.</span></span>

    ![Muodon IBAN-kentän arvo](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="40575-192">Kuten näette, muodon sidonta ei ole vastuussa katkenneista välilyönneistä, sillä toimittajan pankkitilin palauttama IBAN-koodi sisältää välilyöntejä.</span><span class="sxs-lookup"><span data-stu-id="40575-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="40575-193">Siksi **BankIBAN**-elementti on konfiguroitu käyttämään muodon muutosta, joka katkaisee välit.</span><span class="sxs-lookup"><span data-stu-id="40575-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="40575-194">Sulje tietolähteen virheenkorjaus.</span><span class="sxs-lookup"><span data-stu-id="40575-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="40575-195">Tarkastele muodon muunnoksia</span><span class="sxs-lookup"><span data-stu-id="40575-195">Review the format transformations</span></span>

1. <span data-ttu-id="40575-196">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="40575-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="40575-197">Valitse **Konfiguraatiot**-sivulla **maksumalli** \> **ISO20022-tilisiirto**.</span><span class="sxs-lookup"><span data-stu-id="40575-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="40575-198">Valitse **Suunnitteluohjelma** ja laajenna sitten elementit valitaksesi **Tedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Tunnus** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="40575-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN-elementti Muodon suunnittelija -sivulla](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="40575-200">Kuten näette, **BankIBAN**-elementti on määritetty käyttämään **poista ei aakkosnumeerisia** -muunnosta.</span><span class="sxs-lookup"><span data-stu-id="40575-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="40575-201">Valitse **Muunnokset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="40575-201">Select the **Transformations** tab.</span></span>

    ![BankIBAN-elementin muunnokset -välilehti](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="40575-203">Kuten näette, **Poista ei-aakkosnumeerinen** -muunnos on määritetty käyttämään lauseketta, joka katkaisee välit annetun tekstimerkkijonon väliltä.</span><span class="sxs-lookup"><span data-stu-id="40575-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="40575-204">Aloita virheenkorjaus toiminnon suunnittelussa</span><span class="sxs-lookup"><span data-stu-id="40575-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="40575-205">Kun määrität ER-muodon luonnosversion, joka voidaan suorittaa suoraan toiminnon suunnittelutoiminnosta, voit käyttää tietolähteen virheenkorjausta valitsemalla toimintoruudusta **Aloita virheenkorjaus**.</span><span class="sxs-lookup"><span data-stu-id="40575-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Muotoilun suunnittelu -sivun virheenkorjauspainikkeen käynnistäminen](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="40575-207">Muokattavan ER-muodon määritys- ja muotoilukomponentit ovat käytettävissä virheenkorjausta varten.</span><span class="sxs-lookup"><span data-stu-id="40575-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="40575-208">Aloita virheenkorjaus mallin määrityksen suunnittelussa</span><span class="sxs-lookup"><span data-stu-id="40575-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="40575-209">Kun määrität ER-muodon määrityksen, joka voidaan suorittaa **Muodon määritys**-sivulta, voit käyttää tietolähteen virheenkorjausta valitsemalla toimintoruudusta **Aloita virheenkorjaus**.</span><span class="sxs-lookup"><span data-stu-id="40575-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Mallin määrityksen suunnittelu -sivun virheenkorjauspainikkeen käynnistäminen](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="40575-211">Muokattavan ER-määrityksen mallimäärityskomponentti on käytettävissä virheen korjausta varten.</span><span class="sxs-lookup"><span data-stu-id="40575-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="40575-212">Lisäys 1: ER-ratkaisun hankkiminen</span><span class="sxs-lookup"><span data-stu-id="40575-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="40575-213">Lataa ER-ratkaisu</span><span class="sxs-lookup"><span data-stu-id="40575-213">Download an ER solution</span></span>

<span data-ttu-id="40575-214">Jos haluat käyttää ER-ratkaisua sähköisen maksutiedoston luomiseen käsiteltävälle toimittajamaksulle, voit [ladata](download-electronic-reporting-configuration-lcs.md) **ISO20022-tilisiirron** ER-maksumuotoa, joka on käytettävissä Microsoft Dynamics Lifecycle Servicesin (LCS) jaetun käyttöomaisuuden kirjastossa tai yleisestä tietovarastosta.</span><span class="sxs-lookup"><span data-stu-id="40575-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![ER-maksumuodon tuominen konfiguraation tietovarasto -sivulla](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="40575-216">Valitun ER-muodon lisäksi seuraavat [kokoonpanot](general-electronic-reporting.md#Configuration) on tuotava automaattisesti Microsoft Dynamics 365 Finance -instanssiin osana **ISO20022-tilisiirron** ER-ratkaisua:</span><span class="sxs-lookup"><span data-stu-id="40575-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="40575-217">**Maksun malli** [ER-tietomallien määritys](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="40575-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="40575-218">**ISO20022-tilisiirto** [ER-muodon konfiguraatio](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="40575-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="40575-219">**Maksumallin yhdistämismääritys 1611** [ER-mallin yhdistämismääritys](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="40575-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="40575-220">**Maksumallin yhdistämismääritys kohteeseen ISO20022** ER-mallin yhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="40575-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="40575-221">Nämä konfiguraatiot löytyvät ER-kehyksen **Konfiguroinnit**-sivulta (**Organisaation hallinta** \> **Sähköinen raportointi** \> **Kokoonpanot**).</span><span class="sxs-lookup"><span data-stu-id="40575-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Tuodut määritykset määrityssivulla](./media/er-data-debugger-configurations.png)

<span data-ttu-id="40575-223">Jos jokin aiemmin luetelluista konfiguraatioista puuttuu määrityspuusta, ne on ladattava manuaalisesti LCS-jaetun käyttöomaisuuden kirjastosta samalla tavalla kuin **ISO20022-tilisiirron** ER-maksumuoto on ladattu.</span><span class="sxs-lookup"><span data-stu-id="40575-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="40575-224">Ladatun ER-ratkaisun analysoiminen</span><span class="sxs-lookup"><span data-stu-id="40575-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="40575-225">Mallin määrityksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="40575-225">Review the model mapping</span></span>

1. <span data-ttu-id="40575-226">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="40575-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="40575-227">Valitse **Maksumalli** \> **Maksumallin kartoitus 1611**.</span><span class="sxs-lookup"><span data-stu-id="40575-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="40575-228">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="40575-228">Select **Designer**.</span></span>
4. <span data-ttu-id="40575-229">Valitse **Maksumallin yhdistämismääritys ISO20022** -kartoitustietue.</span><span class="sxs-lookup"><span data-stu-id="40575-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="40575-230">Valitse **Suunnittelu** ja tarkista sitten avattava mallimääritys.</span><span class="sxs-lookup"><span data-stu-id="40575-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="40575-231">Huomaa, että tietomallin **Maksut**-kenttä on sidottu **\$notSentTransactions**-tietolähteeseen, joka palauttaa käsiteltävien toimittajien maksurivien luettelon.</span><span class="sxs-lookup"><span data-stu-id="40575-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Mallikartoituksen suunnittelusivun maksukenttä](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="40575-233">Muodon määrityksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="40575-233">Review the format mapping</span></span>

1. <span data-ttu-id="40575-234">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="40575-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="40575-235">Valitse **Maksumalli** \> **ISO20022-tilisiirto**.</span><span class="sxs-lookup"><span data-stu-id="40575-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="40575-236">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="40575-236">Select **Designer**.</span></span>
4. <span data-ttu-id="40575-237">Tarkista **Yhdistämismääritys**-välilehdestä avattava muotomääritys.</span><span class="sxs-lookup"><span data-stu-id="40575-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="40575-238">Huomaa, että **Asiakirja** \> **ICstmrCdtTrfInitn** \> **PmtInf**-elementti kohdassa **ISO20022CTReports** \> **XMLHeader**-tiedosto on sidottu **\$PaymentByDebtor**-tietolähteeseen, joka on määritetty tietomallin **Maksu**-kentän tietueiden ryhmittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="40575-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf-elementti Muodon suunnittelija -sivulla](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="40575-240">Muodon tarkastelu</span><span class="sxs-lookup"><span data-stu-id="40575-240">Review the format</span></span>

1. <span data-ttu-id="40575-241">Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="40575-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="40575-242">Valitse **Maksumalli** \> **ISO20022-tilisiirto**.</span><span class="sxs-lookup"><span data-stu-id="40575-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="40575-243">Valitse **Suunnittelu** ja tarkista sitten avattava muoto.</span><span class="sxs-lookup"><span data-stu-id="40575-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="40575-244">Huomaa, että **Tiedosto** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Tunnus** \> **IBAN** \> **BankIBAN** on määritetty antamaan toimittajatilin IBAN-koodi maksutiedostossa.</span><span class="sxs-lookup"><span data-stu-id="40575-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN-elementti Muodon suunnittelija -sivulla](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="40575-246">Liite 2: Ostoreskontran määrittäminen</span><span class="sxs-lookup"><span data-stu-id="40575-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="40575-247">Toimittajan ominaisuuden muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="40575-247">Modify a vendor property</span></span>

1. <span data-ttu-id="40575-248">Siirry kohtaan **Ostoreskontra** \> **Toimittajat** \> **Kaikki toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="40575-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="40575-249">Valitse toimittaja **DE-01002** ja valitse sitten **Toimittaja**-välilehden **Määritä**-ryhmässä **Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="40575-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="40575-250">Kirjoita **Tunnus**-pikavälilehden **IBAN**-kenttään <a name="enteredIBANcode"></a> **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="40575-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="40575-251">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="40575-251">Select **Save**.</span></span>

![IBAN-kenttä määritetty toimittajan pankkitilit -sivulla](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="40575-253">Määritä maksutapa</span><span class="sxs-lookup"><span data-stu-id="40575-253">Set up a method of payment</span></span>

1. <span data-ttu-id="40575-254">Valitse **Ostoreskontra** \> **Maksun asetukset** \> **Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="40575-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="40575-255">Valitse **SEPA CT**-maksutapa.</span><span class="sxs-lookup"><span data-stu-id="40575-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="40575-256">Määritä **Tiedostomuodot**-pikavälilehden **Tiedostomuodot**-osassa **Yleinen sähköinen vientimuoto** -kohdan asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="40575-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="40575-257">Valitse **Vientimuodon konfigurointi** -kentässä **ISO20022-tilisiirto**-ER-muoto.</span><span class="sxs-lookup"><span data-stu-id="40575-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="40575-258">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="40575-258">Select **Save**.</span></span>

![Tiedostomuodon asetukset toimitustapasivulla](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="40575-260">Lisää toimittajamaksu</span><span class="sxs-lookup"><span data-stu-id="40575-260">Add a vendor payment</span></span>

1. <span data-ttu-id="40575-261">Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="40575-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="40575-262">Lisää uusi maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="40575-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="40575-263">Valitse **Rivit** ja lisää uusi toimitusrivi.</span><span class="sxs-lookup"><span data-stu-id="40575-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="40575-264">Valitse **Tili**-kentässä toimittaja **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="40575-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="40575-265">Syötä **Debet**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="40575-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="40575-266">Valitse **Maksutapa**-kentässä **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="40575-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="40575-267">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="40575-267">Select **Save**.</span></span>

![Toimittajamaksun lisäys toimittajan maksut -sivulla](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="40575-269">Liite 3: Toimittajamaksun käsittely</span><span class="sxs-lookup"><span data-stu-id="40575-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="40575-270">Valitse **Ostoreskontra** \> **Maksut** \> **Toimittajan maksukirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="40575-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="40575-271">Valitse **Toimittajan maksukirjauskansio** -sivulla aiemmin luomasi kirjauskansio ja valitse sitten **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="40575-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="40575-272">Valitse ensin maksurivi ja sitten **Maksun tila** \> **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="40575-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="40575-273">Valitse **Muodosta maksut**.</span><span class="sxs-lookup"><span data-stu-id="40575-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="40575-274">Valitse **Maksutapa**-kentässä **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="40575-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="40575-275">Valitse **Pankkitili**-kentässä **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="40575-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="40575-276">Valitse **Luo maksuja** -valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="40575-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="40575-277">Valitse **Sähköisen raportin parametrit** -valintaikkunasta **OK**.</span><span class="sxs-lookup"><span data-stu-id="40575-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
