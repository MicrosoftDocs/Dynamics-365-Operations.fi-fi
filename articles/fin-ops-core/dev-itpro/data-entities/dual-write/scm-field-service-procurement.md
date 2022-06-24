---
title: Supply Chain Managementin ja Field Servicen hankinnan integrointi
description: Tässä artikkelissa käsitellään tapaa, jolla kaksoiskirjoituksen integrointi tukee ostotilauksen luontia ja päivitystä sekä Supply Chain Managementista että Field Servicestä.
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a59365b3a524b8a5ec9e1e829fe181aa3d3660
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897141"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Supply Chain Managementin ja Field Servicen hankinnan integrointi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisältää vakaat hankintatoiminnot. Dynamics 365 Field Service sisältää vastaavanlaisia toimintoja, jotka tukevat palveluprosessiin liitettyjä ostoprosesseja. Näiden kahden sovelluksen toiminnot integroidaan kaksoiskirjoituksen avulla, ja tuloksena olevat toimintojen väliset käyttötapaukset otetaan käyttöön taulukoiden yhdistämisten, ratkaisulogiikan, näkymien ja lomakkeiden avulla.

Tämä integrointi tukee ostotilauksen luontia ja useimmissa tapauksissa myös päivityksiä kummastakin sovelluksesta. Supply Chain Management kuitenkin hallitsee hinnoittelua, osoitteita ja tuotteen vastaanottoa. Useita tehokkaista toimintojen välisiä käyttötapauksia otetaan käyttöön organisaatioissa, joissa on käytössä sekä Field Service että Supply Chain Management. Näiden käyttötapausten avulla hankintoja voidaan käynnistää ja seurata molemmissa järjestelmissä.

Seuraavassa kuvassa on kummassakin järjestelmässä olevat taulukota ja tapa, jolla ne yhdistetään toisiinsa. Field Servicen ostotilaukset viittaavat *tiliriville*, kun taas Supply Chain Managementin ostotilaukset viittaavat *toimittajariville*. Kaksoiskirjoitus ratkaisee integroinnin käyttämällä viitettä, joka linkittää *toimittajarivit* *tiliriveihin*. Lisätietoja on kohdassa [Integroidut toimittajan päätiedot](vendor-mapping.md).

![Hankintojen yhdistämismääritykset.](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Edellytykset

Supply Chain Managementin ja Field Servicen integrointia varten on asennettava seuraavat osat:

- Field Servicen versio 8.8.31.60 tai sitä uudempi kattavaa ostotilauksen integrointia varten
- Supply Chain Managementin versio 10.0.14 tai uudempi
- Kaksoiskirjoitus OneFSSCM-ratkaisun suorittamiseen

## <a name="installation-guidelines"></a>Asennusohjeet

### <a name="prerequisites"></a>Edellytykset

- **Kaksoiskirjoitus** – lisätietoja on kohdassa [Kaksoiskirjoituksen aloitussivu](dual-write-home-page.md#dual-write-setup).
- **Dynamics 365 Field Service** – lisätietoja on kohdassa [ Dynamics 365 Field Servicen asentaminen](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Jos kaksoiskirjoitus ja Field Service on otettu käyttöön Microsoft Dataversessa, käyttöön saadaan useita ratkaisutasoja, jotka laajentavat ympäristöä uusilla metatiedoilla, lomakkeilla, näkymillä ja logiikalla. Näiden ratkaisujen käyttöönottojärjestyksellä ei ole merkitystä, vaikkakin ne yleensä asennetaan seuraavassa järjestyksessä.

1. **Field Service Common** – Field Service Common asennetaan, kun Field Service on asennettu ympäristöön.
2. **Field Service Common** – Field Service (Anchor) asennetaan, kun Field Service on asennettu ympäristöön. 
3. **Supply Chain Management Extended** – Supply Chain Management Extended asennetaan automaattisesti, kun kaksoiskirjoitus on otettu käyttöön ympäristössä. 
4. **OneFSSCM-ratkaisu** – Viimeksi asennettu ratkaisu (Field Service tai Supply Chain Management) asentaa OneFSSCM:n.

    - Jos Field Service on jo asennettu ympäristöön ja Supply Chain Management Extendedin asentava kaksoiskirjoitus otetaan käyttöön, OneFSSCM asennetaan.
    - Jos Supply Chain Management Extended on jo asennettu ympäristöön ja Field Service asennetaan, OneFSSCM asennetaan.

## <a name="initial-synchronization"></a>Ensimmäinen synkronointi

Uuden ostotilauksen luonti ja aiemmin luotujen ostotilausten käyttäminen edellyttää, että Supply Chain Managementin ja Dataversen väliset viitetiedot synkronoidaan. Ensimmäisellä kirjoitustoiminnolla havaitaan taulukkosuhteet ja etsitään taulukot, jotka on otettava käyttöön tietyssä määrityksessä.

Seuraavat taulukot on synkronoitava:

- Tuotemallit

    Ensimmäisen kirjoituksen yhteydessä saadaan täydellinen luettelo tarvittavista taulukoista. Malliesimerkkejä:

    - Kaikki tuotteet
    - Vapautetut tuotteet V2
    - Dataversen vapautetut erilliset tuotteet

- Toimipaikat
- Varastot
- Hankintaluokkamallit

    Malliesimerkkejä:

    - Hankintaluokat
    - Tuo
    - Tuoteluokkahierarkia
    - Tuoteluokan määritykset

- Toimittajamallit, kuten Toimittaja V2
- Yhteyshenkilömallit, kuten Dataversen Yhteyshenkilöt V2
- Työntekijämallit, kuten Työntekijä

Taulukoiden synkronoinnilla varmistetaan, että kaikki Supply Chain Managementin asiakirjat (ostotilaukset ja tuotteen vastaanotot) ovat käytettävissä Dataversessa.

### <a name="account-and-vendor-tables"></a>Tili- ja Toimittaja-taulukot

Field Servicen ostotilaukset käyttävät Tili-taulukko toimittajien seuraamiseen. Tämän vuoksi ostotilausten Dataverse-taulukot käyttävät tilejä toimittajien seuraamiseen. Tämä keskeisen eron huomioon ottaminen edellyttää, tilit ja toimittajat pidetään synkronoituina aktivoimalla seuraavat neljä työnkulkua: 

- Toimittajien luonti Tilit-taulukossa
- Toimittajien luonti Toimittajat-taulukossa
- Toimittajien päivitys Tilit-taulukossa
- Toimittajien päivitys Toimittajat-taulukossa

Jos OneFSSCM on asennettu, koska sekä Field Service että Supply Chain Management Extended on asennettu, kyseiset työnkulut aktivoidaan automaattisesti. Jos Field Servicea ei ole asennettu mutta ostotilaustaulukot halutaan integroida Dataverseen, kyseiset työnkulut on aktivoitava. Ellei luonti aloiteta tyhjästä, kummassakin tapauksessa on ehkä varmistettava ennen ostotilausten luontia, että kaikki toimittajat luodaan tileinä Dataversessa. Muussa tapauksessa voi tapahtua virheitä.

### <a name="initial-synchronization"></a>Ensimmäinen synkronointi

Kun kaikki edellytykset täyttyvät ja aiemmin luotujen ostotilausten ja tuotteen vastaanottojen halutaan olevan käytettävissä molemmissa järjestelmissä, seuraavat mallit on synkronoitava ensimmäisen kerran:

- Ostotilausotsikko V2
- CDS-ostotilausrivi
- Poistettavaksi merkitty CDS-ostotilausrivi
- Ostotilauksen vastaanotto
- Ostotilauksen vastaanotettu tuote

## <a name="mappings-with-logic"></a>Logiikkaa käyttävät yhdistämismääritykset

Hankinnan integraatio laajentaa tuotteen yhdistämismääritystä seuraavalla logiikalla. Näin varmistetaan, että **Field Service -tuotetyyppi** -sarake on määritetty oikein Dataversen tuotetaulukossa.

- Jos **Tuotetyyppi**-määrityksenä on *Tuote* ja **Nimikemalliryhmä, varastotuote** -määrityksenä on *Tosi*, **Field Service -tuotetyyppi** määrityksenä on *Varasto*.
- Jos **Tuotetyyppi**-määrityksenä on *Tuote* ja **Nimikemalliryhmä, varastotuote** -määrityksenä on *Epätosi*, **Field Service -tuotetyyppi** määrityksenä on *Muu kuin varasto*.
- Jos **Tuotetyyppi**-määrityksenä on *Palvelu*, **Field Service -tuotetyyppi** -määrityksenä on *Palvelu*.

Dataverse sisältää myös logiikan, joka yhdistää toimittajat niihin liittyviin tileihin. Tämä logiikka määrittää laskun oletustoimittajatilin. Palvelinpuolen laajennuslogiikka määrittää luonnin yhteydessä laskun oletustoimittajatilin tiliin liittyvän toimittajan perusteella. Toimittajalla on viite laskutiliin, jolla tämä arvo määritetään.

## <a name="supported-scenarios"></a>Tuetut skenaariot

- Dataverse-käyttäjät voivat luoda ja päivittää ostotilauksia. Supply Chain Management kuitenkin hallitsee prosessia ja tietoja. Supply Chain Managementin ostotilaussarakkeiden päivitysten rajoituksia käytetään, kun kyse on Field Service -päivityksistä. Esimerkiksi viimeisteltyä ostotilausta ei voi päivittää. 
- Jos ostotilausta hallitaan Supply Chain Managementin muutostenhallinnan avulla, Field Servicen käyttäjä voi päivittää ostotilauksen vain silloin, kun Supply Chain Managementin hyväksyntätila on *Luonnos*.
- Useiden sarakkeiden hallinta on mahdollista vain Supply Chain Managementista eikä niitä voi päivittää Field Servicessa. Tuotteen yhdistämistaulukoista voi tarkistaa, mitä sarakkeita ei voi päivittää. Yksinkertaistaen voi sanoa, että useimmissa näistä sarakkeissa on Dataverse -sivuilla vain luku -määritys. 

    Supply Chain Management hallitsee esimerkiksi hintatietojen sarakkeita. Supply Chain Managementissa on kauppasopimuksia, joiden sarakkeista on hyötyä Field Servicessa. Tällaisia vain Supply Chain Managementista saatavia sarakkeita ovat esimerkiksi **Yksikköhinta**, **Alennus** ja **Nettosumma**. Hinnan synkronointi Field Serviceen voidaan varmistaa käyttämällä **Synkronoi**-toimintoa Dataversen **Ostotilaus**- ja **Ostotilauksen tuotteet** -sivuilla, kun ostotilauksen tiedot on annettu. Lisätietoja on kohdassa [Dynamics 365 Supply Chain Management in hankintatietojen synkronointi tarvittaessa](#sync-procurement).

- **Summat**-sarake on käytettävissä vain Field Servicessa, koska Supply Chain Managementissa ei ole ostotilauksen ajantasaisia summia. Supply Chain Managementin summat laskeminen perustuu useisiin parametreihin, jotka eivät ole käytettävissä Field Servicessa.
- Jos ostotilausriveillä on määritetty vain hankintaluokka tai jos määritetty tuote on *Palvelu*- tuotetyypin tai Field Service -tuotetyypin nimike, kyseinen rivi voidaan käynnistää vain Supply Chain Managementissa. Rivit synkronoidaan sitten Dataverseen, ja ne näkyvät Field Servicessa.
- Jos vain Field Service on asennettu, Supply Chain Managementin **Varasto**-sarake on pakollinen ostotilauksessa. Jos Supply Chain Management on kuitenkin asennettu, tämä edellytys ei ole ehdoton, koska Supply Chain Management sallii tietyissä tilanteissa ostotilausrivit, joissa varastoa ei ole määritetty.
- Supply Chain Management hallitsee tuotteen vastaanottoja (ostotilauksen vastaanottoja Dataversessa) eikä niitä voi luoda Dataversesta, jos Supply Chain Management on asennettu. Supply Chain Managementin tuotteen vastaanotot synkronoidaan Supply Chain Managementista Dataverseen.
- Supply Chain Management sallii alitoimituksen. OneFSSCM-ratkaisu lisää logiikan siten, että kun tuotteen vastaanottorivi (tai ostotilauksen vastaanotettu tuote Dataversessa) luodaan tai päivitetään, varastokirjauskansion rivi luodaan Dataversessa säätämään alitoimitusskenaarioiden tilauksessa jäljellä olevaa määrää.

## <a name="unsupported-scenarios"></a>Skenaariot, joita ei tueta

- Field Service estää rivien lisäämisen Supply Chain Managementin peruutettuun ostotilaukseen. Tämä on mahdollista kiertää muuttamalla ostotilauksen järjestelmän tila Field Servicessa ja lisäämällä sitten uusi rivi joko Field Servicessa tai Supply Chain Managementissa.
- Vaikka hankintarivit vaikuttavat kummankin järjestelmän varastotasoihin, tämä integraatio ei varmista varaston kohdistusta Supply Chain Managementin ja Field Servicen välillä. Sekä Field Servicessa että Supply Chain Managementissa on muita varastotasot päivittäviä prosesseja. Nämä prosessit eivät sisälly hankintaan.

## <a name="status-management"></a>Tilan hallinta

Field Servicen ostotilausten tilat ja Supply Chain Managementin tilat eroavat toisistaan.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Field Servicen ostotilauksen ja ostotilaustuotteen tilat

| Otsikko – järjestelmän tila | Otsikko – hyväksynnän tila | Nimikkeen tila |
|---|---|---|
| <ul><li>Luonnos</li><li>Lähetetty</li><li>Peruutettu</li><li>Tuote vastaanotettu</li><li>Laskutettu</li></ul> | <ul><li>Null</li><li>Hyväksytty summa</li><li>Hylätty</li></ul> | <ul><li>Odottava</li><li>Vastaanotettu</li><li>Peruutettu</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Supply Chain Managementin ostotilauksen ja ostotilaustuotteen tilat

Rivin hyväksynnän tilat ovat aktiivisia vain rivin työnkulun yhteydessä.

| Otsikko – asiakirjojen tila | Otsikko – hyväksynnän tila | Rivin tila | Rivin hyväksynnän tila |
|---|---|---|---|
| <ul><li>Avoin tilaus (jälkitoimitus)</li><li>Vastaanotettu</li><li>Laskutettu</li><li>Peruutettu</li></ul> | <ul><li>Luonnos</li><li>Tarkistuksessa</li><li>Hyväksytty summa</li><li>Hylätty</li><li>Ulkoisessa tarkistuksessa</li><li>Vahvistettu</li><li>Päätetty</li></ul> | <ul><li>Avoin tilaus (jälkitoimitus)</li><li>Vastaanotettu</li><li>Laskutettu</li><li>Peruutettu</li></ul> | <ul><li>Ei lähetetty</li><li>Tarkistuksessa</li><li>Hyväksytty summa</li><li>Hylätty</li></ul> |

Tilasarakkeissa käytetään seuraavia sääntöjä:

- Supply Chain Managementin ei voi päivittää Field Servicessa. Joissakin tapauksissa Field Servicen tila kuitenkin päivitetään, kun Supply Chain Managementin ostotilauksen tila muuttuu.
- Jos Supply Chain Managementin ostotilauksessa on käytössä muutostenhallinta ja muutos käsitellään, hyväksynnän tila on *Luonnos* tai *Tarkistuksessa*. Tässä tapauksessa Field Servicen hyväksynnän tilaksi määritetään *Tyhjäarvo*.
- Jos Supply Chain Managementin ostotilauksen hyväksynnän tilaksi on määritetty *Hyväksytty*, *Ulkoisessa tarkistuksessa*, *Vahvistettu* tai *Päätetty*, Field Servicen ostotilauksen hyväksynnän tilaksi määritetään *Hyväksytty*.
- Jos Supply Chain Managementin ostotilauksen hyväksynnän tilaksi on määritetty *Hylätty*, Field Servicen ostotilauksen hyväksynnän tilaksi määritetään *Hylätty*.
- Jos asiakirjan otsikon tilaksi vaihdetaan Supply Chain Managementissa *Avoin tilaus (jälkitoimitus)* ja Field Servicen ostotilauksen tila on *Luonnos* tai *Peruutettu*, Field Servicen ostotilauksen tilaksi vaihtuu *Lähetetty*.
- Jos asiakirjan otsikon tilaksi vaihdetaan Supply Chain Managementissa *Peruutettu* eikä Field Servicen ostotilauksen vastaanottotuotteita ole liitetty ostotilaukseen (ostotilauksen tuotteiden kautta), Field Servicen järjestelmän tilaksi määritetään *Peruutettu*.
- Jos ostotilausrivin tila Supply Chain Managementissa on *Peruutettu*, ostotilaustuotteen tilaksi määritetään Field Servicesessa *Peruutettu*. Jos Supply Chain Managementin tuotetilausrivin tila *Peruutettu* lisäksi vaihdetaan tilaksi *Jälkitoimitus*, ostotilauksen tuotenimikkeen tilaksi määritetään Field Servicessa *Odottaa*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Supply Chain Managementin hankintatietojen synkronointi tarvittaessa

Supply Chain Management sisältää hankintatietoja, jotka käsittelevät kauppasopimuksia, alennuksia ja muita skenaarioita, jotka tarvitsevat Supply Chain Managementin toissijaisia prosesseja. Hankintamoduuli määrittää tietyn ostotilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä. Kaksoiskirjoitusta käytettäessä tietoja ei aina pidetä synkronoituina kahden ympäristön välillä etenkään skenaarioissa, joissa rivi luotiin tai päivitettiin Dataversessa, ja tämä voi käynnistää seurantaprosesseja Supply Chain Managementissa.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Supply Chain Managementin hankintatietojen synkronointi

1. Valitse Dataversessa **Varasto \> Ostotilaus**.
2. Luo uusi ostotilaus valitsemalla **Uusi** tai valitse aiemmin luodun ostotilauksen rivi.
3. Ostotilauksesta tai ostotilausriviltä.
4. Valitse toimintoruudussa **Synkronoi**.

Kaikki Supply Chain Managementin jakamat Dataversen ja Field Servicen sarakkeet synkronoidaan.

**Synkronoi**-toimintoa käytetään esimerkiksi seuraavissa tilanteissa:

- Jos samalle Dataversen riville tehdään useita peräkkäisiä muutoksia, suorita **Synkronoi**-toiminto.
- Jos et ole varma, onko muutos toinen peräkkäinen muutos Dataversessa, **Synkronoi**-toiminto kannattaa ehkä suorittaa.
- Jos Supply Chain Managementin arvon päivittämisestä annetaan virhesanoma, suorita **Synkronoi**-toiminto ja yritä päivitystä uudelleen Dataversessa.

## <a name="cancelling-the-posting-process"></a>Kirjausprosessin peruuttaminen

Jos tuotteen vastaanoton kirjausprosessi peruutetaan käsittelyn aikana, kaksoiskirjoitus voi ehkä luoda tuotteen vastaanottorivin Dataversessa mutta ei luo sitä Supply Chain Managementissa. Tämä johtuu siitä, että kaksoiskirjoitus ei tue hajautettuja tapahtumia.

## <a name="templates"></a>Mallit

Seuraavat malli ovat käytettävissä hankintaan liittyvien asiakirjojen integroinnissa.

| Toimitusketjun hallinta | Field Service | kuvaus |
|---|---|---|
| [Ostotilausotsikko V2](mapping-reference.md#183) | msdyn\_Purchaseorders | Tämä taulukko sisältää ostotilauksen otsikon ilmaisevia sarakkeita. |
| [Ostotilausrivin yksikkö](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | Tämä taulukko sisältää rivejä, jotka ilmaisevat ostotilauksen rivejä. Tuotenumeroa käytetään synkronointiin. Tämä määrittää tuotteen varastointiyksikkönä, mukaan lukien tuotedimensiot. Lisätietoja tuotteen integroinnista Dataversen kanssa on kohdassa [Yhtenäinen tuotekokemus](product-mapping.md). |
| [Tuotteen vastaanoton otsikko](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | Tämä taulukko sisältää tuotteen vastaanoton otsikot, jotka luotiin, kun tuotteen vastaanotto kirjattiin Supply Chain Managementissa. |
| [Tuotteen vastaanottorivi](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | Tämä taulukko sisältää tuotteen vastaanottorivit, jotka luotiin, kun tuotteen vastaanotto kirjattiin Supply Chain Managementissa. |
| [Ostotilausrivin poistettavaksi merkitty yksikkö](mapping-reference.md#182) | msdyn\_purchaseorderproducts | Tämä taulukko sisältää tietoja poistettavaksi merkityistä ostotilausriveistä. Supply Chain Managementin ostotilausrivi voi merkitä poistettavaksi vain, kun ostotilaus on vahvistettu tai hyväksytty, jos muutostenhallinta on otettu käyttöön. Rivi on Supply Chain Management -tietokannassa ja sen merkintänä on **IsDeleted**. Koska Dataverse ei sisällä poistamisen merkintäkäsitettä, on tärkeää, että nämä tiedot synkronoidaan Dataverseen. Tällä tavoin Supply Chain Managementissa poistettavaksi merkityt rivit voidaan poistaa automaattisesti Dataversesta. Tässä tapauksessa Dataversen rivin poistamislogiikka sijaitsee Supply Chain Management Extendedissä. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
