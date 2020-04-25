---
title: Ostotilausten luominen
description: Tässä artikkelissa käsitellään ostotilauksen manuaalisen luonnin prosesseja ja vaihtoehtoja.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16e6170bdc8f0adcefbe310fcbf61c06aa68f02d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207968"
---
# <a name="create-purchase-orders"></a>Ostotilausten luominen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään ostotilauksen manuaalisen luonnin prosesseja ja vaihtoehtoja.

Ostotilauksen luonnin yhteydessä koko tilausta koskevat yleiset tiedot määritetään ostotilauksen otsikossa, jonka jälkeen voit lisätä ostotilausrivejä. Tässä artikkelissa käsitellään muutamia käytettävissä olevia usein käytettyjä asetuksia.  

Voit luoda ostotilauksia myös kopioimalla rivit toisesta ostotilausasiakirjasta tai myyntitilauksesta. Voit tässä tapauksessa muuntaa varaston merkin päinvastaiseksi samoin kuin voit muuntaa laskun merkin käänteiseksi osoituksena hyvityksestä.  

Vaikka ostotilauksia voi luoda manuaalisesti, ne luodaan yleensä muista prosesseista. Tilaukset voidaan luoda automaattisesti muiden asiakirjojen, kuten ehdotusten, perusteella. Ne voidaan luoda myös pääsuunnitteluprosessin osana suunniteltuja ostotilauksia hyödyntämällä. Jos käytät ostosopimuksia, ostotilaukset voidaan luoda **Vapauta tilaus** -toiminnolla. Ostotilauksen luontiin myös muita kehittyneitä menetelmiä. Tilaukset voidaan esimerkiksi luoda, kun käytät suoratoimitusta tai konsernin sisäisiä tilausketjuja.

## <a name="creating-a-purchase-order-header"></a>Ostotilauksen otsikon luonti
Kun luot uuden ostotilauksen, voit antaa avautuvaan valintaikkunaan yleisimmät ostotilauksen otsikon tiedot. Kun suljet valintaikkunan valitsemalla **OK**, tilaus luodaan ja voit sitten määrittää lisätietoja otsikkoon.  

Ensimmäinen ostotilausta luotaessa harkittava tieto on tilauksen tyyppi. Eniten käytetty **Ostotilaus**-tyyppi. Jos kuitenkin tarvitaan hyvityslaskua, voit käyttää **Palautettu tilaus** -tyyppiä.  

Määritä toimittaja **Toimittajatili**-kentässä. Voit etsiä tässä kentässä joko asiakasta tai toimittajan nimiä. Jos toimittajan toimitukset tulevat useasta sijainnista mutta käytössä on yksi laskutustili, voit valita kyseisen laskutustilin **Laskutustili**-kenttä ja käyttää sitä sitten eri toimittajatilien kanssa. Jos sinun on luotava ostotilaus tuotteille, joita ei tilata toistuvasti, voit käyttää **Kertatoimittaja**-vaihtoehtoa. Tämä asetus luo automaattisesti uuden toimittajatilin, joka on merkitty kertatiliksi. Tämä helpottaa kertatilien tyhjentämistä myöhemmin **Ostoreskontra**-moduulissa. Kun valitset toimittajatilin, monet ostotilauksen otsikon kentät perivät oletusarvot toimittajatiliin liitetyistä tiedoista. Esimerkiksi oletustoimituspaikka ja -varasto kopioidaan toimittajan tiedoista. Voit kuitenkin ohittaa nämä oletusarvot, jos osto on tarkoitettu toiseen sijaintiin.  

Jos toimittaja on antanut tilaukselle viitenumeron, voit tallentaa nämä tiedot **Toimittajaviite**-kenttään. Palautustilauksille on määritettävä arvo **Palautusnumero**-kenttään, joka viittaa toimittajan palautuskäsittelyn valtuutukseen.  

Jos tilaukseen on liitetty ostosopimus, voit määrittää nämä tiedot **Ostosopimus**-kenttään.  

Ostotilauksen otsikossa on myös tietoja kuluista, jotka koskevat koko tilausta eikä yksittäisiä rivejä. Kulut voidaan lisätä automaattisesti tilaukseen, jos automaattiset kulut on määritetty toimittajalle tai toimittajan kuluryhmälle. Voit lisätä kuluja myös manuaalisesti tilauksen otsikkoon valitsemalla toimintoruudussa **Kulujen ylläpito**.

## <a name="adding-purchase-order-lines"></a>Ostotilausrivien lisääminen
Ostotilaukset voivat koskea fyysisiä tuotteita tai palveluja. Varastomalliryhmän asetus määrittää, käytetäänkö tiettyä nimiketunnusta tuotteessa tai palvelussa. Yleensä nimiketunnus määrittää ostetun tuotteen. Jos tilaus on kuitenkin suoraan kulutettaville tuotteille tai palveluille, voit määrittää nimikkeen myös hankintaluokan avulla.  

Ostotilausriveille on paljon kenttiä, monissa kentissä on oletusarvo tai tilauksen otsikosta peritty arvo. Lisää kenttiä määritetään, kun valitset tuotteen tai palvelun. Useimmin manuaalisesti määritettäviä kenttiä ovat nimiketunnus-, määrä- ja pyydetty toimituspäiväkenttä. Myös yksikköhintaa ja alennuksia koskevat tiedot ovat erittäin tärkeitä, mutta näiden kenttien arvot tulevat usein kauppasopimuksista tai ostosopimuksista.  

Kun valitset tuotteen, voit hakea tuotetta koko nimellä tai sen osalla tuotetunnuksen sijaan. Jos tuotteella on useita variantteja, kuten eri kokoja, saat yleiskuvan käytettävistä olevista varianteista käyttämällä **Lisää rivejä** -toiminnolla tai käyttämällä **Muuttujan numero** -kentän hakua.  

Kullekin ostotilausriville valitulle nimikkeelle on usein määritettävä useita dimensioita. Määritettävät dimensiot määräytyvät päätuotemääritykseen määritettyjen dimensioryhmien mukaan. Usein on esimerkiksi määritettävä sijainti ja varasto ilmaisemaan toimipaikkaa, johon tuote on toimitettava. Tuotevariantit tunnistetaan määrittämällä muuttujan numero tai antamalla vähintään yhden tuotedimension arvot, kuten väri, koko, määritykset tai tyyli. Voit tunnistaa kunkin varastoerän yksilöllisesti seurantadimensioilla, kuten erä- ja sarjanumerolla. Kun olet luonut tilauksen, voit siepata tilauksen dimensioarvot **Rekisteröinti**-toiminnolla. Olet esimerkiksi tilannut tuotetta viisi kappaletta. Rekisteröit myöhemmin, että kappaleista kolme on mustia ja kaksi sinisiä. Tämä on vaihtoehtoinen tapa siepata dimension tiedot saapumisrekisteröinnin aikana.  

Voit tarkistaa varastoitujen tuotteiden varastotapahtuman tilatiedot. Haluat ehkä esimerkiksi tarkistaa varastosaldon, jotta voit päättää tilausmäärästä. Vaihtoehtoisesti voit haluta tarkistaa tilatun määrän varastotilan ja selvittää, onko saapumisrekisteröinti tehty.  

Ostotilausrivillä, jota käytetään tuotteen palauttamiseen toimittajalle, on negatiivinen määrä. Voit valita palautettavan erän **Varaus**-toiminnolla.  

Haluat ehkä joskus jakaa tilatun määrän, jotta sen eri osat toimitetaan eri päivämäärinä. Voit määrittää nämä toimitukset **Toimitusaikataulu**-toiminnolla, jonka voi valita **Ostotilausrivi**-valikossa **Rivit**-näkymässä.  

Kulut voidaan lisätä automaattisesti ostotilausriveille, jos automaattiset kulut on määritetty toimittajalle tai toimittajan kuluryhmälle ja nimike tai nimikkeen kuluryhmälle. Kulut lisätään kuitenkin enemmän yleensä kulut lisätään manuaalisesti että tilausrivin tasolla. Voit lisätä kulun avaamalla **Kulujen ylläpito** -sivun **Kulujen ylläpito** -toiminnon **Myyntitiedot**-valikossa **Rivit**-näkymässä. Kulujen lisäämisen etuna suoraan tilausrivitasolla on kulujen kohdistaminen varastokustannuksena. Voit määrittää koodit tilin tuotekustannukseen **Nimike**-debet-vaihtoehdolla. Tällaiset kulut on kohdistettava ostotilauksen otsikosta riveille ennen tilauksen vahvistamista. Haluat ehkä esimerkiksi kohdistaa kulut kullekin riville määrän perusteella. Kululuokan vaikuttaa myös siihen, miten kulut lasketaan. Kiinteät kulut esimerkiksi määrittävät kiinteän summan ja prosenttikulut lasketaan tilausrivin nettosumman prosenttiosuutena. Ostotilaukset voidaan määrittää kuormalle, ja kuorma voi sisältää arvion kuljetuskustannusten odotetuista kuluista. Voit kohdistaa tämän kulun kuormasta takaisin ostotilausriveille.

## <a name="purchase-order-actions"></a>Ostotilaustehtävät
Kun olet lisännyt otsikon ja rivit ostotilaukseen, lisävaiheet on täydennettävä, ennen kuin tilaus voidaan vahvistaa. Koska valittavia vaihtoehtoja on niin monia, [Toiminnon haku](../../fin-and-ops/get-started/action-search.md) voi auttaa löytämään sopivan valikkovaihtoehdon.  

Voit määrittää tilauksen tuotteet niin, että niillä lisänimikkeitä. Lisänimikkeet ovat tuotteita, jotka on ostettava tai jotka voidaan ostaa yhdessä muiden tuotteiden kanssa. Lisätuotteita voidaan lisätä maksutta liittyvinä tuotteina tai voit päättää, lisätäänkö ne tilaukseen vai ei. Voit tarkistaa lisätuotteet, kun kukin tilausrivi on lisätty. Todennäköisesti on kuitenkin kätevämpää tarkastella kaikkien tilausrivien lisänimikkeitä tai lisätä niitä **Lisänimikkeet**-sivulla, jonka voit avata toimintoruudusta.  

Alennukset lisätään yleensä riveille rivejä luotaessa. Muutamat alennukset koskevat kuitenkin koko tilausta.

-   **Kokonaisalennus**-toiminto laskee koko tilaukseen käytettävän kokonaisalennusprosentin. Tätä alennusta ei pidä sekoittaa käteisalennusprosenttiin. Käteisalennuksia käytetään laskun maksun yhteydessä, ja ne määräytyvät tietyn päivämäärän mukaisen maksunselvityksen mukaan.
-   Jos käytössä on monirivialennus, laske ja määritä se tilaukseen **Monirivialennus**-toiminnolla. Monirivialennukset ovat alennuksia, jotka voidaan tarjota, jos tilauksen tuoteyhdistelmä ylittää yhteisen raja-arvon. Vain muutamat yritykset käyttävät tätä alennustyyppiä.

Jos kulujen kulukoodi käyttää **Nimike**-veloitustyyppiä, se on määritettävä rivitasolla ennen tilauksen vahvistamista. Nämä kulut kannattaa ehkä määrittää tilauksen otsikkotasolla, jolloin voit määrittää kulun kokonaissumman. Tässä tapauksella kulu on kuitenkin kohdistettava kullekin riville, ennen kuin tilaus voidaan vahvistaa. Voit käyttää **Kohdista kulut** -toimintoa jakamaan summat kuluista, jotka on määritetty otsikkotasolla tilausriveille. Kulut voidaan jakaa kunkin rivin nettosumman tai tilatun määrän mukaan tai tasaisesti kaikille tilausriveille. Kun kulut on kohdistettu riveille, kulu poistetaan tilauksen otsikosta.  

Ostotilauksen voidaan määrittää edellyttämään, että budjettirahoitus kohdistetaan tilaukseen, ennen kuin se voidaan käsitellä. Tässä tapauksessa voit kohdistaa budjetin **Budjetin tarkastus** -toiminnolla.  

Joudut ehkä viivyttämään ostotilauksen valmistumista. Joudut esimerkiksi ehkä pyytämään lisätietoja tuotteista tai palveluista tai sinun on ehkä hankittava kulutuslupa. Tilauksen pidättämiseen on useita tapoja. Voit esimerkiksi odottaa tilauksen vahvistusta. Vaihtoehtoisesti, jos käytössä on muutoksenhallinnan työnkulku, tilausta ei lähetetä hyväksyttäväksi. Jos tietyn toimittajan kaikki tilauksen on estettävä, voit merkitä toimittajan **pitoon** päätoimittajassa käsiteltäväksi. Myös tietyt tilanteet voivat estää tilauksen käsittelyn. Käsittely voidaan esimerkiksi estää, jos luottorajat on ylitetty tai tarvittava budjettirahoitus ei ole käytettävissä.

<a name="additional-resources"></a>Lisäresurssit
--------

[Ostotilausten yleiskatsaus](purchase-order-overview.md)

[Ostotilausten hyväksyminen ja vahvistaminen](purchase-order-approval-confirmation.md)

[Tuotteen vastaanotto ostotilausten perusteella](product-receipt-against-purchase-orders.md)

[Toimittajan laskujen yleiskatsaus](../../finance/accounts-payable/vendor-invoices-overview.md)



