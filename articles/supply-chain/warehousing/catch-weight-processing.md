---
title: Todellisen painon tuotteen käsittely varastonhallinnan avulla
description: Tässä ohjeaiheessa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä työ tehdään varastossa.
author: perlynne
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 5a751b360b2da8f786dd7b8d139e1a0a44052894
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211971"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Todellisen painon tuotteen käsittely varastonhallinnan avulla

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Ominaisuuden näyttäminen

Jos haluat, että varastonhallinta käsittelee todellisen painon tuotteita, voit ottaa toiminnon käyttöön käyttöoikeuden määritysavaimen avulla. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**. Laajenna sitten **Konfigurointiavaimet**-välilehdessä **Kauppa \> Varaston ja kuljetusten hallinta** ja valitse **Todellinen paino varastoa varten** -valintaruutu.

> [!NOTE]
> Myös kohtien **Varaston ja kuljetusten hallinta** ja **Prosessijako \> Todellinen paino** käyttöoikeuksien määritysavaimien on oltava käytössä. Todellisen painon määritysavaimien määrittämistä varten myös toiminto on otettava käyttöön **Toimintojen hallinta** -työtilassa. Tärkein käyttöön otettava toiminto on **Todellisen painon tuotteen käsittely varastonhallinnan avulla**. Kaksi liittyvää, mutta valinnaista toimintoa, jotka voit ottaa käyttöön, ovat **Todellisen painon tuotteiden varaston tilamuutokset** ja **Käytä olemassa olevia todellisen painon tunnisteita, kun raportoinnin tuotantotilaukset ovat valmiita**.

Kun käyttöoikeuden määritysavain on otettu käyttöön, voit valita vapautetun tuotteen luonnin yhteydessä **Todellinen paino**. Voit myös liittää vapautetun tuotteen siihen varastodimensioryhmään, jolle **Käytä varastonhallintaprosesseja** -parametri on valittu.

Ennen kuin tuotetta voi käyttää varastonhallinnassa, todelliselle painolle on määritettävä tietyt tuotekohtaiset perusasetukset:

- Määritä todellisen painoyksikön (laatikko) ja varastoyksikön (kilogramma \[kg\]) nimellispainon muunto yksikön muuntomääritelmän osana.
- Määritä minimi- ja maksimipainon toleranssit todellisen painon yksikkömäärityksen osana.
- Määritä sarjaryhmä, jossa todellisen painon yksikkö on määritetty pienimpänä varastointiyksikkönä (SKU).
- Määritä todellisen painon nimikkeen käsittelykäytäntö.

Lisätietoja on kohdassa [Todellisen painon nimikkeiden määrittäminen ja ylläpitäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Tapahtuman oikaisut

Koska varastoon saapuvan varaston paino voi poiketa fyysisestä varastosta otettavan varaston painosta, todellisen painon tuotteen käsittelyä on käytettävä varaston oikaisuun.

> [!NOTE]
> Mobiililaitetehtävä käynnistää tapahtumaoikaisun vain, jos nimikkeen todellisen painon nimikkeen käsittelykäytännön lähtevän painon varianssimenetelmä on **Salli painon varianssi**.

**Esimerkki 1**

**Ilmoita valmiiksi** -tuotantoprosessin aikana sellaisen rekisterikilven saapuvaksi painoksi, joka koostuu kahdeksasta todellisen painon tuotteen laatikosta, taltioidaan 80,1 kg. Rekisterikilpi varastoidaan sitten valmiiden tavaroiden alueelle, jossa osa painosta katoaa varastoinnin aikana ilmaan.

Myöhemmin myyntitilauksen keräilyprosessin osana saman rekisterikilven painoksi taltioidaan 79,8 kg. Tämän vuoksi järjestelmän fyysisessä dimensioyhdistelmässä on nyt painoero.

Järjestelmä oikaisee siinä tapauksessa eron kirjaamalla tapahtuman puuttuvalle 0,3 kilogrammalle.

**Esimerkki 2**

Tuotteen määritelmässä tuotteen vähimmäispainoksi määritetään 8 kg ja enimmäispainoksi 12 kg, kun todellisen painon yksikkönä on **laatikko**.

Sinulla on kaksi tuotelaatikkoa, joiden rekisteröity paino on 16 kg. Jos varastotyöntekijä kerää ja punnitsee toisen laatikoista ja painoksi taltioidaan 9 kg, jäljellä olevan laatikon paino on 7 kg. Koska 7 kg kuitenkin aloittaa minimipainon, järjestelmä tekee automaattisen oikaisun ja nostaa käytettävissä olevan varaston painoa 1 kilogrammalla.

Voit määrittää tilit, joihin nämä oikaisut kirjataan, valitsemalla **Kustannusten hallinta \> Kirjanpidon integrointikäytäntöjen määrittäminen \> Kirjaus**. Määritä sitten **Varasto**-välilehdessä seuraavat tilit:

- Todellisen painon tappiotili
- Todellisen painon voittotili

## <a name="catch-weight-item-handling-policy"></a>Todellisen painon nimikkeen käsittelykäytäntö

Todellisen painon nimikkeen käsittelykäytännössä määritetään kaksi nimikkeiden ensisijaista varastonhallinnan työnkulkua: nimikkeiden painojen taltiointiajankohta ja kirjaustapa.

Voit määrittää, milloin paino taltioidaan myynti- ja siirtotilauksen käsittelyä varten. Paino voidaan taltioida jommankumman seuraavan prosessin aikana:

- **Keräily** – Paino taltioidaan tilaustyön työrivien ensimmäisen keräilyn aikana.
- **Pakkaus** – Paino taltioidaan manuaalisen pakkauksen aikana. (Nimikkeet on lähetettävä pakkausasemalle.)

Jos todellinen paino kirjataan pakkausasemalla kontin pakkausprosessien aikana, varastotyöntekijöitä ei pyydetä taltioimaan painoa keräilytyön aikana. Pakkausalueelle siirtyvän kerätyn varaston painona käytetään sen sijaan fyysisen varaston keskimääräistä painoa. Tämä käsite koskee myös tunnisteilla seurattavia todellisen painon nimikkeitä. Nämä parametrit määrittävät tunnisteilla määritetyissä nimikkeissä, milloin tunniste taltioituu. Tunniste taltioidaan joko keräilyaikana käyttämällä mobiililaitetta tai manuaalisen pakkauksen aikana.

> [!NOTE]
> Koska **Pakkaus**-asetus aiheuttaa varaston päivittämisen keskimääräisellä keräillyllä paino, se voi käynnistää ristiriidan, joka voi aiheuttaa todellisen painon voiton/tappion oikaisun ja/tai eron varaston todellisen painon ja todellisen painon tunnisteen painon välillä.

Sisäisissä varastonhallintaprosesseissa, kuten inventoinnin ja oikaisun korjauksissa, voidaan määrittää, taltioidaanko paino. Jos sitä ei taltioida, käytetään nimellispainoa. Muilla vaihtoehdoilla voi taltioida painon todellisen painoyksikön mukaan ja laskentamäärän mukaan.

Voit myös määrittää, miten paino taltioidaan. Todellisen painon tunnisteita seurataan ja käytetään painon taltioimiseen kahdessa pääasiallisessa työnkulussa. Toisessa työnkulussa todellisen painon tunnisteita ei seurata.

- **Kyllä** – Nimike käyttää todellisen painon tunnisteita. Kukin tunnistenumero vastaa yhtä todellisen painon yksikköä (laatikkoa), ja tunnisteeseen liitetään paino ja muita tietoja. Lähtevissä prosesseissa käytetään tunnisteeseen liitettyä painoa.
- **Ei** – Nimike ei käytä todellisen painon tunnisteita. Saapuvan ja lähtevän painon punnitusprosessit perustuvat kunkin prosessin aikana taltioituun todelliseen painoon.

Todellisen painon tunnisteiden seurantaprosessia voidaan käyttää nimikkeille, joiden paino ei muutu varastoinnin aikana. Paino taltioidaan vain saapuvan varastoprosessin aikana. Todellisen painon tunnisteet vain luetaan lähtevän prosessin aikana ja tunnisteisiin liitettyjä painoja käytetään lähtevään tapahtumasidonnaiseen käsittelyyn.

Toinen todellisen painon tunnisteiden käsittelyyn liittyvä toinen tärkeä parametri on **Todellisen painon tunnistedimension seurantamenetelmä**. Tunnisteita voidaan seurata joko osittain tai kokonaan. Jos tunnistetta seurataan osittain, se seuraa tuotedimensioita, seurantadimensioita ja varaston tilaa. Jos tunnistetta seurataan kokonaisuudessaan, se seuraa tuotedimensioita, seurantadimensioita ja **kaikkia** varastodimensioita.

Kun nimikettä seurataan tunnisteella, käytössä on lisäksi **Lähtevän painon taltiointimenetelmä** -parametri. Voit määrittää tämän parametrin siten, että sinulta kysytään tunniste lähtevien tapahtumien yhteydessä mobiililaitetta käytettäessä. Vaihtoehtoisesti voit määrittää parametrin siten, että tunnisteita pyydetään vain silloin, kun niitä tarvitaan. Tietyssä varaston rekisterikilvessä on esimerkiksi viisi todellisen painon tunnistetta, ja olet ilmoittanut, että haluat kerätä kaikki viisi tunnistetta rekisterikilvestä. Jos tässä tapauksessa **Lähtevän painon taltiointimenetelmä** -parametriksi on määritetty **Pyydä tunnistetta vain tarvittaessa**, viisi tunnistetta kerätään automaattisesti. Yksittäisiä tunnisteita ei siis tarvitse skannata. Jos parametriksi on määritetty **Pyydä tunniste aina**, jokainen tunniste on skannattava, vaikka kaikki viisi tunnistetta kerätään.

> [!NOTE]
> Tunnisteet taltioidaan ja päivitetään pääsääntöisesti vain mobiililaitteen valikon vaihtoehdoista. Muutamissa skenaariossa tunnisteet kuitenkin taltioidaan muualla (esimerkiksi manuaalisella pakkausasemalla). Yleensä mobiililaitteen valikon vaihtoehtoja pitäisi kuitenkin käyttää kaikissa varastotehtävissä tunnisteita käytettäessä.

### <a name="how-to-capture-catch-weight"></a>Todellisen painon taltiointi

**Kun todellisen painon tunnisteseurantaa käytetään**, jokaiselle vastaanotetulle todellisen painon yksikölle on luotava tunniste ja jokaiseen tunnisteeseen on aina liitettävä paino.

Esimerkki: Todellisen painon yksikkö on **laatikko** ja vastaanotetulla kuormalavalla on kahdeksan laatikkoa. Tässä tapauksessa on luotava kahdeksan yksilöivää todellisen painon tunnistetta ja kuhunkin tunnisteeseen on liitettävä paino. Saapuvan todellisen painon tunnisteen mukaan taltioidaan joko kaikkien kahdeksan laatikon paino, jonka jälkeen keskimääräinen paino jaetaan kullekin laatikolle. Vaihtoehtoisesti kullekin laatikolle voidaan taltioida yksilöivä paino.
Kun käytät **Käytä olemassa olevia todellisen painon tunnisteita, kun raportoinnin tuotantotilaukset ovat valmiita** -toimintoa ja prosessi on otettu käyttöön mobiililaitteen valikkonimikkeen kautta, varasto päivittyy olemassa olevan todellisen painon tunnisteen tiedoilla. Tämän vuoksi varastointisovellus ei pyydä tallentamaan todellisen painon tunnisteen tietoja osana tuotantoraporttia valmiina työvaiheena.

**Jos todellisen painon seurantaa ei käytetä**, paino voidaan taltioida kullekin dimensioyhdistelmälle (kuten kullekin rekisterikilvelle ja seurantadimensiolle). Vaihtoehtoisesti paino voidaan taltioida koontitason perusteella, kuten viitenä rekisterikilpenä (kuormalavana).

Lähtevän painon taltiointimenetelmistä **Todellisen painon yksikköä kohti** -asetuksella voi määrittää, että punnitus on tehtävä kullekin todellisen painon yksikölle (esimerkiksi laatikon mukaan). **Keräily-yksikkö kohti** -asetuksella voi määrittää taltioitavan painon kerättävän painon perusteella (esimerkiksi kolme laatikkoa). Huomaa, että tuotantolinjan keräysprosessissa ja sisäisissä siirtoprosesseissa käytetään keskimääräistä painoa, jos **Ei taltioitu** -asetus on käytössä.

Todellisen painon nimikkeen käsittelykäytännössä määritetään useita painon taltiointimenetelmiä. Eri tapahtumat käyttävät kutakin painon taltiointimenetelmän parametria. Seuraavassa taulukossa on yhteenveto tapahtumien käyttämistä parametreista.

| Tapa                                     | Tapahtuma                                |
|--------------------------------------------|--------------------------------------------|
| Lähtevän painon taltiointimenetelmä           | Myynnin keräily, siirron keräily            |
| Tuotannon keräilypainon taltiointimenetelmä | Tuotannon keräily, tuotannon kulutus |
| Liikkeen painon taltiointimenetelmä           | Siirto                                   |
| Ilmaisee, milloin painon oikaisu taltioidaan       | Oikaisut, inventointi                      |
| Laskentapainon taltiointimenetelmä           | Inventointi                                   |
| Varaston siirtopainon taltiointimenetelmä | Varastosiirto                         |

Voit estää varastonhallinnan keräysprosessit siten, että todellisen painon voiton/tappion oikaisujen tuloksena saatavien painojen keräilyä ei tehdä. Käytössä voi olla lähtevän painon varianssin menetelmä. Lähtevän painon varianssin menetelmää käytetään seuraavissa mobiililaitteen prosesseissa: myynnin keräily, siirron keräily, tuotannon keräily, siirrot, laskenta ja varastosiirrot. Voit käyttää **Rajoita painon varianssia** -asetusta, jos todellisen painon nimikkeen paino ei vaihtele varastosäilytyksen aikana ja jos todellisen painon voiton/tappion oikaisuja ei tarvita. Voit käyttää **Salli painon varianssi** -asetus, jos paino voi vaihdella ja jos todellisen painon voiton/tappion oikaisuja tarvitaan, kun painon vaihtelu kirjataan.

## <a name="unsupported-scenarios"></a>Skenaariot, joita ei tueta

Todellisen painon tuotteen käsittely varastonhallinnan avulla ei tueta kaikissa työnkuluissa. Seuraavat rajoitukset ovat käytössä tällä hetkellä. Ne koskevat kaikkia todellisen painon nimikkeitä riippumatta siitä, käytetäänkö niissä tunnisteita.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Todellisen painon tuotteiden määrittäminen varastonhallintaprosesseja varten

- Todellisen painon tuotteissa tuetaan vain kaavan käsittelyä (mutta ei tuoterakenteen käsittelyä).
- Todellisen painon tuotteita ei voi liittää seurantadimensioryhmään omistajadimension avulla.
- Todellisen painon tuotteita ei voi käyttää palveluina.
- Todellisen painon tuotteita voi käyttää varastoitavina tuotteina vain nimikemalliryhmän osana.
- Todellisen painon tuotteita ei voi käyttää yhdessä aktiivisen myyntiprosessin seurantatoiminnon kanssa.
- Todellisen painon tuotteita ei voi käyttää yhdessä sarjanumeroiden taltiointitoiminnon kanssa. Tämän vuoksi tuotteita ei voi siirtää tyhjästä sarjanumeroon keräily- tai pakkausprosessin osana.
- Todellisen painon tuotteita ei voi käyttää yhdessä ennen kulutusta tapahtuvan sarjojen rekisteröintitoiminnon kanssa.
- Jos variantit on otettu käyttöön todellisen painon tuotteissa, niitä ei voi käyttää yhdessä mittayksikkövarianttien muuntotoiminnon kanssa.
- Todellisen painon tuotetta ei voi merkitä kaupallisena tuotteen myyntirakenteena.
- Todellisen painon tuotteita voi käyttää vain sellaisen yksikkösarjaryhmän kanssa, jossa on todellisen painon käsittely-yksiköitä ja jossa todellisen painon yksikkö on pienimpänä sarjana.
- Todellisen painon tuotteiden varastoyksikkö voidaan muuntaa todellisen painon yksiköksi vain, jos muunnon tuloksena saatava nimellismäärä on suurempi kuin 1.
- Todellisen painon tuotteiden viivakoodimääritys ei tue muuttuvien painojen määritystä.

### <a name="order-processing"></a>Tilausta käsitellään

- Lähetysilmoituksen (ASN/pakkausrakenteet) luonti ei tue painotietoja.
- Tilausmäärä on ylläpidettävä todellisen painon yksikön perusteella.

### <a name="inbound-warehouse-processing"></a>Saapuvan varaston käsittely

- Rekisterikilpien vastaanotto edellyttää, että painot määritetään rekisteröinnin aikana, sillä painotietoja ei tueta lähetysilmoituksen osana. Todellisen painon tunnisteprosesseja käytettäessä tunnistenumero on määritettävä manuaalisesti kullekin todellisen painon yksikölle.
- Saapuvaa laaduntarkistustyötä ei tueta todellisen painon tuotteissa. Jos määritetty, laaduntarkistus työ ohitetaan.

### <a name="inventory-and-warehouse-operations"></a>Varastotoiminnot

- Todellisen painon tuotteissa ei tueta karanteenitilausten manuaalista luontia.
- Avoimeen työhön liittyvän varaston manuaalista siirtoa ei tueta todellisen painon tuotteissa.
- Varaston varastotason alustamista lataamalla rekisterikilpi ei tueta todellisen painon tuotteissa.
- Erän tasausprosesseja ei tueta todellisen painon tuotteissa.
- Negatiivisen varastotilanteen käsittelyä ei tueta todellisen painon tuotteissa.
- Varastomerkintää ei voi käyttää todellisen painon tuotteissa.

### <a name="outbound-warehouse-processing"></a>Lähtevän varaston käsittely

- Klusterikeräilyä ei tueta todellisen painon tuotteissa.
- Keräilyn ja pakkauksen varastokäsittelyä ei tueta todellisen painon tuotteissa.
- Todellisen painon tuotteiden työmallissa määritetty työ voidaan suorittaa automaattisesti.
- Järjestelmä ei tue todellisen painon tuotteissa sellaista manuaalista pakkausasemakäsittelyä, jossa pakatun kontin keräilytyö on luotu konttien sulkemisen jälkeen.
- Kappalekohtaista lukutoimintoa ei tueta todellisen painon tuotteissa.

### <a name="production-processing"></a>Tuotannon käsittely

- Todellisen painon tuotteissa tuetaan vain kaavatuotteiden erätilauksia.
- Kanban-toimintoa ei tueta todellisen painon tuotteissa.
- Todellisen painon tuotteissa sarjanumeroita ei voi rekisteröidä ennen kulutusta.
- Tuotannon rekisterikilpien peruuttamistoimintoa ei tueta todellisen painon tuotteissa.
- Todellisen painon tuotteissa valmiiksi ilmoittamista ei voi rekisteröidä sarjanumeron mukaan.

### <a name="transportation-management-processing"></a>Kuljetustenhallinnan käsittely

- Kuormituksen luonnin työtilan käsittelyä ei tueta todellisen painon tuotteissa.
- Kuljetuspyynnön rivejä ei tueta todellisen painon tuotteissa.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Muita rajoituksia ja toimintoja, jotka liittyvät todellisen painon tuotteen käsittelyyn varastonhallinnan avulla

- Jos käyttäjää ei pyydetä määrittämään seurantadimensioita keräilyprosessien aikana, paino määritetään keskimääräisen painon perusteella. Näin tapahtuu esimerkiksi silloin, kun seurantadimensioiden yhdistelmää käytetään samassa sijainnissa ja sijainnissa on jäljellä vain yksi seurantadimension arvon sen jälkeen, kun käyttäjä on käsitellyt keräilyn.
- Kun varasto on varattu tuotteelle, joka on määritetty varastonhallintaprosesseja varten, tehty varaus perustuu määritettyyn minimipainoon, vaikka tämä määrä on viimeksi käsitellyn määrän varastosaldo. Tämä toiminta poikkeaa niiden nimikkeiden toiminnasta, joita ei ole määritetty varastonhallintaprosesseja varten. Tähän rajoitukseen on yksi poikkeus. Kun tuotannon keräilyn sarjanumero-ohjatun todellisen painon tuotteen viimeksi käsitelty määrä kerätään, todellista painoa käytetään.
- Varaston todellista painoa ei käytetä prosesseissa, joissa painoa käytetään kapasiteettilaskemien osana (kuten aallon raja-arvot, työn pisimmät tauot, suurin kontti ja sijainnin kuormakapasiteetti). Prosessit perustuvat sen sijaan tuotteelle määritettyyn fyysiseen käsittelypainoon.
- Kaupallisia toimintoja ei yleisesti ottaen tueta todellisen painon tuotteissa.
- Todellisen painon tuotteiden varaston tilaa ei voi päivittää **Varaston tilamuutos** -kohdassa.

### <a name="catch-weight-tags"></a>Todellisen painon tunnisteet

Todellisen painon tunnus voidaan luoda varastosovelluksen prosessilla, manuaalisesti lomakkeessa tai tietoyksikköprosessin avulla. Jos todellisen painon tunniste liitetään saapuvaan lähdeasiakirjan riviin, kuten ostotilausriviin, tunniste rekisteröidään. Jos riviä käytetään lähtevien käsittelyyn, tunniste päivitetään toimitetuksi.

Todellisen painon tuotteissa tällä hetkellä käytettyjen rajoitusten lisäksi tunnisteella varustetuissa todellisen painon tuotteissa on myös muita rajoituksia.

- Kaikkien varaston manuaalisten päivitysten (eli muut kuin mobiililaitteella tehdyt päivitykset) on sisällettävä vastaavat liittyvien todellisen painon tunnisteiden manuaaliset päivitykset, koska näitä päivityksiä ei tehdä automaattisesti. Esimerkiksi manuaaliset oikaisukirjauskansiot päivittävät varaston mutta eivät liitettyjä todellisen painon tunnisteita.
- Todellisen painon tunnisteet on päivitettävä manuaalisesti vastaamaan täydennystyösiirtoja. Tämä johtuu siitä, että järjestelmä ei voi taltioida painoja täydennystyötä käsiteltäessä, minkä vuoksi keskimääräinen paino kirjataan.
- Yhdistetyn rekisterikilven vastaanottamista ei tueta tällä hetkellä tunnisteella varustetuissa todellisen painon nimikkeissä.
- Myyntipalautustilauksen vastaanottokäsittely voi kirjata todellisen painon tunnisteet. Käsittely ei kuitenkaan tarkista, että palautustunniste on sama tunniste, joka lähetettiin alun perin tietylle myyntitilaukselle.
- Mobiililaitteen valikon vaihtoehto, jossa on **Rekisteröi materiaalikulutus** -tehtäväkoodi, ei tällä hetkellä tue todellisen painon tunnisteiden kirjaamista.
- Vaikka inventointiprosesseja tuetaan tunnisteella varustetuissa todellisen painon nimikkeissä, ne ovat rajoitettuja. Voit esimerkiksi käyttää mobiililaitteen asetuksia tunnisteella varustettujen todellisen painon nimikkeiden inventointiin, ja käytössä on keskimääräinen paino. Inventointitapahtuma ei kuitenkaan päivitä todellisen painon tunnisteita automaattisesti. Kun inventointitapahtuma on valmis, todellisen painon tunnisteet on päivitettävä manuaalisesti vastaamaan varastoa. Jos nimikkeet, jotka eivät alun perin olleet sijainnissa, inventoidaan kyseiseen sijaintiin, käytössä on nimellispaino.
- Rekisterikilven konsolidointi ei tällä tue tunnisteella varustettuja todellisen painon nimikkeitä.
- Työn palautustoimintoa ei tueta todellisen painon nimikkeissä, joita seurataan tunnistenumeroilla.

> [!NOTE]
> Edellä olevat todellisen painon tunnisteet pitävät paikkansa vain, jos todellisen painon tuotteessa on todellisen painon tunnistedimension seurantamenetelmänä täydellinen seuranta. (Toisin sanoen todellisen painon nimikkeen käsittelykäytännön **Todellisen painon tunnistedimension seurantamenetelmä** -parametriksi määritetään **Tuotantodimensiot, seurantadimensiot ja kaikki varastodimensiot**.) Lisärajoituksia käytetään, jos todellisen painon nimike on vain osittain tunnisteseurattu. (Toisin sanoen todellisen painon nimikkeen käsittelykäytännön **Todellisen painon tunnistedimension seurantamenetelmä** -parametriksi on määritetty **Tuotantodimensiot, seurantadimensiot ja varaston tila**.) Koska tässä tunnisteen ja varaston näkyvyys menetetään, joitakin lisäskenaarioita ei tueta.
