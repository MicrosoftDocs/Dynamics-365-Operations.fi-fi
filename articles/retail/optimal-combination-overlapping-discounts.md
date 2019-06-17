<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="fi-FI">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Määritä optimaalinen yhdistelmä päällekkäisiä alennuksia</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun alennukset menevät päällekkäin, sinun on määritettävä alennuksien yhdistelmä, joka tuottaa pienimmän tapahtumasumman tai suurimman kokonaisalennuksen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun alennuksen määrä vaihtelee ostettujen tuotteiden hinnan mukaan (kuten yleisessä vähittäismyynnin "osta 1, saat toisen X prosentin alennuksella" -alennuksessa), tästä prosessista tulee yhdistelmäoptimoinnin ongelma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Määritä optimaalinen yhdistelmä päällekkäisiä alennuksia</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun alennukset menevät päällekkäin, sinun on määritettävä alennuksien yhdistelmä, joka tuottaa pienimmän tapahtumasumman tai suurimman kokonaisalennuksen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun alennuksen määrä vaihtelee ostettujen tuotteiden hinnan mukaan (kuten yleisessä vähittäismyynnin Osta 1, saat toisen X prosentin alennuksella -alennuksessa), tästä prosessista tulee yhdistelmäoptimoinnin ongelma.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä artikkeli koskee Microsoft Dynamics AX 2012 R3 -versiota, jossa KB 3105973 (julkaistu 2. marraskuuta 2015) tai uudempaa, Microsoft Dynamics 365 for Retailia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Päällekkäisten alennusten käyttöä varten on otettu menetelmä, jolla voidaan määrittää päällekkäisten alennusten yhdistelmän käyttö mahdollisimman nopeasti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kutsumme tätä uutta menetelmää <bpt id="p1">**</bpt>rajan-arvojen luokitteluksi<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raja-arvojen luokittelua käytetään silloin kun aika, joka vaaditaan mahdollisten päällekkäisten alennusten yhdistelmien arvioimiseen, ylittää raja-arvon, joka määritetään <bpt id="p1">**</bpt>Vähittäismyynnin parametrit<ept id="p1">**</ept> -sivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raja-arvon luokittelumenetelmässä arvo lasketaan kullekin päällekkäiselle alennukselle käyttämällä jaettujen tuotteiden alennuksen arvoa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sitten päällekkäisiä alennuksia käytetään suurimmasta suhteellisesta arvosta pienimpään suhteelliseen arvoon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisätietoja tästä uudesta menetelmästä on jäljempänä tässä artikkelissa olevassa Raja-arvo-osassa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raja-arvon luokittelua ei käytetä, kun tuotteen alennussummat eivät vaikuta tapahtuman toisiin tuotteisiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tätä menetelmää ei käytetä esimerkiksi kahden yksinkertaisen alennuksen tapauksessa tai yksinkertaisen määräalennuksen yhteydessä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkkejä alennuksista</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voit luoda rajoittamattoman määrän vähittäismyynnin alennuksia yhteisille tuotejoukoille.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kuitenkin ilman rajoituksia saattaa ilmaantua suorituskyvyn ongelmia, kun yrität laskea alennukset, joita pitäisi käyttää eri tuotteissa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seuraavissa esimerkeissä kuvataan tarkemmin tätä ongelmaa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkissä 1 aloitamme kahdesta tuotteesta ja kahdesta päällekkäisestä alennuksesta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sitten esimerkissä 2 näytämme, miten ongelma kehittyy, kun tuotteita on useampia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkki 1: Kaksi tuotetta ja kaksi alennusta</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä esimerkissä tarvitaan kaksi tuotetta kunkin alennuksen saadakseen ja alennuksia ei voi yhdistää.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä esimerkissä alennukset ovat <bpt id="p1">**</bpt>Paras hinta<ept id="p1">**</ept> -alennuksia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Molemmat tuotteet oikeuttavat molempiin alennuksiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tässä ovat nämä kaksi alennusta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Esimerkki kahdesta parhaan hinnan alennuksesta</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Mille tahansa kahdelle tuotteelle parempi näitä alennuksista määräytyy kummankin tuotteen hinnan perusteella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun molempien tuotteiden hinta on sama tai lähes sama, alennus 1 on parempi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kun yhden tuotteen hinta on huomattavasti pienempi kuin toisen tuotteen hinta, alennus 2 on parempi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Näitä kahta alennusta voi vertailla keskenään tällä matemaattisella säännöllä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Alennusten arviointisääntö</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kun tuotteen 1 hinta on yhtä suuri kuin kaksi kolmasosaa tuotteen 2 hinnasta, kaksi alennusta ovat yhtä suuria.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä esimerkissä voimassa oleva alennusprosentti alennukselle 1 vaihtelee muutamasta prosentista (kun näiden kahden tuotteen hinnat ovat kaukana toisistaan) enintään 25 prosenttiin (kun kahdella tuotteella on sama hinta).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alennuksen 2 voimassa oleva alennusprosentti on kiinteä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Se on aina 20 prosenttia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koska alennuksen 1 voimassa oleva alennusprosentti voi olla suurempi tai pienempi kuin alennus 2, paras alennus riippuu näiden kahden alennettavan tuotteen hinnoista.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä esimerkissä laskutoimitukset on suoritettu nopeasti, koska käytetään vain kahta alennusta kahteen tuotteeseen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">On vain kaksi mahdollista yhdistelmää: alennuksen 1 yksi käyttö tai alennuksen 2 yksi käyttö.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä ei tarvitse laskea permutaatioita, koska niitä ei ole.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kunkin alennuksen arvo lasketaan käyttämällä kumpaakin tuotetta ja parasta alennusta käytetään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkki 2: Neljä tuotetta ja kaksi alennusta</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seuraavaksi käytämme neljää tuotetta ja samaa kahta alennusta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaikki neljä tuotetta oikeuttavat molempiin alennuksiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä tapauksessa on 12 mahdollista yhdistelmää.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lopuksi kahta alennusta sovelletaan tapahtumaan jossain seuraavista kolmesta yhdistelmästä: kaksi alennuksen 1 käyttöä, kaksi alennuksen 2 käyttöä tai sekä yksi alennuksen 1 käyttö että yksi alennuksen 2 käyttö.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mahdollisten yhdistelmien esittelemiseksi tarkastelemme kahta eri neljän tuotteen joukkoa, joilla on eri hinnat:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaikilla neljällä tuotteella on sama hinta 15,00 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä tapauksessa paras alennusyhdistelmä on kaksi alennuksen 1 käyttöä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kaksi tuotetta on täysihintaisia ja kahdesta tuotteesta saa 50 prosenttia alennusta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tapahtuman alennettu loppusumma on 45 $ (15 + 15 + 7,50 + 7,50), joka on 15 $ (25 prosenttia) alentamattomasta hinnasta 60 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Alennus 2 on vain 12 $ (20 prosenttia).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kahden tuotteen hinta on 20 $, yhden tuotteen 15 $ ja yhden 5 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä tapauksessa paras alennusyhdistelmä alennuksen 2 yksi käyttö ja alennuksen 1 käyttö.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seuraavissa taulukoissa on kuvattu alennukset.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voit lukea taulukoita käyttämällä yhtä tuotetta riviltä ja yhtä tuotetta sarakkeesta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Esimerkiksi alennuksen 1 taulukossa yhdistämällä kaksi 20 dollarin tuotetta saat alennusta 10 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Alennuksen 2 taulukossa yhdistämällä yhden 15 dollarin tuotteen ja 5 dollarin tuotteen saat alennusta 4 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Esimerkki, jossa käytetään neljää tuotetta samoissa kahdessa alennuksessa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ensin etsimme suurimman alennuksen, joka on saatavilla mille tahansa kahdelle tuotteelle käyttäen kumpaa tahansa alennusta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nämä kaksi taulukkoa näyttävät kaikkien kahden tuotteen yhdistelmien alennussummat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Taulukoiden varjostetut osiot edustavat joko tuotteen yhdistämistä itsensä kanssa (jota ei voi tehdä) tai kahden tuotteen käänteistä yhdistämistä, joka tuottaa saman alennussumman (ja voidaan jättää huomiotta).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Katsomalla taulukoita näet, että alennus 1 on kahdelle 20 dollarin tuotteelle suurin alennus, joka on saatavilla kummalla tahansa alennuksella kaikille neljälle tuotteelle.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Tämä alennus näkyy korostettuna ensimmäisessä taulukossa vihreällä.) Jäljelle jää vielä 15 ja 5 dollarin tuotteet.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Katsomalla taulukoita uudelleen näet, että näille kahdelle tuotteelle alennus 1 antaa 2,50 dollarin alennuksen, kun taas alennus 2 antaa 4 dollarin alennuksen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Näin ollen voimme valita alennuksen 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kokonaisalennus on 14 $.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Havainnollistamisen avuksi tässä on kaksi lisätaulukkoa, joissa näkyy voimassa oleva alennusprosentti kaikille mahdollisille kahden tuotteen yhdistelmille sekä alennukselle 1 että alennukselle 2.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vain puolet yhdistelmien luettelosta näytetään, koska näille kahdelle alennukselle ei ole merkitystä, missä järjestyksessä kaksi tuotetta alennetaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Korkein tehokas alennus (25 prosenttia) on korostettu vihreällä ja pienin tehokas alennus (10 prosenttia) on korostettu punaisella.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Kummankin alennuksen kaikkien kahden tuoteyhdistelmän todellinen alennusprosentti</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kun hinnat vaihtelevat ja vähintään kaksi alennusta kilpailee, ainoa tapa varmistaa paras alennusten yhdistelmä on arvioida molemmat alennukset ja verrata niitä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Mahdollisia yhdistelmiä yhteensä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä osassa jatketaan edellisen osan esimerkkiä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lisäämme enemmän tuotteita ja vielä yhden alennuksen, jolloin näemme, kuinka monta yhdistelmää pitää laskea ja verrata.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Seuraavassa taulukossa on esitetty mahdollisten alennusyhdistelmien määrä tuotteen määrän kasvaessa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Taulukosta näkyy, mitä tapahtuu, kun on kaksi päällekkäistä alennusta, kuten edellisessä esimerkissä, ja kun on kolme päällekkäistä alennusta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Mahdollisten arvioitavien alennusyhdistelmien määrä ylittää määrän, jota edes nopea tietokone ei voi laskea ja verrata riittävän nopeasti vähittäismyynnin tarpeisiin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">Mahdollisten alennusyhdistelmien määrä tuotteen määrän kasvaessa</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kun käytetään vielä suurempia määriä tai useampia päällekkäisiä alennuksia, mahdollisten alennusyhdistelmien kokonaismäärä nousee nopeasti miljooniin, ja parhaan yhdistelmän valinta kestää jo huomattavan pitkään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vähittäismyynnin hintamoduuliin on tehty joitain optimointeja, jotta voitaisiin vähentää arvioitavien yhdistelmien määrää.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Koska tapahtuman päällekkäisten alennusten määriä ja tuotemääriä ei ole rajoitettu, paljon yhdistelmiä on arvioitava aina, kun on päällekkäisiä alennuksia.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raja-arvojen luokittelumenetelmä on yksi ratkaisu tähän ongelmaan.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raja-arvomenetelmä</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Eksponentiaalisesti kasvavan arvioitavien yhdistelmien määrän ongelman ratkaisemiseksi on olemassa optimointi, joka laskee arvon per jaettu tuote kullekin alennukselle, joka on kohdistettu tuotejoukkoon, johon voidaan käyttää kahta tai useampaa alennusta.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Viittaamme tähän arvoon jaettujen tuotteiden alennuksen <bpt id="p1">**</bpt>raja-arvona<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Raja-arvo on tuotemäärän nostamisen keskimääräinen kokonaisalennussumman nousu, kun jaetut tuotteet kuuluvat kunkin alennuksen piiriin.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Raja-arvo lasketaan ottamalla kokonaisalennussumma (DTotal), vähentämällä alennussumma ilman jaettuja tuotteita (DMinus<ph id="ph1">\\</ph> Shared) ja jakamalla kyseinen erotus jaettujen tuotteiden määrällä (ProductsShared).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Raja-arvon laskentakaava</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kun jaetun tuotejoukon kunkin alennuksen raja-arvo on laskettu, alennukset käytetään jaettuihin tuotteisiin järjestyksessä, läpi kaikkien tapausten, korkeimmasta raja-arvosta pienimpään raja-arvoon.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tässä menetelmässä kaikkia jäljellä olevia alennusmahdollisuuksia ei verrata aina, kun yhtä alennuksen ilmentymää käytetään.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sen sijaan päällekkäisiä alennuksia verrataan yhden kerran ja käytetään sitten järjestyksessä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Muita vertailuja ei tehdä.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Voit määrittää ylärajan, joka ylitettäessä siirrytään käyttämään raja-arvomenetelmää, <bpt id="p1">**</bpt>Alennus<ept id="p1">**</ept>-välilehdessä <bpt id="p2">**</bpt>Vähittäismyynnin parametrit<ept id="p2">**</ept> -sivulla.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hyväksyttävä aika kokonaisalennuksen laskentaan vaihtelee vähittäiskaupan toimialasta riippuen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tämä aika on yleensä kuitenkin kymmenistä millisekunneista yhteen sekuntiin.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>