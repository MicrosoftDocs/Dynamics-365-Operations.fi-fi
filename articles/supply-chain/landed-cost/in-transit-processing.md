---
title: Kuljetettavien tuotteiden käsittely
description: Tässä ohjeaiheessa käsitellään kuljetettavien tuotteiden tilauksia. Kun tilaus tai merikuljetus on määritetty käyttämään kuljetettavien tuotteiden käsittelyä, tuotteet voidaan laskuttaa, ennen kuin ne on vastaanotettu varastoon kulutusta varten.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 77e30f8679c9422e895432c023997b5ff4768ebd
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500401"
---
# <a name="goods-in-transit-processing"></a>Kuljetettavien tuotteiden käsittely

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa käsitellään kuljetettavien tuotteiden tilauksia. Tätä tilaustyyppiä käytetään vain **Aiheutunut kustannus** -moduulissa. Kun tilaus tai merikuljetus on määritetty käyttämään kuljetettavien tuotteiden käsittelyä, tavarat voidaan laskuttaa jo ennen kuin ne on vastaanotettu varastoon. Sen sijaan tuotteet laskutetaan, kun ne lähtevät toimittajan varastosta tai lähtösatamasta, ja taloudelliset kustannukset tunnistetaan, kun merikuljetus alkaa. Tämän toiminnon avulla voit ottaa oikein varaston omistajuuden, koska tavaroista tulee usein organisaation omaisuutta, kun ne lähtevät lähtösatamasta.

Kun kuljetettavien tuotteiden tilauksia käytetään, taloudellisesti päivitetyt nimikkeet vastaanotetaan väliaikaiseen varastoon, jota kutsutaan kuljetettavien tuotteiden varastoksi. Tämän jälkeen tavarat ovat tässä varastossa, kunnes ne voidaan vastaanottaa lopullisessa kohdevarastossa (joka on ostorivillä määritetty varasto). Niitä ei voi poistaa manuaalisesti.

Niin kauan kuin nimikkeet ovat kuljetuksessa, ne eivät ole käytettävissä varastossa eikä niitä voi keräillä varastosta toimitusta varten. Voit kuitenkin tarkastella kuljetettavien tuotteiden varastoa. Voit käyttää tuotteita myös pääsuunnitteluun. Tässä tapauksessa ostotilausrivin vahvistettua toimituspäivää käytetään odotettuna päivämääränä, jolloin varasto on käytettävissä kulutusta varten.

Seuraavissa osissa kuvaillaan määrityksiä, jotka vaaditaan varaston ja merikuljetusten käsittelyyn kuljetettavien tuotteiden käsitteen ja toimintojen avulla.

## <a name="terms-of-delivery"></a>Toimitusehdot

Kun otat **Aiheutunut kustannus** -moduulin käyttöön, *vakiotoimitusehtoja* tehostetaan kuljetettavien tuotteiden ominaisuuden tueksi.

Kun **Kuljetettavien tuotteiden hallinta** -asetuksena on *Kyllä* toimitustietueen sovellettavia ehtoja varten, tuotteet laitetaan kuljetettavien tuotteiden varastoon. Tämä toimenpide käynnistyy vain, jos varastovastaanottoa ei käsitellä ennen laskun käsittelyä. Kun tilauksen toimitusehdot on määritetty käyttämään kuljetettavia tuotteita, käyttäjät eivät voi enää kirjata ostotilaukseen tuotteen vastaanottoa. Jos he yrittävät, tapahtuu virhe. Virhesanomassa sanotaan, että heidän on käytettävä kuljetettavien tuotteiden toimintoa, jotta he voivat jatkaa.

Kun haluat käyttää toimitusehtojen tietoja kuljetettavien tuotteiden kohdalla, siirry kohtaan **Hankinta \> Määritys \> Jakelu \> Toimitusehdot**. Seuraavassa taulukossa kuvataan kenttiä, jotka **Aiheutunut kustannus** -moduuli lisää **Toimitusehdot**-sivulle ja tukevat kuljettavien tuotteiden toimintoa. Molemmat kentät ovat **Yleiset**-pikavälilehdessä. Lisätietoja muista tämän sivun kentistä on kohdassa [Toimitusehdot (lomake)](https://technet.microsoft.com/library/aa575567.aspx).

| Kenttä | kuvaus |
|---|---|
| Lähetyssatama on pakollinen | Aseta arvoksi *Kyllä*, jos lähtösatama on pakollinen, kun toimitusehdot ovat voimassa. |
| Matkalla olevien tavaroiden hallinta | Aseta arvoksi *Kyllä*, jos haluat käyttää kuljetettavien tuotteiden hallintaa, kun toimitusehdot ovat voimassa. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Kuljetettavien tuotteiden ja alitoimitusten varastot

Kun otat **Aiheutunut kustannus** -moduulin käyttöön, *varastojen* vakiokohdetta on parannettu niin, että ostotilaukset voidaan laskuttaa tavaroiden ollessa kuljetettavien tuotteiden varastossa.

Aiheutunut kustannus lisää kaksi uutta varastotyyppiä: *kuljetettavat tuotteet* ja *alitoimitukset*. Kummankin tyyppisiä varastoja voidaan valita oletusvarastoina. Kuljetettavien tuotteiden onnistunut prosessointi edellyttää, että sekä kuljetettavien tuotteiden varasto että alitoimitusvarasto on konfiguroitu **Varastot**-sivulla. Jokaisen sellaisen oletusvaraston osalta, jota käytetään aiheutuneen kustannuksen ja kuljetettavien tuotteiden kanssa, on valittava kuljetettavien tuotteiden varasto ja alitoimitusvarasto kunkin tyypin käytettävissä olevia varastoja varten.

*Kuljetettavien tuotteiden* varastotyyppi liitetään kuljetettavien tuotteiden varastoon, ja tätä varastoa käytetään kuljetettavien tuotteiden tilausten tuotteiden käsittelemiseen, ennen kuin ne vastaanotetaan lopulliseen kohdevarastoon. Yleensä kutakin toimipaikkaa varten riittää yksi kuljetettavien tuotteiden varasto, jos toimipaikka ja varasto ovat ainoat varastonhallinnassa käytettävät varastodimensiot. Jos käytetään myös Sijainti-varastodimensiota, kullekin toimipaikan ja varaston yhdistelmälle on määritettävä kuljetettavien tuotteiden varasto, jotta oletussijainti voidaan määrittää myös.

Voit käsitellä varastojen kuljetettavien tuotteiden asetuksia kohdassa **Varastonhallinta \> Määritys \> Inventaarioanalyysi \> Varastot**. Seuraavassa taulukossa kuvataan kenttiä, jotka **Aiheutunut kustannus** -moduuli lisää **Varastot**-sivulle ja tukevat kuljettavien tuotteiden toimintoa. Molemmat kentät ovat **Yleiset**-pikavälilehdessä. Lisätietoja muista sivun kentistä on kohdassa [Varastot (lomake)](https://technet.microsoft.com/library/aa620570.aspx).

| Kenttä | kuvaus |
|---|---|
| Matkalla olevien tavaroiden varasto | Määritä päävarastoon liittyvä kuljetettavien tuotteiden varasto. |
| Alitoimituksen varasto | Määritä päävarastoon liittyvä alitoimitusvarasto. |

## <a name="posting-rules-for-landed-cost"></a>Aiheutuneen kustannuksen kirjaussäännöt

Aiheutunut kustannus lisää kaksi uutta kirjaussääntöjä, jotka voit konfiguroida. Näitä kirjaussääntöjä käytetään suoran ostotilauslaskun summien rahoitukselliseen kirjaamiseen, jotta tavaroiden omistusoikeus tunnistetaan, kun ne poistuvat lähtöpisteestä. Tämä prosessi korvaa *vastaanotettujen mutta ei laskutettujen tavaroiden* käsitteen, koska tavarat laskutetaan ennen niiden saapumista. <!-- KFM: Add a link to the related scenario when available. -->

Voit käyttää kirjausprofiileja kohdassa **Varastonhallinta \> Määritys \> Kirjaus \> Kirjaus**. **Ostotilaus**-välilehdessä ovat käytettävissä seuraavat uudet kirjaussäännöt:

- **Aiheutunut kustannus, kuljetettavat tuotteet** – Määritä kuljetettavien tuotteiden hallintaa koskevat kirjaussäännöt.
- **Aiheutunut kustannus, kustannusten jaksotus** – Määritä veloitustilin jaksotukselle kirjaussäännöt.

## <a name="goods-in-transit-orders"></a>Kuljetettavien tuotteiden tilaukset

Voit tarkistaa ja hallita kuljetettavien tuotteiden tilauksia suoraan **Aiheutunut kustannus** -moduulissa. Voit käsitellä kuljetettavien tuotteiden tilauksia suoraan **Kuljetettavien tuotteiden tilaukset** -sivulla. Voit vaihtoehtoisesti palata kuljetettavien tuotteiden tilauksiin liittyvään merikuljetukseen ja käsitellä koko merimatkan, kuljetuskontin tai pakkauksen. Kun laskutat merikuljetuksen ja luot kuljetettavien tuotteiden tilauksia, uusi kuljetettavien tuotteiden tilaus luodaan kullekin ostotilausriviin liittyvälle varasto- ja varastodimensioiden yhdistelmälle.

Aiheutunut kustannus hallitsee kuljetettavia tuotteita kahden vaiheen menetelmällä:

1. Nimike vastaanotetaan, kun varastolaskua käsitellään ja sen tilaksi määritetään *Kuljetettavana*.
1. Kuljetettavien tuotteiden tilaus käsitellään **Kuljetettavien tuotteiden tilaukset** -sivulla ja vastaanotetaan ostotilauksessa määritettyyn varastoon. Tässä vaiheessa tilaksi tulee *Vastaanotettu*.

Voit käsitellä kuljetettavien tuotteiden tilauksia kohdassa **Aiheutunut kustannus \> Kausittaiset tehtävät \> Kuljetettavien tuotteiden tilaukset**.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Varaston vastaanotto kuljetettavien tuotteiden varastosta

Järjestelmäsi määrityksen mukaan voit vastaanottaa tavaroita kuljetettavien tuotteiden tilauksesta monella tavalla.

### <a name="in-transit-receiving"></a>Kuljetetuksen vastaanotto

Voit vastaanottaa kuljetuksen seuraavilta sivuilta:

- Valitse **Kuljetettavien tuotteiden tilaukset** -sivulla rivi ja valitse sitten toimintoruudusta **Vastaanota**.
- Valitse tai avaa merikuljetus **Kaikki merikuljetukset** -sivulla. Valitse sitten toimintoruudun **Hallitse**-välilehden **Kuljetettavat tuotteet** -ryhmässä **Vastaanota kuljetettavat tuotteet**.
- Valitse tai avaa kuljetuskontti **Kaikki kuljetuskontit** -sivulla. Valitse sitten toimintoruudun **Hallitse**-välilehden **Kuljetettavat tuotteet** -ryhmässä **Vastaanota kuljetettavat tuotteet**.
- Valitse tai avaa pakkaus **Kaikki pakkaukset** -sivulla. Valitse sitten toimintoruudun **Hallitse**-välilehden **Kuljetettavat tuotteet** -ryhmässä **Vastaanota kuljetettavat tuotteet**.

> [!NOTE]
> Kuljetuksen vastaanottoa käytetään yleensä tilanteissa, joissa sijainteja ja erä-/sarjaseurantaa ei käytetä.

### <a name="arrival-journal"></a>Saapumisen kirjauskansio

Voit vastaanottaa tavaroita myös luomalla saapumisen kirjauskansion. Voit luoda saapumisen kirjauskansion suoraan merikuljetussivulta. Organisaation määrittämät parhaat käytännöt määrittävät, käytetäänkö saapumisen kirjauskansiota tuotteiden vastaanottamiseen.

1. Avaa merikuljetus, kontti tai pakkaus.
1. Valitse **Hallinta**-välilehden **Toiminnot**-ryhmän toimintoruudussa **Luo saapumisten kirjauskansio**.
1. Aseta **Luo saapumisten kirjauskansio** -valintaikkunassa seuraavat arvot:
    - **Alusta määrä** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat määrittää määrän kuljetusmäärästä. Jos tämän asetuksen arvoksi on määritetty *Ei*, kuljetettavien tuotteiden riveiltä ei aseteta oletusmäärää.
    - **Luo kuljetettavista tuotteista** - Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat ottaa määrät valituilta kuljetettavien tuotteiden riveiltä valittua merikuljetusta, konttia tai pakkausta varten.
    - **Luo tilausriveiltä** – Määritä tämän asetuksen arvoksi *Kyllä*, jos haluat määrittää saapumisen kirjauskansion oletusmäärän ostotilausriveiltä. Saapumisen kirjauskansion oletusmäärä voidaan määrittää tällä tavalla vain, jos ostotilausrivin määrä vastaa kuljetettavien tuotteiden tilauksen määrää.

1. Käsittele saapumisen kirjauskansio kohdassa [Rekisteröi nimikekuitit nimikesaapumiskirjauskansion kanssa](https://technet.microsoft.com/library/aa571129.aspx) kuvatulla tavalla.

> [!NOTE]
> Saapumisen kirjauskansiota käytetään yleensä tilanteissa, joissa käytetään sijainteja ja erä- tai sarjaseurantaa, mutta varastonhallintaa ei käytetä.
>
> Oletusvastaanottosijainteja ei tule määrittää tilausriveille, jos saapumisen kirjauskansioon on määritetty hyllytyssijainti.

## <a name="warehouse-management"></a>Varastonhallinta  

Kun otat **Aiheutunut kustannus** -moduulin käyttöön, useita **Varastonhallinta**-moduulin sivuja muokataan siten, että tilausten käsittely (erityisesti kuljetettavien tuotteiden käsittely) voidaan tehdä **Aiheutunut kustannus** -moduulin kautta. Tässä osassa on kuvattu **Varastonhallinta** -moduuliin lisätyt kentät ja prosessit.

### <a name="mobile-device-menu-items"></a>Mobiililaitteen valikkovaihtoehdot

Tavarat voidaan vastaanottaa mobiililaitteella, jos mobiililaitteen valikko ja **Varastonhallinta** -moduuli on määritetty vastaanottamaan tavaroita kuljetettavien tuotteiden tilauksessa. Tässä osassa kuvaillaan määritykset, jotka liittyvät kuljetettavien tuotteiden vastaanottoon.

Voit määrittää mobiililaitteita kuljetettavien tuotteiden käsittelyyn kohdassa **Varastonhallinta \> Määritys \> Mobiililaite \> Mobiililaitteen valikkovaihtoehdot**.

Aiheutunut kustannus lisää seuraavat työn luontiprosessit mobiililaitteen valikkokohteisiin kuljetettavien tuotteiden käsittelyn tukemiseksi:

- Matkalla olevien tavaroiden nimikkeiden vastaanotto
- Kuljetettavien tuotteiden nimikkeiden vastaanotto ja hyllytys

Näiden prosessien konfigurointiasetukset muistuttavat [ostotilauksen vastaanoton ja hyllytyksen luomisprosesseja](https://technet.microsoft.com/library/dn553216.aspx). *Kuljetettavien tuotteiden nimikkeiden vastaanotto ja hyllytysprosessi* kuitenkin lisää seuraavan kentän.

- **Ota käyttöön Kuljetuskontti valmis** – Jos tämän asetuksen arvoksi on määritetty *Kyllä*, kun hyllytystyö on valmis, varastosovellus määrittää lisävaihtoehdon, jonka nimi on **Kuljetuskontti valmis**. Kun tämä vaihtoehto on valittuna, työntekijää pyydetään vahvistamaan, että kontti on valmis. Tässä vaiheessa kaikki lyhyet vastaanotot käsitellään alitustapahtumana.

### <a name="location-directives"></a>Sijaintidirektiivit

Aiheutunut kustannus lisää uuden työtilaustyypin, jonka nimi on *Kuljetettavat tavarat*, **Sijaintidirektiivit**-sivulle. Tämä työtilaustyyppi tulee konfiguroida samalla tavalla kuin [ostotilauksen työtilaustyypit](https://technet.microsoft.com/library/dn553184.aspx).

### <a name="work-templates"></a>Työmallit

Aiheutunut kustannus lisää uuden työtilaustyypin, jonka nimi on *Kuljetettavat tavarat*, **Työmallit**-sivulle. Tämä työtilaustyyppi tulee konfiguroida samalla tavalla kuin [ostotilauksen työmallit](https://technet.microsoft.com/library/dn553184.aspx).
