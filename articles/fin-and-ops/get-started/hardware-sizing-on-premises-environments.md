<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="hardware-sizing-on-premises-environments.md" target-language="fi-FI">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>hardware-sizing-on-premises-environments.e242d0.4832a056a99e0f7521e022982b7db7b16d7064a3.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4832a056a99e0f7521e022982b7db7b16d7064a3</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\fin-and-ops\get-started\hardware-sizing-on-premises-environments.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Hardware sizing requirements for on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laitteiston kokovaatimukset paikallisissa ympäristöissä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic lists the hardware sizing requirements for an on-premises environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä ohjeaiheessa käsitellään laitteiston kokovaatimukset paikallisissa ympäristöissä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Hardware sizing requirements for on-premises environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laitteiston kokovaatimukset paikallisissa ympäristöissä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the <bpt id="p1">[</bpt>System requirements<ept id="p1">](system-requirements.md)</ept> and <bpt id="p2">[</bpt>Setup and deployment instructions<ept id="p2">](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md)</ept> to gain a solid understanding off the underlying infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tutustu ennen laitteiston ja infrastruktuurin koon määrittämistä paikallisiin ympäristöihin <bpt id="p1">[</bpt>järjestelmävaatimuksiin<ept id="p1">](system-requirements.md)</ept> sekä <bpt id="p2">[</bpt>asennus- ja käyttöönotto-ohjeisiin<ept id="p2">](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md)</ept>, sillä saat niiden avulla selkeän käsityksen perustana olevasta infrastruktuurista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Pay close attention to the system setup best practices for optimum performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Perehdy huolellisesti järjestelmän asetuksen parhaisiin käytäntöihin, jotta järjestelmä toimisi mahdollisimman hyvin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun olet perehtynyt dokumentaatioon, voit aloittaa tapahtumien ja samanaikaisten käyttäjien määrää sekä määrittämään ympäristön koon ytimen keskimääräisen siirtomäärän perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Factors that affect sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kokoon vaikuttavia tekijöitä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>All the factors shown in the following illustration contribute to sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaikki seuraavan kuvan tekijät vaikuttavat koon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The more detailed information that is collected, the more precisely you can determine sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mitä tarkempia kerätyt tiedot ovat, sitä tarkemmin voit määrittää koon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Hardware sizing, without supporting data, is likely to be inaccurate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos laitteiston koko määritetään ilman taustatietoja, lopputulos ei ole todennäköisesti tarkka.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The absolute minimum requirement for necessary data is the peak transaction line load per hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Suurin tapahtumarivien määrä tunnissa on tieto, joka vähintäänkin tarvitaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Hardware sizing for on-premises environments<ept id="p1">](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Laitteiston koon määrittäminen paikallisissa ympäristöissä<ept id="p1">](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vasemmalta oikealle tarkasteltaessa tärkein tekijä, jonka avulla koko voidaan määrittää tarkasti, on tapahtumaprofiili tai tapahtuman kuvaus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>It's important to always find the peak transactional volume per hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">On tärkeää, että suurin tapahtumien määrä tunnissa on tiedossa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If there are multiple peak periods, then these periods need to be accurately defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jos kuormitushuippuja on useita, nämä jaksot on määritettävä tarkasti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun tiedät, miten kuormitus vaikuttaa infrastruktuuriin, sinun on saatava tarkemmat tiedot myös seuraavista tekijöistä:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Transactions<ept id="p1">**</ept> – Typically transactions have certain peaks throughout the day/week.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Tapahtumat<ept id="p1">**</ept> – Tapahtumilla on tavallisesti tietty huippu päivän tai viikon aikana.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>This mostly depends on the transaction type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Se puolestaan määräytyy lähinnä tapahtumatyypin mukaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aika- ja tapahtumakirjauksissa huippu on yleensä kerran viikossa, kun taas myyntitilauskirjaukset tapahtuvat usein kerralla integroinnin kautta tai vähitellen päivän mittaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Number of concurrent users<ept id="p1">**</ept> – The number of concurrent users is the second most important sizing factor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Yhtäaikaisten käyttäjien määrä<ept id="p1">**</ept> – Yhtäaikaisten käyttäjien määrä on toiseksi tärkein kokoon vaikuttava tekijä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kokoarvioita ei saa luotettavasti yhtäaikaisten käyttäjien määrän perusteella, joten jos sinulla on vain nämä tiedot, arvioi määrä suunnilleen ja palaa tähän kohtaan, kun sinulla on enemmän tietoja.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>An accurate concurrent user definition means that:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yhtäaikaisen käyttämän tarkan määritelmän mukaan</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Named users are not concurrent users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">nimetyt käyttäjät eivät ole yhtäaikaisia käyttäjiä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Concurrent users are always a subset of named users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">yhtäaikaiset käyttäjät ovat aina nimettyjen käyttäjien alijoukko</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Peak workload defines the maximum concurrency for sizing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">suurin kuormitus määrittää suurimman yhtäaikaisten käyttäjien määrän kokoa määritettäessä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Criteria for concurrent users is that the user meets all the following criteria:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yhtäaikainen käyttäjä on käyttäjä, joka täyttää kaikki seuraavat ehdot:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Logged on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">kirjautunut sisään</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Working transactions/inquiries at the time of counting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">käyttää tapahtumia tai kyselyjä laskennan aikana</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Not an idle session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">istunto ei ole käyttämätön.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Data composition<ept id="p1">**</ept> – This is mostly about how your system will be set up and configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Tietoja kokoonpano<ept id="p1">**</ept> – Tämä tarkoittaa lähinnä sitä, miten järjestelmä asennetaan ja määritetään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kyse voi olla esimerkiksi yritysten, nimikkeiden ja tuoterakennetasojen määrästä sekä suojausasetusten monimutkaisuudesta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kukin näistä tekijöistä voi vaikuttaa jonkin verran suorituskykyyn, joten älykkäät infrastruktuuriratkaisut voivat kumota näiden tekijöiden vaikutuksen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Extensions<ept id="p1">**</ept> – Customizations can be simple or complex.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Laajennukset<ept id="p1">**</ept> – Mukautukset voivat olla yksinkertaisia tai monimutkaisia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mukautusten määrä ja niiden monimutkaisuus ja käyttö vaikuttavat eri tavoin tarvittavan infrastruktuurin kokoon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Monimutkaisissa mukautuksissa kannattaa suorittaa suorituskykyarviointeja ja varmistaa näin teho testataan. Samalla saadaan parempi käsitys infrastruktuurin tarpeista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>This is even more critical when the extensions are not coded according to best practices for performance and scalability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä on entistäkin tärkeämpää, kun laajennuksia ei ole koodattu suorituskyvyn ja skaalautuvuuden parhaiden käytäntöjen mukaisesti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Reporting and analytics<ept id="p1">**</ept> – These factors typically include running heavy queries against the various databases in the Finance and Operations database systems.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Raportointi ja analytiikka<ept id="p1">**</ept> – Nämä tekijät sisältävät yleensä raskaiden kyselyjen tekemistä useissa Finance and Operations -tietokantajärjestelmien tietokannoissa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tieto siitä, milloin laajoja raportteja ajetaan, ja niiden vähentäminen auttaa ymmärtämään, mikä vaikutus niillä on.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Third-party solutions<ept id="p1">**</ept> – These solutions, like ISVs, have the same implications and recommendations as extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Kolmannen osapuolen ratkaisut<ept id="p1">**</ept> – näillä ratkaisuilla, kuten riippumattomilla ohjelmistotoimittajilla, on samat vaikutukset ja suositukset kuin laajennuksilla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Sizing your Finance and Operations environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations -ympäristön koon määrittäminen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sinun on tiedettävä suurin käsiteltävä tapahtumien määrä kokovaatimusten selvittämiseksi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Useimmat lisäjärjestelmät, kuten Management Reporter tai SSRS, eivät ole toiminnan kannalta yhtä tärkeitä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>As a result, this document focuses mostly on AOS and SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämän vuoksi tässä asiakirjassa käsitellään lähinnä AOS-palvelinta ja SQL Serveriä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yleensä ottaen laskentatasot skaalautuvat ylöspäin ja ne on syytä määrittää muodossa N+1 – toisin sanoen jos arvioit tarpeeksi kolme AOS-palvelinta, lisää neljäs AOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The database tier should be set up in an Always On highly-available setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tietokantataso on määritettävä aina päällä olevana suuren käytettävyyden asennuksena.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>SQL Server (OLTP)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server (OLTP)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koko</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>3K to 15K transaction lines per hour per core on DB server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 000–15 000 tapahtumariviä/tunti/ydin tietokantapalvelimessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ensisijaisen SQL Serverin tavallinen AOS–SQL-ydinsuhde on 3:1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Additional cores are required based on the chosen high availability configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisäytimiä tarvitaan valitun suuren käyttävyyden määrityksen perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Processing database-heavy operations may regress this to 2:1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Paljon tietokantoja käyttävien toimenpiteiden käsittely jo pienentää suhteeksi 2:1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The following factors influence variations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seuraavat tekijät vaikuttavat vaihteluun:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Parameter settings in use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käytettävät parametriasetukset.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Levels of extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Laajennusten tasot.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Usage of additional functionality, such as database log and alerts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisätietojen, kuten tietokantalokin ja hälytysten, käyttö.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Extreme database logging will further reduce throughput per hour per core below 3K lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Suuri tietokantalokiin kirjaus pienentää entisestään tunti- ja ydinkohtaisen siirtomäärän alle 3 000 riviin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tietojen kokopanon monimutkaisuus – esimerkiksi yksinkertaisen tilikartan tai tarkan ja yksityiskohtaisen tilikartan valitsimen vaikuttaa siirtomäärään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Transaction characterization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tapahtuman kuvaus.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>2 GB to 16 GB memory for each core.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2–16 Gt muistia/ydin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Auxiliary databases on DB server such as Management reporter and SSRS databases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tietokantapalvelimen lisätietokannat, kuten Management Reporter- ja SSRS-tietokannat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Temp DB = 15% of DB size, with as many files as physical processors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tilapäistietokanta = 15 prosenttia tietokannan koosta, ja tiedostoja on yhtä paljon kuin fyysisiä suorittimia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>SAN size and throughput based on total concurrent transaction volume/usage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SAN-koko ja -siirtomäärä yhtäaikaisten tapahtumien yhteismäärän ja -käytön perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>High availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Suuri käytettävyys</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>We recommend always utilizing SQL Server in either a cluster or mirroring setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Serveriä kannattaa aina käyttää joko klusterina tai peilaavana asennuksena.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The second SQL node should have the same number of cores as the primary node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toisessa SQL-solmussa on oltava yhtä monta ydintä kuin ensisijaisessa solmussa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Active Directory Federation Services (AD FS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Active Directory -liittoutumispalvelut (AD FS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>For AD FS sizing, see the <bpt id="p1">[</bpt>AD FS Server Capacity documentation<ept id="p1">](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisätietoja AD FS -kokomäärityksistä on <bpt id="p1">[</bpt>AD FS:n palvelinkapasiteetin dokumentaatiossa<ept id="p1">](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>A <bpt id="p1">[</bpt>sizing spreadsheet<ept id="p1">](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)</ept> is available for planning the number of instances in your deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Käyttöönoton esiintymien määrän suunnittelua varten on <bpt id="p1">[</bpt>kokotaulukko<ept id="p1">](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>AOS (Online and batch)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS (verkko ja erä)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Sizing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koko</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Sizing by transaction volume/usage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tapahtumien määrän ja käytön mukaan tapahtuva koon määritys</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>2K to 6K lines per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 000–6 000 riviä/ydin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>16 GB per instance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">16 Gt/esiintymä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Standard box – 4 to 24 cores</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vakiorunko – 4–24 ydintä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>10 to 15 Enterprise users per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10–15 Enterprise-käyttäjää/ydin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>15 to 25 Activity users per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">15–25 tehtäväkäyttäjää/ydin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>25 to 50 Team members per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">25–50 ryhmän jäsentä/ydin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Batch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Erä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>1 to 4 batch threads per core</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1–4 eräsäiettä/ydin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Size based on batch window characterization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koko perustuu eräikkunan kuvaukseen</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Huomaa, että AOS, tietojen hallinta ja erä ovat samassa roolissa Service Fabricissa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koko on määritettävä näiden kolmen toiminnon yhdistetylle kuormitukselle eikä erikseen niin kuin Microsoft Dynamics AX 2012:ssa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The same variability factors for SQL Server apply here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Serverin vaihtelutekijät koskevat myös näitä kokomäärityksiä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>High availability</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Suuri käytettävyys</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Ensure that you have at least 1 to 2 more AOS available than you estimate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista, että käytettävissä on vähintään 1–2 AOS-palvelinta enemmän kuin mitä arvioit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Ensure that you have at least 3 to 4 virtual hosts available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista, että käytettävissä on ainakin 3–4 virtuaali-isäntää.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Management reporter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Management Reporter</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ellei käyttö ole erittäin suurta suositeltu vähimmäisvaatimus on useimmissa tapauksissa kaksi solmua.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Only in cases where there is heavy use will you need more than two nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vain siinä tapauksessa, että käyttö on erittäin runsasta, tarvitaan enemmän kuin kaksi solmua.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Please scale as needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Skaalaa tarpeen mukaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>SQL Server Reporting Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server -raportointipalvelut.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>For the general availability release, only one SSRS node can be deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Yleisesti saatavilla olevassa julkaisuversiossa voidaan ottaa käyttöön vain yksi SSRS-solmu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seuraa SSRS-solmua testauksen aikana ja lisää SSRS:n käytössä olevien ytimien määrää tarvittaessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varmista, että virtuaali-isäntään valmiiksi määritetty toissijainen solmu ei ole sama kuin SSRS VM.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä on tärkeää, jos SSRS:ää isännöivässä virtuaalikoneessa tai virtuaali-isännässä on ongelma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>If this the case, they would need to be replaced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Siinä tapauksessa ne on vaihdettava.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Environment Orchestrator</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ympäristön Orchestrator-palvelu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The Orchestrator service is the service that manages your deployment and the related communication with LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Orchestrator-palvelu hallitsee käyttöönottoa ja siihen liittyviä LCS-yhteyksiä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>This service is deployed as the primary Service Fabric service and requires at least three VMs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Palvelu otetaan käyttöön ensisijaisena Service Fabric -palveluna, ja sitä varten tarvitaan vähintään kolme VM-konetta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>This service is co-located with the Service Fabric orchestration services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Palvelu on samassa sijainnissa kuin Service Fabricin Orchestration-palvelut.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>This and should be sized to the peak load of the cluster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sen koon pitäisi perustua klusterin suurimpaan kuormitukseen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>For more information, see <bpt id="p1">[</bpt>Service Fabric cluster capacity planning considerations<ept id="p1">](/azure/service-fabric/service-fabric-cluster-capacity)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisätietoja on ohjeaiheessa <bpt id="p1">[</bpt>Service Fabric -klusterin kapasiteettisuunnittelussa huomioon otettavaa<ept id="p1">](/azure/service-fabric/service-fabric-cluster-capacity)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Virtualization and oversubscription</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Virtualisointi ja ylitilaus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toiminnan kannalta keskeiset palvelut, kuten AOS, on isännöitävä virtuaali-isännissä, joille on varattu omat resurssit (ytimet, muisti ja levy).</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>