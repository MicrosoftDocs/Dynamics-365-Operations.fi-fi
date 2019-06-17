<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="fi-FI">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Monikanavaiset edistyneet automaattiset kulut</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä ohjeaiheessa käsitellään Retail-kanavan tilausten lisäkulujen hallintaa edistyneiden automaattisten kuluominaisuuksien avulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Monikanavaiset edistyneet automaattiset kulut</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä ohjeaiheessa on tietoja edistyneiden automaattisten kulujen määrittämisestä ja käyttöönottamisesta. Tämä ominaisuus on käytössä Dynamics 365 for Retailin versiossa 10.0.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun edistyneet automaattiset kuluominaisuudet on otettu käyttöön, missä tahansa tuetussa Retail-kanavassa (POS, puhelinkeskus tai online) luoduissa tilauksissa voi käyttää <bpt id="p1">[</bpt>automaattisten kulujen<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> määrityksiä, jotka on määritetty ERP-sovelluksessa otsikko- ja rivitason kuluille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retailin versiota 10.0 edeltävissä versioissa <bpt id="p1">[</bpt>automaattisen kulun<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> määrityksiä voitiin käyttää vain sähköinen kaupankäynti- ja puhelinkeskuskanavissa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Versiosta 10.0 alkaen myyntipisteessä luoduissa tilauksissa voidaan käyttää automaattisten kulujen määrityksiä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tällöin tavoin sekalaiset lisäkulut voi lisätä järjestelmällisesti myyntitapahtumiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun käytössä on versiota 10.0 edeltävä versio, myyntipistekäyttäjää pyydetään lisäämään toimitusmaksu manuaalisesti myyntipisteen Lähetä kaikki- tai Lähetä valitut -tapahtuma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Vaikka sovelluksen muiden kulujen toimintoja käytetään kulujen kirjoittamiseen tilaukseen, mikään järjestelmällinen laskenta ei ole käytettävissä, sillä laskenta määrittää kulujen arvon käyttäjän antamien tietojen perusteella.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kulut voidaan lisätä vain yhtä lähetykseen liittyvänä kulukoodina eikä niitä voi juurikaan muokata tai muuttaa myyntipisteessä sen jälkeen, kun ne on luotu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lähetyskulujen lisäämiskehotuksia voi edelleen käyttää versiossa 10.0 ja sitä uudemmissa versioissa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos organisaatio ei ota <bpt id="p1">**</bpt>Edistyneet automaattiset kulut<ept id="p1">**</ept> -parametria käyttöön, myyntipisteen manuaalisen kulujen antamiskehotteet pysyvät entisellään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Edistyneen automaattisen kuluominaisuuden ansiosta myyntipistekäyttäjät saavat käyttöönsä järjestelmälliset, automaattisiin kulujen määritystaulukoihin perustuvat laskutoimitukset kaikille määritetyille muille kuluille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjät voivat myös lisätä tai muokata rajoittamatonta määrää lisäkuluja ja -maksuja minkä tahansa myyntipisteen myyntitapahtuman otsikko- tai rivitasolla (kun kyse on itsepalvelutukku- tai asiakastilauksesta).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Edistyneiden automaattisten kulujen ottaminen käyttöön</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Valitse <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Pääkonttorin asetukset <ph id="ph2">\&gt;</ph> Parametrit <ph id="ph3">\&gt;</ph> Vähittäismyynnin parametrit<ept id="p1">**</ept> -sivulla <bpt id="p2">**</bpt>Asiakastilaukset<ept id="p2">**</ept>-välilehti. Määritä <bpt id="p3">**</bpt>Kulut<ept id="p3">**</ept>-pikavälilehdessä <bpt id="p4">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p4">**</ept> -asetukseksi <bpt id="p5">**</bpt>Kyllä<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Edistyneet automaattiset kulut -parametri</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun edistyneet automaattiset kulut on otettu käyttöön, käyttäjiä ei enää pyydetä lisäämään lähetyskulua manuaalisesti kassapäätteessä Lähetä kaikille- tai Lähetä valituilla -asiakastilausta luotaessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteen tilauskulut lasketaan ja lisätään järjestelmällisesti myyntipistetapahtumaan (jos luotavan tilauksen ehtoa vastaava automaattisten kulujen taulukko löytyy).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjät voivat lisätä tai ylläpitää otsikko- tai rivitason kuluja myös manuaalisesti juuri lisättyjen myyntipisteen toimintojen kautta. Tämä ominaisuus voidaan lisätä myyntipisteen näyttöasetteluihin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun edistyneet automaattiset kulut on otettu käyttöön, aiemmin luotuja <bpt id="p2">**</bpt>kuljetusmaksukoodin<ept id="p2">**</ept> ja <bpt id="p3">**</bpt>palautettavien toimitusmaksujen<ept id="p3">**</ept> <bpt id="p1">**</bpt>vähittäismyynnin parametreja<ept id="p1">**</ept> ei enää käytetä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näitä parametreja käytetään vain, jos <bpt id="p1">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p1">**</ept> -parametrin asetuksena on <bpt id="p2">**</bpt>Ei<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista ennen tämän ominaisuuden käyttöönottoa, että olet testannut toimintoa ja kouluttanut työntekijät, sillä ominaisuus muuttaa liiketoimintaprosessia, jolla toimituskulut ja muut kulut lasketaan ja lisätään myyntipisteen myyntitilauksiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista, että tiedät, miten prosessi vaikuttaa tapahtumien luontiin myyntipisteestä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Edistyneiden automaattisten kulujen käyttöönottaminen ei juurikaan vaikuta puhelinkeskuksen ja sähköisen kaupankäynnin tilauksiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Puhelinkeskuksen ja sähköisen kaupankäynnin sovellukset toimivat samalla tavalla kuin aiemminkin, kun kyse on tilauksen lisämaksujen laskemisesta automaattisen kulutaulukoiden avulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Puhelinkeskuskanavan käyttäjät voivat jatkossakin muokata manuaalisesti mitä tahansa järjestelmän laskemaa automaattista kulua otsikko- tai rivitasolla tai lisätä manuaalisesti muita kuluja otsikko- ja rivitasolla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteen lisätyövaiheet</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Edistyneet automaattiset kulut toimivat myyntipistesovelluksessa odotustenmukaisesti vain, jos myyntipisteen uudet työvaiheet on lisätty.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nämä työvaiheet on lisättävä <bpt id="p1">[</bpt>myyntipisteen näyttöasetteluihin<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> ja otettava käyttöön myyntipistelaitteissa, kun edistyneet automaattiset kulut otetaan käyttöön.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos näitä työvaiheita ei lisätä, käyttäjät eivät voi hallita eivätkä ylläpitää muita kuluja myyntipistetapahtumissa. He eivät voi myöskään muokata eivätkä muuttaa niiden kulujen arvoja, jotka lasketaan järjestelmällisesti automaattisten kulujen määritysten perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tämän vuoksi ainakin <bpt id="p1">**</bpt>Kulujen hallinta<ept id="p1">**</ept> -työvaihe on syytä ottaa käyttöön myyntipisteen asettelussa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Uudet työvaiheet:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>142 – Kulujen hallinta<ept id="p1">**</ept> – Myyntipistekäyttäjät voivat tarkastella ja muokata tämän työvaiheen avulla myyntipisteen tapahtuman muita kuluja, jotka lisättiin joko manuaalisesti tai järjestelmällisesti automaattisten kulujen laskennan kautta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>141 – Lisää otsikon kulut<ept id="p1">**</ept> – Käyttäjä voi lisätä tällä työvaiheella otsikkotason muun kulun manuaalisesti mihin tahansa myyntipisteen myyntitapahtumaan (ja valita käytettävän kulukoodin).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>140 – Lisää rivin kulut<ept id="p1">**</ept> – Käyttäjä voi lisätä tällä työvaiheella rivitason muun kulun manuaalisesti mille tahansa myyntipisteen myyntiriville (ja valita käytettävän kulukoodin).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>143 – Laske kulut uudelleen<ept id="p1">**</ept> – Tällä työvaiheella voi laskea myyntitapahtuman kulut kokonaisuudessaan uudelleen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjän aiemmin mahdollisesti korvaavat automaattiset kulut lasketaan uudelleen nykyisen ostoskorimäärityksen perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuten muissakin myyntipisteen työvaiheissa suojausmääritysten avulla on mahdollista edellyttää esimiehen hyväksyntää ennen työvaiheen suorittamista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">On tärkeää huomata, että edellä mainitut myyntipistetoiminnot voidaan lisätä myyntipisteasetteluun myös silloin, kun <bpt id="p1">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p1">**</ept> -parametri on poistettu käytöstä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä skenaariossa organisaatiot saavat lisäetua siitä, että ne voivat tarkastella manuaalisesti lisättyjä kuluja ja muokata niitä <bpt id="p1">**</bpt>Kulujen hallinta<ept id="p1">**</ept> -toiminnolla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjät voivat käyttää myös myyntipistetapahtumien <bpt id="p1">**</bpt>Lisää otsikon kulut<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>Lisää rivin kulut<ept id="p2">**</ept> -toimintoja, kun <bpt id="p3">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p3">**</ept> -parametri on poistettu käytöstä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Laske kulut uudelleen<ept id="p1">**</ept> -toiminto ei ole yhtä hyödyllinen, jos sitä käytetään, kun <bpt id="p2">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p2">**</ept> on poistettu käytöstä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä skenaariossa mitään ei laskettaisi uudelleen ja tapahtumaan manuaalisesti lisättyjen kulujen arvoksi palautuisi 0,00 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkkejä käyttötapauksista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämän osan esimerkkitapaukset auttavat hahmottamaan automaattisten kulujen ja muiden kulujen määrityksiä ja käyttöä Retail-kanavatilausten yhteydessä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nämä esimerkit näyttävät, miten sovellus toimii, kun <bpt id="p1">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p1">**</ept> -parametri on otettu käyttöön.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Automaattisten kulujen otsikon kulujen esimerkki</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttötapausskenaario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä haluaa lisätä rahtikulut automaattisesti, kun tapahtumat luodaan jossain Retail-kanavassa, jossa tuotteet on lähetettävä asiakkaalle.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä antaa kaksi toimitusvaihtoehto: maakuljetus ja lentorahti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos asiakas valitsee maakuljetuksen ja tilauksen arvo on alle 100 dollaria, jälleenmyyjä halua veloittaa asiakkaalta rahtikuluna 10 dollaria.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos tilauksen arvo on yli 100 dollaria ja asiakas valitsee maakuljetuksen, asiakkaalta ei veloiteta rahtikuluja.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos asiakas valitsee kaikkien tilausten toimitustavaksi lentorahdin, rahtikuluna veloitetaan kokonaisarvosta riippumatta 20,00 dollaria.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Asetukset ja määrittäminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä skenaario edellyttää kahden automaattisten kulujen taulukon määrittämistä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Myyntireskontra <ph id="ph1">\&gt;</ph> Kulujen määritys <ph id="ph2">\&gt;</ph> Automaattiset kulut<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Määritä kaksi erilaista otsikkotason automaattista kulua.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Määritä toinen maakuljetukselle ja toinen lentorahdille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Määritä tässä skenaariossa, että niitä käytetään kaikille asiakkaille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Määritä maakuljetuksen toimituskuluiksi <bpt id="p1">**</bpt>Automaattiset kulut<ept id="p1">**</ept> -sivun riviosassa kulu, jota käytetään, kun tilauksen arvo on 0,01–100 dollaria. Tässä tapauksessa toimituskuluksi määritetään 10,00 dollaria.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Luo toinen kulurivi ilmaisemaan, että tilauksilla, joiden arvo on yli 100,01 dollaria, ei ole kuluja.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkki automaattisista kuluista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Määritä lentorahdin toimituskuluiksi automaattisten kulujen lomakkeessa 20 dollaria. Tätä kulua käytetään kaikissa tilauksissa (joiden arvo 0,01–9 999 999 dollaria).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lähetä muutokset Retail Serveriin ja kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla <bpt id="p1">**</bpt>1040 jakeluaikataulu<ept id="p1">**</ept> -työn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myynnin käsittely tässä skenaariossa</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun edellä mainitut määritysvaiheet on tehty ja muutokset on otettu käyttöön kanavatietokannassa, mikä tahansa myyntipiste-, puhelinkeskus- tai sähköinen kaupankäynti -kanavassa luotu asiakastilaus tai myyntitapahtuma, jonka toimitustavaksi on määritetty maakuljetus tai lentorahti otsikkotasolla, hyödyntää näitä kuluja ja käyttää niitä automaattisesti myyntiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tällä hetkellä kuluja käytetään kaikissa myyntitapahtumissa, jotka on luotu näitä toimitustapoja käyttävässä yrityksessä, sillä millään toiminnolla ei voi määrittää, että automaattisen kulun määritystä käytetään vain tietyssä myyntikanavassa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteen ja sähköisen kaupankäynnin skenaarioissa näissä tilauksissa ei ole selkeästi määritettyä otsikkoa, joten otsikkotason kuluja käytetään vain, jos kaikki tapahtuman myyntirivit on määritetty toimitettavaksi täsmälleen samalla toimitustavalla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos myyntipisteessä tai sähköisen kaupankäynnissä luoduissa tapahtumissa on yhdistelmätoimituksia, vain rivitason automaattiset kulut otetaan huomioon ja vain niitä käytetään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Puhelinkeskusskenaarioissa käyttäjä voi hallitta toimitustapa-asetusta otsikkotasolla, joten otsikkotason kuluja käytetään näissä tilauksissa, vaikka jotkin myyntirivit olisi määritetty käyttämään toista toimitustapaa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Puhelinkeskustilausten otsikkotason kulut perustuvat aina siihen toimitustapaan, joka on määritetty myyntitilauksen tilausotsikkotasolla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Automaattisten kulujen rivin kulujen esimerkki</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttötapausskenaario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä halua lisätä asiakkaalle lisäkulun asennuskuluiksi, kun asiakas ostaa tietyn mallisen tietokoneen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä tietokone edellyttää pakollisia lisäasennuksia, jotka jälleenmyyjä tekee asiakkaalle.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä on ilmoittanut asiakkaalle, että tämän asennuksen vuoksi käytössä on lisämaksu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä haluaa hallita tähän maksuun liittyviä kuluja erillään tuotteen myyntihinnasta taloushallinnon raportoinnin vuoksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">19,99 dollarin asennusmaksu veloitetaan asiakkaalta, kun tämä kyseinen tietokone ostetaan jossakin vähittäismyyntikanavassa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Asetukset ja määrittäminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä skenaario edellyttää yhden rivitason automaattisten kulujen taulukon määrittämistä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Valitse <bpt id="p1">**</bpt>Myyntireskontra <ph id="ph1">\&gt;</ph> Kulujen määritys <ph id="ph2">\&gt;</ph> Automaattiset kulut<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Valitse avattavassa <bpt id="p1">**</bpt>Taso<ept id="p1">**</ept>-valikossa <bpt id="p2">**</bpt>Rivi<ept id="p2">**</ept> ja uusi automaattisten kulujen tietue, joka koskee kaikkia asiakkaita sekä tiettyä tuotetta tai tuoteryhmää, jossa asennusmaksut veloitetaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkki automaattisista kuluista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lähetä kulut Retail Serveriin ja kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla <bpt id="p1">**</bpt>1040 jakeluaikataulu<ept id="p1">**</ept> -työn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myynnin käsittely tässä skenaariossa</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun edellä mainitut määritysvaiheet on tehty ja muutokset on otettu käyttöön kanavatietokannassa, mikä tahansa myyntipiste-, puhelinkeskus- tai sähköinen kaupankäynti -kanavassa luotu asiakastilaus tai myyntitapahtuma, jonka tilauksessa tämä nimike on, käynnistää rivitason kulun järjestelmällisen lisäämiseen tilauksen kokonaissummaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tällä hetkellä kuluja käytetään niille myyntiriveille, jotka vastaavat rivitason automattisten kulujen määritystä yrityksessä, sillä millään toiminnolla ei voi määrittää, että rivitason automaattista kulua käytetään vain tietyssä myyntikanavassa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkki manuaalisista otsikon kuluista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttötapausskenaarion kuvaus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä tekee poikkeuksen tyypillisiin prosesseihin tarjoamalla tuotteiden kotiinkuljetuksen asiakkaille, jotka tilaavat tuotteet myymälässä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä ja asiakas ovat sopineet, että asiakas maksaa 25 dollarin lisämaksun tämän palvelun käsittelykuluna.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilauksen vastaanottajan on lisättävä tämä lisämaksu tapahtumaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koska maksu on yleismaksu eikä liity mihinkään tiettyyn tilauksen tuotteeseen, otsikon kulun käyttö on mahdollista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Asetukset ja määrittäminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista, että tässä skenaariossa käytettävä kulukoodi on määritetty oikein, valitsemalla <bpt id="p1">**</bpt>Myyntireskontra <ph id="ph1">\&gt;</ph> Kulujen määritys <ph id="ph2">\&gt;</ph> Kulut<ept id="p1">**</ept> ja määritä skenaarioon sopiva kulukoodi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkki kuluista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Jo kulu on toimitukseen liittyvä kulu, jota käytetään toimitusalennuksissa tai -kampanjoissa, valitse kulukoodin <bpt id="p1">**</bpt>Toimitusmaksu<ept id="p1">**</ept>-asetukseksi <bpt id="p2">**</bpt>Kyllä<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos tämä kulu voidaan palauttaa järjestelmällisesti, kun palautustapahtumaa käsitellään myyntipistesovelluksessa, valitse <bpt id="p1">**</bpt>Palautettava<ept id="p1">**</ept>-asetukseksi <bpt id="p2">**</bpt>Kyllä<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Palautettava<ept id="p1">**</ept>-merkintää käytetään vain, kun <bpt id="p2">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p2">**</ept> -parametrin asetuksena on <bpt id="p3">**</bpt>Kyllä<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lähetä kulut Retail Serveriin ja kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla <bpt id="p1">**</bpt>1040 jakeluaikataulu<ept id="p1">**</ept> -työn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Lisää otsikon kulut<ept id="p1">**</ept> -työvaiheen on oltava määritettynä <bpt id="p2">[</bpt>myyntipisteen näyttöasettelussa<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>, jotta käyttäjän myyntipisteestä käytettävä painike voi kutsua tämän toimenpiteen (toimenpide 141).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näyttöasettelun muutokset on jaettava jälleenmyyntikanavaan; lisäksi ne jaettava jakeluaikataulutoiminnon kautta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Manuaalisten otsikon kulujen myyntikäsittely</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skenaarion suorittaminen myyntipistesovelluksessa edellyttää, että myyntipisteen käyttäjä luo myyntitapahtuman tavalliseen tapan lisäämällä tuotteet ja mahdolliset muut määritykset myyntiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjä on suoritettava ennen maksun keräämistä <bpt id="p1">**</bpt>Lisää otsikon kulu<ept id="p1">**</ept> -työvaihe, joka pyytää käyttäjää valitsemaan kulukoodin ja antamaan kulujen arvon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun käyttäjä on suorittanut prosessin loppuun, kulu lisätään myyntitilaukseen otsikkotason kuluna.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tätä prosessia voidaan käyttää puhelinkeskuksessa käyttämällä <bpt id="p1">**</bpt>Kulut<ept id="p1">**</ept>-ominaisuutta, joka sijaitsee työkalurivin <bpt id="p2">**</bpt>Myynti<ept id="p2">**</ept>-välilehdessä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjä voi lisätä uusia kulurivejä tilauksen otsikkoon <bpt id="p1">**</bpt>Kulujen ylläpito<ept id="p1">**</ept> -sivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkki manuaalisista rivin kuluista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttötapausskenaario</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Asiakas on pyytänyt, että kaksi viidestä myyntitilauksen nimikkeestä paketoidaan lahjaksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jälleenmyyjä tarjoaa tämän palvelun valinnaisena 2,00 dollariin nimikekohtaisella maksulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilauksen vastaanottajan on lisättävä nämä maksut niihin nimikkeisiin, jotka on paketoitava lahjaksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Asetukset ja määrittäminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista, että tässä skenaariossa käytettävä kulukoodi on määritetty oikein, valitsemalla <bpt id="p1">**</bpt>Myyntireskontra <ph id="ph1">\&gt;</ph> Kulujen määritys <ph id="ph2">\&gt;</ph> Kulut<ept id="p1">**</ept> ja määritä skenaarioon sopiva kulukoodi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jo kulu on toimitukseen liittyvä kulu, jota käytetään toimitusalennuksissa tai -kampanjoissa, valitse kulukoodin <bpt id="p1">**</bpt>Toimitusmaksu<ept id="p1">**</ept>-asetukseksi <bpt id="p2">**</bpt>Kyllä<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos kulu voidaan palauttaa järjestelmällisesti, kun palautustapahtumaa käsitellään myyntipistesovelluksessa, valitse <bpt id="p1">**</bpt>Palautettava<ept id="p1">**</ept>-asetukseksi <bpt id="p2">**</bpt>Kyllä<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Palautettava<ept id="p1">**</ept>-merkintää käytetään vain, kun <bpt id="p2">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p2">**</ept> -parametrin asetuksena on <bpt id="p3">**</bpt>Kyllä<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lähetä kulut Retail Serveriin ja kanavatietokantaan, jotta myyntipiste voi käyttää niitä suorittamalla <bpt id="p1">**</bpt>1040 jakeluaikataulu<ept id="p1">**</ept> -työn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Lisää rivin kulut<ept id="p1">**</ept> -työvaiheen on oltava määritettynä <bpt id="p2">[</bpt>myyntipisteen näyttöasettelussa<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>, jotta käyttäjän myyntipisteestä käytettävä painike voi kutsua tämän toimenpiteen (toimenpide 140).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näyttöasettelun muutokset on jaettava jälleenmyyntikanavaan; lisäksi ne jaettava jakeluaikataulutoiminnon kautta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Manuaalisen rivin kulun myyntikäsittely</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skenaarion suorittaminen myyntipistesovelluksessa edellyttää, että myyntipisteen käyttäjä luo myyntitapahtuman tavalliseen tapan lisäämällä tuotteet ja mahdolliset muut määritykset myyntiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjän on valittava ennen maksun keräämistä myyntipisteen nimikeluettelonäytössä rivi, johon maksu kohdistetaan, ja suoritettava <bpt id="p1">**</bpt>Lisää rivin kulu<ept id="p1">**</ept> -työvaihe.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjää pyydetään valitsemaan kulukoodi ja antamaan kulujen arvo.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun käyttäjä on suorittanut prosessin loppuun, kulu linkitetään riviin ja lisätään tilauksen kokonaissummaan rivitason kuluna.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjä voi tarvittaessa toistaa rivin lisäkulujen lisäämisen muille tapahtuman nimikeriveille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Samaa prosessia voidaan käyttää puhelinkeskuksessa käyttämällä kulujen ylläpito-ominaisuutta, joka sijaitsee <bpt id="p3">**</bpt>Myyntitilaus<ept id="p3">**</ept>-sivun <bpt id="p2">**</bpt>Myyntitilauksen rivit<ept id="p2">**</ept> -osan avattavassa <bpt id="p1">**</bpt>Myyntitiedot<ept id="p1">**</ept>-valikossa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjä voi lisätä uuden rivikohtaisen kulun tapahtumaan avautuvassa <bpt id="p1">**</bpt>Ylläpidä kuluja<ept id="p1">**</ept> -sivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisätoiminnot</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteen myyntitapahtuman kulujen muokkaaminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Kulujen hallinta<ept id="p1">**</ept> -työvaihe (142) on lisättävä <bpt id="p2">[</bpt>myyntipisteen näyttöasetteluun<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept>, jotta käyttäjä voi tarkastella ja muokata tai korvata järjestelmän laskeman tai manuaalisesti luodut otsikko- tai rivitason kulut.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos työvaihetta ei lisätä, käyttäjät eivät voi säätää kulujen arvoa myyntipistetapahtumassa. He eivät voi myöskään tarkastella kulujen tietoja, kuten kuluun sidotun kulukoodin tyyppiä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjä voi tarkastella myyntipisteen <bpt id="p1">**</bpt>Kulujen hallinta<ept id="p1">**</ept> -sivulla sekä otsikko- että rivitason kulujen tietoja.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjä voi tehdä tämän sivun <bpt id="p1">**</bpt>Muokkaa<ept id="p1">**</ept>-toiminnolla muutoksia summaan, joka veloitetaan tietyllä kulurivillä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun kulurivi ohitetaan manuaalisesti, sitä ei lasketa järjestelmällisesti uudelleen, ellei käyttäjä käynnistä <bpt id="p1">**</bpt>Laske kulut uudelleen<ept id="p1">**</ept> -työvaihetta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos <bpt id="p1">**</bpt>Kulun ohituksen syykoodi<ept id="p1">**</ept> on määritetty <bpt id="p2">**</bpt>Vähittäismyynnin parametrit<ept id="p2">**</ept> -asetussivulla, käyttäjää pyydetään antamaan syykoodi, kun kuluja on muokattu myyntipistesovelluksessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos ohitettujen kulujen syykoodit on taltioitu, käytettävissä on uusi raportti, jossa näitä ohituksia voi tarkastella ja jossa ne voidaan tarkistaa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raportin voi hakea valitsemalla <bpt id="p1">**</bpt>Vähittäismyynti <ph id="ph1">\&gt;</ph> Kyselyt ja raportit <ph id="ph2">\&gt;</ph> Kulun ohituksen historia<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteen palautustapahtuman palautuskulut</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos <bpt id="p1">**</bpt>Käytä edistyneitä automaattisia kuluja<ept id="p1">**</ept> -parametrin asetuksena on <bpt id="p2">**</bpt>Kyllä<ept id="p2">**</ept>, aiempaa vähittäismyynnin <bpt id="p3">**</bpt>Palauta toimitusmaksut<ept id="p3">**</ept> -parametria ei enää käytetä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos haluat ilmaista, mitkä kulut palautetaan järjestelmällisesti asiakkaalle edistyneitä automaattisia kuluja käytettäessä, varmista, että liittyvä kulukoodiksi on määritetty <bpt id="p1">**</bpt>Palautettava<ept id="p1">**</ept> <bpt id="p2">**</bpt>Kulujen koodi<ept id="p2">**</ept> -asetussivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista, että asetukset on synkronoitu Retail-kanavan tietokantoihin jakeluaikataulun käsittelyn avulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Palautustilaustapahtuman palautuskulut</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuluja ei palauteta järjestelmällisesti Retailissa luotuihin <bpt id="p1">**</bpt>palautustilauksiin<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttäjien on valittava <bpt id="p1">**</bpt>Kopioi kulut<ept id="p1">**</ept> -asetus <bpt id="p2">**</bpt>palautustilausta<ept id="p2">**</ept> luotaessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos <bpt id="p1">**</bpt>Kopioi kulut<ept id="p1">**</ept> -asetusta ei valita, alkuperäisen myyntitapahtuman kuluja ei automaattisesti palauteta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos <bpt id="p1">**</bpt>Kopioi kulut<ept id="p1">**</ept> on valittu, kaikki kulut kopioidaan palautustilaukseen, ja käyttäjä voi manuaalisesti muokata tai poistaa kuluja, joita he eivät halua palauttaa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Puhelinkeskuksen palautustilausprosessi ei tällä hetkellä tunnista <bpt id="p1">**</bpt>Palautettava<ept id="p1">**</ept>-merkintää <bpt id="p2">**</bpt>Kulujen koodi<ept id="p2">**</ept> -asetuksissa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Myyntipisteen kuittien määrittäminen näyttämään kulut</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Seuraavat kuittielementit on lisättävä kuittiriville ja alatunnisteeseen tukemaan edistynyttä automaattisten kulujen toimintoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Rivin toimituskulut<ept id="p1">**</ept> – Tällä rivitason elementillä voidaan kerrata tietyt myyntirivillä käytetyt kulujen koodit.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tässä näkyy vain ne kulujen koodit, jotka on merkitty <bpt id="p1">**</bpt>toimituskuluiksi<ept id="p1">**</ept> <bpt id="p2">**</bpt>Kulujen koodi<ept id="p2">**</ept> -sivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Rivin muut kulut<ept id="p1">**</ept> – Tällä rivitason elementillä voidaan kerrata kaikki muut kuin lähetyksen myyntirivillä käytetyt kulujen koodit.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ne ovat kulujen koodeja, joissa <bpt id="p1">**</bpt>Lähetys<ept id="p1">**</ept>-merkintää ei ole otettu käyttöön <bpt id="p2">**</bpt>Kulujen koodi<ept id="p2">**</ept> -sivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Tilauksen toimituskulujen tiedot<ept id="p1">**</ept> – Tämä alatunnistetason elementti näyttää niiden kulujen koodien kuvaukset, joita on käytetty tilaukseen, joka on merkitty <bpt id="p2">**</bpt>toimituskuluiksi<ept id="p2">**</ept> <bpt id="p3">**</bpt>Kulujen koodi<ept id="p3">**</ept> -asetussivulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Tilauksen toimituskulut<ept id="p1">**</ept> – Tämä alatunnistetason elementti näyttää toimitukseen liittyvien kulujen dollariarvon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Tilauksen muiden kulujen tiedot<ept id="p1">**</ept> – Tämä alatunnistetason elementti näyttää niiden kulujen koodien kuvaukset, joita ei ole käytetty tilaukseen, joka on merkitty toimitukseen kuluiksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Tilauksen muut kulut<ept id="p1">**</ept> – Tämä alatunnistetason elementti näyttää muuhun kuin toimitukseen liittyvien kulujen dollariarvon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisäksi organisaatiota suositellaan lisäämään vapaatekstikentät kuitin alatunnisteeseen, jotta alueet, joissa kuluja kerrataan, voidaan määritetään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kulujen laskennan estäminen ennen myyntipistetilauksen valmistumista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jotkin organisaatiot haluavat ehkä odottaa, että käyttäjä on lisännyt kaikki myyntirivit myyntipistetapahtumaan ennen kulujen laskemista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos haluat estää kulujen laskemisen, kun nimikkeitä lisätään myyntipistetapahtumaan, ota <bpt id="p1">**</bpt>Manuaalinen veloituksen laskenta<ept id="p1">**</ept> -parametri käyttöön myymälän käyttämässä <bpt id="p2">**</bpt>toimintoprofiilissa<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämän parametrin ottaminen käyttöön edellyttää, että myyntipistekäyttäjä käyttää <bpt id="p1">**</bpt>Laske loppusummat<ept id="p1">**</ept> -työvaihetta, kun tuotteiden lisääminen myyntipistetapahtumaan on päättynyt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Laske loppusummat<ept id="p1">**</ept> -työvaihe käynnistää sitten tilauksen otsikon tai rivien mahdollisten automaattisten kulujen laskennan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kulujen ohitusraportit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos käyttäjät ohittavat lasketut kulut manuaalisesti tai lisäävät manuaalisen kulun tapahtumaan, nämä tiedot ovat käytettävissä tarkistusta varten <bpt id="p1">**</bpt>Kulujen ohituksen historia<ept id="p1">**</ept> -raportissa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raporttia voi käyttää valitsemalla <bpt id="p1">**</bpt>Vähittäismyynti <ph id="ph1">\&gt;</ph> Kyselyt ja raportit <ph id="ph2">\&gt;</ph> Kulun ohituksen historia<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">On tärkeää huomata, että tähän raporttiin tarvittavat tiedot tuodaan kanavatietokannata HQ-sovellukseen P-jakeluaikataulutöinä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämän vuoksi tiedot juuri myyntipisteessä tehdyistä ohituksista eivät ehkä ole heti käytettävissä tässä raportissa, vaan tämän työn on ladattava myymälän tapahtumatiedot ensin HQ-sovellukseen.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>