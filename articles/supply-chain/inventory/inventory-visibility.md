---
title: Varaston näkyvyyden apuohjelman yleiskatsaus
description: Tässä artikkelissa käsitellään varaston näkyvyyden sisältöä ja sen ominaisuuksia.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762804"
---
# <a name="inventory-visibility-add-in-overview"></a>Varaston näkyvyyden apuohjelman yleiskatsaus

[!include [banner](../includes/banner.md)]

Varaston näkyvyyden apuohjelma (eli *varaston näkyvyyspalvelu*) tarjoaa itsenäisen ja erittäin skaalautuvan mikropalvelun, joka mahdollistaa reaaliaikaiset varastomuutoskirjaukset ja näkyvyyden seurannan kaikissa tietolähteissäsi ja kanavissasi. Se tarjoaa alustan, jonka avulla voit hallita yleisiä varastoja käyttämällä toimintoja, jotka sisältävät (mutta eivät rajoitu vain) seuraavan luettelon:

- Jäljitä varaston viimeisin tila (esimerkiksi käytettävissä oleva, tilattu, ostettu, kuljetettava, palautettu ja karanteenissa) kaikkien tietolähteiden, varastojen ja sijaintien välillä liittämällä Supply Chain Managementin tai kolmannen osapuolen logistiikan tietolähteet (kuten tilaustenhallintajärjestelmät, kolmannen osapuolen yritysresurssisuunnittelun \[ERP\]-järjestelmät, myyntipisteen \[POS\]-järjestelmät ja varastonhallintajärjestelmät) varaston näkyvyyspalveluun.
- Kysele käytettävissä olevan varaston saatavuutta ja puutteita ja hae vastaukset välittömästi kutsumalla varaston näkyvyyspalvelua suoraan.
- Vältä ylimyyminen erityisesti silloin, kun kysyntä on peräisin eri kanavien kautta, tekemällä reaaliaikaista pehmeää varausta varaston näkyvyyspalvelussa.
- Hallitse luvattuja tilauksia ja asiakkaiden odotuksia paremmin antamalla tarkat nykyiset tai seuraavat saatavilla olevat päivämäärät, jotta monikanavainen saatavilla luvattaviksi (ATP) -ominaisuus voi laskea odotetut tilausten toteutumispäivät.

## <a name="extensibility"></a>Laajennettavuus

Varaston näkyvyyspalvelu on erittäin laajeneva, koska tietojen syöttöä ja tulostusta ei rajoiteta Microsoft-sovellusten käyttöön. Ulkoiset järjestelmät voivat käyttää palvelua RESTful-sovellusohjelmaliittymän (API:n) kautta. Sen lisäksi, että käytät Supply Chain Managementin tietolähteen ja -ulottuvuuksien valmiita kartoituksia, voit integroida varaston näkyvyyden useisiin kolmannen osapuolen järjestelmiin määrittämällä lisätietolähteitä, varastotilamittauksia (kutsutaan nimellä *fyysiset mitat* Varaston näkyvyys -palvelussa) ja varaston mitat määrityssovelluksen kautta. Näin voit tehdä liukumakyselyn ja muuttaa useita tietolähteitä ja ennalta määritettyjä varastodimensioita.

Koska varaston näkyvyys perustuu Microsoft Dataverseen, sen tietoja voidaan käyttää Power Appsin kanssa muodostamiseen ja integroimiseen. Lisäksi Power BI:tä voidaan käyttää luomaan mukautettuja liiketoiminnan tarpeita vastaavia koontinäyttöjä.

## <a name="scalability"></a>Skaalautuvuus

Varaston näkyvyyspalvelua voidaan skaalata ylös tai alas tietojen määrästä riippuen. Skaalattavuuskokemus on yleensä puoliksi suljettu, ja sen suorittaa Microsoftin ympäristötiimi. Se perustuu tapahtumatietojen automaattiseen tunnistukseen ja arviointiin.

Seuraavassa kuvassa on Inventory Visibilityn arkkitehtuuri.

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title="Inventory Visibilityn arkkitehtuuri" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>Toiminnon tärkeimmät ominaisuudet

### <a name="get-a-global-view-of-real-time-inventory"></a>Reaaliaikaisen varaston yleisen näkymän hakeminen

Varaston näkyvyys varmistaa, että käytettävissäsi ovat kaikkien kanavien, sijaintien ja varastojen viimeisimmät varastomäärät. Sitä käytetään eniten päivittäisen toiminnan liiketoiminnan tueksi aina, kun varastotietueita on hankittava. Valmiina käytettävissä ovat fyysinen käytettävissä oleva varasto, myydyt määrät ja ostetut määrät. Voit myös määrittää muut fyysisen varaston mitat (kuten palautetut, karanteeniin kirjatut ja kirjatut tiedot) tarpeen mukaan, jotta nämä tiedot saadaan reaaliaikaisesti. Varaston näkyvyys voi tehokkaasti käsitellä miljoonia varaston muutosten kirjaamisia. Nämä tiedot voidaan koota ja kuvata uusilla huollon varastomäärillä heti, sekuntia tai minuuttia kohti sen mukaan, miten usein tiedot kirjataan. Lisätietoja on kohdassa [Varaston näkyvyyden julkiset API:t](inventory-visibility-api.md).

### <a name="central-inventory-adjustment"></a>Keskusvaraston oikaisu

Inventory Visibilityn avulla ulkoiset järjestelmät voivat kutsua sen ohjelmointirajapintoja varastomuutosten kirjausta varten. Muutokset tulevat voimaan heti Inventory Visibilityssa. Tämän vuoksi varastosaldoa vähennetään heti.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Pehmeä varaus ylimyynnin välttämiseksi kaikissa tilauskanavissa

*Pehmeän varauksen* avulla voit määrittää tai merkitä tiettyjä määriä tilauksen tai kysynnän täyttämiseksi. Pehmeä varaus ei vaikuta fyysiseen varastoon, mutta se vähentää *käytettävissä olevan varauksen* varastomäärän ja antaa päivitetyn määrän tilauksen tulevaa täyttämistä varten. Tämä ominaisuus on hyödyllinen, jos myyntipyynnöt tai -tilaukset tulevat liiketoimiisi yhdestä tai muista kanavien tai tietolähteiden lähteistä, jotka ovat ERP-järjestelmän (System of Record Enterprise Resource Planning) ulkopuolella.

Jos Inventory Visibility -palvelussa ei käytetä alustavia varauksia, odota, kunnes ERP-järjestelmä on synkronoinut ja käsitellyt tilauksen. Tämän jälkeen saat käyttöön fyysisen varastomäärän päivityksen. Tällä prosessilla on yleensä suuri viive. Pehmeät varaukset tulevat kuitenkin voimaan heti aina, kun myyntikanavien myyntitilauksista luodaan myyntipyyntö tai -tilaus. Siksi ne auttavat ehkäisemään ylimyynnit varmistamalla, että ylimyynnit eivät tule toistensa ylimyyntitilauksiin, kun ne saavuttavat lopulta ERP-järjestelmän. Pehmeät varaukset varmistavat myös, että voit täyttää kaikki luvatut tilaukset. Siksi ne auttavat vastaamaan asiakkaan odotuksiin ja ylläpitämään asiakkaan lojaaliutta. Lisätietoja on kohdassa [Varaston näkyvyyden varaukset](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-quantity-and-dates"></a>ATP-määrän ja -päivämäärien välitön vastaus

Näkyvyys lähellä tulevaan arvioituun varastoon (mukaan lukien tarjonta, kysyntä ja arvioidut käytettävissä olevan varaston tiedot) on tärkeää, koska se auttaa yritystäsi saavuttamaan seuraavat tavoitteet:

- Minimoi varastotasot vähentääksesi varastonhallintakuluja.
- Helpottaa sisäistä tilausten käsittelyä, jotta myyjät voivat laskea lähetys- ja toimituspäivät tilatuttujen tuotteiden saatavuuden mukaan.
- Lisää läpinäkyvyys siitä, milloin asiakkaat voivat odottaa, että varastosta loppunut nimike tulee saataville, antamalla seuraavan käytettävissä olevan päivämäärän.

ATP-ominaisuus on helppo ottaa käyttöön päivittäisessä tilauksen täyttämisprosessissa. Muiden varastonäkyvyyksien lisäksi ATP-ominaisuus on *yleinen ja reaaliaikainen*. Voit näin ollen määrittää useita ATP-laskentakaavoja, jos haluat, että koko varaston käytettävyyskyselyt kattavat kaikki liiketoimintasi kanavat ja tietolähteet. Lisätietoja on kohdassa [Käytettävissä olevan varaston näkyvyyden muutosaikataulut ja luvattavissa olevat aikataulut](inventory-visibility-available-to-promise.md).

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>Varaston esikohdistus tärkeitä kanavia tai asiakkaita varten varaston kohdistuksen avulla

Inventory Visibilityn kohdistusominaisuuden avulla voit suojata ja merkitä arvokkaan varastosaldon tärkeissä kanavissa, asiakasryhmissä ja sijainneissa. Kun varasto on kohdistettu, varaston kulutus rajoittuu kohdistettuun pooliin. Pooliin jääneet määrät vähennetään lähes reaaliaikaisesti vastaamaan määrää, joka yhä on käytettävissä kulutusta varten. Lisätietoja on kohdassa [Varaston näkyvyyden varaston kohdistus](inventory-visibility-allocation.md).

### <a name="compatibility-with-wms-items"></a>Yhteensopivuus WMS-nimikkeiden kanssa

Microsoftin tavoitteena on tuottaa käyttövalmis varastohallintaprosessien (WMS) integrointi, jotta myös WMS-asiakkaat voivat nauttia varaston näkyvyyspalvelun eduista. Vuoden 2022 1. julkaisuaallon (julkinen esiversio maaliskuussa) varastopalvelu tukee WMS-nimikkeen käytettävissä olevan varaston kyselyitä ja ATP:tä. Alustavaa varausta ja kohdistustoimintoa tuetaan WMS:n asiakkaita varten seuraavassa aallossa. Lisätietoja on kohdassa [Varaston näkyvyyden tuki WMS-nimikkeille](inventory-visibility-whs-support.md).

Seuraavassa kuvassa on korkean tason yhteenveto olemassa olevista ominaisuuksista ja siitä, miten ne voidaan sijoittaa tietovuossa.

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title="Inventory Visibility -ominaisuuden yleiskatsaus" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>Käyttöoikeudet

Varaston näkyvyyspalvelu on käytettävissä seuraavissa versioissa:

- **Inventory Visibility -apuohjelma Microsoft Dynamics 365 Supply Chain Managementissa** – yrityksille, joilla on voimassa oleva Supply Chain Management -käyttöoikeus Inventory Visibility on käytettävissä ilman lisäkustannuksia. Koska Inventory Visibility perustuu Microsoft Power Platformiin, sitä koskevat Microsoft Power Platformin tallennustilan kapasiteetin ja ohjelmointirajapinnan rajat. Supply Chain Management -käyttöoikeuden tulee sisältää oletustallennustila- ja ohjelmointirajapintakapasiteetti. Jos tarvitset lisää tallennustila- ja ohjelmointirajapintakapasiteettia, voit ostaa Professional-käyttöoikeuden. Lisätietoja ohjelmointirajapinnan oletuskohdistuksesta ja Professional-käyttöoikeudesta on kohdassa [Pyyntöjen rajat ja kohdistukset](/power-platform/admin/api-request-limits-allocations) ja [Microsoft Power Platformin käyttöoikeuksien yleiskatsaus](/power-platform/admin/pricing-billing-skus). Oletustallennustilan ja ohjelmointirajapinnan kohdistusten avulla voit aloittaa Inventory Visibility -apuohjelman kokeilemisen jo tänään. Lisätietoja on kohdassa [varaston näkyvyyden asennus ja määritys](inventory-visibility-setup.md). Jos arvioitu ohjelmointirajapinta- ja tallennustilakäyttö ylittää vakiokohdistuksen, voit pyytää myyntiedustajaa pyytämään poikkeusta ympäristötiimiltä.
- **Varaston näkyvyyspalvelu komponenttina IOM:ssä** – Tämä versio on tarkoitettu joko Intelligent Order Management (IOM) -asiakkaille tai yrityksille, jotka eivät käytä Supply Chain Management -järjestelmää ERP-järjestelmänään. Lisenssi sisältyy Intelligent Order Management -nippuun. Lisätietoja on kohdassa [Intelligent Order Management – yleiskatsaus](/dynamics365/intelligent-order-management/overview).

## <a name="inventory-visibility-terminology"></a>Inventory Visibilityn terminologia

On tärkeää ymmärtää seuraavat käsitteet ja termit Inventory Visibility -apuohjelman käsittelemisen yhteydessä:

- **Tietolähde** – Tietolähde ilmaisee järjestelmän, josta tiedot saadaan.
- **Dimensiot** – Dimensiot tunnistavat tuotteiden ominaisuudet. Ne voivat olla tallennustiladimensioita (kuten toimipaikka tai varasto) tai tuotedimensioita (kuten väri, koko ja tyyli).
- **Fyysiset mitat** – Fyysiset mitat ovat määriä, jotka mittaavat erilaisia varaston tiloja, kuten varastosaldoa sekä ostettuja, tilauksessa olevia ja myytyjä tuotteita.
- **Lasketut mitat** – Lasketut mitat ovat kvantitatiivisia mittoja, jotka lasketaan fyysisten mittojen joukosta. Esimerkiksi laskettu *Käytettävissä yhteensä* -mitta lasketaan seuraavasti: *varastosaldo* + *ostetut* – *tilauksessa* – *myydyt*.
- **Osio** – Osio määrittää, miten varaston näkyvyys jakaa vastaanotetut tiedot. Tällä hetkellä oletusosio on toimipaikka ja sijainti.
- **Indeksihierarkia** – Indeksihierarkia määrittää lisää sitä, miten varastosta tehdään kysely. Sen avulla saadaan yksityiskohtaiset tulokset.

Lisätietoja näistä termeistä ja käsitteistä on kohdassa [Inventory Visibilityn määrittäminen](inventory-visibility-configuration.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
