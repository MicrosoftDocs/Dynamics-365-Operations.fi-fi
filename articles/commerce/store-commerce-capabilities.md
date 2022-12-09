---
title: Store Commerce ‑sovelluksen ominaisuudet
description: Tässä artikkelissa kuvataan toimintoja, jotka ovat käytettävissä Microsoft Dynamics 365 Commercen Store Commerce -sovelluksessa.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788509"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce ‑sovelluksen ominaisuudet

[!include [banner](includes/banner.md)]

Store Commerce -sovellus on Microsoft Dynamics 365 Commercen moderni myyntipistekokemus (POS). Sen avulla yritykset voivat käsitellä myymälän maksutapahtumia ja hallita taustatoimintoja, kuten varaston ja tilausten hallinta. Sovellus sallii yritysten myös hallita asiakassuhteita kanta-asiakasohjelmilla ja asiakashallinnalla. 

Commerce Scale Unit (CSU) -arkkitehtuuriin perustuva Store Commerce -sovellus tarjoaa täydellisen monikanavaratkaisun. Asiakas voi esimerkiksi ostaa tuotteen verkosta ja noutaa sen läheisestä myymälästä, jatkaen näin ostosmatkaansa eri kanavissa menettämättä tietoja. 

Tämä artikkeli tarjoaa yleiskatsauksen Store Commerce -sovelluksen ominaisuuksista.

## <a name="platform"></a>Ympäristö

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Kaikkikanavainen | Dynamics 365 Commerce tarjoaa kaikenkattavan monikanavaratkaisun, joka yhdistää taustajärjestelmän, myymälän, puhelinkeskuksen ja digitaaliset kokemukset. | [Yleiskuvaus](index.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Päätelaitteeton kaupankäynti | Commerce Scale Unit isännöi päättömän verkkokaupan järjestelmää. Päättömän verkkokaupan järjestelmä toimii keskipisteenä kaikelle verkkokaupan liiketoimintalogiikalle sekä perustana kaikenkattavalle monikanavaratkaisulle. | <p>[Arkkitehtuurin yleiskatsaus](commerce-architecture.md)</p><p>[Päätön arkkitehtuuri](dev-itpro/retail-server-architecture.md)</p> | [Teknisiä tietoja](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce headquarters | Commerce headquarters tarjoaa taustatoimintoja, jotka mahdollistavat tuotteiden, työntekijöiden, liiketoimintaprosessien, hinnoittelun ja muiden liiketoiminnassa tarvittavien toimintojen määrittämisen. | [Arkkitehtuurin yleiskatsaus](commerce-architecture.md) | |
| Myyntipiste (POS) | Store Commerce -sovellus on Dynamics 365 Commercen myyntipistekokemus. Se tarjoaa monipuolisia ja kattavia POS-ominaisuuksia, jotka auttavat myyjiä, kassanhoitajia ja esimiehiä tarjoamaan asiakkailleen ylivertaista palvelua. Lisäksi se tarjoaa jälleenmyyjille useita käyttöönottovaihtoehtoja, auttaa tehostamaan suorituskykyä ja parantaa sovellusten elinkaaren hallintaa (ALM). | [Store Commerce -sovellus](dev-itpro/store-commerce.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Video](https://youtu.be/7B332XH_zfs)</p><p>[Siirtyminen MPOS-sovelluksesta Store Commerceen](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Pilvikäyttöönotto | Useita Commerce Scale Units -esiintymiä voidaan ottaa käyttöön kuormituksen jakamista ja maantieteellisen etäisyyden vähentämistä varten. | [Pilvikäyttöönotto](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Paikallinen käyttöönotto | Commerce-asiakkaat voivat omistaa ja hallita Dynamics 365 -ympäristöjä tarkemmin käyttämällä paikallista yritystietojen käyttöönottoa. | [Paikallinen käyttöönotto](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Laitehallinta

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Useita laitetyyppejä | Store Commerce -sovellusta tuetaan useilla laitetyypeillä, kuten tietokoneilla, tableteilla ja mobiililaitteilla. Responsiivinen käyttöliittymä (UI) mahdollistaa asettelun koon muuttamisen ja säätämisen näytön koon perusteella. | [Visuaaliset kokoonpanot](pos-screen-layouts.md) |  |
| Tukee useita alustoja | Store Commerce -sovellusta tuetaan verkossa sekä Windows-, iOS- ja Android-alustoilla. | [Alustat](dev-itpro/hybridapp.md) | |
| Tuotemerkki | Näytön suunnitteluohjelma sallii sinun mukauttaa näyttöasetteluita liiketoimintavaatimuksiesi mukaisiksi. Lisäksi voit luoda teemoja, asetteluita, värejä ja kuvia työntekijöiden roolien perusteella sekä jakaa niitä käyttäjille pitääksesi brändisi yhtenäisenä ja edistääksesi helppokäyttöisyyttä. | [Visuaaliset kokoonpanot](pos-screen-layouts.md) | [Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topologia | Erilaisia myymälöiden topologioita tuetaan verkon saatavuuden perusteella. | <p>[Topologia](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infograafi](dev-itpro/retail-in-store-topology.md)</p> | |
| Useiden laitteiden hallinta | Eri myymälöiden useita laitteita voidaan hallita helposti Commerce headquarters -sovelluksesta. | [Aktivointi](set-up-activation-accounts-validate-devices-hq.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Työntekijöiden hallinta

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Sisäänkirjautuminen | Jokaisella myymälän työntekijällä voi olla oma kirjautumistunnuksensa. Kirjautumistyyppejä ovat käyttäjänimi, viivakoodi, magneettinauhan lukulaite (MSR), biometriikka ja Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Laajennettu kirjautuminen](extended-logon.md)</p> | |
| Käyttöoikeudet | Työntekijöille tuetaan eri käyttöoikeustasoja, kuten tilausten luontioikeudet ja tilausten muokkausoikeudet. | [Käyttöoikeudet](tasks/create-pos-permission-groups.md) | |
| Ajan ja läsnäolon hallinta | Läsnäoloa voidaan hallita Kellonaika-toiminnon avulla. Läsnäolotiedot voidaan käsitellä palkanlaskentaan käyttämällä Dynamics 365 Human Resources -sovellusta. | [Ajanhallinta](retail-time-attendance.md) | |
| Myyntiprovisio | Myyntiedustaja voi seurata myyntiä provisioiden ja muiden kannustimien laskemista varten. | [Provisio](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Myynninedistäminen

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Toimintojen hallinta | Myynninedistämispäälliköt voivat lajitella tuotteita siten, että ne ovat valmiina myyntiä varten tietyssä kanavassa ja tiettynä ajanjaksona. | [Valikoimat](assortments.md) | |
| Luettelot | Myynninedistämispäälliköt voivat hallita luetteloita ja tunnistaa tuotteet, joita haluat tarjota luettelokohtaisella hinnoittelulla. | [Luettelot](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Tuotteiden ja luokkien hallinta | Myynninedistämispäälliköt voivat luoda Commerce headquarters -sovelluksessa tuotteita, joilla on variantteja, määritteitä, mittayksikköä ja niin edelleen. He voivat määrittää myös luokkahierarkian tuotteiden organisointia varten. | [Tuote](retail-hierarchies.md) | |
| Niput | Myynninedistämispäälliköt voivat ryhmitellä tuotteita siten, että ne myydään pakettina tai sarjana. | [Myyntirakenteet](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Tietokoodit | Käytä tietokoodeja pyytääksesi kassanhoitajaa syöttämään tietoja myyntipisteen eri toimintojen aikana, kuten tuotteiden myynnin, tuotteiden palautuksen tai asiakkaan valinnan aikana. | [Tietokoodit](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Linkitetyt nimikkeet | Käytä linkitettyjä nimikkeitä tuotteiden lisämyyntiä varten, kun nimike lisätään tapahtumaan. | [Linkitetyt nimikkeet](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Takuut | Laajennettuja takuita voidaan myydä yhdessä tuotteiden kanssa. | [Takuu](extended-warranty.md) | |
| Etiketin tulostus | Luodut etiketit voivat sisältää tuotetietoja, kuten eränumero, sarjanumero ja vanhenemispäivämäärä. | [Etiketin tulostus](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Avustettu myynti

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Tuotteiden selailu | Selaa tuotteita luokittain. | [Tuotehierarkia](retail-hierarchies.md) | |
| Tuotehaku | Hae tuotteita nimen perusteella ja tarkenna hakuja käyttämällä tuotteen määritteitä, kuten tuotemerkki, hinta ja materiaali. Tämä ominaisuus perustuu Azure Cognitive Search -palveluun. | [Pilvipohjainen haku](cloud-powered-search-overview.md) | |
| Tuotteen tiedot -sivut | Monipuoliset tuotetietosivut voivat sisältää kuvia, kuvauksen, tuotteen määritteet ja suositeltuja tuotteita. Suositukset perustuvat suosituspalveluun. | | |
| Tuotteiden vertailu | Vertaile useita tuotteita ja auta asiakkaita valitsemaan tuote ja lisäämään se tapahtumaan. | | |
| Loputon käytävä | Tutki muiden myymälöiden varastoa helposti ja luo tilauksia. | [Varastohaku](pos-inventory-lookup-operation.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Suositukset | Edistä tuotteiden lisä- ja ristiinmyyntiä suosituspalvelun palvelulla. Tämä palvelu hyödyntää patentoitua teknologiaa ehdottaakseen suosituksia ostotrendien ja erilaisten ominaisuuksien perusteella, esimerkiksi juuri saapuneita, samankaltaisia tai suosituimpia tuotteita. Nämä suositukset ovat käytettävissä tuotetietosivuilla, **Asiakastiedot**-sivulla ja **Tapahtumat**-sivulla. | [Suositukset](product-recommendations.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Asiakassuhde

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Asiakkaiden hallinta | Luo, muokkaa ja hallitse asiakastilejä. Asiakastilejä voidaan hallita asynkronoidussa tilassa, jotta vältytään reaaliaikaiselta käsittelyltä. | [Hallinta](customer-mgmt-stores.md) | |
| Asiakkaan määritteet | Asiakkaiden määritteiden kehys mahdollistaa asiakkaisiin liittyvien lisätietojen keräämisen liiketoimintavaatimusten perusteella. | [Ominaisuudet](dev-itpro/customer-attributes.md) | |
| Asiakastietojen sivu | Monipuolinen asiakastietojen sivu tarjoaa kaikkikanavaisen näkymän asiakkaan vuorovaikutuksista eri kanavilla. Näihin vuorovaikutukset sisältävät ostokset, toivomusluettelot ja kanta-asiakkuuspisteet. | | |
| Pilvipohjainen asiakashaku | Hae asiakkaita esimerkiksi nimen, puhelinnumeron, sähköpostiosoitteen, kanta-asiakaskortin ja osoitteen perusteella. | [Pilvipohjainen haku](pos-search-improvements.md#customer-search) | |
| Kanta-asiakkuus ja palkkiot | Asiakkaat voivat liittyä kanta-asiakasohjelmiin ja ansaita ja lunastaa kanta-asiakkuuspisteitä eri kanavien kautta. | [Kanta-asiakkuus](set-up-customer-loyalty-program.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Asiakashallinta | Hallitse tärkeimpiä asiakkaita asiakaskirjan avulla ja seuraa tehtäviä ja huomautuksia asiakasprofiilissa. Dynamics 365 Customer Insights -integraation avulla myymälän työntekijät saavat vinkkejä siitä, miten kunkin asiakkaan kanssa kannattaisi seuraavaksi toimia. | [Asiakashallinta](clienteling-overview.md#activities-and-notes) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Hinnoittelu ja alennukset

| Ominaisuus | kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Kauppasopimukset | Hinnoittelupäälliköt voivat käyttää kauppasopimuksia määrittääkseen erikoishintoja, jotka perustuvat tiettyjen asiakkaiden pitkäaikaisiin sopimuksiin. | [Hinnoittelu](price-management.md)| [Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Myyntisopimukset | Hinnoittelupäälliköt voivat käyttää myyntisopimuksia määrittääkseen sopimuksiin perustuvia hintoja yritysten välisille kaupankäyntiskenaarioille (B2B). | [Hinnoittelu](price-management.md) | |
| Hinnanoikaisut | Hinnoittelupäälliköt voivat käyttää hinnanoikaisuja luodakseen, seuratakseen ja hallitakseen tuotteidensa hinnanalennuksia. | [Hinnanoikaisut](price-adjustments-discounts.md) | |
| Alennukset | Hinnoittelupäälliköt voivat määrittää useita erityyppisiä alennuksia erilaisia kampanjoita varten. Nämä alennukset voivat olla yksinkertaisia alennuksia, laatualennuksia, raja-alennuksia, yhdistelmäalennuksia, maksuvälineperusteisiä alennuksia ja toimitusalennuksia. | [Alennukset](retail-discounts-overview.md) | |
| Kupongit | Hinnoittelupäälliköt voivat määrittää kuponki- tai viivakoodeja, linkittää ne alennuksiin ja jakaa ne asiakkaille. Myyjät voivat lisätä kuponkeja myyntitapahtumiin tai poistaa niitä. | [Kupongit](coupons.md) | |
| Hintaryhmät | Hinnoittelupäälliköt voivat käyttää hintaryhmiä määrittääkseen asiayhteydestä riippuvia hintoja kanavien, luetteloiden, liitosten tai kanta-asiakasohjelmien perusteella. | [Hinnoittelu](price-management.md) | |
| Käytettävissä olevat kampanjat | Myyjät voivat etsiä helposti kampanjoita, jotka ovat saatavilla esimerkiksi myymälän tuotteille, tapahtumaan lisätyille tuotteille jne. | [Hinnoittelutoiminnot](pos-pricing-functions.md) | |
| Hinnantarkistukset | Myyjät voivat tarkistaa myymälän tuotteiden aktiiviset myyntihinnat nopeasti. | [Hinnoittelutoiminnot](pos-pricing-functions.md) | |
| Hintojen korvaaminen | Myyjät, joilla on tarvittavat käyttöoikeudet, voivat korvata järjestelmän määrittämät tai laskemat hinnat. | [Hinnoittelutoiminnot](pos-pricing-functions.md) | |
| Manuaaliset alennukset | Myyjät, joilla on tarvittavat käyttöoikeudet, voivat lisätä manuaalisia alennuksia myyntitapahtumiin tai myyntiriveille. | [Hinnoittelutoiminnot](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Sähköiset maksut

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Kredit ja debet | Store Commerce -sovellus tukee useimpia luotto- ja pankkikorttimaksuja Adyen-maksuyhdyskäytävän kautta ja tilauksen täyttämistä PayPalin kautta. Maksujen SDK sallii ulkoiset yhdyskäytäväyhteydet, joita itsenäisten ohjelmistotoimittajien (ISV) integraatiot tukevat. | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Maksut](payment-methods.md)</p> | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Digilompakoiden tuki | Store Commerce -sovellus tukee maksuja digilompakoiden maksutavoilla, jotka eivät käytä perinteisten luotto- ja pankkikorttien käyttämiä pankkien tunnusnumeroita (BIN). Maksutavat voidaan yhdistää digilompakoiden maksuihin, kuten Adyen. | [Lompakko](wallets.md) | |
| Lahjakorttien tuki | Pankin tunnusnumeroa käyttävä Dynamics 365 -lahjakortti, Stored Value Solutions (SVS) ja Givex-lahjakortit. Lahjakortteja voidaan ostaa ja lunastaa tilauksessa. | [Lahjakortit](dev-itpro/gift-card.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Fraud Protection | Dynamics 365 Fraud Protection auttaa estämään vilpilliset toimet ja tunnistamaan paikat, joissa petoksia ei välttämättä huomata. | [Fraud Protection](dev-itpro/dfp.md) | [Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Verot ja veloitukset

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Verot | Store Commerce -sovellus tukee monenlaisia välillisiä veroja, kuten myyntiveroa, arvonlisäveroa (ALV), GST-veroa, yksikköperusteisia maksuja ja ennakonpidätystä. | [Verot](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Kulut | Veloitukset voidaan määrittää rivitasolla, otsikon tasolla, automaattisina veloituksina, kanavittain ja niin edelleen. | [Kulut](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Tilausten käsittely ja täyttäminen

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Tilauksen luonti | Tilauksen voi luoda toimitettavaksi tai noudettavaksi lähimyymälästä. Noudolle voidaan varata aikavälit. | [Yleiskuvaus](customer-orders-overview.md) | |
| Tilausten muokkaaminen | Tilauksia voidaan muokata, palauttaa, peruuttaa ja niin edelleen. | <p>[Peruuta](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Palautukset](pos-returns.md)</p> | |
| Hae | Voit hakea ja suodattaa tilauksia käyttämällä tilauskohtaisia tietoja. | [Hae](enhancedorderrecall.md) | |
| Tilauksen määritteet | Tilausten määritteiden kehys mahdollistaa tilauksiin liittyvien tietojen keräämisen liiketoimintavaatimusten perusteella. | [Ominaisuudet](dev-itpro/order-attributes.md) | |
| Suoratoimitus | Toimittaja voi merkitä nimikkeitä toimitettavaksi suoraan asiakkaan osoitteeseen. Suoraa toimitusta kutsutaan myös suoratoimitukseksi. | [Suoratoimitus](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Tarjous | Myymälän työntekijät voivat luoda asiakkaille tarjouksia ja määrittää erikoishinnan, manuaalisia alennuksia ja tarjouksen voimassaolopäivän. | [Tarjous](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Täyttäminen | Myymälät voivat noutaa, pakata ja lähettää tilauksia. Paketteihin, jotka ovat valmiita toimitettavaksi, voidaan lisätä pakkausluettelo. | [Täyttäminen](order-fulfillment-overview.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[Video](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Jaettu tilausten hallinta (JTH) | Store Commerce -sovellus tukee tilausten täyttämisen älykästä optimointia, jossa liiketoimintastrategioita voidaan määrittää liiketoiminnan luonteen, asiakkaan tyypin, tilauksen alkuperän ja tilauksen toimitustavan perusteella. | [JTH](dom.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Varastonhallinta

| Ominaisuus | kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Ostovaatimus | Tehosta saatavilla olevan varaston jakelua jakelukeskuksesta useisiin myymälöihin tai varastoihin. | [Ostovaatimus](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Cross-docking | Tehosta saapuvien ostotilausten varaston jakelua useisiin myymälöihin tai varastoihin. | [Cross-docking](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Saapuva varasto | Vastaanota varastoa toimittajalta ostotilauksen kautta tai toisesta varastosta siirtotilauksen avulla. Luo saapuva ostotilaus tai siirtotilauspyyntö. | [Saapuva](pos-inbound-inventory-operation.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Lähtevä varasto | Toimita varastoa toiseen varastoon siirtotilauksen avulla ja luo lähtevä siirtotilauspyyntö. | [Lähtevä](pos-outbound-inventory-operation.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Varastohaku | Tarkista myymälöissä ja varastoissa saatavilla oleva tuotevarasto sekä varaston luvattavissa oleva määrä (ATP) tulevilta päivämääriltä. | [Varastohaku](pos-inventory-lookup-operation.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Varaston oikaisu | Oikaise myymälän saapuva tai lähtevä varasto tiettyjen liiketoimintavaatimusten täyttämiseksi ilman myyntiä, vastaanottoa tai uudelleenlaskentaa. | [Varaston oikaisu](work-with-store-inventory.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Varaston inventoinnit | Laske fyysinen varasto ja säädä järjestelmän kirjanpitovarastoa sen mukaisesti. | [Inventointi](work-with-store-inventory.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Varaston siirto | Siirrä varastoa myymälän sisäisten sijaintien välillä. | [Varastotapahtuma](work-with-store-inventory.md) | <p>[Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Myyntitiedot

| Ominaisuus | kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Kassanhallinta | Store Commerce -sovellus tukee käteisen ja muiden myymälässä määritettyjen maksuvälineiden hallintaa. Lisäksi myymälässä voidaan ottaa käyttöön työvuorojen täsmäytys käteisvarojen edistyneiden hallintatoimintojen käyttämistä varten. | [Maksu](cash-mgmt.md) | |
| Tilinpäätökset ja täsmäytys | Myymälän käteis- ja maksutapahtumat kirjataan Commerce headquarters -sovellukseen laskelmien kirjausprosessien avulla. | [Laskelmat](retail-statements.md) | |
| Tulo- ja kulutapahtumat | Käsittele myymälän pienet käteistapahtumat ja kirjaa tulot, jotka saadaan epäperinteisin tavoin, kuten löydetty käteinen, aulakahvilasta saadut tuotot ja mattojen puhdistuspalvelut. | [Laskelmat](retail-statements.md) | |
| Laskujen maksut | Yhdistä maksut laskuihin. | [Lasku](payinvoice.md) | |

## <a name="employee-productivity"></a>Työntekijöiden tuottavuus

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Tehtävien hallinta | Luo tehtäväluetteloita ja tehtäviä ja delegoi ne myymälöille ja työntekijöille. Seuraa tehtävien tilaa eri myymälöissä. Tarjolla on saumaton integrointi Microsoft Teamsiin. | <p>[Tehtävien hallinta](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Laitteisto ja oheislaitteet

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Oheislaitteiden yhdistäminen | Yhdistä kassapäätteeseen oheislaitteita, kuten tulostimia, kassakoneita, viivakoodinlukijoita ja maksulaitteita. | [Oheislaitteet](retail-peripherals-overview.md) ||
| Jaa oheislaitteita | Kuittitulostimet, kassakoneet ja maksulaitteet voidaan jakaa useiden päätteiden kesken yhdistämällä ne jaettuun laitteistoasemaan. | <p>[Laiteasema](retail-peripherals-overview.md) ||
| Myyntipiste ja oheislaitesimulaattori | Oheislaitesimulaattori tukee sellaisten skenaarioiden testaamista, joissa yleensä vaaditaan fyysisiä myyntipisteoheislaitteita. Lisäksi se sisältää myyntipistesimulaattorin, jonka avulla voit testata fyysisten oheislaitteiden yhteensopivuutta ilman POS-asiakasohjelman käyttöönottoa. | [Simulaattori](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Vastaanotot

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Tulosta kuitteja | Erityyppisiä kuittityyppejä, kuten myyntikuitit, luottokorttikuitit, lahjakuitit ja laskut, voidaan tulostaa oletusarvoisesti tai kassanhoitajan kuittauksen jälkeen. Ne voidaan tulostaa myös uudelleen kirjauskansiosta. | [Tulostaminen](receipt-templates-printing.md) | |
| Sähköpostikuitit | Kuitit voidaan lähettää myyntipisteestä sähköpostitse, kun kassaprosessi on valmis. | [Sähköposti](email-receipts.md) | |
| Kuittien suunnittelu | Myymälän kuitteja voidaan mukauttaa siten, että ne näyttävät jälleenmyyjään ja maksutapahtuman tyyppiin liittyvät tiedot ja asettelut. Kuitteja voidaan myös laajentaa siten, että ne näyttävät jälleenmyyjän vaatimat mukautetut tiedot. | [Rakenne](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Offline-tuki

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Saumaton offline-tila | Saumaton offline-kokemus sallii sinun käsitellä tapahtumia, vaikka internetyhteytesi olisi rajallinen tai olematon. Tietojen poissulkeminen auttaa sinua pienentämään offline-tietokantojen kokoa ja parantamaan suorituskykyä. | [Offline](pos-operations.md) | |
| Suorituskykyyn perustuva vaihto | Siirry offline-tilaan, kun suorituskyvyn havaitaan heikentyvän. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI) |
| Offline-koontinäyttö | **Offline-tilan** koontinäyttö näyttää kunkin laitteen offline-tilan, virheet ja yksityiskohtaiset tiedot. Näin ollen useiden laitteiden tilan hallinta on helppoa. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Laajennettavuus

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Commerce headquarters | Commerce headquarters -ratkaisuja voidaan mukauttaa liiketoimintaprosesseja lisäämällä tai muokkaamalla. Commerce headquarters tukee metatietojen ja koodipohjaisen laajennusmallin käyttöä mukautettujen toimintojen lisäämistä varten. Se voidaan integroida helposti ulkoisiin ratkaisuihin. | [Yleiskuvaus](dev-itpro/extend-customer-cdx-package.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Päätön verkkokauppa | Laajennettavaa, monikanavaista ohjelmointirajapintakehystä voidaan käyttää liiketoimintalogiikan mukauttamiseen ja lisäämiseen. Ohjelmointirajapinnat, joilla on pyyntöjen käsittelijät sekä käynnistimiä edeltävät ja käynnistimien jälkeiset laajennusmallit. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce SDK | Commerce SDK sisältää koodin, koodinäytteitä, malleja ja työkaluja, joita tarvitaan Dynamics 365 Commerce -ominaisuuksien laajentamiseen ja mukauttamiseen. SDK julkaistaan eri GitHub-säilöissä (repoissa) laajennuskomponenteista riippuen. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Myyntipiste | Store Commerce -sovellusta voidaan laajentaa itsenäisesti Commerce SDK:n POS-laajennusominaisuuden avulla. Kehysjärjestelmä tukee käyttäjäkokemuksen (UX), työnkulkujen ja liiketoimintalogiikan mukauttamista. | [Myyntipiste](dev-itpro/pos-extension/pos-extension-overview.md) | [Teknisiä tietoja](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Raportointi

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Myyntiraportit | Myymäläpäälliköille on saatavilla myyntiraportteja henkilökunnan, kassan, maksutyypin, palautusten, tuotteen ja muiden tekijöiden mukaan. Päälliköt voivat tarkastella näitä raportteja ja käyttää niitä jakaakseen provisioita ja tunnistaakseen tuotetrendejä. | | |

## <a name="diagnostics"></a>Diagnostiikka

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Operatiiviset näkemykset | Myymäläkohtaisten palveluiden luotettavuutta ja suorituskykyä koskevia tilastoja on saatavilla asiakkaan Application Insights -tilauksessa. Edistyneitä hälytys- ja valvontaominaisuuksia on saatavilla. | | |
| Kuntotarkistus | Myyntipisteeseen liitettyjen oheislaitteiden käytettävyys voidaan tarkistaa suorittamalla kuntotarkistustoiminto. Tämän jälkeen yksittäisten oheislaitteiden ongelmat voidaan korjata ja vahvistaa. | [Kuntotarkistus](pos-healthcheck.md) | [Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Maailmanlaajuinen toiminta

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Useiden markkinoiden tuki | Markkinakohtaisia ominaisuuksia, kuten kirjanpidon integrointia, GST-veroa, ennakkolaskutusta ja ennakkomaksuja, tuetaan käyttövalmiina. Tämä ominaisuus kattaa useita markkinoita Euroopassa, Amerikoissa, Venäjällä, Aasiassa, Saudi-Arabiassa jne. | [Maailmanlaajuinen toiminta](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Yhteensopivuus

| Toiminto | Kuvaus | Dokumentaatio | Lisäsisältö |
|---|---|---|---|
| Microsoftin standardit | Store Commerce -sovellus noudattaa Microsoftin tietoturvaa, yksityisyyttä ja saavutettavuutta koskevia standardeja, yleistä tietosuoja-asetusta (GDPR), Euroopan unionin (EU) tietojen rajaa jne. | | |

