---
title: Tuoterakenteen laskentaryhmät
description: Tässä artikkelissa on tietoja tuoterakenteen laskentaryhmistä ja niiden määrittämisestä. Tuoterakenteen laskennan suorittamista varten yksittäisille nimikkeille laskentaryhmiä on määritettävä laskentaryhmiä. Vaihtoehtoisesti on määritettävä oletuslaskentaryhmä. Laskentaryhmän laskenta-asetuksia käytetään sitten Tuoterakenteen laskenta -sivun oletusarvoina tuoterakennetta laskettaessa.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 098a2fc065f6ace992dba1b1ae78756d456eb73a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579853"
---
# <a name="bom-calculations-groups"></a>Tuoterakenteen laskentaryhmät

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja tuoterakenteen laskentaryhmistä ja niiden määrittämisestä. Tuoterakenteen laskennan suorittamista varten yksittäisille nimikkeille laskentaryhmiä on määritettävä laskentaryhmiä. Vaihtoehtoisesti on määritettävä oletuslaskentaryhmä. Laskentaryhmän laskenta-asetuksia käytetään sitten Tuoterakenteen laskenta -sivun oletusarvoina tuoterakennetta laskettaessa. 

**Varasto ja varastonhallinnan parametrit** -sivulla on käytettävä oletuslaskentaryhmää, kun taas **Vapautetun tuotteen tiedot** -sivulla on käytettävä tuotekohtaista laskentaryhmää. Järjestelmä etsii laskentaryhmän asetuksia ensin **Vapautetun tuotteen tiedot** -sivulta. Jos laskentaryhmä ei ole siellä, järjestelmä etsii sitä **Varasto ja varastonhallinnan parametrit** -sivulta. Jos järjestelmä ei löydä laskentaryhmää, käyttäjä saa virhesanoman laskennan aikana. Laskentaryhmä sisältää kustannushintamallin, myyntihintamallin ja varoitusten tarkistusluettelon käytännöt. Laskentaryhmän laskenta-asetuksia käytetään **Tuoterakenteen laskenta** -sivun oletusarvoina tuoterakennetta laskettaessa.

## <a name="purposes-of-bom-calculation-groups"></a>Tuoterakenteen laskentaryhmien tarkoitukset
Syitä tuoterakenteen laskentaryhmän määrittämiseen nimikkeelle on useita:

-   Määrittämällä **Kustannushintamalli**-kentän voi ilmoittaa ostetun osan kustannusten osuustietojen lähteen valmistetun tuotteen suunniteltua kustannusta laskettaessa. Osa valmistajista laskee suunnitellut kustannukset käyttämällä ostettujen osien ostohinnan kauppasopimuksia tai muuta perustetta, kuten kustannuslaskentaversion ostohintatietuetta.
-   Määrittämällä **Myyntihintamalli**-kentän ilmaiset, miten nimikkeen tietojen käytetään ehdotetun myyntihinnan laskennassa. Voit määrittää joko nimikkeen myyntihinnan tai kustannusryhmän. Osa valmistajista haluaa laskea valmistettujen nimikkeiden ehdotetun myyntihinnan. Laskettu myyntihinta voi perustua osan myyntihintatietuetta käytävään koontihintamenetelmään. Vaihtoehtoisesti laskettu myyntihinta voi perustua hinta+hinnankorotusmalliin, joka perustuu osan hintaan ja nimikkeen kustannusryhmään liittyvään sovellettavaan kateprosenttiin.
-   **Lopeta hajotus** -kentän avulla voit ilmaista, että valmistettua nimikettä on käsiteltävä tuoterakennelaskelmissa kustannusten koontilaskelman ostettuna nimikkeenä. Tavanomaisia skenaarioita voivat liittyä esimerkiksi ostettuun nimikkeeseen, jota valmistetaan satunnaisesti, tai valmistettuun nimikkeeseen, jota ostetaan parhaillaan. Nimike määritetään ensin valmistetuksi nimikkeeksi, jotta tuoterakenne- ja reititystiedot voidaan määrittää sekä tukemaan nimikkeen tuotantotilauksia. **Lopeta hajotus** -merkintä kuitenkin estää nimikkeen tuoterakenteen ja reitin käytön kustannuslaskelmissa. Tuoterakenteen laskenta käyttää sen sijaan nimikkeen määritettyjä kustannuksia.

## <a name="calculation-groups"></a>Laskentaryhmät
Laskentaryhmät määritetään valitsemalla kustannustenhallinnassa **Ennalta määritettyjen kustannusten käytäntöjen määrittäminen**. Voit määrittää nimikkeisiin määritetyissä laskentaryhmissä, miten laskentaryhmän mukaisten osien kustannus- tai myyntihintoja käytetään laskennan lähteenä. Voit määrittää **Laskentaryhmät**-sivulla kustannushintamallin, vaihtoehtoisen kustannushintamallin, myyntihintamallin ja varoitukset.

### <a name="cost-price-model"></a>Kustannushintamalli

**Kustannushintamalli**-kentässä on neljä vaihtoehtoa.

-   **Nimikkeen kustannushinta** – kustannushintana käytetään **Vapautettu tuote** -taulun kustannushintaa tai nimikedimensioiden yhdistelmää.
-   **Nimikkeen ostohinta** – ostohinta **Vapautettu tuoteluettelo** -sivun **Osto**-välilehden **Kustannushinta**-kentässä.
-   **Kauppasopimukset** – Voit määrittää tiettyjen nimike- ja toimittajayhdistelmien tai tiettyjen toimipaikkojen kauppasopimukset. Kun sitten valitset tässä kohdassa **Kauppasopimukset**-vaihtoehdon, käytetään ostohinnalle sekä nimikkeelle ja toimipaikalle luotua kauppasopimusta.
-   **Varastohinta** – Yksikkökustannus lasketaan tuoterakenteen laskennassa käyttämällä nimikkeen nykyistä varastoarvoa. Yksikön kustannushinta lasketaan vain, jos kirjattu määrä ja fyysinen määrä on suurempi kuin 0 (nolla).

### <a name="alternative-cost-price"></a>Vaihtoehtoinen kustannushinta

**Vaihtoehtoinen kustannushinta** -kentässä on samat vaihtoehdot kuin **Kustannushintamalli**-kentässä. Tätä kenttää käytetään kuitenkin vain, kun hintaa ei löydetä ensisijaisesta kustannushintamallista.

### <a name="sales-price-model"></a>Myyntihintamalli

**Myyntihinnat**-kentän laskennassa on kaksi vaihtoehtoa:

-   **Kustannusryhmä** – kun tämä vaihtoehto on valittu, myyntihinta lasketaan kustannusryhmän kustannushinnan ja kateasetusten perusteella.
-   **Nimikkeen myyntihinta** – kun tämä vaihtoehto on valittu, käytetään Vapautetut tuotteet -taulun **Myynti**-pikavälilehden myyntihintaa.

### <a name="stop-explosion"></a>Lopeta hajotus

**Lopeta hajotus** -valintaruudun avulla ilmaistaan, milloin valmistettua tuotetta on käsiteltävä ostettuna nimikkeenä. Yleensä **Lopeta hajotus** -valintaruutu jätetään valitsematta. Valitsemalla tämän valintaruudun voit ilmaista, että valmistettua nimikettä on käsiteltävä tuoterakenteen laskennassa osto-osana eikä valmistettuna osana. Toimipaikan mukaan nimikkeen kustannukset voidaan edelleen laskea tuoterakenteen laskennoissa. Suunniteltujen ostotilausten ja tuotantotilausten hajotus lopetetaan tuoterakenteessa, jonka osat on liitetty siihen laskentaryhmään, jossa on valittu **Lopeta hajotus** -valintaruutu. Pääajoituksessa luodaan suunnitellut tilaukset tuoterakenteen eikä tuoterakenteen nimikkeiden perusteella. Valitsemalla tämän valintaruudun voit määrität käytännössä, että kustannusta ei voi lisätä niiden nimikkeiden tuotantorakenteen laskentaa, joilla on tämä laskentaryhmä.

### <a name="warnings"></a>Varoitukset

Voit valita **Varoitukset**-pikavälilehdessä niiden varoitussanomien asetukset, joita käyttäjät saavat tuoterakenteiden laskennassa. 

Jos valitse esimerkiksi **Ei tuoterakennetta** -valintaruudun, käyttäjää varoitetaan, jos aktiivista tuoterakenneversiota ei löydetä jollekin sellaiselle osalle ja päänimikkeelle, jolle tuoterakenteen laskenta suoritetaan. Jos valitse **Ei reittiä** -valintaruudun, käyttäjä saa varoituksen, jos aktiivista reititysversiota ei löydy. Jos käytät reiteillä ja työvaiheissa resursseja, voit määrittää järjestelmän tarkistamaan nämä resurssit. Jos resurssia ei sitten löydy aktiivisen reitin jokaiselle riville, käyttäjä saa varoituksen. 

Voit varmistaa ja tarkistaa myös kulutukseen. Kulutus on määrä tietyllä reitillä. Yleensä se ilmaisee ajan, joka tarvitaan tietyn tuotantoprosessin työvaiheen suorittamiseen. Voit tarkistaa, jos nimikkeellä ei ole kustannushintaa. Jos nimikkeellä ei ole aktiivista kustannushintaa, kustannusta ei lisätä tuoterakenteen laskentaan. 

Voit tarkistaa ja varmistaa myös kustannushinnan iän. Jos esimerkiksi annat arvon **60**, se ilmaisee, että yksikön kustannushinta on arvioitava uudelleen 60 päivän kuluttua. Jos tämä raja ylittyy, järjestelmä luo varoituksen. Kustannushinta annettiin nimikkeelle esimerkiksi tämän vuoden tammikuussa. Jos nyt on elokuu, kustannushinnan antamisesta on kulunut yli 60 päivää ja käyttäjä saa varoituksen, kun tuoterakenteen laskenta suoritetaan. Voit lisätä prosentin **Kokonaiskatteen vähimmäismäärä** -kenttään. Tämä arvo ilmaisee kohdan, jossa vähimmäiskatetta ei saavuteta. Jos tietyn osan katetuottoa ei saavuteta, käyttäjä saa varoituksen. Tämä kenttä auttaakin varmistamaan, ettet alita kustannuksia ja lisäkuljetuskustannuksia, jotka voivat liittyä nimikkeeseen.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Oletusarvoiset Varasto ja varastonhallinnan parametrit -asetukset

Koska laskelmien suorittaminen edellyttää laskentaryhmiä, oletuslaskentaryhmä on määritettävä varastonhallinnan parametreissa. Näiden asetusten avulla yritykset saavat käyttöönsä kaikkia nimikkeitä koskevat vakiokustannusryhmän ja -katevaatimuksen. Jos tietyllä nimikkeellä on kuitenkin erityisiä laskentavaatimuksia, käyttäjä voi määrittää kyseiselle nimikkeelle toisen laskentaryhmän. Yleensä laskentaryhmät määritetään tuoterakenteen osan nimikkeille eikä tuoterakenteen nimikkeille. Kun varoitukset näytetään, myös laskentaryhmiä voi käyttää. Nimikkeille määritetty laskentaryhmä ohittaa varastonhallinnan parametreissa määritetyn oletusarvon. 

Voit määrittää oletusparametrin valitsemalla **Kustannushintojen hallinta** &gt; **Varaston kirjanpitokäytäntöjen määrittäminen** &gt; **Parametrit** &gt; **Varastokirjanpito** &gt; **Laskentaryhmä**. Määrittämällä oletusmääritysryhmän voit määrittää myös varoitusehdot, jotka esittävät käyttäjille kysymyksiä tuoterakenteen laskentaprosessin aikana, jos valitut osat voivat aiheuttaa laskentavirheitä.

### <a name="view-warning-messages-on-the-complete-page"></a>Näytä varoitussanomat Valmis-sivulla

Tuoterakenteen laskenta luo varoitussanomia. Voit tarkastella valittua nimikettä koskevia varoituksia. Luo esimerkiksi myynnissä ja markkinoinnissa uusi myyntitilaus nimikkeelle D0001. Jos haluat tarkastella tietoja ja varoituksia, valitse myyntilausrivin **Päivitä rivi** -valikossa **tuoterakenteeseen tai kaavaan perustuva laskenta**. Voit näyttää tuoterakenteen laskentatulokset myös **Valmis**-sivulla. Varoitussanomissa vain kaksi varoitusehtoa koskee valmistettuja nimikkeitä, kun taas neljä ehtoa voidaan käyttää missä tahansa nimikkeessä:
-   Tilanne tunnistetaan, kun valmistetulla nimikkeellä ei ole aktiivista tuoterakennetta.
-   Tilanne tunnistetaan, kun valmistetulla nimikkeellä ei ole aktiivista reititystä.
-   Tilanne tunnistetaan, kun tuoterakenteen rivin nimikkeen määrä on 0 (nolla).
-   Tilanne tunnistetaan, kun tuoterakenteen rivin nimikkeen kustannus on 0 (nolla) tai kun sillä ei ole kustannustietuetta.
-   Tilanne tunnistetaan, kun tuoterakenteen rivin nimikkeen kustannus on vanhentunut. Varoitus perustuu vertailuun, jossa laskentapäivämäärää verrataan kustannuksen enimmäisikään päivinä.
-   Tilanne tunnistetaan, kun tuoterakenteen rivin nimikkeen kannattavuusprosentti on haluttua prosenttiosuutta pienempi.

Voit määrittää useita tuoterakenteen laskentaryhmiä sen mukaan, miten paljon varoitussanomissa on oltava vaihtelua. Yhdessä tuoterakennelaskelmaryhmässä voi esimerkiksi riittää varoitusehdoksi, että tuoterakenne on aktiivinen, osien määrä on 0 (nolla) ja osakustannus on niin ikään 0 (nolla). Kun käynnistät tuoterakenteen laskennan, voit ohittaa tuoterakenteen laskentaryhmään liittyvät soveltuvat varoitusehdot. Voit myös lisätä tai poistaa varoitusehtoja. Jos esimerkiksi nykyinen tilanne ei koske reititystietoja, voi poistaa aktiivista reittiä koskevat varoitusehdot. **Huomautus:** Työajan seurannassa on **Laskentaryhmät**-sivu, mutta sivu ei liity tuoterakenteen laskentaryhmiin. Työajan seurannassa työtekijät voidaan määrittää niihin laskentaryhmiin, jotka vastaavat samaan työnjohtajaan tai esimieheen liitettyjä työntekijäryhmityksiä Työntekijän rekisteröintien laskenta voidaan tehdä automaattisesti tai manuaalisesti työnjohtaja- tai esimieskohtaisesti.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]