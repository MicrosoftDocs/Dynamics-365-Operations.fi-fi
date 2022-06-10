---
title: Varastokirjaus
description: Tässä aiheessa kuvataan Varaston kirjaus -välilehti varastokirjausprofiilisivulla.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783367"
---
# <a name="inventory-posting"></a>Varastokirjaus

**Varastokirjausprofiilit**-sivun **Varasto**-välilehden avulla voit hallita, miten varastotapahtumat kirjataan kirjanpitoon. Varastotapahtumat ovat tapahtumia, joita ei luoda myyntitilauksista, ostotilauksista tai tuotantotilauksista. Ne kirjaavat fyysiset ja taloudelliset päivitykset automaattisesti varastoon samanaikaisesti. Yksi poikkeus on siirtotilaukset, jotka erottelevat fyysiset ja taloudelliset päivitykset, kun lähetät varaston ja vastaanotat sen.

Seuraavassa taulukossa on joitakin esimerkkejä varastotapahtumista.

| Tapahtumatyyppi | Vastaanotto tai varasto-otto | Fyysinen kirjaus, kirjanpitokirjaus tai molemmat | Kuvaus |
|---|---|---|---|
| Siirto | Molemmat | Molemmat | <p>Siirtotapahtumien kirjauskansio on varastokirjauskansio, jota voit käyttää varaston lisäämiseen tai poistamiseen. Se toimii kuin varaston oikaisukirjauskansio. Yksi tärkeä ero on kuitenkin se, että merkinnän vastapäätili on määritetty.</p><p>Siirtotapahtumien kirjauskansioon kirjataan alkusaldot ja kertaoikaisut, jotka on kustannuskirjattava. Sitä käytetään esimerkiksi silloin, kun varastoa poistetaan myyntinäytettä varten.</p><p>Kun kirjauskansio kirjataan, fyysiset ja taloudelliset päivitykset tapahtuvat samanaikaisesti.</p><p>Kirjauskansiorivien positiiviset määrät edustavat vastaanottoja ja negatiiviset määrät edustavat varasto-ottoja.</p> |
| Varaston oikaisu | Molemmat | Molemmat | Varaston oikaisukirjauskansiota käytetään varaston lisäämiseen tai poistamiseen. Se ei salli vastatilin valitsemista. Vain **Varaston kirjausprofiili** -sivulla määritettyjä tilejä käytetään kirjanpitotapahtuman päivittämiseen. |
| Siirto (kirjauskansio) | Molemmat | Molemmat | <p>Siirtokirjauskansiota käytetään varaston siirtämiseen varastosijainnista toiseen (käyttämällä varastodimensioita). Se päivittää varastotapahtuman tuotetiedot uusilla tuote- tai seurantadimensioilla.</p><p>Siirtokirjauskansio luo yhden rivin nimikkeen siirtoa varten. Tällä rivillä on varastodimensioiden "lähde" - ja "kohde"-kentät. Kukin siirtokirjauskansion rivi luo kaksi varastotapahtumaa. Yksi tapahtuma luodaan "lähde"-varastodimensioista. Se edustaa varasto-ottoa, ja sen määrä on negatiivinen. Toinen tapahtuma luodaan "kohde"-varastodimensioista. Se edustaa vastaanottoa, ja sen määrä on positiivinen.</p><p>Siirtokirjauskansiot eivät ehkä luo tositetta, jos varaston siirtoa pidetään ei-taloudellisena siirtona. Varastodimensioita, jotka eroavat "lähde"- ja "kohde"-arvoista, ei merkitä **Varastodimensioryhmä**- tai **Seurantadimensioryhmä**-sivulla olevan **Kirjanpitovarasto**-vaihtoehdon avulla. Jos esimerkiksi **Kirjanpitovarasto**-asetusta ei ole merkitty **Sijainti**-dimensiossa ja siirrät varaston paikasta toiseen samassa toimi toimipaikassa ja varastossa, tositetta ei luoda.</p><p>Siirtokirjauskansiot eroavat siirtotilauksista siinä, ettei siirrolle ole asiakirjoja. Päivitys tehdään yhdessä tapahtumassa kirjaamalla kirjauskansio. Siirtotilaus voi sen sijaan luoda keräys- ja lähetysasiakirjoja, ja se edellyttää kahta päivitystä tapahtuman käsittelemiseen.</p> |
| Siirtotilauksen lähetys | Ongelma | Molemmat | <p>Kun luot uuden siirtotilauksen, kullakin rivin ja varastodimension yhdistelmällä on kaksi varastotapahtumaa: yksi siirtotilauslähetykselle ja toinen siirtotilauksen vastaanotolle. Siirtotilauksen lähetystä varten päivitetään kaksi varastotapahtumaa, ja tavaroiden kuljetukselle luodaan kaksi lisävarastotapahtumaa, jotka ovat yhteensä neljä varastotapahtumaa.</p><ol><li>Ensimmäistä varastotapahtumaa käytetään, kun nimike poistetaan lähdevarastosta ja -sijainnista. Tämän tapahtuman varasto-oton tila on **Myyty** sen merkiksi, että nimike ei ole enää käytettävissä varastossa.</li><li>Toista varastotapahtumaa käytetään, kun nimike lisätään siirtovarastoon, joka on valittu varastolle, josta nimike siirretään. Tämän tapahtuman vastaanottotila on **Ostettu**.</li><li>Kolmas varastotapahtuma on siirrolle siirtovarastosta kohdevarastoon. Tämän tapahtuman varasto-ottotila on **Varattu fyysinen**. Tämä tila varmistaa, että toinen prosessi ei voi kuluttaa nimikettä, kun se on vielä kuljetettavana.</li><li>Neljäs varastotapahtuma on tavaroiden vastaanotto kohdevarastossa. Tämän tapahtuman vastaanottotila on **Tilattu**.</li></ol> |
| Siirtotilauksen vastaanotto | Vastaanotto | Molemmat | Kun siirtotilaus vastaanotetaan kohdevarastoon, kuljetusvarastossa olevan varastotapahtuman varaston tila (edellisen esimerkin numero 3) päivitetään arvoon **Myyty** ja kohdevaraston varastotapahtuman varaston tilaksi päivitetään **Ostettu**. |
| Tuoterakenteet | Molemmat | Molemmat | Tuoterakennekirjauskansion avulla voit ilmoittaa tuotteen valmiiksi ja kuluttaa prosessin aikana kuluneet raaka-aineet ilman tuotantotilausta. Tuoterakennekirjauskansiossa on tavallisesti vähintään yksi positiivinen rivi lopputuotteelle ja yksi tai useampia negatiivisia rivejä kulutetuille raaka-aineille. Valmiin tavaran rivi on vastaanotto varastoon, kun taas negatiiviset rivit ovat raaka-aineiden varasto-ottoja. Kun luot tuoterakennekirjauskansion, ensimmäinen rivi on tuoterakenteen otsikko ja seuraavat lisättävät rivit ovat tuoterakennerivejä. |
| Varaston omistajuuden muutos | Molemmat | Molemmat | Varaston omistajuuden muutoksen kirjauskansiota käytetään muuttamaan luovutetun varaston omistajuus toimittajalta omalle organisaatiollesi. Varaston omistajuuden muutoksen kirjauskansiot muistuttavat varastosiirtokirjauskansioita, sillä kaksi varastotapahtumaa liittyy kuhunkin rivin ja varastodimension yhdistelmään. Yksi varastotapahtuma poistaa varaston **Omistajuus**-dimension toimittajalta ja toinen lisää nimikkeen yritykseen **Omistajuus**-dimensiossa. |
| Nimikkeen saapuminen | Vastaanotto | Fyysinen | Nimikkeen saapumisen kirjauskansion avulla varaston vastaanoton tilaksi päivitetään **Rekisteröity**. Sitä käytetään yleensä ostotilauksen tuotteiden vastaanottoon ja myyntitilausten palautuksiin. |
| Tuotannon varastointi | Vastaanotto | Fyysinen | Tuotannon syöttökirjauskansio muistuttaa nimikkeen saapumisen kirjauskansiota. Tuotannon syötettä käytetään valmiiden tuotteiden vastaanottoon tuotantotilauksista varastossa. Kun kirjauskansio kirjataan, varastotapahtuman tilaksi muutetaan **Rekisteröity**. |
| Inventointi | Molemmat | Molemmat | Inventointikirjauskansion avulla kirjataan tiettyyn varastodimensioiden yhdistelmään lasketut nimikkeet. Varastotapahtumat luodaan, kun kirjauskansion rivillä on inventointiero. Rivi, jolla on suurempi laskettu määrä, aiheuttaa vastaanoton varastoon. Rivi, jolla on pienempi laskettu määrä, aiheuttaa varasto-oton varastosta. Rivit, joilla laskettu määrä vastaa odotettua määrää, eivät sisällä varastotapahtumia. |
| Inventointi tunnisteiden perusteella | Ei käytettävissä | Ei käytettävissä | Tunnisteiden inventointikirjauskansion avulla seurataan varastotunnisteita, jotka on määritetty ja joita käytetään koko varaston inventointiin. Kirjauskansion avulla voit liittää tunnistenumeron tiettyyn nimikkeen ja varastodimension yhdistelmään sekä seurata tunnisteen tilaa koko varaston inventoinnin aikana. Tunnisteiden inventoinnin kirjauskansiot eivät luo varastotapahtumia. |
| Laatutilaukset | Ongelma | Fyysinen | <p>Laatutilauksen avulla tallennetaan tietyn varastoerän testitulokset. Kukin laatutilaus liittyy aiemmin luotuun varastotapahtumaan tai varastotapahtuman osaan.</p><p>Laatutilaus luo uuden varastotapahtuman kahdessa tapauksessa:</p><ul><li>Laatutilaus merkitään **Yleiset**-välilehdessä **destruktiiviseksi testiksi**.</li><li>Laatutilaus merkitään **Karanteeni tarkistusvirheen jälkeen** -merkinnällä **Yleiset**-välilehdessä, ja testi epäonnistuu tarkistuksessa. Tässä tapauksessa luodaan kaksi varastotapahtumaa. Yksi varastotapahtuma poistaa nimikkeen alkuperäisestä varastodimensioyhdistelmästä ja -sijainnista ja toinen lisää nimikkeen karanteenivarastoon.</li></ul> |
| Karanteenitilaukset | Molemmat | Molemmat | <p>Karanteenitilausten varastotapahtumat ovat kuin siirtotilaus. Karanteenivaraston avulla seurataan varastoa. Vastaanottotapahtumia on kaksi ja varasto-ottotapahtumia on kaksi.</p><p>Kun luot tilauksen alustavasti, ohjelma luo kaksi tapahtumaa. Vastaanottotapahtuman tila on **Tilattu** karanteenivarastolle, joka on linkitetty varastoon, jossa nimike sijaitsee. Varasto-ottotapahtuman tila on **Tilauksessa** varastolle, jossa nimikettä säilytetään.</p><p>Kun aloitat karanteenitilauksen, ohjelma luo kaksi lisätapahtumaa ja päivittää olemassa olevat tapahtumat. Karanteenivaraston vastaanottotapahtuman tilaksi päivitetään **Vastaanotettu** ja varastointivaraston varasto-ottotapahtuman tilaksi päivitetään **Vähennetty**.</p><p>Kahden uuden tapahtuman avulla ilmaistaan lopullinen siirto takaisin varastointivarastoon. Vastaanottotapahtuman tila on **Tilattu** varastointivarastolle, ja varasto-ottotapahtuman tila on **Varattu fyysinen** karanteenivarastolle.</p><p>Kun karanteenitilaus raportoidaan valmiiksi, tämä toiminto edustaa karanteenitilauksen fyysistä päivitystä. Varastointivaraston vastaanoton tilaksi päivitetään **Vastaanotettu**.</p><p>Kun karanteenitilaus päätetään, tämä toiminto edustaa karanteenitilauksen taloudellista päivitystä. Varasto-ottotapahtumien tilaksi päivitetään **Myyty** ja vastaanottotapahtumien tilaksi päivitetään **Ostettu**.</p><p>Vaihtoehtoisesti voit merkitä karanteenitilauksen hävikiksi. Tämä toiminto poistaa nimikkeen varastosta. Kun merkitset karanteenitilauksen hävikiksi, jäljellä on vain kolme tapahtumaa. Varastointivaraston vastaanottotapahtuma poistetaan ja jäljellä olevan vastaanottotapahtuman tilaksi päivitetään **Ostettu**. Kahden varasto-ottotapahtuman tilaksi päivitetään **Myyty**. Tämä työvaihe on tilauksen fyysinen ja taloudellinen päivitys.</p> |

## <a name="fixed-receipt-price-posting"></a>Kiinteän vastaanottohinnan kirjaus

Kiinteä vastaanottohinta mahdollistaa tuotteen vakiokustannuksen käytön. Se on vaihtoehto sille, että valitset **Standardikustannus**-vaihtoehdon nimikkeen **Nimikemalliryhmä**-sivulla. Pääasiallinen ero on se, että kun käytetään kiinteää vastaanottohintaa, nimikkeelle käytetään tällä hetkellä määritettyä kustannushintaa, kun vastaanotto varastoon kirjataan. Kiinteää vastaanottohintaa varten ei ole kustannusten uudelleenarvostusprosessia. Kun taloudellinen päivitys kirjataan, nykyistä kustannushintaa käytetään kirjauksen yhteydessä. Jos vastaanoton ja laskun kustannushinnan välillä on ero, varianssi kirjataan kiinteän vastaanottohinnan tulostileille.

Jos haluat vaihtoehtoisesti käyttää tuotteen kiinteää vastaanottohintaa, sinun on tehtävä seuraavat määritykset:

- **Nimikemalliryhmä**-sivulla on valittava **Kirjaa varastotilanne** -valintaruutu, joka valitaan varastotapahtuman riviltä.
- Valitse **Kiinteä vastaanottohinta** -valintaruutu **Nimikemalliryhmä**-sivulla.
- Määritä **Varastokirjausprofiili**-sivulla päätilit seuraaville kirjaustyypeille:

    - Kiinteän vastaanottohinnan voitto
    - Kiinteän vastaanottohinnan tappio

Lisätietoja: [Kiinteä vastaanottohinta](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Todellisen painon kirjaus

Todellisen painon tuotteita käytetään usein esimerkiksi elintarviketeollisuudessa, jossa tuotteiden paino, koko tai molemmat voivat vaihdella hieman. Todellisen painon tuotteissa käytetään kahta mittayksikköä: varastoyksikköä ja todellisen painon yksikköä. Varastoon saapuvan varaston paino voi poiketa fyysisestä varastosta otettavan varaston painosta. Todellisen painon tuotteen käsittely oikaisee varaston.

Jos todellisen painon tiedoissa on varianssi, erot kirjataan tileille, jotka on määritetty **Varaston kirjausprofiili** -sivulla määritetyille todellisen **painon tappio**- ja **todellisen painon voitto** -kenttiin. Yleensä molemmissa kentissä määritetään sama päätili.

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista.

- Veloitus/hyvitys? -sarake ilmaisee, kirjaako tapahtuma tavallisesti veloituksen vai hyvityksen. Joissakin tapauksissa tapahtuma voi kirjata joko veloituksen tai hyvityksen.
- Selvitystili-sarake ilmaisee, että kirjaustyyppi on selvitystili. Tämä tarkoittaa, että tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan.
- P/F-sarakkeessa näkyy kirjaustyyppi. "P" tarkoittaa fyysistä kirjausta ja "F" kirjanpitokirjauksia.
- "Seuraa"-sarakkeessa näkyy, onko kirjaustyypin päätili tavallisesti sama kuin toisen kirjaustyypin päätili. Se ilmaisee erityisesti kirjaustyypin, jota käytetään yleensä kirjauksessa.

> [!NOTE]
> Päätilit ja päätilien nimet taulukossa ovat vain ehdotuksia. Suosittelemme, että määrität yrityksesi tarpeille parhaan konfiguraation yhdessä kirjanpitäjän kanssa.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | P/F | Seuraa | Kuvaus |
|---|---|---|---|---|---|---|---|---|
| Todellisen painon tappiotili | 510520 | Varaston oikaisu | Kulut | | En | Molemmat | Todellisen painon voittotili | Tätä tiliä käytetään, kun kirjataan varastotapahtuma, jossa todellisen painon summa on pienempi. |
| Todellisen painon voittotili | 510520 | Varaston oikaisu | Kulut | | En | Molemmat | Todellisen painon tappiotili | Tätä tiliä käytetään, kun kirjataan varastotapahtuma, jossa todellisen painon summa on suurempi. |

Lisätietoja todellisen painon tuotteista on kohdissa [Tietoja todellisen painon nimikkeistä](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) ja [Todellisen painon tuotteen käsittely varastonhallinnan avulla](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Kirjaus varaston siirrosta käyttöomaisuudeksi

Varastosta käyttöomaisuudeksi -kirjauskansiota (**Käyttöomaisuus** \> **Kirjauskansiot** \> **Varastosta käyttöomaisuudeksi -kirjauskansio**) käytetään nimikkeiden siirtoon varastosta ja niiden muuntamiseen käyttöomaisuuseräksi. Lisätietoja on ohjeaiheessa [Käyttöomaisuuden integrointi](/fixed-assets/fixed-asset-integration.md).

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista.

- Veloitus/hyvitys? -sarake ilmaisee, kirjaako tapahtuma tavallisesti veloituksen vai hyvityksen. Joissakin tapauksissa tapahtuma voi kirjata joko veloituksen tai hyvityksen.
- Selvitystili-sarake ilmaisee, että kirjaustyyppi on selvitystili. Tämä tarkoittaa, että tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan.
- P/F-sarakkeessa näkyy kirjaustyyppi. "P" tarkoittaa fyysistä kirjausta ja "F" kirjanpitokirjauksia.
- "Seuraa"-sarakkeessa näkyy, onko kirjaustyypin päätili tavallisesti sama kuin toisen kirjaustyypin päätili. Se ilmaisee erityisesti kirjaustyypin, jota käytetään yleensä kirjauksessa.

> [!NOTE]
> Päätilit ja päätilien nimet taulukossa ovat vain ehdotuksia. Suosittelemme, että määrität yrityksesi tarpeille parhaan konfiguraation yhdessä kirjanpitäjän kanssa.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | P/F | Seuraa | Kuvaus |
|---|---|---|---|---|---|---|---|---|
| Käyttöomaisuuden otto | 180100 | Aineelliset käyttöomaisuuserät | Resurssi | Hyvitys | En | Molemmat | Ei käytettävissä | Tätä tiliä käytetään, kun varasto kirjataan käyttöomaisuuskirjauskansioon nimikkeen poistamiseksi varastosta ja sen muuntamiseksi käyttöomaisuuseräksi. |

## <a name="moving-average-posting"></a>Liukuvan keskiarvon kirjaus

Liukuva keskiarvo on keskimääräisyysperiaatteeseen perustuva jatkuva kustannuslaskentamenetelmä. Varasto-ottojen kustannukset eivät muutu, kun ostokustannus muuttuu. Ero aktivoidaan. Se perustuu suhteelliseen laskelmaan. Jäljelle jäävä summa siirretään kuluksi.

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista.

- Veloitus/hyvitys? -sarake ilmaisee, kirjaako tapahtuma tavallisesti veloituksen vai hyvityksen. Joissakin tapauksissa tapahtuma voi kirjata joko veloituksen tai hyvityksen.
- Selvitystili-sarake ilmaisee, että kirjaustyyppi on selvitystili. Tämä tarkoittaa, että tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan.
- P/F-sarakkeessa näkyy kirjaustyyppi. "P" tarkoittaa fyysistä kirjausta ja "F" kirjanpitokirjauksia.
- "Seuraa"-sarakkeessa näkyy, onko kirjaustyypin päätili tavallisesti sama kuin toisen kirjaustyypin päätili. Se ilmaisee erityisesti kirjaustyypin, jota käytetään yleensä kirjauksessa.

> [!NOTE]
> Päätilit ja päätilien nimet taulukossa ovat vain ehdotuksia. Suosittelemme, että määrität yrityksesi tarpeille parhaan konfiguraation yhdessä kirjanpitäjän kanssa.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | P/F | Seuraa | Kuvaus |
|---|---|---|---|---|---|---|---|---|
| Liukuvan keskiarvon hintaero | 510600 | Liukuvan keskiarvon hintaero | Kulut | Molemmat | En | Molemmat | Ei käytettävissä | Tätä tiliä käytetään, kun vastaanoton ja laskun kustannuksissa on eroja. |
| Liukuvan keskiarvon uudelleenarvostus | 510610 | Liukuvan keskiarvon uudelleenarvostus | Kulut | Molemmat | En | Molemmat | Ei käytettävissä | Tätä tiliä käytetään, kun oikaistaan tuotteen liukuvan keskiarvon kustannusta |

## <a name="sample-posting-profile-configuration"></a>Malli kirjausprofiilin konfiguraatiosta

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä sekä esimerkkejä päätileistä ja kuvauksista.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | P/F | Seuraa | Kuvaus |
|---|---|---|---|---|---|---|---|---|
| Varasto-otto | 140100 | Materiaalivarasto | Resurssi | Hyvitys | En | Molemmat | Varaston vastaanotto | Tätä tiliä käytetään, kun kirjattu varastotapahtuma on varasto-otto (negatiivinen määrä) eikä se liity myyntiin, ostoihin tai tuotantoon. Tämän tilin vastatili on Varastomeno – tappio -tili. Tämä tili yleensä edustaa varastoa taseessa. |
| Varastomeno – tappio | 510100 | Varaston tuotto ja tappio | Kulut | Veloitus | En | Molemmat | Varastomeno – voitto | Tätä tiliä käytetään, kun kirjattu varastotapahtuma on varasto-otto (negatiivinen määrä) eikä se liity myyntiin, ostoihin tai tuotantoon. Tämän tilin vastatili on Varasto-otto-tili. |
| Varaston vastaanotto | 140100 | Materiaalivarasto | Resurssi | Veloitus | En | Molemmat | Varasto-otto | Tätä tiliä käytetään, kun kirjattu varastotapahtuma on vastaanotto (positiivinen määrä) eikä se liity myyntiin, ostoihin tai tuotantoon. Tämän tilin vastatili on Varastomeno – voitto -tili. Tämä tili yleensä edustaa varastoa taseessa. |
| Varastomeno – voitto | 510100 | Varaston tuotto ja tappio | Kulut | Hyvitys | En | Molemmat | Varastomeno – tappio | Tätä tiliä käytetään, kun kirjattu varastotapahtuma on vastaanotto (positiivinen määrä) eikä se liity myyntiin, ostoihin tai tuotantoon. Tämän tilin vastatili on Varaston vastaanotto -tili. |
| Yksiköiden väliset maksettavat | 231500 | Yksikön välinen maksu | Velat | Veloitus | En | Molemmat | | Tätä tiliä käytetään, kun varasto siirretään varastodimensioiden, kuten toimipaikkojen, välillä ja nimikkeen kustannukset vaihtelevat toimipaikkojen välillä. |
| Yksiköiden väliset saatavat | 131500 | Yksikön välinen saatava | Resurssi | Hyvitys | En | Molemmat | | Tätä tiliä käytetään, kun varasto siirretään varastodimensioiden, kuten toimipaikkojen, välillä ja nimikkeen kustannukset vaihtelevat toimipaikkojen välillä. |
