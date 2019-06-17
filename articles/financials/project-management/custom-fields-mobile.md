<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="fi-FI">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssa ja Androidissa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tässä ohjeaiheessa on yleisiä tapoja käyttää laajennuksia mukautettujen kenttien käyttöönottoon.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssa ja Androidissa</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Tässä ohjeaiheessa on yleisiä tapoja käyttää laajennuksia mukautettujen kenttien käyttöönottoon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ohje käsittelee seuraavia aiheita:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Eri tietotyypit, joita mukautettu kenttäkehys tukee</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Miten näytetään luku- tai muokattavat kentät työaikaraportin merkinnöissä ja tallennetaan käyttäjän antamat arvot takaisin tietokantaan</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Vain luku -kenttien näyttäminen työaikaraportin otsikossa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Muun mukautetun liiketoimintalogiikan integroiminen oletusarvojen syöttämiseen kenttiin ja lisätarkistuksen tekemiseksi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Yleisö</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ohjeaihe on tarkoitettu kehittäjille, jotka ovat integroimassa mukautettuja kenttiä Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen piiriin, joka on saatavilla Apple iOS:lle ja Google Androidille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Oletuksena on, että lukijat tuntevat X++-kehitystyön ja projektin työaikaraportin toiminnot.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tietosopimus – TSTimesheetCustomField X++-luokka</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> -luokka on X++-tietosopimusluokka, joka vastaa työaikaraportin toiminnon mukautettua kenttää koskevia tietoja.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Mukautettujen kenttäobjektien luettelot välitetään sekä TSTimesheetDetails-tietosopimuksessa että TSTimesheetEntry-tietosopimuksessa, jolloin mobiilisovelluksen mukautetut kentät näkyvät.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - Työaikaraportin otsikkosopimus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - Työaikaraportin tapahtumasopimus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Näiden objektien ryhmät, joilla on samat projektitiedot ja <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept>-arvo, muodostavat rivin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">fieldBaseType (Tyypit)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept>-objektin <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept>-ominaisuus määrittää sovelluksessa näkyvän kentän tyypin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Seuraavia <bpt id="p1">**</bpt>tyyppi<ept id="p1">**</ept>arvoja tuetaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tyypin arvo</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Laji</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Muistiinpanot</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Merkkijono (ja Enum)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kenttä näkyy tekstikenttänä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kokonaisluku</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Arvo näkyy lukuna ilman desimaalipaikkoja.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Reaaliluku</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Arvo näkyy lukuna, jolla on desimaalipaikkoja.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos haluat, että todellinen arvo näkyy sovelluksessa valuuttana, käytä <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept>-ominaisuutta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept>-ominaisuuden avulla voit määrittää näytettävien desimaalien määrän.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Päivämäärä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Päivämäärämuodot määräytyvät käyttäjän <bpt id="p1">**</bpt>päivämäärä, kellonajan ja numeromuodon<ept id="p1">**</ept> asetuksella , joka on määritetty kohdassa <bpt id="p2">**</bpt>Kieli- ja maa-/alue<ept id="p2">**</ept> -asetukset kohdassa <bpt id="p3">**</bpt>Käyttäjäasetukset<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Boolen arvo</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Int64</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept>-objektissa ei ole <bpt id="p2">**</bpt>stringOptions<ept id="p2">**</ept>-ominaisuutta, käyttäjälle annetaan vapaamuotoinen tekstikenttä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Stringlength<ept id="p1">**</ept>-ominaisuudella voidaan määrittää suurin sallittu merkkijonon pituus, jonka käyttäjät voivat kirjoittaa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept>-objektissa on <bpt id="p2">**</bpt>stringOptions<ept id="p2">**</ept>-ominaisuus, nämä luetteloelementit ovat ainoat arvot, joita käyttäjät voivat valita valintapainikkeiden avulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tässä tapauksessa merkkijonokenttä voi toimia Enum-arvona käyttäjämerkintää varten.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos haluat tallentaa arvon tietokantaan luetteloluetteloksi, määritä merkkijonon arvo manuaalisesti takaisin Enum-arvoksi ennen tallennusta tietokantaan käyttämällä komentoketjua (Katso "Käytä komentoketjua TSTimesheetEntryService-luokassa, kun haluat tallentaa tuntilomake merkinnän sovelluksesta takaisin tietokantaan"-osassa, joka on jäljempänä tässä esimerkissä).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämän ominaisuuden avulla voit muotoilla todellisia arvoja valuutoiksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä menetelmä on käytettävissä vain, kun <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept>-arvo on <bpt id="p2">**</bpt>reaaliluku<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – Muotoilua ei käytetä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Valuutta<ept id="p1">**</ept> – Muotoile arvo valuuttana.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kun valuuttamuotoilu on käytössä, voit käyttää <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept>-kenttää ja siirtääksesi valuuttakoodin, joka näytetään sovelluksessa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Arvo on vain luku -arvo.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>realValue<ept id="p1">**</ept>-kenttä sisältää rahamäärän, joka on tallennettava tietokantaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämän ominaisuuden avulla voit määrittää, missä sovelluksessa mukautetun kentän pitäisi näkyä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>TSCustomFieldSection::Otsikko<ept id="p1">**</ept> – Kenttä näkyy sovelluksen <bpt id="p2">**</bpt>Katso lisätietoja<ept id="p2">**</ept> -osassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Nämä kentät ovat aina vain luku -muotoisia.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>TSCustomFieldSection::Tivi<ept id="p1">**</ept> – Kenttä tulee näkyviin, kun kaikki valmiiksi määritetyt rivikentät ovat aikaraporttikentissä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Nämä kentät voivat olla joko muokattavia tai vain luku -muotoisia.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ominaisuus määrittää kentän, kun sovelluksen luomat arvot tallennetaan takaisin tietokantaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Tämä ominaisuus määrittää kentän, kun sovelluksen luomat arvot tallennetaan takaisin tietokantaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Määrittämällä tämän ominaisuuden arvoksi <bpt id="p1">**</bpt>Kyllä<ept id="p1">**</ept> voit määrittää, että käyttäjät voivat muokata tuntilomakkeen merkintäosan kenttää.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Määritä ominaisuuden arvoksi <bpt id="p1">**</bpt>Ei<ept id="p1">**</ept>, jos haluat tehdä kentästä vain luku -muotoisen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Määrittämällä tämän ominaisuuden arvoksi <bpt id="p1">**</bpt>Kyllä<ept id="p1">**</ept> voit määrittää, että tuntilomakkeen merkintäosan kentän tulisi olla pakollinen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">label (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ominaisuus määrittää otsikon, joka näkyy sovelluksen kentän vieressä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">stringOptions (merkkijonojen luettelo)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ominaisuus on käytettävissä vain, kun <bpt id="p1">**</bpt>fieldbasetype<ept id="p1">**</ept> -arvo on <bpt id="p2">**</bpt>Merkkijono<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> on määritetty, valintapainikkeiden kautta valittavissa olevat merkkijonoarvot (Radiopainikkeet) määritetään luettelon merkkijonojen avulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Jos merkkijonoja ei anneta, merkkijonokentän vapaatekstin syöttö on sallittu (esimerkin löydät kohdassa "komentoketjun käyttäminen Tstimessheedistryservice-luokassa, jolloin tuntilomakekohta tallennetaan sovelluksesta tietokantaan uudelleen" -osassa myöhemmin tässä aiheessa).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ominaisuus määrittää merkkijonokentän enimmäispituuden.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Se on käytettävissä vain, kun <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept>-arvo on <bpt id="p2">**</bpt>Merkkijono<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ominaisuus määrittää todellisen kentän desimaalipaikkojen määrän.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Se on käytettävissä vain, kun <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept>-arvo on <bpt id="p2">**</bpt>Reaaliarvo<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tämä ominaisuus määrittää, missä järjestyksessä mukautetut kentät näkyvät sovelluksessa, kun määritettynä on useita mukautettuja kenttiä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Alanumeroita käyttävät kentät näytetään ensin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">booleanValue (boolean)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept>-tyypin kentissä tämä ominaisuus siirtää kentän totuusarvon palvelimen ja sovelluksen välille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>GUID<ept id="p1">**</ept>-tyypin kentissä tämä ominaisuus siirtää kentän yksilöivän tunnisteen palvelimen ja sovelluksen välille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">int64Value (Int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Int64<ept id="p1">**</ept>-tyypin kentissä tämä ominaisuus siirtää kentän Int64-arvon palvelimen ja sovelluksen välille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Int<ept id="p1">**</ept>-tyypin kentissä tämä ominaisuus siirtää kentän Int-arvon palvelimen ja sovelluksen välille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">realValue (real)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Reaaliarvo<ept id="p1">**</ept>-tyypin kentissä tämä ominaisuus siirtää kentän reaaliarvon palvelimen ja sovelluksen välille .</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Merkkijono<ept id="p1">**</ept>-tyypin kentissä tämä ominaisuus siirtää kentän merkkijonoarvon palvelimen ja sovelluksen välille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Sitä käytetään myös sellaisissa kentissä, joiden <bpt id="p1">**</bpt>reaaliarvo<ept id="p1">**</ept> on muotoiltu valuutaksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Näiden kenttien osalta ominaisuutta käytetään valuuttakoodin välittämiseen sovellukseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">dateValue (date)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>Päivämäärä<ept id="p1">**</ept>-tyypin kentissä tämä ominaisuus siirtää kentän päivämäärän palvelimen ja sovelluksen välille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Mukautetun kentän näyttäminen ja tallentaminen tuntilomakemerkinnän osassa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Alla on näyttökuva aikaraportin merkinnän luomisesta mobiilisovelluksesta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Se näyttää valmiiksi määritetyt kentät ja mukautetun kentän aikamerkintäosassa nimeltä "Testimerkkijono" ja enum-arvo "Toinen vaihtoehto" on jo asetettu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Testimerkkijonon mukautettu kenttä sovelluksessa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Alla on kuvakaappaus käyttäjän mobiilisovelluksesta, jossa valitaan jokin käytettävissä olevista enum-asetuksista Testimerkkijono-kohtaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Kaksi vaihtoehtoa ovat "ensimmäinen vaihtoehto" ja "toinen vaihtoehto", jotka näkyvät valintapainikkeina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Toinen vaihtoehto on valittuna.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Testimerkkijonon mukautetun kentän valintapainikkeita (valintanappeja)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Laajenna TSTimesheetLine-taulukkoa niin, että siinä on mukautettu kenttä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Tyypillisissä skenaarioissa on todennäköistä, että tuntilomakemerkinnän mukautetun kentän tiedot tallennetaan TSTimesheetLine-tauluun.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Muita tauluja voidaan kuitenkin käyttää, jos tiedot voidaan noutaa annetun TSTimesheetTrans-tietueen perusteella tai jos niillä ei ole tiettyä tietuetaustaa (Jos esimerkiksi kenttä on määritetty vain luku -tilaan projektin parametreissä).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Huomaa, että mukautettujen kenttien ei tarvitse sisältää tietokantatietuetta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">Ne voidaan luoda dynaamisesti X++-logiikan perusteella.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämä lähestymistapa voi olla hyödyllinen vain luku -tilassa olevissa skenaarioissa (lisätietoja on kohdassa "komentoketjun käyttäminen TSTimesheetDetails-luokassa, buildCustomFieldListForHeader-menetelmä, joka täyttää tuntilomakkeen tiedot" -osassa, jossa on esimerkki dynaamisesti tuotetuista mukautetuista kenttäarvoista.)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Alla on kuvakaappaus Visual Studion sovellusobjektipuusta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Siinä näkyy TSTimesheetLine-taulun laajennus ja TestLineString-kenttä on lisätty mukautetuksi kentäksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Merkkijono</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän tuntilomakemerkinnän osassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämä koodi ohjaa sovelluksen kentän näyttöasetuksia.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Se määrittää esimerkiksi kentän tyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraavassa esimerkissä näkyy aikamerkintöjen merkkijonokenttä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tässä kentässä on kaksi vaihtoehtoa <bpt id="p1">**</bpt>Ensimmäinen vaihtoehto<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Toinen vaihtoehto<ept id="p2">**</ept>, jotka ovat käytettävissä valintapainikkeiden kautta (valintanapit).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sovelluksen kenttä liitetään <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept>-kenttään, joka lisätään TSTimesheetLine-tauluun.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="0" state="translated">Huomaa <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept>-menetelmän käyttäminen mukautettujen kenttien ominaisuuksien alustamisen yksinkertaistamiseksi: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> ja <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Voit myös määrittää nämä parametrit manuaalisesti kuten haluat.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Käytä komentoketjua TSTimesheetEntry-luokan buildCustomFieldListForEntry-menetelmässä, kun haluat syöttää arvoja tuntilomakkeeseen</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept>-menetelmällä syötetään arvoja mobiilisovellukseen tallennettujen työaikaraporttien riveille.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Se ottaa TSTimesheetTrans-tietueen parametriksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tietueen kenttiä voidaan käyttää sovelluksen mukautetun kentän arvon täyttämiseen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Käyttämällä TSTimesheetEntryService-luokan komentoketjua voit tallentaa tuntilomakemerkinnän sovelluksesta takaisin tietokantaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos haluat tallentaa mukautetun kentän takaisin tietokantaan tyypillisessä käytössä, sinun on laajennettava useita menetelmiä:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept>-menetelmän avulla määritetään, onko käyttäjä muuttanut rivitietuetta sovelluksessa ja pitääkö se tallentaa tietokantaan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos suorituskyky ei ole ongelma, tätä menetelmää voidaan yksinkertaistaa niin, että se palauttaa aina arvon <bpt id="p1">**</bpt>Tosi<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> -menetelmiä voidaan jatkaa siten, että ne syöttävät arvot TSTimesheetLine-tietokantatietueeseen TSTimesheetEntry-tietueesta annetusta tietosopimustietueesta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraavassa esimerkissä ilmoitetaan, miten tietokantakentän ja syöttökentän välinen vastaavuus tehdään manuaalisesti X++-koodin avulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept>-menetelmää voidaan myös jatkaa, jos <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept>-objektiin yhdistettävän mukautetun kentän on kirjoitettava takaisin TSTimesheetLineweek-tietokantatauluun.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraavassa esimerkissä tallennetaan <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept>- tai <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept>-arvo, jonka käyttäjä valitsee tietokantaan raakamerkkijonoarvona.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos tietokantakenttä on <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept>-tyypin kenttä, arvot voidaan määrittää manuaalisesti Enum-arvoksi ja tallentaa sitten tietokantataulun Enum-kenttään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Mukautetun kentän näyttäminen tuntilomakkeen otsikossa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Alla on näyttökuva aikaraportin käyttäjän mobiilisovelluksesta, jossa näkyy käyttäjän tuntilomakenäkymä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lisätietoja-painike on valittu oikeasta yläkulmasta, jolloin näkyviin tulee Näytä lisätiedot -vaihtoehto.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Näytä lisätietoja -komento</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Alla on näyttökuva aikaraportin käyttäjän mobiilisovelluksesta, jossa näkyy tuntilomakkeen Lisää-osa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tuntilomakkeen otsikko-osaan on lisätty mukautettu kenttä, jonka nimi on Tämän tuntilomakkeen käyttöaste (laskettu mukautettu kenttä).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Vain luku -arvo 0,667 on määritetty mukautettuun kenttään.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Lisää-osa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Laajenna TSTimesheetTable-taulukkoa niin, että siinä on mukautettu kenttä</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Tyypillisissä skenaarioissa on todennäköistä, että otsikon mukautetun kentän tiedot haetaan TSTimesheetLine-taulusta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">Muita tauluja voidaan kuitenkin käyttää, jos tiedot voidaan noutaa annetun TSTimesheetTable-tietueen perusteella tai jos niillä ei ole tiettyä tietuetaustaa (Jos esimerkiksi kenttä on määritetty vain luku -tilaan projektin parametreissä).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Huomaa, että mukautettujen kenttien ei tarvitse sisältää tietokantatietuetta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">Ne voidaan luoda dynaamisesti X++-logiikan perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraava esimerkki osoittaa tämän lähestymistavan.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Otsikko-osan kentät ovat aina vain luku -tilassa sovelluksessa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän otsikon osassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tämä koodi ohjaa sovelluksen kentän näyttöasetuksia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Se määrittää esimerkiksi kentän tyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraavassa esimerkissä näkyy laskettu arvo sovelluksen otsikko-osassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Käytä komentoketjua TSTimesheetDetails-luokan buildCustomFieldListForHeader-menetelmässä, kun haluat täyttää arvoja tuntilomakkeen tietoihin</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept>-menetelmällä täytetään arvoja mobiilisovellukseen työaikaraporttien otsikkotietoihin.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Se ottaa TSTimesheetTable-tietueen parametriksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">Tietueen kenttiä voidaan käyttää sovelluksen mukautetun kentän arvon täyttämiseen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraava esimerkki ei lue mitään tietokannan arvoja.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sen sijaan se luo X++-logiikan avulla lasketun arvon, joka näkyy sovelluksessa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Muut konfiguroitavuus- ja laajennettavuusmahdollisuudet</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Lisävahvistuksen lisääminen sovellukselle</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Työaikaraporttien toiminnallisuuden nykyinen logiikka tietokannan tasolla toimii edelleen odotetulla tavalla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos haluat keskeyttää Tallenna- tai Lähetä-toimintojen päättymisen ja näyttää tietyn virhesanoman, voit lisätä koodiin <bpt id="p1">**</bpt>heittovirheen ("sanoma käyttäjälle")<ept id="p1">**</ept> komentolaajennusketjun kautta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Seuraavassa on kolme esimerkkiä hyödyllisistä laajennettavien menetelmien menetelmistä:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> TSTimesheetLine-taulussa palauttaa arvon <bpt id="p2">**</bpt>Epätosi<ept id="p2">**</ept> aikaraportin rivin tallennustoiminnon aikana, mobiilisovelluksessa näkyy virhesanoma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Jos <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> TSTimesheetTable-taulussa palauttaa arvon <bpt id="p2">**</bpt>Epätosi<ept id="p2">**</ept> aikaraportin sovelluksen esittämisen aikana, käyttäjälle näytetään virhesanoma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Logiikka, joka täyttää kentät (esimerkiksi <bpt id="p1">**</bpt>Rivin ominaisuus<ept id="p1">**</ept>) TSTimesheetLine-taulun <bpt id="p2">**</bpt>insert<ept id="p2">**</ept>-menetelmän aikana, suoritetaan edelleen.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Käyttövalmiiden kenttien piilottaminen ja merkitseminen vain luku -muodossa konfiguroinnin kautta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Projektin parametreistä voit määrittää, että käyttövalmiit kentät ovat vain luku -muotoisia tai piilotettuja mobiilisovelluksessa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="0" state="translated">Määritä valinnat <bpt id="p1">**</bpt>Mobiililaitteen aikaraportti<ept id="p1">**</ept> -osalle <bpt id="p2">**</bpt>Aikaraportti<ept id="p2">**</ept>-välilehdellä <bpt id="p3">**</bpt>Projektinhallinta- ja kirjanpidon parametrit<ept id="p3">**</ept> - sivulla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Projektiparametrit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Valintaan käytettävissä olevien tehtävien muuttaminen laajennusten kautta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Projektin valintaan käytettävissä olevat toiminnot täytetään <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept>-menetelmien avulla <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept>-luokassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Voit käyttää komentoketjua, kun haluat muuttaa tätä toimintatapaa niin, että se vastaa tiettyä projektia varten valittavissa olevien toimintojen liiketoimintaskenaariota.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Oletusprojektiluokan syöttäminen työaikaraportin merkinnöille</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Oletusprojektiluokan määritys työaikaraportin merkinnöissä tapahtuu kolmella tasolla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Voit käyttää komentoketjua, kun haluat laajentaa käyttäytymistä millä tahansa tai kaikilla näillä tasoilla halutun toiminnan saavuttamiseksi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Seuraavaa hierarkiaa käytetään:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Sovellus yrittää sijoittaa oletusluokan projektiresurssista.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämä oletus luokka on määritetty <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept>- ja <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept>-menetelmille <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept>-luokassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Jos oletusluokkaa ei ole projektiresurssitasolla, sovellus yrittää vetää sen projektitehtävästä.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Tämä oletusluokka määritetään <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept>-menetelmällä <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>-luokassa.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Jos oletusluokkaa ei ole projektitehtävätasolla, oletuskategoria otetaan projektin parametreista.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Tämä oletusluokka määritetään <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept>-menetelmällä <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>-luokassa.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>