---
title: Todellisen painon tuotteen käsittely varastonhallinnan avulla
description: Tässä ohjeaiheessa kuvataan, miten työmalleja ja sijaintidirektiivejä käytetään määrittämään, miten ja missä työ tehdään varastossa.
author: perlynne
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 14f2c6eb3baf0de65de3b72e10b42b03a8c6b21a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536707"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Todellisen painon tuotteen käsittely varastonhallinnan avulla

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/pivate-preview-banner.md)]


## <a name="feature-exposure"></a>Ominaisuuden näyttäminen

Jos haluat, että varastonhallinta käsittelee todellisen painon tuotteita, voit ottaa toiminnon käyttöön käyttöoikeuden määritysavaimen avulla. (Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**. Laajenna sitten **Konfigurointiavaimet**-välilehdessä **Kauppa \> Varaston ja kuljetusten hallinta** ja valitse **Todellinen paino varastoa varten** -valintaruutu).

> [!NOTE]
> Myös kohtien **Varaston ja kuljetusten hallinta** ja **Prosessijako \> Todellinen paino** käyttöoikeuksien määritysavaimien on oltava käytössä.

Kun käyttöoikeuden määritysavain on otettu käyttöön, voit valita vapautetun tuotteen luonnin yhteydessä **Todellinen paino**. Voit myös liittää vapautetun tuotteen siihen varastodimensioryhmään, jolle **Käytä varastonhallintaprosesseja** -parametri on valittu.

Ennen kuin tuotetta voi käyttää varastonhallinnassa, todelliselle painolle on määritettävä tietyt tuotekohtaiset perusasetukset:

- Määritä todellisen painoyksikön (laatikko) ja varastoyksikön (kilogramma \[kg\]) nimellispainon muunto yksikön muuntomääritelmän osana.
- Määritä minimi- ja maksimipainon toleranssit todellisen painon yksikkömäärityksen osana.
- Määritä sarjaryhmä, jossa todellisen painon yksikkö on määritetty pienimpänä varastointiyksikkönä (SKU).
- Määritä todellisen painon nimikkeen käsittelykäytäntö.

Lisätietoja on kohdassa [Todellisen painon nimikkeiden määrittäminen ja ylläpitäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Tapahtuman oikaisut

Koska varastoon saapuvan varaston paino voi poiketa fyysisestä varastosta otettavan varaston painosta, todellisen painon tuotteen käsittelyä on käytettävä varaston oikaisuun.

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

Jos todellinen paino kirjataan pakkausasemalla kontin pakkausprosessien aikana, varastotyöntekijöitä ei pyydetä taltioimaan painoa keräilytyön aikana. Pakkausalueelle siirtyvän kerätyn varaston painona käytetään sen sijaan fyysisen varaston keskimääräistä painoa.

Sisäisissä varastonhallintaprosesseissa, kuten inventoinnin ja oikaisun korjauksissa, voidaan määrittää, taltioidaanko paino vai ei. Jos sitä ei taltioida, käytetään nimellispainoa.

Voit myös määrittää, miten paino taltioidaan. Todellisen painon tunnisteita seurataan ja käytetään painon taltioimiseen kahdessa pääasiallisessa työnkulussa. Toisessa työnkulussa todellisen painon tunnisteita ei seurata.

- **Kyllä** – Nimike käyttää todellisen painon tunnisteita. Kukin tunnistenumero vastaa yhtä todellisen painon yksikköä (laatikkoa), ja tunnisteeseen liitetään paino ja muita tietoja. Lähtevissä prosesseissa käytetään tunnisteeseen liitettyä painoa.
- **Ei** – Nimike ei käytä todellisen painon tunnisteita. Saapuvan ja lähtevän painon punnitusprosessit perustuvat kunkin prosessin aikana taltioituun todelliseen painoon.

Todellisen painon tunnisteiden seurantaprosessia voidaan käyttää nimikkeille, joiden paino ei muutu varastoinnin aikana. Paino taltioidaan vain saapuvan varastoprosessin aikana. Todellisen painon tunnisteet vain luetaan lähtevän prosessin aikana ja tunnisteisiin liitettyjä painoja käytetään lähtevään tapahtumasidonnaiseen käsittelyyn.

### <a name="how-to-capture-catch-weight"></a>Todellisen painon taltiointi

Kun todellisen painon tunnisteseurantaa käytetään, jokaiselle vastaanotetulle todellisen painon yksikölle on luotava tunniste ja jokaiseen tunnisteeseen on aina liitettävä paino.

Esimerkki: Todellisen painon yksikkö on **laatikko** ja vastaanotetulla kuormalavalla on kahdeksan laatikkoa. Tässä tapauksessa on luotava kahdeksan yksilöivää todellisen painon tunnistetta ja kuhunkin tunnisteeseen on liitettävä paino. Saapuvan todellisen painon tunnisteen mukaan taltioidaan joko kaikkien kahdeksan laatikon paino, jonka jälkeen keskimääräinen paino jaetaan kullekin laatikolle. Vaihtoehtoisesti kullekin laatikolle voidaan taltioida yksilöivä paino.

Jos todellisen painon seurantaa ei käytetä, paino voidaan taltioida kullekin dimensioyhdistelmälle (kuten kullekin rekisterikilvelle ja seurantadimensiolle). Vaihtoehtoisesti paino voidaan taltioida koontitason perusteella, kuten viitenä rekisterikilpenä (kuormalavana).

Lähtevän painon taltiointimenetelmäksi voidaan määrittää, punnitaanko jokainen todellisen painon yksikkö (eli laatikko) vai perustuuko taltioitava paino keräiltävään määrään (kuten kolmeen laatikkoon). Huomaa, että tuotantolinjan keräysprosessissa ja sisäisissä siirtoprosesseissa käytetään keskimääräistä painoa, jos **Ei taltioitu** -asetus on käytössä.

Voit rajoittaa varastonhallinnan keräysprosesseja niin, että todellisen painon voiton/tappion oikaisujen tuloksena saatavien painojen keräilyä ei tehdä. Käytössä voi olla lähtevän painon varianssin menetelmä.

## <a name="supported-scenarios"></a>Tuetut skenaariot

Todellisen painon tuotteen käsittely varastonhallinnan avulla ei tueta kaikissa työnkuluissa. Seuraavat rajoitukset ovat käytössä tällä hetkellä.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Todellisen painon tuotteiden määrittäminen varastonhallintaprosesseja varten

- Nimikkeiden varastodimensioryhmän vaihtaminen ei ole mahdollista todellisen painon tuotteille (jotta varastonhallintaprosessien käyttö olisi niissä mahdollista).
- Todellisen painon tuotteissa tuetaan vain kaavan käsittelyä (mutta ei tuoterakenteen käsittelyä).
- Todellisen painon tuotteita ei voi liittää seurantadimensioryhmään omistajadimension avulla.
- Todellisen painon tuotteita ei voi käyttää palveluina.
- Todellisen painon tuotteita voi käyttää varastoitavina tuotteina vain nimikemalliryhmän osana.
- Todellisen painon tuotteita ei voi käyttää yhdessä aktiivisen myyntiprosessin seurantatoiminnon kanssa.
- Todellisen painon tuotteita ei voi käyttää yhdessä sarjanumeroiden taltiointitoiminnon kanssa. Tämän vuoksi tuotteita ei voi siirtää tyhjästä sarjanumeroon keräily- tai pakkausprosessin osana.
- Todellisen painon tuotteita ei voi käyttää yhdessä ennen kulutusta tapahtuvan sarjojen rekisteröintitoiminnon kanssa.
- Jos variantit on otettu käyttöön todellisen painon tuotteissa, niitä ei voi käyttää yhdessä mittayksikkövarianttien muuntotoiminnon kanssa.
- Todellisen painon tuotetta ei voi merkitä vähittäismyynnin tuotteen myyntirakenteena.
- Todellisen painon tuotteita voi käyttää vain sellaisen yksikkösarjaryhmän kanssa, jossa on todellisen painon käsittely-yksiköitä ja jossa todellisen painon yksikkö on pienimpänä sarjana.
- Todellisen painon tuotteiden varastoyksikkö voidaan muuntaa todellisen painon yksiköksi vain, jos muunnon tuloksena saatava nimellismäärä on suurempi kuin 1.
- Todellisen painon tuotteiden viivakoodimääritys ei tue muuttuvien painojen määritystä.
 
### <a name="order-processing"></a>Tilausta käsitellään

- Lähetysilmoituksen (ASN/pakkausrakenteet) luonti ei tue painotietoja.
- Tilausmäärä on ylläpidettävä todellisen painon yksikön perusteella.
 
### <a name="inbound-warehouse-processing"></a>Saapuvan varaston käsittely

- Rekisterikilpien vastaanotto edellyttää, että painot määritetään rekisteröinnin aikana, sillä painotietoja ei tueta lähetysilmoituksen osana. Todellisen painon tunnisteprosesseja käytettäessä tunnistenumero on määritettävä manuaalisesti kullekin todellisen painon yksikölle.
 
### <a name="inventory-and-warehouse-operations"></a>Varastotoiminnot

- Todellisen painon tuotteissa ei tueta karanteenitilausten manuaalista luontia.
- Työhön liittyvän varaston manuaalista siirtoa ei tueta todellisen painon tuotteissa.
- Rekisterikilpien konsolidointia ei tueta todellisen painon tuotteissa.
- Varaston varastotilan muutoksia ei tueta kausittaisen tehtävän osana todellisen painon tuotteissa.
- Kyselyn määrittämiä varastotilan muutoksia ei tueta todellisen painon tuotteissa. (Myöskään laatutilauksen varastotilan muutoksia ei tueta.)
- Todellisen painon tuotteiden varastotilaa ei muuttaa **Varastosaldo sijainnin mukaan** -sivulla.
- Todellisen painon tuotteiden varastotilaa ei voi muuttaa varastosovelluksen siirtotyön osana.
- Varaston varastotason alustamista lataamalla rekisterikilpi ei tueta todellisen painon tuotteissa.
- Erän tasausprosesseja ei tueta todellisen painon tuotteissa.
- Negatiivisen varastotilanteen käsittelyä ei tueta todellisen painon tuotteissa.
- Varastomerkintää ei voi käyttää todellisen painon tuotteissa.
 
### <a name="outbound-warehouse-processing"></a>Lähtevän varaston käsittely

- Klusterikeräilyä ei tueta todellisen painon tuotteissa.
- Keräilyn ja pakkauksen varastokäsittelyä ei tueta todellisen painon tuotteissa.
- Todellisen painon tuotteiden työtä ei voi viimeistellä **Työ**-sivulla.
- Todellisen painon tuotteiden työmallissa määritetty työ voidaan suorittaa automaattisesti.
- Työn peruuttamistoimintoa ei tueta todellisen painon tuotteissa.
- Todellisen painon tuotteissa ei tueta sellaista manuaalista pakkausasemakäsittelyä, jossa työ on luotu konttien sulkemisen jälkeen.
- Kappalekohtaista lukutoimintoa ei tueta todellisen painon tuotteissa.
 
### <a name="production-processing"></a>Tuotannon käsittely

- Todellisen painon tuotteissa tuetaan vain kaavatuotteiden erätilauksia.
- Kanban-toimintoa ei tueta todellisen painon tuotteissa.
- Todellisen painon tuotteissa sarjanumeroita ei voi rekisteröidä ennen kulutusta.
- Rekisterikilpien peruuttamistoimintoa ei tueta todellisen painon tuotteissa.
- Todellisen painon tuotteissa valmiiksi ilmoittaminen voidaan rekisteröidä sarjanumeron mukaan.

### <a name="transportation-management-processing"></a>Kuljetustenhallinnan käsittely

- Kuormituksen luonnin työtilan käsittelyä ei tueta todellisen painon tuotteissa.
- Kuljetuspyynnön rivejä ei tueta todellisen painon tuotteissa.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Muita rajoituksia ja toimintoja, jotka liittyvät todellisen painon tuotteen käsittelyyn varastonhallinnan avulla

- Jos käyttäjää ei pyydetä määrittämään seurantadimensioita keräilyprosessien aikana, paino määritetään keskimääräisen painon perusteella. Näin tapahtuu esimerkiksi silloin, kun seurantadimensioiden yhdistelmää käytetään samassa sijainnissa ja sijainnissa on jäljellä vain yksi seurantadimension arvon sen jälkeen, kun käyttäjä on käsitellyt keräilyn.
- Kun varasto on varattu tuotteelle, joka on määritetty varastonhallintaprosesseja varten, tehty varaus perustuu määritettyyn minimipainoon, vaikka tämä määrä on viimeksi käsitellyn määrän varastosaldo. Tämä toiminta poikkeaa niiden nimikkeiden toiminnasta, joita ei ole määritetty varastonhallintaprosesseja varten.
- Varaston todellista painoa ei käytetä prosesseissa, joissa painoa käytetään kapasiteettilaskemien osana (kuten aallon raja-arvot, työn pisimmät tauot, suurin kontti ja sijainnin kuormakapasiteetti). Prosessit perustuvat sen sijaan tuotteelle määritettyyn fyysiseen käsittelypainoon.
- Retail-toimintoja ei yleisesti ottaen tueta todellisen painon tuotteissa.
 
### <a name="catch-weight-tags"></a>Todellisen painon tunnisteet

Tällä hetkellä todellisen painon tunnistetoimintoa tuetaan vain seuraavien skenaarioiden osana:

- Käsiteltäessä varastosovelluksen vastaanottamaa ostotilausta.
- Käsiteltäessä kuorman vastaanottoa varastosovelluksen kautta.
- Ostotilauskuormaan liittyvää rekisterikilpeä käsiteltäessä pyydetään painomääritys vastaanottoprosessin aikana. Siirtotilausta vastaanotettaessa käytetään sen sijaan siirtotilauksen lähetystietojen painoa.
- Siirtotilauksen nimikkeen ja rivivastaanoton tullessa muusta kuin varastonhallintaprosessin varastosta.
- Myyntipalautustilauksen vastaanottokäsittely voi kirjata todellisen painon tunnisteet, mutta käsittelyä ei vahvisteta, jos tunnisteet ovat samoja tunnisteita, jotka lähetettiin alun perin tietylle myyntitilausriville.
- Käsiteltäessä varastosovelluksella muutettua varastotilaa.
- Varastosiirto tehdään varastosovelluksella.
- Käsiteltäessä oikaisua sisään tai ulos varastosovelluksella.
- Käsiteltäessä myynti- ja siirtotilausten keräilytyötä. (Huomaa, että todellisen painon tunnisteita ei voi kirjat tuotanto-osan keräilyä varten.)
- Kerättäviä määriä vähennetään kuormariveiltä riippumatta siitä, käytetäänkö kontteja.
- Pakattaessa tuotteita kontteihin pakkausasemalla.
- Avattaessa kontteja uudelleen.
- Ilmoitettaessa kaavatuotteet valmiiksi varastosovelluksen avulla.
- Käsiteltäessä kuljetuksen kuormia varastosovelluksella.

Todellisen painon tunnus voidaan luoda joko varastosovelluksen prosessissa, manuaalisesti lomakkeessa tai tietoyksikköprosessin avulla. Jos todellisen painon tunniste liitetään saapuvaan lähdeasiakirjan riviin, kuten ostotilausriviin, tunniste rekisteröidään. Jos riviä käytetään lähtevässä käsittelyssä. Tunniste päivitetään lähetyksen yhteydessä.
