<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="fi-FI">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="0" state="translated">Jaetun tilausten hallinnan (JTH) kustannusten määrittäminen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tässä aiheessa kuvataan Microsoft Dynamics 365 for Retail -sovelluksen jaetun tilausten hallinnan (JTH) toimintojen kustannusten määrittämistä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Jaetun tilausten hallinnan (JTH) kustannusten määrittäminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Organisaatiot käyttävät useita kustannuskomponentteja tilauksen täyttämisen optimaalisen sijainnin määrittämisessä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kustannuskomponentteja ovat esimerkiksi lähetys-, käsittely- ja pakkauskustannukset.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Näiden kustannusten yhteenlaskettu kustannus määrittää tilauksen täyttämissijainnin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="0" state="translated">Kun Microsoft Dynamics 365 for Retail -sovelluksen jaetun tilausten hallinnan (JTH) ensimmäinen iteraatio optimoi tilausten määrityksen täyttämissijainteihin, se otetaan huomioon vain etäisyytenä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Vaikka etäisyys voi korreloida kustannuksen kanssa, se ei ole sama kuin kustannus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Esimerkiksi lähetystapa yön yli maksaa enemmän kuin kolmen tai seitsemän päivän lähetys samalla etäisyydellä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="0" state="translated">Kustannusten määritystoiminnon avulla jälleenmyyjät voivat määrittää lisäkustannuskomponentteja, jotka lasketaan ja otetaan huomioon tilausrivien toteuttamisessa käytettävän optimaalisen sijainnin määrittämisessä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kun kustannuskomponentit määritetään, JTH:n selvitystoiminto käyttää vain näitä kustannusten määrityksiä tilauksen toteuttamisen optimaalisen sijainnin määrittämisessä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Se ei ota huomioon etäisyyskomponenttia kustannuksena.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos kustannuskomponentteja ei kuitenkaan määritetä, JTH:n selvitystoiminto käyttää etäisyyskomponenttia kustannuksessa tilauksen toteuttamisen optimaalisen sijainnin määrittämisessä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Kustannuskomponenttien määrittäminen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">Järjestelmässä voidaan määrittää kaksi pääkustannuskomponenttia: <bpt id="p1">**</bpt>lähetys<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>muu<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Molemmat kustannuskomponentin tyypit tukevat useita laskentaperusteita seuraavassa taulukossa esitetyllä tavalla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kustannuskomponentin tyyppi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Laskuperuste</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Lähetys</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Yksinkertainen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Porrastettu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Muu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Myyntitilaus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Myyntirivi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Sijainti</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Lähetyskustannuskomponentin tyyppi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="0" state="translated">Tässä osassa kerrotaan, miten kunkin <bpt id="p1">**</bpt>lähetys<ept id="p1">**</ept>kustannuskomponentin tyypin ja lähetyskustannusten laskentaperusteen yhdistelmä määritetään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Osassa kerrotaan myös, miten JTH:n selvitystoiminto käyttää kutakin yhdistelmää.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="0" state="translated">Kustannuskomponentin tyyppi = lähetys ja laskentaperuste = yksinkertainen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="0" state="translated">Jos käytetään <bpt id="p1">**</bpt>lähetys<ept id="p1">**</ept>kustannuksen tyyppiä ja <bpt id="p2">**</bpt>yksinkertaista<ept id="p2">**</ept> laskentaperustetta, toimitustavan lähetyskustannukset perustuvat kiinteään kustannukseen tai etäisyyteen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tälle yhdistelmälle on määritettävä seuraavat kentät:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kustannustekijä<ept id="p1">**</ept> – Anna kustannustekijän yksilöivä tunniste.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kuvaus<ept id="p1">**</ept> – Anna kustannustekijän nimi ja kuvaus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Alkamis<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>päättymispäivä<ept id="p2">**</ept> – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Aktiivinen<ept id="p1">**</ept> – Osoittaa, onko kustannustekijä aktiivinen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Yritys<ept id="p1">**</ept> – Määritä yritys, jolle kustannustekijä on määritetty.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kaikkien laskentakriteerien rivien on koskettava samaa yritystä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Toimitustavat<ept id="p1">**</ept> – Määritä toimitustavat, joille kustannus on määritetty.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Laskentatyyppi<ept id="p1">**</ept> – Määritä, miten tietyn toimitustavan kustannus lasketaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tuettuja laskentatyyppejä on kaksi:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kiinteä<ept id="p1">**</ept> – Toimitustavassa käytetään kiinteää kustannusta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos valitset tämän laskentatyypin, <bpt id="p1">**</bpt>Kustannus<ept id="p1">**</ept>-kenttä määrittää kiinteän kustannuksen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Etäisyysyksikköä kohti<ept id="p1">**</ept> – Toimitustavan kustannus lasketaan kustannuksen arvona. Se määritetään kertomalla <bpt id="p2">**</bpt>Kustannus<ept id="p2">**</ept>-kentän arvo toimitusosoitteen ja sijaintien etäisyydellä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kustannus<ept id="p1">**</ept> – Määritä kustannusarvo, jota käytetään yhdessä <bpt id="p2">**</bpt>Laskentatyyppi<ept id="p2">**</ept>-kentän arvon kanssa, kun toimitustavan kustannus lasketaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Kustannuskomponentin tyyppi = lähetys ja laskentaperuste = porrastettu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">Jos käytetään <bpt id="p1">**</bpt>lähetys<ept id="p1">**</ept>kustannuksen tyyppiä ja <bpt id="p2">**</bpt>porrastettua<ept id="p2">**</ept> laskentaperustetta, toimitustavan lähetyskustannukset perustuvat kiinteään kustannukseen tai etäisyyteen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tässä yhdistelmässä etäisyys perustuu kuitenkin etäisyyksien porrastettuun väliin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tälle yhdistelmälle on määritettävä seuraavat kentät:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kustannustekijä<ept id="p1">**</ept> – Anna kustannustekijän yksilöivä tunniste.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kuvaus<ept id="p1">**</ept> – Anna kustannustekijän nimi ja kuvaus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Oletuskustannus<ept id="p1">**</ept> – Määritä kustannus, jota käytetään toimitustavassa silloin, kun toimitusosoitteen ja sijainnin etäisyys ei ole mikään toimitustavan porrastetuista etäisyyksistä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alkamis<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>päättymispäivä<ept id="p2">**</ept> – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivinen<ept id="p1">**</ept> – Osoittaa, onko kustannustekijä aktiivinen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Yritys<ept id="p1">**</ept> – Määritä yritys, jolle kustannustekijä on määritetty.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Kaikkien laskentakriteerien rivien on koskettava samaa yritystä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Toimitustavat<ept id="p1">**</ept> – Määritä toimitustavat, joille kustannus on määritetty.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Etäisyyden tyyppi<ept id="p1">**</ept> – Määritä, onko porrastettu etäisyys määritetty linnuntietä vai teitä pitkin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Etäisyyden yksiköt<ept id="p1">**</ept> – Määritä yksikkö, jossa porrastettu etäisyys mitataan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Etäisyys kohteesta<ept id="p1">**</ept> – Määritä porrastetun etäisyyden aloitusalue.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Etäisyys kohteeseen<ept id="p1">**</ept> – Määritä porrastetun etäisyyden lopetusalue.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Laskentatyyppi<ept id="p1">**</ept> – Määritä, miten tietyn toimitustavan ja porrastetun etäisyyden kustannus lasketaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tuettuja laskentatyyppejä on kaksi:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kiinteä<ept id="p1">**</ept> – Toimitustavassa käytetään kiinteää kustannusta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jos valitset tämän laskentatyypin, <bpt id="p1">**</bpt>Kustannus<ept id="p1">**</ept>-kenttä määrittää kiinteän kustannuksen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Etäisyysyksikköä kohti<ept id="p1">**</ept> – Toimitustavan ja porrastetun etäisyyden kustannus lasketaan kustannuksen arvona. Se määritetään kertomalla <bpt id="p2">**</bpt>Kustannus<ept id="p2">**</ept>-kentän arvo toimitusosoitteen ja sijaintien etäisyydellä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kustannus<ept id="p1">**</ept> – Määritä kustannusarvo, jota käytetään yhdessä <bpt id="p2">**</bpt>Laskentatyyppi<ept id="p2">**</ept>-kentän arvon kanssa, kun toimitustavan kustannus lasketaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kun määrität porrastetut etäisyydet, järjestelmä tarkistaa, että etäisyyksiä ei puutu ja että ne eivät ole päällekkäisiä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Toimitustavassa käytettävän etäisyyden tyypin on oltava sama kaikissa porrastetuissa etäisyyksissä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Muu kustannuskomponentin tyyppi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tässä osassa kerrotaan, miten kunkin <bpt id="p1">**</bpt>muun<ept id="p1">**</ept> kustannuskomponentin tyypin ja muun kuin lähetyskustannusten muun kustannustyypin laskentaperusteen yhdistelmä määritetään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Osassa kerrotaan myös, miten JTH:n selvitystoiminto käyttää kutakin yhdistelmää.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="0" state="translated">Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = myyntitilaus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Muun<ept id="p1">**</ept> kustannuskomponentin tyypin ja <bpt id="p2">**</bpt>myyntitilauksen<ept id="p2">**</ept> muun kustannuksen tyypin yhdistelmää käytetään määritettäessä muita kuin lähetyskustannuksia myyntitilauksen tasolla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tälle yhdistelmälle on määritettävä seuraavat kentät:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kustannustekijä<ept id="p1">**</ept> – Anna kustannustekijän yksilöivä tunniste.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kuvaus<ept id="p1">**</ept> – Anna kustannustekijän nimi ja kuvaus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alkamis<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>päättymispäivä<ept id="p2">**</ept> – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivinen<ept id="p1">**</ept> – Osoittaa, onko kustannustekijä aktiivinen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kustannus<ept id="p1">**</ept> – Määritä muiden kuin lähetyskustannusten kustannusarvo myyntitilauksen tasolla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = myyntirivi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Muun<ept id="p1">**</ept> kustannuskomponentin tyypin ja <bpt id="p2">**</bpt>myyntirivin<ept id="p2">**</ept> muun kustannuksen tyypin yhdistelmää käytetään määritettäessä muita kuin lähetyskustannuksia myyntitilausrivin tasolla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tälle yhdistelmälle on määritettävä seuraavat kentät:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kustannustekijä<ept id="p1">**</ept> – Anna kustannustekijän yksilöivä tunniste.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kuvaus<ept id="p1">**</ept> – Anna kustannustekijän nimi ja kuvaus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alkamis<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>päättymispäivä<ept id="p2">**</ept> – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivinen<ept id="p1">**</ept> – Osoittaa, onko kustannustekijä aktiivinen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Kustannus<ept id="p1">**</ept> – Määritä muiden kuin lähetyskustannusten kustannusarvo myyntitilausrivin tasolla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Kustannuskomponentin tyyppi = muu ja muun kustannuksen tyyppi = sijainti</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Muun<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>sijainnin<ept id="p2">**</ept> muun kustannustyypin yhdistelmää käytetään sijaintiryhmien tai yksittäisen sijainnin muiden kuin lähetyskustannusten määrittämisessä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tälle yhdistelmälle on määritettävä seuraavat kentät:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kustannustekijä<ept id="p1">**</ept> – Anna kustannustekijän yksilöivä tunniste.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Kuvaus<ept id="p1">**</ept> – Anna kustannustekijän nimi ja kuvaus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Alkamis<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>päättymispäivä<ept id="p2">**</ept> – Näiden kenttien avulla kustannustekijän voi rajata koskemaan tiettyä ajanjaksoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Jos nämä kentät jätetään tyhjiksi, kustannustekijä on voimassa toistaiseksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktiivinen<ept id="p1">**</ept> – Osoittaa, onko kustannustekijä aktiivinen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">JTH ottaa huomioon vain aktiiviset täyttämisprofiilin liitetyt kustannustekijät.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Täyttämisryhmä<ept id="p1">**</ept> – Määritä niiden sijaintien ryhmä, joille muun kuin lähetyksen kustannus määritetään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Täyttämissijainti<ept id="p1">**</ept> – Määritä se sijainti, jolle muun kuin lähetyksen kustannus määritetään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Et voi määrittää täyttämisryhmää ja -sijaintia samalle sijaintiin perustuvalle laskentakriteerien riville.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>Kustannus<ept id="p1">**</ept> – Määritä muun kuin lähetyskustannuksen kustannusarvo täyttämisryhmän tai täyttämissijainnin tasolla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lisää kustannustekijä soveltuvaan täyttämisprofiiliin, jotta JTH voi käyttää näitä kustannuksia suorittamisen aikana.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>