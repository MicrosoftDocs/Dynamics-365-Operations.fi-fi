---
title: "Sähköisen raportoinnin kohteet"
description: "Voit määrittää kohteen jokaiselle sähköisen raportoinnin (ER) muotokokoonpanolle ja sen tuloskomponentille (kansio tai tiedosto). Käyttäjät, joille on myönnetty tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana. Tässä artikkelissa käsitellään ER-kohteiden hallintaa, tuettuja kohdetyyppejä ja suojausta."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Sähköisen raportoinnin kohteet

Voit määrittää kohteen jokaiselle sähköisen raportoinnin (ER) muotokokoonpanolle ja sen tuloskomponentille (kansio tai tiedosto). Käyttäjät, joille on myönnetty tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana. Tässä artikkelissa käsitellään ER-kohteiden hallintaa, tuettuja kohdetyyppejä ja suojausta.

Sähköisen raportoinnin (ER) muotomäärityksissä on yleensä vähintään yksi tulosteosa: tiedosto. Yleensä määrityksissä on useita eri tyyppisiä tiedostotulosteosia (kuten XML, TXT tai XLSX), jotka on ryhmitelty joko yhteen kansioon tai moneen kansioon. Voit määrittää ER-kohteen hallinnassa valmiiksi, mitä tapahtuu, kun kukin osa suoritetaan. Oletusarvon mukaan kun kokoonpano suoritetaan, näyttöön tulee valintaikkuna, jonka avulla käyttäjä tallentaa tai avata tiedostoa. Samaa toimintaa voi käyttää myös ER-määrityksiä tuotaessa, joten sitä varten ei tarvitse määrittää tiettyä kohdetta. Kun päätulosteosalle on luotu kohde, kyseisen kohde ohittaa oletustoiminnallisuuden ja kansio tai tiedosto lähetetään kohdeasetusten mukaisesti.

## <a name="availability-and-general-prerequisites"></a>Saatavuus ja yleiset edellytykset
ER kohteisiin-toiminto ei ole käytettävissä toiminnot 7.0 (helmikuu 2016)-version Microsoft Dynamics-365. Siksi sinun on asennettava Microsoft Dynamics-365 työvaiheiden (marraskuussa 2016 versio) voit käyttää kaikkia toimintoja, jotka on kuvattu tässä ohjeaiheessa. Vaihtoehtoisesti voit asentaa jokin seuraavista edellytyksistä. Huomaa kuitenkin, että nämä vaihtoehtoiset antaa enemmän rajoitettu ER-kohteen kokemus.

-   Microsoft Dynamics-365 toimintoja sovelluksen version 7.0.1 (toukokuussa 2016)
-   ER-kohteen hallinnan [sovelluksen hotfix-korjaus](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Voit määrittää kohteet vain tuoduissa ER-määrityksissä ja voit käyttää vain **Sähköisen raportoinnin konfiguraatiot** -sivulla olevia muotoja.

## <a name="overview"></a>Yleiskuvaus
ER-kohteen hallintatoiminnot ovat osoitteessa **organisaation hallinta**&gt;**sähköinen raportointi**. Voit ohittaa sieltä määrityksen oletustoiminnan. Tuotuja määrityksiä ei näytetä täällä, ennen kuin valitset **Uusi** ja valitset sitten **Viittaus**-kentässä määrityksen, jolle kohdeasetukset luodaan.

[![Määrityksen valitseminen viite-kenttään.](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Kun olet luonut viittauksen, voit luoda tiedoston kohteen kullekin kansiolle tai tiedostolle. 

[![Tiedoston kohteen luominen](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Huomautus:**Voit luoda yhden tiedostokohteen kullekin samanmuotoiselle, **Tiedostonimi**-kentässä valitulle tulosteosalle, kuten kansiolle tai tiedostolle. Voit ottaa käyttöön ja poistaa käytöstä yksittäisiä kohteita-tiedoston kohde on **kohteen asetukset** valintaikkuna. **Asetukset**-painikkeella voidaan hallita kaikki valitun tiedostokohteen kohteita. Voit hallita **Kohdeasetukset**-valintaikkunassa kutakin kohdetta erikseen valitsemalla sen kohdalla **käytössä**.

[![Kohteen asetukset](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Kohdetyypit
Erityyppisiä kohteita tuetaan. Voit poistaa kaikki tyypit käytöstä tai ottaa ne käyttöön samanaikaisesti. Voit tällä tavoin joko olla tekemättä mitään tai lähettää osan kaikkiin määritettyihin kohteisiin. Seuraavissa osioissa käsitellään tuettavia kohteita.

### <a name="email-destination"></a>Sähköpostikohde

Lähetä tulostetiedosto sähköpostitse valitsemalla **Käytössä**-asetukseksi **Kyllä**. Sen jälkeen, kun tämä asetus on käytössä, voit määrittää sähköpostin vastaanottajat ja muokata aihe ja tekstiosa sähköpostiviestin. Voit määrittää vakion tekstiä sähköpostiviestin aihe-ja elin tai ER-kaavojen avulla voit dynaamisesti luoda sähköposti tekstejä. ER, voit määrittää sähköpostiosoitteet kahdella tavalla. Samoin kuin Dynamics 365 toimintojen Tulosta hallinta-ominaisuus on valmis, se voidaan suorittaa kokoonpano. Vaihtoehtoisesti voit ratkaista käyttämällä suoraa viittausta ER kokoonpanon kaavan kautta sähköpostiosoite.

### <a name="email-address-types"></a>Sähköposti osoite tyypit

Kun valitset **Muokkaa** varten **,** tai **Cc** -kenttään **sähköpostiviesti** valintaikkuna tulee näyttöön. Voit sitten valita mitä sähköpostiosoitetta haluat käyttää.

[![Sähköpostin valintaikkuna](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Tulostuksenhallinta

Jos valitset **tulostuksenhallinnan sähköposti** tyyppi-kenttään voidaan syöttää kiinteä email osoitteet **,** kenttä. Sähköpostiosoitteet, jotka eivät ole korjattu käyttämään tiedoston kohteen sähköposti lähdetyyppi on valittava. Seuraavia arvoja tuetaan: **asiakkaan**, **toimittajan**, **prospektin**, **Contact**, **kilpailija**, **työntekijöiden**, **hakijan**, **mahdollisen toimittajan**, ja **ei-sallitut toimittajan**. Kun olet valinnut sähköposti-lähdetyyppi, Käytä-painiketta vieressä **lähdetili sähköposti** kenttä, jos haluat avata ** Reseptien suunnittelu ** lomakkeen. Tämän lomakkeen avulla voit liittää kaavan, joka vastaa valitun osapuolen tili sähköposti-kohde.

[![Määrittää tulostuksenhallinnan sähköposti](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Huomaa, että kaavat ovat ER-määrityskohtaisia. Kirjoita **Kaava**-kenttään asiakirjakohtainen viittaus asiakas- tai toimittajaosapuolen tyyppiin. Kirjoittamisen asemesta voit etsiä tietolähdesolmun, joka vastaa asiakkaan tai toimittajan tiliä, ja päivittää kaavan valitsemalla **Lisää tietolähde**. Jos käytössä on esimerkiksi ISO 20022 Tilisiirto -määritys, toimittajatiliä vastaava solmu on **$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Muussa tapauksessa voit tallentaa kaavan antamalla minkä tahansa merkkijonoarvon, kuten **DE-001**.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

- **Sähköposti** -valintaikkunassa kierrätys varastopaikan seuraava **lähdetili sähköposti** poistaa sähköpostitili lähde kaava-kenttään. Vaihtoehtoisesti Avaa muuttaa kaavaa, joka on tallennettu aikaisemmin Reseptien suunnittelu. Voit määrittää sähköpostiosoitteet, valitse **Muokkaa** Avaa **määrittää sähköpostiosoitteet** valintaikkuna.

[![Sähköposti-kohteen sähköpostiosoitteiden määrittämisen](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Määrityssähköposti

Käytä tätä sähköposti Jos kokoonpanon, jonka avulla solmu tietolähteiden, joka kuvaa sähköpostiosoite. Voit käyttää tietolähteitä ja funktiot reseptin suunnittelua saada oikein muotoiltu sähköpostiosoite.

[![Sähköposti osoite tietolähde email-kohteen määrittäminen](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Huomautu:** SMTP (Simple Mail Transfer Protocol) -palvelimen on oltava määritettynä ja käytettävissä. Voit määrittää SMTP-palvelimen Dynamics 365 toimintoja, osoitteessa **järjestelmän hallinta**&gt;**asennus**&gt;**sähköposti**&gt;**sähköpostin parametrien**.

### <a name="archive-destination"></a>Arkistokohde

Voit lähettää tällä asetuksella tulosteen joko Microsoft SharePoint -kansion tai Microsoftin Azuren tallennustilaan. Lähetä tuloste valitun asiakirjatyypin mukaan määritettyyn kohteeseen valitsemalla **Käytössä**-asetukseksi **Kyllä**. Valittavana on vain asiakirjatyyppejä, joiden ryhmäksi on valittu **Tiedosto**. Asiakirjatyyppien osoitteessa **organisaation hallinta**&gt;**tiedostojen hallinta**&gt;**asiakirjatyypit**. ER-kohteiden määritys on sama kuin tiedostonhallintajärjestelmän määritys.

[![Tyypit-sivulta asiakirjaan](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Sijainti määrittää, mihin tiedosto tallennetaan. Jälkeen **arkisto** määrityksen suorittamisen tulokset voidaan tallentaa projektin arkistona, kohde on käytössä. Voit tarkastella tuloksia kohteessa **organisaation hallinta**&gt;**sähköinen raportointi**&gt;**arkistoida sähköiseen raportointiin töitä**. **Huomautus:** työ arkisto-Dynamics 365 toimintoja, asiakirjatyypin voit valita **organisaation hallinta**&gt;**työtilojen**&gt;**sähköisen raportoinnin**&gt;**sähköinen raportointi parametrit**.

#### <a name="sharepoint"></a>SharePoint

Voit tallentaa tiedoston määritettyyn SharePoint-kansioon. Määritä oletuspalvelin, SharePoint, **organisaation hallinta**&gt;**tiedostojen hallinta**&gt;**Tiedostonhallintaparametrit**, **SharePoint** välilehti. Kun SharePoint-kansio on määritetty, voit valita kansion, johon ER tuloste tallennetaan asiakirjan tyyppiä. 

[![SharePoint-kansion valitseminen](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azuren tallennustila

Kun asiakirjatyypin sijainniksi on määritetty **Arkistointihakemisto**, voit tallentaa tiedoston Azuren tallennustilaan.

### <a name="file-destination"></a>Tiedostokohde

Jos määrität **käytössä**, **Kyllä**, Avaa- tai Tallenna-valintaikkuna tulee näyttöön, kun määritys on suoritettu.

### <a name="screen-destination"></a>Näytön kohteen

Jos määrität **käytössä**, **Kyllä**, tulosteen esikatselua luodaan. Voit tarkastella joitakin tiedostotyyppejä, kuten XML, TXT tai PDF, suoraan selainikkunassa. Muiden tiedostotyyppien, tällainen Microsoft Exceliin tai Wordiin, Microsoft Office Online-palvelua käytetään.

### <a name="power-bi-destination"></a>Power BI-kohde

Määritä **käytössä**, **Kyllä** ER-määrityksen avulla voit järjestää tietojen siirrosta että esiintymä Dynamics 365 toimintoja Microsoft Power BI palveluihin. Siirretyt tiedostot tallennetaan Microsoft SharePoint Server-esiintymässä on määritettävä tähän tarkoitukseen. Lisätietoja on ohjeaiheessa [antaa virtaa BI tietoja Dynamics 365-toimille sähköisen raportoinnin määritysten avulla](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Vihje:** voit ohittaa oletustoiminnan (eli määrityksen valintaikkunan) luomalla päätulostekohteelle kohdeviittauksen ja tiedostokohteen ja poistamalla sitten kaikki kohteet käytöstä.

## <a name="security-considerations"></a>Tietojen suojaamisesta
ER-kohteissa on käytössä kahdenlaisia oikeuksia ja tehtäviä. Yksi ohjaa kykyä ylläpitää yleistä kohteisiin, jotka on määritetty oikeushenkilö (eli se ohjaa **sähköinen raportointi kohteisiin** sivun). Toisella hallitaan sovelluksen käyttäjän mahdollisuutta ohittaa suorituksen aikana ER-kehittäjän tai ER-toimintokonsultin määrittämiä kohdeasetuksia.

| Rooli (AOT-nimi)                     | Roolin nimi                                  | Velvollisuus (AOT-nimi)                     | Velvollisuuden nimi                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Sähköisen raportoinnin kehittäjä             | ERFormatDestinationConfigure        | Määritä sähköisen raportoinnin muodon kohde                |
| ERFunctionalConsultant              | Sähköisen raportoinnin toiminnallinen konsultti | ERFormatDestinationConfigure        | Määritä sähköisen raportoinnin muodon kohde                |
| PaymAccountsPayablePaymentsClerk    | Ostoreskontran maksuliikenneassistentti            | ERFormatDestinationRuntimeConfigure | Määritä sähköisen raportoinnin muodon kohde ajon aikana |
| PaymAccountsReceivablePaymentsClerk | Myyntireskontran maksuliikenneassistentti         | ERFormatDestinationRuntimeConfigure | Määritä sähköisen raportoinnin muodon kohde ajon aikana |

**Huomautus:** Edellisissä tehtävissä käytettiin kahta oikeutta. Näiden oikeuksien nimet vastaavat tehtävien nimiä: **ERFormatDestinationConfigure** ja **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Olen tuonut sähköisiä määrityksiä ja näen ne Sähköisen raportoinnin konfiguraatiot -sivulla Mutta Miksi en näe niitä sähköisen raportoinnin kohteet-sivulla?

Varmista, että valitset **uusi** ja valitse sitten configuration- **viite** kenttä. **Sähköisen raportoinnin kohteet** -sivulla on näkyvissä on vain määritykset, joille on määritetty kohteet.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Onko millään tavalla voit määrittää, mitkä Azure-tallennustilan tili ja Azure Blob-etäsäilöpalvelun käytetään?

Nro Käytetään oletusarvon Azure Blob varastointia, joka on määritelty ja käytetty hallintajärjestelmä.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Mikä on tiedoston kohteen kohteen asetusten tarkoitus? Mitä tällä asetuksella tehdään?

**Tiedosto**-kohteen avulla hallitaan valintaikkunaa. Jos tämä kohde on otettu käyttöön tai jos kohde ei ole määritetty konfiguraatio, katso avointa tai Tallenna-valintaikkuna, kun tuotos-tiedosto on luotu.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Saisinko esimerkin sellaiseen toimittajatiliin viittaavasta kaavasta, johon voin lähettää sähköpostia?

Kaava on ER-määrityskohtainen. Jos esimerkiksi käytät ISO 20022 tilisiirto -määritystä, voit hakea liitetyn toimittajatilin kaavalla **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** tai **model.Payments.Creditor.Identification.SourceID**.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Yhdessä muotomäärityksessäni on useita tiedostoja, jotka on ryhmitelty yhteen kansioon (esimerkiksi Kansio1 sisältää tiedostot Tiedosto1, Tiedosto2 ja Tiedosto3). Miten määritän kohteet siten, että Kansio1.zip-tiedostoa ei luoda lainkaan, Tiedosto1 lähetetään sähköpostitse ja Tiedosto2 lähetetään SharePointiin ja että voin avata tiedoston Tiedosto3 heti, kun määritys on suoritettu?

Edellytys on muodon on oltava käytettävissä ER-kokoonpanoissa. Jos sinulla on muoto, avaa **Sähköisen raportoinnin kohde** -sivu ja luo uusi viittaus tähän määritykseen. Tarvitset seuraavaksi neljä tiedostokohdetta, eli yhden kullekin tulosteosalle. Luo ensimmäinen tiedostokohde, anna sille nimi, kuten **Kansio**, ja sitten kansiota määrityksessä edustava tiedostonimi. Valitse sitten **Asetukset** ja varmista, että kaikki kohteet on poistettu käytöstä. Kansiota ei luoda tähän tiedostokohteeseen. Koska tiedostojen ja pääkansioiden välillä on hierarkkisia riippuvuuksia, tiedostot toimivat oletusarvoisesti samalla tavoin. Niitä ei toisin sanoen lähetetä mihinkään. Voit ohittaa tämän oletustoiminnan luomalla vielä kolme tiedostosijaintia eli yksi kullekin tiedostolle. Ota kunkin tiedoston kohdeasetuksissa käyttöön kohde, johon tiedosto on lähetettävä.

# <a name="see-also"></a>Lisätietoja

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)


