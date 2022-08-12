---
title: Varaston näkyvyyden apuohjelman yleiskatsaus
description: Tässä artikkelissa käsitellään varaston näkyvyyden sisältöä ja sen ominaisuuksia.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 274f9b368a6074725d1938de5f2172d2810a5985
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066637"
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

## <a name="feature-highlights"></a>Toiminnon tärkeimmät ominaisuudet

### <a name="get-a-global-view-of-real-time-inventory"></a>Reaaliaikaisen varaston yleisen näkymän hakeminen

Varaston näkyvyys varmistaa, että käytettävissäsi ovat kaikkien kanavien, sijaintien ja varastojen viimeisimmät varastomäärät. Sitä käytetään eniten päivittäisen toiminnan liiketoiminnan tueksi aina, kun varastotietueita on hankittava. Valmiina käytettävissä ovat fyysinen käytettävissä oleva varasto, myydyt määrät ja ostetut määrät. Voit myös määrittää muut fyysisen varaston mitat (kuten palautetut, karanteeniin kirjatut ja kirjatut tiedot) tarpeen mukaan, jotta nämä tiedot saadaan reaaliaikaisesti. Varaston näkyvyys voi tehokkaasti käsitellä miljoonia varaston muutosten kirjaamisia. Nämä tiedot voidaan koota ja kuvata uusilla huollon varastomäärillä heti, sekuntia tai minuuttia kohti sen mukaan, miten usein tiedot kirjataan. Lisätietoja on kohdassa [Varaston näkyvyyden julkiset API:t](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Pehmeä varaus ylimyynnin välttämiseksi kaikissa tilauskanavissa

*Pehmeän varauksen* avulla voit määrittää tai merkitä tiettyjä määriä tilauksen tai kysynnän täyttämiseksi. Pehmeä varaus ei vaikuta fyysiseen varastoon, mutta se vähentää *käytettävissä olevan varauksen* varastomäärän ja antaa päivitetyn määrän tilauksen tulevaa täyttämistä varten. Tämä ominaisuus on hyödyllinen, jos myyntipyynnöt tai -tilaukset tulevat liiketoimiisi yhdestä tai muista kanavien tai tietolähteiden lähteistä, jotka ovat ERP-järjestelmän (System of Record Enterprise Resource Planning) ulkopuolella.

Jos varaston näkyvyyspalvelussa ei käytä pehmeää varausta, odota, kunnes ERP-järjestelmä synkronoi tilauksen ja käsittelee sen fyysisen varastomäärän päivityksen takia. Tällä prosessilla on yleensä suuri viive. Pehmeät varaukset tulevat kuitenkin voimaan heti aina, kun myyntikanavien myyntitilauksista luodaan myyntipyyntö tai -tilaus. Siksi ne auttavat ehkäisemään ylimyynnit varmistamalla, että ylimyynnit eivät tule toistensa ylimyyntitilauksiin, kun ne saavuttavat lopulta ERP-järjestelmän. Pehmeät varaukset varmistavat myös, että voit täyttää kaikki luvatut tilaukset. Siksi ne auttavat vastaamaan asiakkaan odotuksiin ja ylläpitämään asiakkaan lojaaliutta. Lisätietoja on kohdassa [Varaston näkyvyyden varaukset](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>ATP-päivämäärien vahvistuksen välitön vastaus

Näkyvyys lähellä tulevaan arvioituun varastoon (mukaan lukien tarjonta, kysyntä ja arvioidut käytettävissä olevan varaston tiedot) on tärkeää, koska se auttaa yritystäsi saavuttamaan seuraavat tavoitteet:

- Minimoi varastotasot vähentääksesi varastonhallintakuluja.
- Helpottaa sisäistä tilausten käsittelyä, jotta myyjät voivat laskea lähetys- ja toimituspäivät tilatuttujen tuotteiden saatavuuden mukaan.
- Lisää läpinäkyvyys siitä, milloin asiakkaat voivat odottaa, että varastosta loppunut nimike tulee saataville, antamalla seuraavan käytettävissä olevan päivämäärän.

ATP-ominaisuus on helppo ottaa käyttöön päivittäisessä tilauksen täyttämisprosessissa. Muiden varastonäkyvyyksien lisäksi ATP-ominaisuus on *yleinen ja reaaliaikainen*. Voit näin ollen määrittää useita ATP-laskentakaavoja, jos haluat, että koko varaston käytettävyyskyselyt kattavat kaikki liiketoimintasi kanavat ja tietolähteet. Lisätietoja on kohdassa [Käytettävissä olevan varaston näkyvyyden muutosaikataulut ja luvattavissa olevat aikataulut](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-warehouse-management-processes-wms-items"></a>Yhteensopivuus varastonhallintaprosessien (WMS) kanssa

Microsoftin tavoitteena on tuottaa käyttövalmis varastohallintaprosessien (WMS) integrointi, jotta myös WMS-asiakkaat voivat nauttia varaston näkyvyyspalvelun eduista. Vuoden 2022 1. julkaisuaallon (julkinen esiversio maaliskuussa) varastopalvelu tukee WMS-nimikkeen käytettävissä olevan varaston kyselyitä ja ATP:tä. Pehmeää varausta ja kohdistustoimintoa tuetaan WMS:n asiakkaille seuraavassa aallossa. Lisätietoja on kohdassa [Varaston näkyvyyden tuki WMS-nimikkeille](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Käyttöoikeudet

Varaston näkyvyyspalvelu on käytettävissä seuraavissa versioissa:

- **Varaston näkyvyyden lisäosa Microsoft Dynamics 365 Supply Chain Managementissa** – yrityksille, joilla on voimassa oleva Supply Chain Management -käyttöoikeus, varaston näkyvyys on käytettävissä ilman ylimääräisiä käyttöoikeuskustannuksia. Voit aloittaa sen kokeilun tänään. Lisätietoja on kohdassa [varaston näkyvyyden asennus ja määritys](inventory-visibility-setup.md).
- **Varaston näkyvyyspalvelu komponenttina IOM:ssä** – Tämä versio on tarkoitettu joko Intelligent Order Management (IOM) -asiakkaille tai yrityksille, jotka eivät käytä Supply Chain Management -järjestelmää ERP-järjestelmänään. Lisenssi sisältyy IOM-nippuun. Lisätietoja on kohdassa [Intelligent Order Management – yleiskatsaus](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
