<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="work-with-store-inventory.md" target-language="fi-FI">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>work-with-store-inventory.418f90.551a8408aa730bc1916f1c57b7cfd773966ce8bf.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>551a8408aa730bc1916f1c57b7cfd773966ce8bf</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\work-with-store-inventory.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myymälän varastonhallinta</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the types of documents that you can use to manage inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä ohjeaiheessa käsitellään asiakirjatyyppejä, joiden avulla hallitaan varastoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myymälän varastonhallinta</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When working with inventory in Dynamics 365 for Retail and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun varastoa käsitellään Dynamics 365 for Retailissa ja käytössä on myyntipistesovellus, on tärkeää muistaa, että myyntipiste tukee vain rajoitetusti varastodimensioita ja tiettyjä varastonimiketyyppejä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The POS solution does not support the following item configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteratkaisu ei tue seuraavia nimikemäärityksiä:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>BOM items (except kit products, which utilize some components of the BOM framework)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tuoterakennenimikkeet (lukuun ottamatta myyntirakenteita, joissa käytetään joitakin tuoterakennekehikon osia)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Catch weight items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Todellisen painon nimikkeet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Batch-controlled items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eräohjatut nimikkeet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The POS application currently does not support the following tracking dimensions in the POS:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipistesovellus ei tue tällä hetkellä myyntipisteessä seuraavia seurantadimensioita:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Batch tracking dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Erän seurantadimensio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Owner dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omistajadimensio</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The POS solution provides limited support for the following dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteratkaisu tukee rajoitetusti seuraavia dimensioita.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rajoitettu tuki ilmaisee, että myyntipiste voi palauttaa jotkin näistä dimensioista automaattisesti varastotapahtumiksi varaston tai kaupan asetusten määritysten perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Myyntipiste ei tue dimensioita täysin sillä tavoin kuin niitä tuetaan, jos myyntitapahtuma viedään manuaalisesti ERP:hen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Warehouse Location<ept id="p1">**</ept> – Users will not have the ability to manage the receiving warehouse location for items received into a store warehouse when the store has not been configured to use the warehouse management process.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Fyysisen varastoinnin sijainti<ept id="p1">**</ept> – Käyttäjillä ei ole mahdollisuutta hallita vastaanottovaraston sijaintia nimikkeille, jotka on vastaanotettu myymälävarastoon, kun säilöä ei ole konfiguroitu käyttämään varastonhallintaprosessia.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A default receiving location defined on the store warehouse will be used for these items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näille nimikkeille käytetään myymälän varastossa määritettyä oletusarvoista vastaanottosijaintia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If the warehouse management process has been enabled for the store, limited support that prompts the user to choose a receiving location for the entire receipt will be triggered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos varastonhallintaprosessi on otettu käyttöön myymälälle, järjestelmä käynnistää rajoitetun tuen, joka pyytää käyttäjää valitsemaan vastaanottopaikan koko kuittiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Items sold from the store will always be sold out of the default retail location as defined on the store warehouse setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myymälästä myydyt nimikkeet myydään aina oletusarvoiseen vähittäismyyntisijaintiin, joka on määritetty myymälän varaston määrityksissä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The location for managing return inventory can be controlled through default return location definition on the store warehouse or based on return reason codes as defined in the return location policy.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Palautettavan varaston hallinnan sijaintia voidaan hallita myymälävaraston oletusarvon mukaisen palautuksen sijaintimäärityksen avulla tai palautusten syykoodien perusteella, jotka on määritetty palautuksen sijaintikäytännössä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>License plate<ept id="p1">**</ept> – License plates are only applicable when <bpt id="p2">**</bpt>Use warehouse management process<ept id="p2">**</ept> has been enabled on the item and the store warehouse.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Rekisterikilpi<ept id="p1">**</ept> – Rekisterikilvet ovat käytössä vain, kun <bpt id="p2">**</bpt>Käytä varastonhallintaprosesseja<ept id="p2">**</ept> on otettu käyttöön nimikkeessä ja kaupan varastossa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In POS, if inventory is received into a store warehouse where the warehouse management process has been enabled, and the location chosen to receive the item into is tied to a location profile that requires license plate control, the POS application will systematically apply a license plate to the receiving line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipistesovelluksessa, jos varasto vastaanotetaan myymälävarastoon, jossa varaston hallintaprosessi on otettu käyttöön, ja jos nimikkeen vastaanottamiselle valittu sijainti on sidottu sijaintiprofiiliin, joka edellyttää rekisterikilpiohjausta, myyntipistesovellus käyttää vastaanottavan rivin rekisterikilpeä järjestelmällisesti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Users in POS will not have the ability to change or manage this license plate data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipistekäyttäjillä ei ole mahdollisuutta muuttaa tai hallita tämän rekisterikilven tietoja.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If full management of license plates is required, it is suggested the store use the WMS mobile application or the back office ERP client to manage the receipt of these items.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Jos rekisterikilpien hallinta on pakollista, myymälästä käytetään WMS-mobiilisovellusta tai Back Office ERP -asiakasohjelmaa näiden nimikkeiden vastaanottamisen hallintaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Serial number<ept id="p1">**</ept> – The POS application has limited support for single serial number to be registered on a transaction sales line for orders created in POS with serialized items.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Sarjanumero<ept id="p1">**</ept> – Myyntipistesovelluksella on rajallinen tuki yksittäiselle sarjanumerolle, joka rekisteröidään tapahtumamyyntiriville myyntipistesovelluksessa luoduille tilauksille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This serial number is not validated against registered serial numbers already in inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tätä sarjanumeroa ei ole vahvistettu varastossa jo rekisteröidyille sarjanumeroille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If a sales order is created in the call center channel or fulfilled through the ERP and multiple serial numbers are registered to a single sales line during the fulfillment process in the ERP, these serial numbers will not be able to be applied or validated if a return is processed in POS for these orders.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Jos myyntitilaus luodaan Call Center -kanavalla tai se toteutuu ERP-järjestelmän ja useiden sarjanumeroiden kautta, se kirjataan yhdelle myyntiriville ERP-järjestelmän toteutusprosessin aikana, näitä sarjanumeroita ei voida käyttää tai vahvistaa, jos palautukset käsitellään näiden tilausten myyntipisteessä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Inventory status<ept id="p1">**</ept> – For items that use the warehouse management process and require an inventory status, this status field is not able to be set or modified through the POS application.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Varaston tila<ept id="p1">**</ept> – Nimikkeille, jotka käyttävät varastonhallintaprosessia ja vaativat varastontilan, tätä tilakenttää ei voi määrittää tai muokata myyntipistesovelluksen kautta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The default inventory status as defined on the store warehouse configuration will be used when items are received into inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myymälän varaston konfiguraatiossa määritettyä varaston oletustilaa käytetään vastaanotettaessa nimikkeitä varastoon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>All organizations must test item configurations through POS in development or test environments before deploying them to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaikkien organisaatioiden on testattava nimikemääritykset myyntipisteen kehitys- tai testiympäristössä, ennen kuin ne otetaan käyttöön tuotannossa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Testaa nimikkeet suorittamalla tavallinen itsepalvelutukun myyntitapahtuma ja luomalla (tarvittaessa) nimikkeille asiakastilauksia myyntipisteessä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Testauksen on sisällettävä täydelliset laskelmien kirjaamisprosessit testiympäristössä ja sen varmistaminen, että mitään ongelmia ei esiinny.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos nimikkeet määritetään tavalla, jota myyntipistesovellus ei tue ja ilman asianmukaista testausta, voi aiheuttaa laskelmien kirjaamisprosessin epäonnistumisen tuotantoympäristössä ilman, että ongelmat voitaisiin korjata kätevästi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kumppanin tai asiakkaan sovellukseen tekemiä mukautuksia on mahdollista harkita, jotta nämä kirjausprosessit onnistuisivat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos mukautuksia ei tarvita, organisaation on varmistettava, että tuotteiden tuotemääritykset on tehty siten, että tavanomaista myyntipistesovellusta, tilausten luontia ja laskelmien kirjausprosessia tuetaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Purchase orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ostotilaukset</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Purchase orders are created at the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ostotilaukset luodaan pääkonttorilla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail through the <bpt id="p1">**</bpt>Picking/Receiving<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos vähittäismyynnin varasto sisältyy ostotilauksen otsikkoon, tilaus voidaan vastaanottaa myymälään käyttämällä Modern POS- tai Cloud POS-toimintoja Microsoft Dynamics 365 for Retailissa <bpt id="p1">**</bpt>Poiminta / vastaanottaminen<ept id="p1">**</ept> -toiminnolla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After the quantities that are received at the store are entered in the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> field in POS for the purchase order document, they can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun myymälälle vastaanotetut määrät on syötetty ostotilausasiakirjan myyntipisteen <bpt id="p1">**</bpt>vastaanota nyt<ept id="p1">**</ept> -kenttään, ne voidaan tallentaa paikallisesti tai sitoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Saving this data locally has no effect on in-stock inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näiden tietojen tallentaminen paikallisesti ei vaikuta varastossa olevaan varastoon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and just needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tallentaminen on tehtävä vain, jos käyttäjä ei ole valmis kirjaamaan vastaanottoa HQ-järjestelmään ja tarvitsee vain tavan tallentaa tilapäisesti aiemmin kirjoitetut <bpt id="p1">**</bpt>Vastaanota tiedot nyt<ept id="p1">**</ept> -tiedot.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tällöin vastaanottotiedot tallennetaan paikallisesti käyttäjän kanavatietokantaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the purchase order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun asiakirja on käsitelty <bpt id="p1">**</bpt>Toimitus<ept id="p1">**</ept>-valinnalla, <bpt id="p2">**</bpt>Vastaanota nyt<ept id="p2">**</ept> -tiedot lähetetään HQ-kohteeseen ja ostotilauksen vastaanotto kirjataan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Transfer orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Siirtotilaukset</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A transfer order can specify that a particular store is the location that items can be shipped from or the location the inventory will be received into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Siirtotilaus voi määrittää, että tietty myymälä on sijainti, josta nimikkeet voidaan toimittaa, tai varastopaikka, johon nimike saapuu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the POS user is the shipping warehouse for a transfer order, they will be able to enter <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos POS-käyttäjä on siirtotilauksen toimitusvarasto, hän voi syöttää <bpt id="p1">**</bpt>Toimitus nyt<ept id="p1">**</ept> -määriä suoraan POS:ista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The data entered by the shipping store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lähetysmyymälän syöttämiä tietoja voidaan tallentaa paikallisesti tai sitoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>When saved locally, no updates are made to the transfer order document in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun tallennetaan paikallisesti, HQ-siirtotilausasiakirjaan ei tehdä päivityksiä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Saving should be done only if the user is not ready to post the shipment to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tallentaminen on tehtävä vain, jos käyttäjä ei ole valmis kirjaamaan lähetystä HQ-järjestelmään ja tarvitsee vain tavan tallentaa tilapäisesti aiemmin kirjoitetut <bpt id="p1">**</bpt>Lähetä nyt<ept id="p1">**</ept> -tiedot.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>After the store is ready to confirm shipment, the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun myymälä on valmis vahvistamaan lähetyksen, tulee valita <bpt id="p1">**</bpt>Toimitus<ept id="p1">**</ept>-vaihtoehto.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This posts the shipment of the transfer order in HQ so that the receiving warehouse will now be able to receive against it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä kirjaa siirtotilauksen lähetyksen HQ-tilaan, jotta vastaanottava varasto voi vastaanottaa sitä vastaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the POS user is the receiving warehouse for a transfer order, they will be able to enter the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos POS-käyttäjä on siirtotilauksen vastaanottava varasto, hän voi syöttää <bpt id="p1">**</bpt>Vastaanota nyt<ept id="p1">**</ept> -määriä suoraan POS:ista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The data entered by the receiving store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vastaanottavan myymälän syöttämiä tietoja voidaan tallentaa paikallisesti tai sitoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tallentaminen on tehtävä vain, jos käyttäjä ei ole valmis kirjaamaan vastaanottoa HQ-järjestelmään ja tarvitsee tavan tallentaa tilapäisesti aiemmin kirjoitetut <bpt id="p1">**</bpt>Vastaanota tiedot nyt<ept id="p1">**</ept> -tiedot.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tällöin vastaanottotiedot tallennetaan paikallisesti käyttäjän kanavatietokantaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the transfer order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun asiakirja on käsitelty <bpt id="p1">**</bpt>Toimitus<ept id="p1">**</ept>-valinnalla, <bpt id="p2">**</bpt>Vastaanota nyt<ept id="p2">**</ept> -tiedot lähetetään HQ-kohteeseen ja siirtotilauksen vastaanotto kirjataan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It's important to note that the receiving store will be restricted to only being able to commit receive quantities that are equal to or less than shipped quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">On tärkeää huomata, että vastaanottava myymälä voi sitoutua vastaanottamaan vain määriä, jotka ovat yhtä suuria tai pienempiä kuin toimitetut määrät.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An attempt to receive quantities on a transfer order that have not previously shipped will result in errors and the receipt will not be confirmed in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yritys vastaanottaa siirtotilauksen määriä, joita ei ole aiemmin lähetetty aiheuttaa virheitä, eikä vastaanottoa vahvisteta HQ-ohjelmassa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Stock counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varaston inventoinnit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Stock counts can be either scheduled or unscheduled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varaston inventoinnit voidaan ajoittaa tai niiden ajoitus voidaan peruuttaa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ajastetut varaston inventoinnit määritetään pääkonttorilla. Ne määrittävät nimikkeet, joista on tehtävä inventointi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pääkonttori luo inventointiasiakirjan, joka voidaan vastaanottaa myymälässä, jossa todelliset käytettävissä olevat määrät syötetään Modern POS- tai Cloud POS -sovelluksessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ajoittamattomat varaston inventoinnit aloitetaan myymälässä ja todelliset käytettävissä olevat varastomäärät päivitetään Modern POS- tai Cloud POS -sovelluksessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ajoittamattomilla varaston inventoinneilla ei ole ennalta määritettyä nimikeluetteloa kuten ajoitetun varaston inventoinneilla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>When a stock count of either type is completed, it is committed and sent to the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun jompikumpi varaston inventointi on suoritettu, se vahvistetaan ja lähetetään pääkonttorille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>At the head office, the count is validated and posted as a separate step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pääkonttorissa inventointi tarkistetaan ja kirjataan erillisenä vaiheena.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Inventory lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varastohaku</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The current product quantity on hand for multiple stores and warehouses can be viewed on the <bpt id="p1">**</bpt>Inventory lookup<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nykyistä tuotteen määrää useissa myymälöissä ja varastoissa voi tarkastella <bpt id="p1">**</bpt>Varaston haku<ept id="p1">**</ept> -sivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nykyisen käytettävissä olevan määrän lisäksi luvattavissa oleva määrä (ATP) nähdään yksittäisistä myymälöistä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>To do so, select the store that you want to view the ATP for and then click <bpt id="p1">**</bpt>Show store availability<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voit tehdä tämän valitsemalla ensin myymälän, jonka ATP:tä haluat tarkastella, ja sitten <bpt id="p1">**</bpt>Näytä myymälän käytettävissä oleva määrä<ept id="p1">**</ept>.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>