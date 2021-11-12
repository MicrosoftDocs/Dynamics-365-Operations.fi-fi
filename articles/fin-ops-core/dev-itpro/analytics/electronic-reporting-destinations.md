---
title: Sähköisen raportoinnin (ER) kohteet
description: Tässä ohjeessa esitetään tietoja sähköisen raportoinnin kohteista, tuetuista kohdetyypeistä ja turvallisuusnäkökohdista.
author: nselin
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e8e176b8d4e14eee2050b3c66f7547ff878b5174
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647090"
---
# <a name="electronic-reporting-er-destinations"></a>Sähköisen raportoinnin (ER) kohteet

[!include [banner](../includes/banner.md)]

Voit määrittää kohteen jokaiselle sähköisen raportoinnin (ER) muotokokoonpanolle ja sen tuloskomponentille (kansio tai tiedosto). Käyttäjät, joilla on tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana. Tässä aiheessa käsitellään ER-kohteiden hallintaa, tuettuja kohdetyyppejä ja suojausta.

ER-muotomäärityksissä on yleensä vähintään yksi tulosteosa: tiedosto. Yleensä määrityksissä on useita eri tyyppisiä tiedostotulosteosia (kuten XML, TXT, XLSX, DOCX tai PDF), jotka on ryhmitelty joko yhteen kansioon tai moneen kansioon. Voit määrittää ER-kohteen hallinnassa valmiiksi, mitä tapahtuu, kun kukin osa suoritetaan. Kun määritys suoritetaan, käyttäjälle näytetään valintaikkuna, jolla tiedoston voi tallentaa tai avata. Sama toiminta toteutuu myös ER-määrityksiä tuotaessa, joten sitä varten ei tarvitse määrittää tiettyä kohdetta. Kun päätulosteosalle on luotu kohde, kyseisen kohde ohittaa oletustoiminnallisuuden ja kansio tai tiedosto lähetetään kohdeasetusten mukaisesti.

## <a name="availability-and-general-prerequisites"></a>Saatavuus ja yleiset edellytykset

ER-kohteiden toiminto ei ole käytössä Microsoft Dynamics AX 7.0:ssa (helmikuu 2016). Siksi sinun on asennettava Microsoft Dynamics 365 for Operationsin versio 1611 (marraskuu 2016) tai sitä uudempi, jotta voit käyttää seuraavia kohdetyyppejä:

- [Sähköposti](er-destination-type-email.md)
- [Arkistoi](er-destination-type-archive.md)
- [Tiedosto](er-destination-type-file.md)
- [Näyttö](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

Vaihtoehtoisesti voit asentaa jonkin seuraavista edellytyksistä: Huomaa kuitenkin, että nämä vaihtoehdot tarjoavat rajoitetumman ER-käyttökokemuksen.

- Microsoft Dynamics AX -sovelluksen versio 7.0.1 (toukokuu 2016)
- [Sähköisen raportoinnin kohteiden hallinnan sovelluksen hotfix-korjaus](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

On myös olemassa [Tuloste](er-destination-type-print.md)-kohdetyyppi. Sen käyttämiseksi sinun on asennettava Microsoft Dynamics 365 Financen versio 10.0.9 (huhtikuu 2020).

## <a name="overview"></a>Yleiskatsaus

Voit määrittää kohteet vain kulloiseenkin Finance-esiintymään [tuoduissa](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) ER-määrityksissä ja voit käyttää vain **Sähköisen raportoinnin konfiguraatiot** -sivulla olevia muotoja. ER-kohdehallinnan toiminto on käytettävissä kohdassa **Organisaation hallinto** \> **Sähköinen raportointi** \> **Sähköisen raportoinnin kohde**.

### <a name="default-behavior"></a>Oletusarvoinen käyttäytyminen

ER-muodon konfiguroinnin oletustoiminta määräytyy sen mukaan, mikä suoritustyyppi määritetään, kun ER-muoto alkaa.

Jos määrität **Eräkäsittely**-asetuksen arvoksi **Ei**, **Intrastat-raportti**-valintaikkunan **Suorita taustalla** -pikavälilehdessä voit käyttää ER-muotoa heti vuorovaikutteisessa tilassa. Kun tämä suoritus on suoritettu onnistuneesti, luotu lähtevä asiakirja on ladattavissa.

Jos määrität **Eräkäsittely**-asetukseksi **Kyllä**, ER-muoto suoritetaan [erä](../sysadmin/batch-processing-overview.md)-tilassa. Luodaan oikea erätyö, joka perustuu parametreihin, jotka määrität **Suorita taustalla**-välilehdellä **ER-parametrit**-valintaikkunassa.

> [!NOTE]
> Työn kuvauksessa ilmoitetaan ER-muotomäärityksen suoritus. Lisäksi se sisältää suoritettavan ER-osan nimen.

[![ER-muodon käyttö.](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Tietoja tästä työstä on useissa paikoissa:

- Siirry kohtaan **Yleiset** \> **Kyselyt** \> **Erätyöt** \> **Omat erätyöt** tarkistaaksesi ajoitetun työn tilan.
- Siirry kohtaan **Organisaation hallinta** \> **Sähköinen raportointi** \> **sähköisen raportoinnin työt** tarkistaaksesi ajoitetun työn tilan ja valmiin työn suoritustulokset. Kun työn suorittaminen on suoritettu onnistuneesti, hae luotu lähtevä asiakirja valitsemalla **sähköisen raportoinnin työt**-sivulta **Näytä tiedostot**.

    > [!NOTE]
    > Tämä tiedosto tallennetaan nykyisen työtietueen liitteenä, ja sitä hallitaan [tiedostonhallinta](../../fin-ops/organization-administration/configure-document-management.md) -kehyksellä. [Tiedostotyyppi](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), jota käytetään tämäntyyppisten artefakteja varten, määritetään [ER-parametreissa](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- Valitse **Sähköisen raportoinnin työt** -sivulla **Näytä tiedostot**, jos haluat nähdä luettelon töiden suorituksen aikana luoduista virheistä ja varoituksista.

    [![ER-töiden luettelon tarkasteleminen.](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Käyttäjän määrittämä toiminta

**Sähköisen raportoinnin kohde** -sivulla voit ohittaa määrityksen oletusarvoisen toiminnan. Tuotuja määrityksiä ei näytetä tällä sivulla, ennen kuin valitset **Uusi** ja valitset sitten **Viittaus**-kentässä määrityksen, jolle kohdeasetukset luodaan.

[![Määrityksen valitseminen viitekenttään.](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Kun olet luonut viitteen, voit luoda tiedostokohteen kullekin viitatun ER-muodon **Kansio**- tai **Tiedosto**-tuloskomponentille.

[![Tiedostokohteen luonti.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Voit sitten ottaa tiedostokohteen yksittäiset kohteet käyttöön tai poistaa ne käytöstä **Kohdeasetukset**-valintaruudussa. **Asetukset**-painikkeella voidaan hallita kaikki valitun tiedostokohteen kohteita. Voit hallita **Kohdeasetukset**-valintaikkunassa kutakin kohdetta erikseen valitsemalla sen kohdalla **käytössä**.

**Versiota 10.0.9 aikaisemmissa** Financen versioissa voit luoda **yhden tiedostokohteen** kullekin samanmuotoiselle, **Tiedostonimi**-kentässä valitulle tulosteosalle, kuten kansiolle tai tiedostolle. **Versiossa 10.0.9 ja sitä uudemmissa** sen sijaan voit luoda **useita tiedostokohteita** kullekin samanmuotoiselle tulosteosalle.

Tämän ominaisuuden avulla voit esimerkiksi määrittää tiedostojen kohteet tiedostokomponentille, jota käytetään lähtevän asiakirjan luomiseen Excel-muodossa. Yksi kohde ([Arkisto](er-destination-type-archive.md)) voidaan määrittää tallentamaan alkuperäinen Excel-tiedosto ER-tehtävien arkistoon ja toinen kohde ([Sähköposti](er-destination-type-email.md)) voidaan määrittää samanaikaisesti [muuntamaan](#OutputConversionToPDF) Excel-tiedosto PDF-muotoon ja lähettämään PDF-tiedosto sähköpostitse.

[![Useiden kohteiden määrittäminen yksittäistä muotoelementtiä varten.](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Kun ER-muoto suoritetaan, kaikki muodon osille määritetyt kohteet suoritetaan aina. Lisäksi Finance **versiossa 10.0.17 ja sitä uudemmissa versioissa**, ER-kohteiden toimintoa on parannettu, ja sillä voi nyt määrittää erilaisia kohdejoukkoja yhdelle ER-muodolle. Tämä määritys merkitsee kunkin joukon tietylle käyttäjätoiminnolle määritetyksi. ER-ohjelmointirajapintaa on [laajennettu](er-apis-app10-0-17.md) siten, että käyttäjä suorittaa annetun toiminnon suorittamalla ER-muodon. Annettu toimintokoodi välitetään ER-kohteeseen. ER-muodon eri kohteita voidaan suorittaa annetun toimintokoodin perusteella. Lisätietoja on kohdassa [Toiminnosta riippuvaisten ER-kohteiden määrittäminen](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Kohdetyypit

ER-kohteille tuetaan tällä hetkellä seuraavia kohteita. Voit poistaa kaikki tyypit käytöstä tai ottaa ne käyttöön samanaikaisesti. Voit tällä tavoin joko olla tekemättä mitään tai lähettää osan kaikkiin määritettyihin kohteisiin.

- [Sähköposti](er-destination-type-email.md)
- [Arkistoi](er-destination-type-archive.md)
- [Tiedosto](er-destination-type-file.md)
- [Näyttö](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Tulostus](er-destination-type-print.md)

## <a name="applicability"></a>Soveltuvuus

Voit määrittää kohteet vain tuoduissa ER-määrityksissä ja voit käyttää vain **Sähköisen raportoinnin konfiguraatiot** -sivulla olevia muotoja.

> [!NOTE]
> Määritetyt kohteet ovat yrityskohtaisia. Jos aiot käyttää ER-muotoa nykyisen Finance-esiintymän eri yrityksissä, sinun on määritettävä kyseiselle ER-muodolle kohteet jokaisen yrityksen osalta.

Kun määrität valitun muodon tiedostokohteita, määrität ne koko muotoa varten.

[![Määrityslinkki.](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Samalla sinulla voi olla useita [versioita](general-electronic-reporting.md#component-versioning) siitä muodosta, joka on tuotu kulloiseenkin Finance-esiintymään. Voit tarkastella niitä valitsemalla **Määritys**-linkin, joka tarjotaan, kun valitset **Viite**-kentän.

[![Määritysversiot.](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Oletusarvoisesti määritettyjä kohteita käytetään vain, kun suoritat ER-muotoversion, jonka tila on joko **Valmis** tai **Jaettu**. Sinun on kuitenkin joskus käytettävä määritettyjä kohteita, kun suoritetaan ER-muodon luonnosversio. Saatat esimerkiksi muokata muotosi luonnosversiota ja haluta käyttää määritettyjä kohteita sen testaamiseksi, miten luotu tulos toimitetaan. Seuraavia vaiheita noudattamalla sovellat kohteita ER-muodolle, kun suoritetaan luonnosversio.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Käytä kohteita luonnostilassa** -asetuksen arvoksi **Kyllä**.

[![Käytä kohteita luonnostilassa -asetus.](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Käyttääksesi ER-muodon luonnosversiota sinun on merkittävä ER-muoto vastaavasti.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Suorita asetus** -vaihtoehdoksi **Kyllä**.

[![Suorita asetus -vaihtoehto.](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Kun olet suorittanut tämän määrityksen, **Suorita luonnos** -vaihtoehto on käytettävissä muokattavien ER-muotojen yhteydessä. Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat alkaa käyttää muodon luonnosversiota, kun se suoritetaan.

[![Suorita luonnos -vaihtoehto.](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Kohdevirheiden käsittely

Yleensä ER-muoto suoritetaan tietyn liiketoimintaprosessin puitteissa. ER-muodon suorittamisen aikana luotavan lähtevän asiakirjan toimitus on kuitenkin joskus katsottava osaksi kyseistä liiketoimintaprosessia. Tässä tapauksessa, jos luodun lähtevän tiedoston toimittaminen määritetylle kohteelle epäonnistuu, liiketoimintaprosessin suorittaminen on peruttava. Jos haluat määrittää oikean ER-kohteen, valitse **Lopeta käsittely virheestä** -vaihtoehto.

Voit esimerkiksi määrittää toimittajan maksukäsittelyn siten, että ER-muoto **ISO20022-tilisiirto** suoritetaan maksutiedoston ja täydentävien asiakirjojen (esimerkiksi lähetekirje ja valvontaraportti) luomista varten. Jos maksu on tarkoitus katsoa onnistuneesti käsitellyksi vain, jos lähetekirje toimitetaan onnistuneesti sähköpostitse, sinun on valittava **Lopeta käsittely virheestä** -valintaruutu **CoveringLetter** -komponentin osalta asianmukaisessa tiedostokohteessa seuraavan kuvan mukaisesti. Tällöin maksun tila, joka valitaan käsittelyä varten vaihtuu tilasta **Ei mitään** tilaksi **Lähetetty** vain, kun Finance-esiintymässä määritetty sähköpostipalvelujen tarjoaja on hyväksynyt luodun lähetekirjeen toimitettavaksi.

[![Prosessikäsittelyn määrittäminen tiedostokohdevirheelle.](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Jos tyhjennät **Lopeta käsittely virheestä** -valintaruudun **CoveringLetter**-komponentin osalta kohteessa, maksu katsotaan onnistuneesti käsitellyksi, vaikka lähetekirjettä ei toimitettaisi onnistuneesti sähköpostin kautta. Maksun tila muuttuu tilasta **Ei mitään** tilaksi **Lähetetty**, vaikka lähetekirjettä ei voida lähettää johtuen esimerkiksi puuttuvasta tai virheellisestä vastaanottajan tai lähettäjän sähköpostiosoitteesta.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Tuloksen muuntaminen PDF-muotoon

Voit muuntaa PDF-muunnosasetuksella tuloksen Microsoft Office (Excel tai Word) -muodosta PDF-muotoon.

### <a name="make-pdf-conversion-available"></a>Ota PDF-muunnos käyttöön

Ota PDF-muunnosasetus käyttöön kulloisessakin Finance-esiintymässä avaamalla **Ominaisuuksien hallinta** -työtila ja ottamalla toiminto **Muunna sähköisen raportoinnin lähtevät asiakirjat Microsoft Office -muodoista PDF -muotoon** käyttöön.

[![Lähtevien asiakirjojen PDF-muunnostoiminnon käyttöönotto ominaisuuksien hallinnassa.](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Soveltuvuus

Financen versioissa **ennen 10.0.18 -versiota** PDF-muuntoasetus voidaan ottaa käyttöön vain käyttöön vain **Excel\\Tiedosto**-komponenteissa, joita käytetään tulostamiseen Office-muodossa (Excel tai Word). Kun tämä asetus on käytössä, Office-muodossa luotu tulos muunnetaan automaattisesti PDF-muotoon. **Version 10.0.18** ja sitä myöhempien versioiden osalta voit kuitenkin ottaa tämän vaihtoehdon käyttöön myös **Yhteiset\\Tiedosto**-tyypin komponenteille.

> [!NOTE]
> Huomaa varoitussanoma, joka tulee näyttöön, kun otat käyttöön **Yhteiset\\Tiedosto**-tyyppisen ER-komponentin PDF-muuntovaihtoehdon. Tämä sanoma kertoo, että suunnittelun aikana ei ole mahdollista varmistaa, että valittu tiedostokomponentti paljastaa sisällön PDF-muodossa tai PDF-muunnettavana sisältönä suorituksen aikana. Tämän vuoksi asetus on otettava käyttöön vain, jos olet varma, että valittu tiedostokomponentti on määritetty siten, että se paljastaa sisällön PDF-muodossa tai PDF-muunnettavassa muodossa suorituksen aikana.
> 
> Jos otat muotokomponentin PDF-muuntovaihtoehdon käyttöön ja jos tämä komponentti paljastaa sisältöä jossakin muussa kuin PDF-muodossa ja jos sen sisältöä ei voi muuntaa PDF-muotoon, ajon aikana tapahtuu poikkeus. Sanoma, jonka vastaanotat, ilmoittaa, että luotua sisältöä ei voi muuntaa PDF-muotoon.

### <a name="limitations"></a>Rajoitukset

PDF-muunnoksen asetus on käytettävissä vain pilvikäyttöönotoissa.

Tuloksena olevan PDF-tiedoston enimmäispituus on 300 sivua.

Financen **versiossa 10.0.9** tuetaan tällä hetkellä vain vaakasuuntaista asettelua Excel-tuloksesta luotavassa PDF-asiakirjassa. Financen **versiossa 10.0.10 (toukokuu 2020) ja sitä myöhemmissä versioissa** voidaan [määrittää sivun suunta](#SelectPdfPageOrientation) PDF-tiedostossa, joka tuotetaan Excelin tulosteesta samalla, kun ER-kohde määritetään.

Sellaisten tulosten muuntamisessa, jotka eivät sisällä upotettuja fontteja, käytetään vain Windows-käyttöjärjestelmän yleisiä järjestelmäfontteja.

### <a name="use-the-pdf-conversion-option"></a>PDF-muunnosasetuksen käyttö

Ota PDF-muunnos käyttöön tiedostokohteen osalta valitsemalla **Muunna PDF-muotoon** -valintaruutu.

[![PDF-muunnoksen käyttöönotto tiedostokohteen osalta.](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Sivun suunnan valitseminen PDF-muunnosta varten</a>

Jos luot Excel-muodossa ER-konfiguraation ja haluat muuntaa sen PDF-muotoon, voit nimenomaisesti määrittää PDF-tiedoston sivun suunnan. Kun valitset **Muunna PDF -muotoon** -valintaruudun ja otat PDF-muunnoksen käyttöön tiedostokohteelle, joka tuottaa tulostetiedoston Excel-muodossa, **Sivun suunta** -kenttä on käytettävissä **PDF-muunnosasetukset** -pikavälilehdessä. Valitse **Sivun suunta** -kentästä haluamasi suunta.

[![Sivun suunnan valitseminen PDF-muunnosta varten.](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

Jos haluat valita PDF-sivun suunnan, asenna Financen versio 10.0.10 tai uudempi. Financen **versiota 10.0.23 edeltävissä** versioissa tällä asetuksella on seuraavat sivun suuntavaihtoehdot:

- Pystytulostus
- Vaakatulostus

Valittua sivun suuntaa käytetään kaikissa Excel-muodossa luoduissa lähtevän asiakirjan sivuissa, jotka sitten muunnetaan PDF-muotoon.

**Versiossa 10.0.23 ja sitä uudemmissa versioissa** sivun suuntavaihtoehtojen luetteloa on laajennettu seuraavasti:

- Pystytulostus
- Vaakatulostus
- Laskentataulukkokohtainen

Kun valitset **Laskentataulukkokohtainen**-vaihtoehdon, kaikki luodun Excel-työkirjan laskentataulukot muunnetaan PDF-tiedostoiksi käyttämällä sivun suuntaa, joka on määritetty laskentataulukolle käytetyssä Excel-mallissa. Siten lopullisessa PDF-asiakirjassa voi olla pysty- ja vaakasivuja. 

Jos Word-muotoinen ER-määritys muunnetaan PDF-muotoon, PDF-tiedoston sivun suunta otetaan aina Word-asiakirjasta.

## <a name="output-unfolding"></a>Tulosteen avautuminen

Kun konfiguroit ER-muodon **Kansio**-osan kohteen, voit määrittää, miten komponentin tuloste toimitetaan konfiguroituun kohteeseen.

### <a name="make-output-unfolding-available"></a>Aseta tuotoksen avaaminen käytettäväksi

Voit ottaa vaihtoehdot käyttöön nykyisessä taloushallinnassa, kun avaat **ominaisuudenhallinnan** työtilan ja otat **ER-kohteiden määrittäminen ja kansioiden sisällön lähettäminen erillisinä tiedostoina** -ominaisuuden käyttöön.

### <a name="applicability"></a>Soveltuvuus

Vaihtoehdon muodoksi voidaan määrittää vain **Kansio**-tyypin muotokomponentit. Kun alat konfiguroida **Kansio**-komponenttia, **Yleinen**-pikavälilehti on käytettävissä **Sähköisen raportoinnin kohde** -sivulla. 

### <a name="use-the-output-unfolding-option"></a>Käytä tulosteen avaamisvaihtoehtoa

Valitse **Yleinen**-pikavälilehden **Lähetä kansio nimellä** -kentästä jokin seuraavista arvoista:

- **Zip-arkisto** – Toimita luotu tiedosto zip-tiedostona.
- **Erilliset tiedostot** – Toimita jokainen luodun zip-kansion tiedosto yksittäisenä tiedostona.

    > [!NOTE]
    > Kun valitset **Erilliset tiedostot**, muodostettu tulostus kerätään muistissa zip-muodossa. Sen vuoksi [tiedoston enimmäiskokorajaa](er-compress-outbound-files.md) käytetään zip-tuotoksen yhteydessä, kun todellinen tiedostokoko saattaa ylittää tämän rajan. Tämä arvo kannattaa valita, kun myös luodun tuotoksen koon odotetaan olevan liian suuri.

[![Kansion muotokomponentin kohteen konfiguroiminen.](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Rajoitukset

Jos määrität **Lähetä kansio muodossa** -kentän arvoksi **Erota tiedostot** **Kansio**-komponentille, joka sisältää muita sisäkkäisiä **Kansion** osia, asetusta ei käytetä uudelleen sisäkkäisiin **Kansio**-komponentteihin.

## <a name="security-considerations"></a>Tietojen suojaamisesta

ER-kohteissa on käytössä kahdenlaisia oikeuksia ja tehtäviä. Yhdellä tyypillä hallitaan käyttäjän yleistä mahdollisuutta ylläpitää yritykselle määritettyjä kohteita (eli se hallitsee **Sähköisen raportoinnin kohteet** -sivun käyttöoikeutta). Toisella hallitaan sovelluksen käyttäjän mahdollisuutta ohittaa suorituksen aikana ER-kehittäjän tai ER-toimintokonsultin määrittämiä kohdeasetuksia.

| Rooli (AOT-nimi)                     | Roolin nimi                                  | Velvollisuus (AOT-nimi)                     | Velvollisuuden nimi                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Sähköisen raportoinnin kehittäjä             | ERFormatDestinationConfigure        | Määritä sähköisen raportoinnin muodon kohde                |
| ERFunctionalConsultant              | Sähköisen raportoinnin toiminnallinen konsultti | ERFormatDestinationConfigure        | Määritä sähköisen raportoinnin muodon kohde                |
| PaymAccountsPayablePaymentsClerk    | Ostoreskontran maksuliikenneassistentti            | ERFormatDestinationRuntimeConfigure | Määritä sähköisen raportoinnin muodon kohde ajon aikana |
| PaymAccountsReceivablePaymentsClerk | Myyntireskontran maksuliikenneassistentti         | ERFormatDestinationRuntimeConfigure | Määritä sähköisen raportoinnin muodon kohde ajon aikana |

> [!NOTE]
> Edellisissä tehtävissä käytettiin kahta oikeutta. Näiden oikeuksien nimet vastaavat tehtävien nimiä: **ERFormatDestinationConfigure** ja **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Olen tuonut sähköisiä määrityksiä ja näen ne Sähköisen raportoinnin konfiguraatiot -sivulla Miksi ne eivät kuitenkaan ole näkyvissä Sähköisen raportoinnin kohteet -sivulla?

Varmista, että olet valinnut ensin **Uusi** ja sitten määrityksen **Viittaus**-kentässä. **Sähköisen raportoinnin kohteet** -sivulla ovat näkyvissä vain määritykset, joille on määritetty kohteet.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Onko olemassa jonkin tapa, jolla voi määrittää, mitä Microsoft Azure Storage -tiliä ja Azure Blob -säilöä käytetään?

Nro Käytössä on tiedostonhallintajärjestelmälle määritetty ja siinä käytettävä Microsoft Azure Blob -oletussäilö.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Minkä takia kohdeasetuksissa on tiedostokohde? Mitä tällä asetuksella tehdään?

**Tiedosto**-kohteen avulla hallitaan selaimen valintaikkunaa, kun ER-muoto suoritetaan vuorovaikutteisessa tilassa. Jos otat tämän kohteen käyttöön tai jos määrityksellä ei ole määritetty lainkaan sijaintia, tulostetiedoston luonnin jälkeen selaimessa avautuu avaamis- tai tallennusikkuna.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Saisinko esimerkin sellaiseen toimittajatiliin viittaavasta kaavasta, johon voin lähettää sähköpostia?

Kaava on ER-määrityskohtainen. Jos esimerkiksi käytät ISO 20022 tilisiirto -määritystä, voit hakea liitetyn toimittajatilin kaavalla **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** tai **model.Payments.Creditor.Identification.SourceID**.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Yhdessä muotomäärityksessäni on useita tiedostoja, jotka on ryhmitelty yhteen kansioon (esimerkiksi Kansio1 sisältää tiedostot Tiedosto1, Tiedosto2 ja Tiedosto3). Miten määritän kohteet siten, että Kansio1.zip-tiedostoa ei luoda lainkaan, Tiedosto1 lähetetään sähköpostitse ja Tiedosto2 lähetetään SharePointiin ja että voin avata tiedoston Tiedosto3 heti, kun määritys on suoritettu?

Muodon on ensin oltava käytettävissä ER-määrityksissä. Jos tämä edellytys täyttyy, avaa **Sähköisen raportoinnin kohde** -sivu ja luo uusi viittaus määritykseen. Tarvitset seuraavaksi neljä tiedostokohdetta, eli yhden kullekin tulosteosalle. Luo ensimmäinen tiedostokohde, anna sille nimi, kuten **Kansio**, ja sitten kansiota määrityksessä edustava tiedostonimi. Valitse sitten **Asetukset** ja varmista, että kaikki kohteet on poistettu käytöstä. Kansiota ei luoda tähän tiedostokohteeseen. Koska tiedostojen ja pääkansioiden välillä on hierarkkisia riippuvuuksia, tiedostot toimivat oletusarvoisesti samalla tavoin. Niitä ei toisin sanoen lähetetä mihinkään. Voit ohittaa tämän oletustoiminnan luomalla vielä kolme tiedostosijaintia eli yksi kullekin tiedostolle. Ota kunkin tiedoston kohdeasetuksissa käyttöön kohde, johon tiedosto on lähetettävä.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[Toiminnosta riippuvaisten ER-kohteiden määrittäminen](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
