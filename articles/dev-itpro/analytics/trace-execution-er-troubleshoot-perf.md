<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="fi-FI">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tässä ohjeaiheessa on tietoja suorituskykyongelmien vianmäärityksestä sähköisen raportoinnin (ER) suorituskyvyn jäljitystoiminnon avulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Osana sähköisten raportointikonfiguraatioiden suunnittelua sähköisten asiakirjojen luomista varten määritetään menetelmä, jonka avulla tiedot haetaan Microsoft Dynamics 365 for Finance and Operationsista ja syötetään tuotavaan tuotokseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ER Performance Trace -toiminto auttaa vähentämään huomattavasti aikaa ja kustannuksia, jotka liittyvät ER-muodon suorituksen yksityiskohtien keräämiseen ja niiden käyttämiseen suorituskykyongelmien vianmäärityksessä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tässä opetusohjelmassa on ohjeita siitä, miten suorituskykyä voidaan seurata suoritettavissa ER-muodoissa Finance and Operationsin yhteydessä ja miten suorituskykyä voidaan parantaa näiden jälkien tietojen avulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Edellytykset</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämän opetusohjelman esimerkkien suorittaminen edellyttää seuraavia käyttöoikeuksia:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Finance and Operations -käyttöoikeudet seuraaville rooleille:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sähköisen raportoinnin kehittäjä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Sähköisen raportoinnin toiminnallinen konsultti</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Järjestelmänvalvoja</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Voit käyttää järjestelmän (RCS) esiintymää, joka on valmisteltu samalle vuokralaiselle kuin Finance and Operations jostakin seuraavista rooleista:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Sähköisen raportoinnin kehittäjä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Sähköisen raportoinnin toiminnallinen konsultti</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Järjestelmänvalvoja</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Seuraavat tiedostot täytyy myös ladata ja tallentaa paikallisesti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tiedosto</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Sisältö</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Suorituskyvyn jäljitysmalli.versio.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Esimerkin ER-tietomallin konfigurointi<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Suorituskyvyn jäljitysmetadata.versio.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Esimerkin ER-metadatan konfigurointi<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Suorituskyvyn jäljitysmapping.versio.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Esimerkin ER-mallikartoituksen konfigurointi<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Suorituskyvyn jäljitysformat.versio.1</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">[</bpt>Esimerkin ER-format-konfigurointi<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Konfiguroi ER-parametrit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kukin Finance and Operationsin suorituskyvyn jäljitys tallennetaan suorituslokitietueen liitteenä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Näiden liitteiden hallinnassa käytetään Finance and Operationsin tiedostohallinnan (DM) kehystä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sinun on määritettävä ER-parametrit etukäteen ja määritettävä DM-tiedosto tyyppi, jota käytetään suorituskykyjälkien liittämiseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Valitse Finance and Operationissa <bpt id="p1">**</bpt>Sähköisen raportoinnin<ept id="p1">**</ept> työtilassa <bpt id="p2">**</bpt>Sähköisen raportoinnin parametrit<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Valitse sitten <bpt id="p1">**</bpt>Sähköisen raportoinnin parametrit<ept id="p1">**</ept> -sivun <bpt id="p2">**</bpt>Liitteet<ept id="p2">**</ept>-välilehden <bpt id="p3">**</bpt>Muut<ept id="p3">**</ept>-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sähköisen raportoinnin parametrisivu Finance and Operationsissa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos haluat olla käytettävissä <bpt id="p1">**</bpt>Muut<ept id="p1">**</ept> -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla <bpt id="p2">**</bpt>Asiakirjatyypit<ept id="p2">**</ept>-sivulla (<bpt id="p3">**</bpt>Organisaation hallinta <ph id="ph1">\&gt;</ph> Asiakirjan hallinta <ph id="ph2">\&gt;</ph> Asiakirjatyypit<ept id="p3">**</ept>):</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Luokka:<ept id="p1">**</ept> Liitä tiedosto</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Ryhmä:<ept id="p1">**</ept> Tiedosto</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Finance and Operations -tiedostotyypit-sivu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Valitun tiedostotyypin on oltava käytettävissä kaikissa nykyisen Finance and Operations -esiintymän yrityksissä, koska DM-liitteet ovat yrityskohtaisia.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Konfiguroi RCS-parametrit</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Finance and Operationsissa luodut ER-suorituskykyjäljet tuodaan RCS-määritykseen analysointia varten käyttämällä ER Format Designeria ja ER Mapping Designeria.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Koska ER-suorituskykyjäljet tallennetaan ER-muotoon liittyvän suorituslokitietueen liitteinä, RCS-parametrit on määritettävä etukäteen, jotta voidaan määrittää DM-tiedostotyyppi, jota käytetään suorituskykyjälkien liittämiseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Valitse yrityksellesi määritetyn RCS-esiintymän <bpt id="p1">**</bpt>Sähköisen raportoinnin<ept id="p1">**</ept> -työtilassa <bpt id="p2">**</bpt>Sähköiset raportointiparametrit<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Valitse sitten <bpt id="p1">**</bpt>Sähköisen raportoinnin parametrit<ept id="p1">**</ept> -sivun <bpt id="p2">**</bpt>Liitteet<ept id="p2">**</ept>-välilehden <bpt id="p3">**</bpt>Muut<ept id="p3">**</ept>-kentästä suorituskyvyn jäljille käytettävä DM-tiedostotyyppi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sähköisen raportoinnin parametrit -sivu RCS:ssä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Jos haluat olla käytettävissä <bpt id="p1">**</bpt>Muut<ept id="p1">**</ept> -hakukentässä, DM-tiedostotyyppi on konfiguroitava seuraavalla tavalla <bpt id="p2">**</bpt>Asiakirjatyypit<ept id="p2">**</ept>-sivulla (<bpt id="p3">**</bpt>Organisaation hallinta <ph id="ph1">\&gt;</ph> Asiakirjan hallinta <ph id="ph2">\&gt;</ph> Asiakirjatyypit<ept id="p3">**</ept>):</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Luokka:<ept id="p1">**</ept> Liitä tiedosto</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Ryhmä:<ept id="p1">**</ept> Tiedosto</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Suunnittele ER-ratkaisu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Oletetaan, että olet aloittanut uuden ER-ratkaisun suunnittelun, joka luo toimittajatapahtumia esittelevän uuden raportin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tällä hetkellä voit etsiä valitun toimittajan tapahtumat <bpt id="p1">**</bpt>Toimittajatapahtumat<ept id="p1">**</ept>-sivulta (Siirry <bpt id="p2">**</bpt>Ostoreskontra <ph id="ph1">\&gt;</ph> Toimittajat <ph id="ph2">\&gt;</ph> Kaikki toimittajat<ept id="p2">**</ept>, valitse toimittaja ja sitten toimintoruudun <bpt id="p3">**</bpt>Toimittaja<ept id="p3">**</ept>-välilehti kohdassa valitse <bpt id="p4">**</bpt>Tapahtumat<ept id="p4">**</ept>-ryhmästä <bpt id="p5">**</bpt>Tapahtumat<ept id="p5">**</ept>).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Haluat kuitenkin saada kaikki toimittajatapahtumat samaan aikaan yhdessä sähköisessä asiakirjassa XML-muodossa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ratkaisu koostuu useista ER-konfiguraatioista, jotka sisältävät vaaditun tietomallin, metatiedot, mallien yhdistämismääritykset ja muotokomponentit.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kirjaudu yrityksen RCS-esiintymään, joka on valmisteltu yrityksellesi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tässä opetusohjelmassa luodaan ja muokataan konfiguraatioita malliyritykselle <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Varmista siksi, että tämä konfigurointipalvelu on lisätty RCS-järjestelmään ja valittu aktiiviseksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Lisätietoja on kohdassa <bpt id="p1">[</bpt>Luo konfigurointipalvelut ja merkitse ne aktiivisiksi<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> menettelyiksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Sähköisen raportoinnin<ept id="p1">**</ept> työtilassa <bpt id="p2">**</bpt>Raportointimääritykset<ept id="p2">**</ept>-ruutu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tuo <bpt id="p1">**</bpt>Konfiguraatiot<ept id="p1">**</ept> -sivulla lataamasi ER-kokoonpanot RCS-edellytyksenä seuraavassa järjestyksessä: tietomalli, metatiedot, mallikartoitus, muoto.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Luo kukin mukautus seuraavasti:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Valitse toimintoruudusta <bpt id="p1">**</bpt>Vaihda <ph id="ph1">\&gt;</ph> Lataa XML-tiedostosta<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Valitse haluamasi ER-kokoonpanon tiedosto XML-muodossa valitsemalla <bpt id="p1">**</bpt>Selaa<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Konfiguroinnit-sivu RCS:ssä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ER-ratkaisun suorittaminen jäljityksen suorittamista varten</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Oletetaan, että olet suunnitellut ER-ratkaisun ensimmäisen version.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Haluat nyt testata sen Finance and Operations -esiintymässä ja analysoida suorituskykyä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>ER-konfiguraation tuominen RCI:sta Finance and Operationsiin</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kirjaudu omaan Finance and Operations -esiintymään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämän opetusohjelman avulla voit tuoda konfiguraatiot RCS-esiintymästä (jossa suunnittelet ER-komponentteja) Finance and Operations -esiintymään (jossa testaat ja lopulta käytät niitä).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Siksi on varmistettava, että kaikki vaaditut tiedot on valmisteltu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ohjeita on kohdassa <bpt id="p1">[</bpt>Sähköisen raportoinnin konfiguraatioiden tuonti Regulatory Configuration Services (RCS) -palvelusta<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Seuraavien vaiheiden mukaisesti voit tuoda konfiguraatiot RCS-asetuksista Finance and Operationsiin:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Valitse <bpt id="p1">**</bpt>Sähköisen raportoinnin<ept id="p1">**</ept> työtilassa<bpt id="p2">**</bpt>Litware, Inc<ept id="p2">**</ept>-määrityspalveluruudussa <bpt id="p3">**</bpt>Arkistot<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source><target logoport:matchpercent="0" state="translated">Valitse <bpt id="p1">**</bpt>Konfiguraatiosäilö<ept id="p1">**</ept>-sivun ruudukossa oleva säilö, jonka tyyppi on <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> ja valitse sitten <bpt id="p3">**</bpt>Avaa<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>Konfiguraatiot<ept id="p1">**</ept>-pikavälilehdessä <bpt id="p2">**</bpt>Suorituskyvyn jäljitysmuodon<ept id="p2">**</ept> konfiguraatio.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source><target logoport:matchpercent="0" state="translated">Valitse <bpt id="p1">**</bpt>Versiot<ept id="p1">**</ept>-pikavälilehdellä valitun konfiguraation versio <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> ja valitse sitten <bpt id="p3">**</bpt>Tuo<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Konfigurointivaraston sivu Finance and Operationsissa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tietomallin ja mallin yhdistämismääritysten vastaavat versiot tuodaan automaattisesti valmiiksi tuodun ER-muodon konfiguroinnin edellytyksinä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER-suorituskykyjäljityksen ottaminen käyttöön</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">Valitse Finance and Operationsissa <bpt id="p1">**</bpt>Organisaation hallinto <ph id="ph1">\&gt;</ph> Sähköinen raportointi <ph id="ph2">\&gt;</ph> Määritykset<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Valitse <bpt id="p1">**</bpt>Määritykset<ept id="p1">**</ept>-sivun toimintoruudun <bpt id="p2">**</bpt>Määritykset<ept id="p2">**</ept>-välilehden <bpt id="p3">**</bpt>Lisämääritykset<ept id="p3">**</ept>-ryhmässä <bpt id="p4">**</bpt>Käyttäjäparametrit<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Toimi <bpt id="p1">**</bpt>Käyttäjäparametrit<ept id="p1">**</ept>-valintaikkunan <bpt id="p2">**</bpt>Suorituksen jäljitys<ept id="p2">**</ept> -osassa seuraavasti:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>Suorituksen jäljitys muoto<ept id="p1">**</ept> -kentässä <bpt id="p2">**</bpt>Korjaa jäljitystiedosto<ept id="p2">**</ept> -kentässä, joka alkaa keräämään tietoja ER-muodon suorittamisesta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kun tämä arvo valitaan, suorituskyvyn jäljitys kerää seuraaviin toimiin kuluvaa aikaa koskevia tietoja:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kunkin tietolähteen suorittamista mallikartoituksista, joita kutsutaan tietojen hakemiseksi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kunkin muotoilunimikkeen käsitteleminen siten, että se syöttää tietoja luotavalle tulosteelle</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Suorituksen jäljitysmuoto<ept id="p1">**</ept> -kentän avulla voit määrittää sen luodun suorituskykyjäljityksen muodon, johon suoritustiedot tallennetaan ER-ja Mapping-elementeissä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kun valitset arvoksi <bpt id="p1">**</bpt>Virheen korjauksen jäljitysmuodon<ept id="p1">**</ept>, pystyt analysoimaan jäljityksen sisältöä ER Operation Designerissa ja näkemään ER-muodon tai määrityselementit, jotka mainitaan jäljityksessä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Määritä seuraavat asetukset: <bpt id="p1">**</bpt>Kyllä<ept id="p1">**</ept>, jos haluat kerätä tarkempia tietoja ER-mallin kartoituksesta ja ER-muotokomponenttien suorittamisesta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kyselyn tilastotietojen kerääminen<ept id="p1">**</ept> – Kun tämä vaihtoehto on käytössä, suorituskyvyn jäljitys kerää seuraavat tiedot:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tietolähteiden tekemien kutsujen määrä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Tietokantaan lisättyjen toistettujen kutsujen määrä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tietokantakutsujen tekemiseen käytettävien SQL-lauseiden tiedot</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Jäljitysvälimuistin käyttäminen<ept id="p1">**</ept> – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja ER-mallikartoituksen välimuistin käytöstä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Jäljitystietojen käyttö<ept id="p1">**</ept> – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Jäljitystietojen luettelointi<ept id="p1">**</ept> – Kun tämä asetus on käytössä, suorituskyvyn jäljitys kerää tietoja siitä, kuinka monta käyntiä tietokantaan on tehty tietueluettelotyypin suoritettavissa tietolähteissä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Käyttäjäparametrit<ept id="p1">**</ept> -valintaikkunan parametrit koskevat käyttäjää ja nykyistä yritystä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Käyttäjäparametrit-valintaikkuna Finance and Operationsissa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Suorita ER-muoto</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source><target logoport:matchpercent="66" state="translated" state-qualifier="fuzzy-match">Valitse <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept>-yritys Finance and Operationsissa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">Siirry kohtaan <bpt id="p1">**</bpt>Organisaation hallinto <ph id="ph1">\&gt;</ph> Sähköinen raportointi <ph id="ph2">\&gt;</ph> Konfiguraatiot<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Valitse <bpt id="p1">**</bpt>Konfiguraatiot<ept id="p1">**</ept>-sivulla konfiguraatiopuussa <bpt id="p2">**</bpt>Suorituskyvyn jäljitysmuodon<ept id="p2">**</ept> nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Valitse toimintoruudussa <bpt id="p1">**</bpt>Suorita<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että luotu tiedosto sisältää tietoja kuuden toimittajan 265-tapahtumista.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorituksen jäljityksen tarkasteleminen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Vie luotu jäljitys Finance and Operationsista</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorituskykyjäljet irrotetaan lähde-ER-muodosta, ja ne voidaan sarjoittaa ulkoiseen zip-tiedostoon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match">Valitse Finance and Operationsissa <bpt id="p1">**</bpt>Organisaation hallinto <ph id="ph1">\&gt;</ph> Sähköinen raportointi <ph id="ph2">\&gt;</ph> Määritysten virheenkorjauslokit<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="0" state="translated">Valitse <bpt id="p1">**</bpt>Sähköisen raportoinnin ajon lokit<ept id="p1">**</ept> -sivun vasemmanpuoleisen ruudun <bpt id="p2">**</bpt>Konfiguration nimi<ept id="p2">**</ept> -kentässä <bpt id="p3">**</bpt>Suorituskyvyn jäljitysmuoto<ept id="p3">**</ept> jos haluat löytää lokitiedostot, jotka on luotu <bpt id="p4">**</bpt>Suoritus kyvyn jäljitysmuodon<ept id="p4">**</ept> konfiguraatiolle.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">Valitse <bpt id="p1">**</bpt>Liitteet<ept id="p1">**</ept>-painikkeen sivun oikeassa yläkulmassa (paperiliitinsymboli) tai paina <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Liitteet-painike sähköisen raportoinnin ajon lokit -sivulla Finance and Operationsissa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Valitse sähköisen raportoinnin ajon lokit<ept id="p1">**</ept> -sivun toimintoruudussa <bpt id="p2">**</bpt>Avaa<ept id="p2">**</ept>, jos haluat saada suorituskyvyn jäljityksen zip-tiedostona ja tallentaa sen paikallisesti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Liitteet sähköisen raportoinnin ajon lokit -sivulla Finance and Operationsissa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Luotu jäljitys viittaa lähde-ER-raporttiin yksilöivän raporttitunnuksen avulla vain <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept>-muodossa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Muodon versionumerointia ei oteta huomioon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että suoritetun ER-muodon ja ER-mallikartoituksen muodostaman suorituskyvyn jäljittämisen välinen yhteys perustuu käytössä olevaan juurihakemistoon ja yhteiseen tietomalliin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Muodon versionumerointia ja mallin yhdistämistä ei oteta huomioon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Mallimerkinnän <bpt id="p1">**</bpt>oletusarvoa mallimerkintää varten<ept id="p1">**</ept> ei myöskään oteta huomioon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Tuo tuotettu jälki RCS:ään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">Valitse RCS:ssä <bpt id="p1">**</bpt>Sähköisen raportoinnin<ept id="p1">**</ept> työtilassa <bpt id="p2">**</bpt>Raportointimääritykset<ept id="p2">**</ept>-ruutu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Laajenna <bpt id="p1">**</bpt>Konfiguraatiot<ept id="p1">**</ept>-sivun konfiguraatiopuussa <bpt id="p2">**</bpt>Suorituskyvyn jäljitysmalli<ept id="p2">**</ept> -nimike ja valitse <bpt id="p3">**</bpt>Suorituskyvyn seurannan muoto<ept id="p3">**</ept> -nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Valitse toimintoruudussa <bpt id="p1">**</bpt>Suunnittelija<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Valitse <bpt id="p1">**</bpt>Muodon suunnittelija<ept id="p1">**</ept>-sivulla hallintapaneelista <bpt id="p2">**</bpt>Suorituskyvyn jäljitysmuoto<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>Suorituskyvyn jäljitystulosten asetukset<ept id="p1">**</ept> -valintaikkunasta <bpt id="p2">**</bpt>Tuo suorituskyvyn jäljitys<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>Selaa<ept id="p1">**</ept> ja valitse zip-tiedosto, jonka olet vienyt Finance and Operationsista aiemmin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorituskyvyn jäljitystulosten asetukset -valintaikkuna RCS-kohteessa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorituskyvyn seurannan käyttäminen RCS – Format -suoritusanalyysissä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Laajenna kaikkien muotoilukohteiden sisältö valitsemalla <bpt id="p1">**</bpt>Laajenna/tiivistä<ept id="p1">**</ept>-vaihtoehto <bpt id="p2">**</bpt>Muodon suunnittelija<ept id="p2">**</ept>-sivulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että joistakin nykyisen muodon kohteista näytetään lisätietoja:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Todellinen aika, joka käytettiin tietojen syöttämiseen luotuun tulosteeseen kohteen muotoilun avulla</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko tuotoksen tuottamiseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Muodon suunnittelutoiminto -sivu RCS:ssä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="0" state="translated">Sulje <bpt id="p1">**</bpt>Muodon suunnittelutoiminto<ept id="p1">**</ept> -sivu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Valitse RCS:ssä <bpt id="p1">**</bpt>Konfiguraatiot<ept id="p1">**</ept>-sivulla konfiguraatiopuussa <bpt id="p2">**</bpt>Suorituskyvyn jäljitysmääritys<ept id="p2">**</ept> -nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="85" state="translated" state-qualifier="leveraged-inherited">Valitse toimintoruudussa <bpt id="p1">**</bpt>Suunnittelija<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Suunnittelu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Valitse <bpt id="p1">**</bpt>Mallin määrityssuunnittelija<ept id="p1">**</ept> -sivulla hallintapaneelista <bpt id="p2">**</bpt>Suorituskyvyn jäljitysmuoto<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse aiemmin tuotu jäljitys.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että joidenkin nykyisen mallimääritysten tietolähdenimikkeiden käytettävissä on uusia tietoja:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tietolähteen avulla tietoja haettaessa käytetty todellinen aika</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Sama aika ilmaistaan prosentteina kokonaisajasta, joka käytettiin koko mallin määrityksen suorittamiseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että ER ilmoittaa, että nykyisen mallin yhdistämismääritys kopioi tietokantapyynnöt, kun VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans<ph id="ph2">\_</ph>. VendTable AccountNum-tietolähde suoritetaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämä päällekkäisyys johtuu siitä, että toimittajatapahtumien luetteloa kutsutaan kaksi kertaa kutakin iteroitua toimittajatietuetta varten:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Yksi kutsu tehdään tietomallin kunkin tapahtuman tietojen syöttämiseen määritettyjen sidosten perusteella.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Yksi kutsu tehdään, kun toimittaja määrittää lasketun määrän tapahtumia toimittajakohtaisesti tietomallissa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Virheilmoitus tietokantapyyntöjen kopioista RCS-mallin malli kartoituksen suunnittelusivulla</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Arvo <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> ilmaisee, että VendTrans-taulua kutsuttiin 530 kertaa palauttamaan kyseisessä taulussa oleva tietue VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans. VendTable<ph id="ph4">\_</ph>AccountNum-tieto lähteeseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Arvo <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> ilmaisee, että VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans. VendTable<ph id="ph4">\_</ph>AccountNum-tietolähdettä kutsuttiin 530 kertaa palaamaan, jolloin tietue palautetaan kyseiseen tietolähteeseen ja sen tiedot syötetään tietomalliin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suosittelemme, että käytät VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans. VendTable<ph id="ph2">\_</ph>AccountNum-tietolähteen välimuistia, jotta voit vähentää 265-tapahtumien tietojen saamiseksi tehtyjen kutsujen määrää ja parantaa mallimäärityksen suorituskykyä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Voi myös olla hyödyllistä vähentää LedgerTransTypeList-tietolähteeseen tehtyjen kutsujen määrää.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tätä tietolähdettä käytetään liittämään kaikki <bpt id="p1">**</bpt>lLedgerTransType<ept id="p1">**</ept>-luetteloinnin arvot sen otsikkoon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Käyttämällä tätä tietolähdettä voit löytää asianmukaisen tunnisteen ja syöttää sen kunkin toimittajatapahtuman tietomalliin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tähän tietolähteeseen soitettujen kutsujen määrä (9 027) on melko suuri 265-tapahtumissa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Mallin määrityksen suunnittelijasivu RCS:ssä näyttää 9 027 puhelua tietolähteeseen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Paranna mallin määritystä suorituksen jälkeisten tietojen perusteella</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Mallin määrityksen logiikan muokkaaminen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraavia ohjeita noudattamalla voit käyttää välimuistia, joka estää kaksoissoittoja tietokantaan:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse RCS:ssä <bpt id="p1">**</bpt>Mallin määrityksen suunnittelu<ept id="p1">**</ept> -sivun <bpt id="p2">**</bpt>Tietolähteet<ept id="p2">**</ept>-ruudusta <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept>-nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>Välimuisti<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source><target logoport:matchpercent="0" state="translated">Laajenna <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept>-nimike, laajenna VendTable-tietolähde ( <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Suhde<ept id="p2">**</ept>-nimike), yksi-moneen-suhteiden luettelo ja valitse <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept>-nimike</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Valitse <bpt id="p1">**</bpt>Välimuisti<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Asetusten tallentaminen välimuistiin, jotta kaksinkertaiset kutsut voidaan estää</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Siirrä LedgerTransTypeList-tietolähde VendTable-tietolähteen käyttöalueeseen seuraavasti:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Laajenna <bpt id="p1">**</bpt>Tietolähdetyypit<ept id="p1">**</ept>-ruudussa <bpt id="p2">**</bpt>Funktiot<ept id="p2">**</ept>-nimike ja valitse <bpt id="p3">**</bpt>Laskettu kenttä<ept id="p3">**</ept> -nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>Tietolähteet<ept id="p1">**</ept>-ruudusta <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>-nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Lisää<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Kirjoita <bpt id="p1">**</bpt>Nimi<ept id="p1">**</ept>-kenttään <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Valitse <bpt id="p1">**</bpt>Muokkaa kaavaa<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">Kirjoita <bpt id="p1">**</bpt>Kaava<ept id="p1">**</ept>-kenttään <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Tallenna<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sulje <bpt id="p1">**</bpt>Kaavaeditori<ept id="p1">**</ept>-sivu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorita <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>-kentän tallentaminen välimuistiin seuraavien vaiheiden mukaisesti:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source><target logoport:matchpercent="0" state="translated">Valitse <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept>-nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Valitse <bpt id="p1">**</bpt>Välimuisti<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept>-nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Valitse <bpt id="p1">**</bpt>Välimuisti<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">$TransType-kentän asetusten tallentaminen välimuistiin</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Näiden vaiheiden avulla voit muuttaa <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept>-kenttää siten, että se alkaa käyttää välimuistissa olevaa <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept>-kenttää:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Laajenna <bpt id="p1">**</bpt>Tietolähteet<ept id="p1">**</ept>-ruudussa <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept>-nimike, laajenna <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Suhteet<ept id="p3">**</ept>-nimike, laajenna <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept>-nimike ja valitse <bpt id="p5">**</bpt>VendTable. VendTrans. VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>Transtyperecord<ept id="p5">**</ept> -nimike.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Muokkaa<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Valitse <bpt id="p1">**</bpt>Muokkaa kaavaa<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Etsi <bpt id="p1">**</bpt>Kaava<ept id="p1">**</ept>-kentästä seuraava lauseke:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Syötä <bpt id="p1">**</bpt>Kaava<ept id="p1">**</ept>-kenttään seuraava lauseke:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Tallenna<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Sulje <bpt id="p1">**</bpt>Kaavaeditori<ept id="p1">**</ept>-sivu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Tallenna<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="0" state="translated">Sulje <bpt id="p1">**</bpt>Mallimäärityksen sunnittelun<ept id="p1">**</ept> sivu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">Sulje <bpt id="p1">**</bpt>Mallimääritykset<ept id="p1">**</ept>-sivu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER-mallin yhdistämismäärityksen muokatun version täydentäminen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="0" state="translated">Valitse RCS-järjestelmän <bpt id="p1">**</bpt>Konfiguraatiot<ept id="p1">**</ept>-sivun <bpt id="p2">**</bpt>Versiot<ept id="p2">**</ept>-pikavälilehdessä <bpt id="p3">**</bpt>Suorituskyvyn jäljityksen<ept id="p3">**</ept> määrityksen versio <bpt id="p4">**</bpt>1.2<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">Valitse <bpt id="p1">**</bpt>Muutoksen tila<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">Valitse <bpt id="p1">**</bpt>Valmis<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tuo muutettu ER-mallin kartoitusmääritys RCI:sta Finance and Operationsiin</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tuo tämän jakson aikaisemmissa osissa esitetyt vaiheet <bpt id="p1">[</bpt>Tuo ER-konfiguraatio RCS:stä Finance and Operationsiin<ept id="p1">](#import-configuration)</ept> tuodaksesi <bpt id="p2">**</bpt>Suorituskyvyn jäljityskartoitus<ept id="p2">**</ept> -konfiguraation versiot 1.2 Finance and Operationsiin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">Muokatun ER-ratkaisun suorittaminen jäljityksen suorittamista varten</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Suorita ER-muoto</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Luo uusi suoritusjälki <bpt id="p1">[</bpt>Suorita ER-muoto<ept id="p1">](#run-format)</ept> toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Suorituksen jäljityksen tarkasteleminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Vie luotu jäljitys Finance and Operationsista</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Toista aiemmin tässä aiheessa kerrotut jakson vaiheet <bpt id="p1">[</bpt>Valitse luotu jälki Finance and Operationsista<ept id="p1">](#export-trace)</ept> jos haluat tallentaa uuden suoritusjäljen paikallisesti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Tuo tuotettu jälki RCS:ään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Toista tässä osassa aiemmin kerrotut vaiheet <bpt id="p1">[</bpt>Tuo luodut jäljet RCS<ept id="p1">](#import-trace)</ept> tuodaksesi uudet suorituskykyjäljet RCS:ään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorita aiemmin tämän ohjeaiheen <bpt id="p1">[</bpt>Suorituskyvyn seurannan käyttäminen RCS:ssä – Mallin määritys<ept id="p1">](#use-trace)</ept> -osassa kuvatut suorituskyvyn jäljitys -kohdan vaiheet, kun haluat analysoida viimeisimmän suorituskyvyn jäljityksen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että mallimääritykseen tehdyt oikaisut ovat poistaneet tietokannasta päällekkäisiä kyselyitä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämän mallimäärityksen tietokantataulukoihin ja tietolähteisiin tehtyjen kutsujen määrä on myös vähennetty.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Näin ollen koko ER-ratkaisun suorituskyky on parantunut.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Jäljitä tietoja VendTable-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jäljitystiedoissa VendTable-tietolähteen arvo <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> ilmaisee, että tätä tietolähdettä kutsuttiin 12 kertaa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Arvo <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> ilmaisee, että tietokantakutsuille on käännetty kuusi kutsua VendTable-tauluun.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Arvo <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> ilmaisee, että tietokannasta noudetut tiedot tallennettiin välimuistiin ja kuusi muuta kutsua käsiteltiin välimuistin avulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että LedgerTransTypeList-tietolähteeseen soitettujen kutsujen määrä on vähentynyt 9 027:sta 240:een.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Jäljitä tietoja LedgerTransTypeList-tietolähteestä RCS-mallin mallinmäärityssuunnittelija-sivulta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorituksen jäljityksen tarkasteleminen Finance and Operationsissa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS-ohjelman lisäksi jotkin Finance and Operations -versiot voivat tarjota ER-kehyssuunnittelijakokemuksen ominaisuuksia.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Näissä Finance and Operations -versioissa on <bpt id="p1">**</bpt>Ota käyttöön suunnittelutila<ept id="p1">**</ept> -vaihtoehto, joka voidaan ottaa käyttöön.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämä vaihtoehto löytyy <bpt id="p1">**</bpt>Sähköisen raportoinnin parametrit<ept id="p1">**</ept> -sivun <bpt id="p2">**</bpt>Yleiset<ept id="p2">**</ept>-välilehdestä, jonka voit avata <bpt id="p3">**</bpt>Sähköisen raportoinnin<ept id="p3">**</ept> työtilassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ota suunnittelutilan vaihtoehto käyttöön Finance and Operationsin sähköisen raportoinnin parametrit -sivulla</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos käytät jotakin näistä Finance and Operations -versioista, voit analysoida luotuja suorituskykytietoja suoraan Finance and Operationsissa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sinun ei tarvitse viedä niitä Finance and Operationsista ja tuoda niitä RCS-järjestelmään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Suorituksen jäljityksen tarkasteleminen ulkoisten työkalujen avulla</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Konfiguroi käyttäjäparametrit</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Valitse Finance and Operationsissa <bpt id="p1">**</bpt>Organisaation hallinto <ph id="ph1">\&gt;</ph> Sähköinen raportointi <ph id="ph2">\&gt;</ph> Määritykset<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited">Valitse <bpt id="p1">**</bpt>Määritykset<ept id="p1">**</ept>-sivun toimintoruudun <bpt id="p2">**</bpt>Määritykset<ept id="p2">**</ept>-välilehden <bpt id="p3">**</bpt>Lisämääritykset<ept id="p3">**</ept>-ryhmässä <bpt id="p4">**</bpt>Käyttäjäparametrit<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valitse <bpt id="p1">**</bpt>Käyttäjäparametrit<ept id="p1">**</ept> -valintaikkunan <bpt id="p2">**</bpt>Suorituksen jäljitys<ept id="p2">**</ept> -osan <bpt id="p3">**</bpt>Suorituksen jäljitys muoto-osan<ept id="p3">**</ept> -kentässä <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Suorita ER-muoto</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Luo uusi suoritusjälki <bpt id="p1">[</bpt>Suorita ER-muoto<ept id="p1">](#run-format)</ept> toistamalla tämän aiheen aikaisemmissa jaksoissa esitetyt vaiheet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Huomaa, että Internet-selain tarjoaa zip-tiedoston ladattavaksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämä tiedosto sisältää suorituskyvyn jäljityksen PerfView-muodossa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämän jälkeen voit analysoida ER Format Execution -toiminnon tietoja Perxview-suorituskyvyn analysointityökalun avulla.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>