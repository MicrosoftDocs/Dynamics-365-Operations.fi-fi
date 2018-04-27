---
title: "Sähköisen raportoinnin kohteet"
description: "Voit määrittää kohteen jokaiselle sähköisen raportoinnin (ER) muotokokoonpanolle ja sen tuloskomponentille (kansio tai tiedosto). Käyttäjät, joille on myönnetty tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana. Tässä artikkelissa käsitellään ER-kohteiden hallintaa, tuettuja kohdetyyppejä ja suojausta."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5c92c1ca3f46d80a58ca315f1f695f082d1929ca
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="electronic-reporting-destinations"></a>Sähköisen raportoinnin kohteet

[!INCLUDE [banner](../includes/banner.md)]

Voit määrittää kohteen jokaiselle sähköisen raportoinnin (ER) muotokokoonpanolle ja sen tuloskomponentille (kansio tai tiedosto). Käyttäjät, joille on myönnetty tarvittavat käyttöoikeudet, voivat myös muokata kohdeasetuksia suorituksen aikana. Tässä artikkelissa käsitellään ER-kohteiden hallintaa, tuettuja kohdetyyppejä ja suojausta.

Sähköisen raportoinnin (ER) muotomäärityksissä on yleensä vähintään yksi tulosteosa: tiedosto. Yleensä määrityksissä on useita eri tyyppisiä tiedostotulosteosia (kuten XML, TXT tai XLSX), jotka on ryhmitelty joko yhteen kansioon tai moneen kansioon. Voit määrittää ER-kohteen hallinnassa valmiiksi, mitä tapahtuu, kun kukin osa suoritetaan. Kun määritys suoritetaan, käyttäjälle näytetään valintaikkuna, jolla tiedoston voi tallentaa tai avata. Samaa toimintaa voi käyttää myös ER-määrityksiä tuotaessa, joten sitä varten ei tarvitse määrittää tiettyä kohdetta. Kun päätulosteosalle on luotu kohde, kyseisen kohde ohittaa oletustoiminnallisuuden ja kansio tai tiedosto lähetetään kohdeasetusten mukaisesti.

## <a name="availability-and-general-prerequisites"></a>Saatavuus ja yleiset edellytykset
ER-kohdetoiminto ei ole käytössä Microsoft Dynamics AX 7.0:ssa (helmikuu 2016). Sinun on asennettava Microsoft Dynamics 365 for Operationsin versio 1611 (marraskuu 2016), jotta voit käyttää kaikkia toimintoja, jotka on kuvattu tässä ohjeaiheessa. Vaihtoehtoisesti voit asentaa jonkin seuraavista edellytyksistä: Huomaa kuitenkin, että nämä vaihtoehdot tarjoavat rajoitetumman ER-käyttökokemuksen.

-   Microsoft Dynamics AX -sovellusversio 7.0.1 (toukokuu 2016)
-   ER-kohteen hallinnan [sovelluksen hotfix-korjaus](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Voit määrittää kohteet vain tuoduissa ER-määrityksissä ja voit käyttää vain **Sähköisen raportoinnin konfiguraatiot** -sivulla olevia muotoja.

## <a name="overview"></a>Yleiskuvaus
ER-kohteen hallintatoimintoon pääsee valitsemalla **Organisaation hallinta** &gt; **Sähköinen raportointi**. Voit ohittaa sieltä määrityksen oletustoiminnan. Tuotuja määrityksiä ei näytetä täällä, ennen kuin valitset **Uusi** ja valitset sitten **Viittaus**-kentässä määrityksen, jolle kohdeasetukset luodaan.

[![Määrityksen valitseminen viitekenttään](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Kun olet luonut viittauksen, voit luoda kullekin kansiolle tai tiedostolle tiedostokohteen. 

[![Tiedostokohteen luonti](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

> ![Huomautus] Voit luoda yhden tiedostokohteen kullekin samanmuotoiselle, **Tiedostonimi**-kentässä valitulle tulosteosalle, kuten kansiolle tai tiedostolle. Voit sitten ottaa tiedostokohteen yksittäiset kohteet käyttöön tai poistaa ne käytöstä **Kohdeasetukset**-valintaikkunassa. **Asetukset**-painikkeella voidaan hallita kaikki valitun tiedostokohteen kohteita. Voit hallita **Kohdeasetukset**-valintaikkunassa kutakin kohdetta erikseen valitsemalla sen kohdalla **käytössä**.

[![Kohdeasetukset-valintaikkuna](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Kohdetyypit
Erityyppisiä kohteita tuetaan. Voit poistaa kaikki tyypit käytöstä tai ottaa ne käyttöön samanaikaisesti. Voit tällä tavoin joko olla tekemättä mitään tai lähettää osan kaikkiin määritettyihin kohteisiin. Seuraavissa osioissa käsitellään tuettavia kohteita.

### <a name="email-destination"></a>Sähköpostikohde

Lähetä tulostetiedosto sähköpostitse valitsemalla **Käytössä**-asetukseksi **Kyllä**. Kun tämä asetus on otettu käyttöön, voit muokata sähköpostin aihetta ja määrittää sähköpostin vastaanottajat. Voit määrittää vakiotekstit sähköpostiviestin aiheelle ja perustekstille tai voit ER-kaavojen avulla dynaamisesti luoda sähköpostitekstejä. Voit määrittää sähköisen raportoinnin sähköpostiosoitteet kahdella tavalla. Määritys voidaan suorittaa samalla tavoin kuin Finance and Operationsin Tulostuksenhallinta-toiminto suorittaa sen. Vaihtoehtoisesti voit ratkaista sähköpostiosoitteen käyttämällä suoraa viittausta ER-kokoonpanoon kaavan kautta.

### <a name="email-address-types"></a>Sähköpostiosoitteen tyyppi

Kun valitset **Muokkaa** **Vastaanottaja**- tai **Kopio**-kentässä **Sähköpostin vastaanottaja** -valintaikkuna tulee näyttöön. Voit sitten valita minkä tyyppistä sähköpostiosoitetta haluat käyttää.

[![Sähköpostin vastaanottaja -valintaikkuna](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Tulostuksenhallinta

Jos valitset **Tulostuksenhallinnan sähköposti** -tyypin, voit syöttää kiinteät sähköpostiosoitteet **Vastaanottaja**-kenttään. Jos haluat käyttää muita kuin kiinteitä sähköpostiosoitteita, tiedostokohteen sähköpostin lähdetyyppi on valittava. Seuraavia arvoja tuetaan: **Asiakas**, **Toimittaja**, **Prospekti**, **Yhteyshenkilö**, **Kilpailija**, **Työntekijä**, **Hakija**, **Mahdollinen toimittaja** ja **Ei-sallittu toimittaja**. Kun olet valinnut sähköpostin lähdetyypin, käytä **Sähköpostin lähdetili** -kentän vieressä olevaa painiketta, jos haluat avata **Reseptien suunnittelu** -lomakkeen. Tämän lomakkeen avulla voit liittää kaavan, joka vastaa valitun osapuolen tilin sähköpostikohdetta.

[![Määritä Tulostuksenhallinta-sähköpostityyppi](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Huomaa, että kaavat ovat ER-määrityskohtaisia. Kirjoita **Kaava**-kenttään asiakirjakohtainen viittaus asiakas- tai toimittajaosapuolen tyyppiin. Kirjoittamisen asemesta voit etsiä tietolähdesolmun, joka vastaa asiakkaan tai toimittajan tiliä, ja päivittää kaavan valitsemalla **Lisää tietolähde**. Jos käytössä on esimerkiksi ISO 20022 Tilisiirto -määritys, toimittajatiliä vastaava solmu on **$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Muussa tapauksessa voit tallentaa kaavan antamalla minkä tahansa merkkijonoarvon, kuten **DE-001**.

[![Reseptien suunnittelu](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Napsauta **Sähköpostin vastaanottaja** -valintaikkunassa **Sähköpostin lähdetili** -kentän vieressä olevaa roskakorikuvaketta poistaaksesi sähköpostin lähdetilin kaavan pysyvästi. Vaihtoehtoisesti, avaa Reseptien suunnittelu muuttaaksesi aiemmin tallennettua kaavaa. Voit määrittää sähköpostiosoitteet valitsemalla **Muokkaa** avataksesi **Määritä sähköpostiosoitteet** -valintaikkunan.

[![Sähköpostikohteen sähköpostiosoitteiden määrittäminen](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Määrityssähköposti

Käytä tätä sähköpostityyppiä, jos käyttämässäsi määrityksessä tietolähteissä solmu, joka kuvaa sähköpostiosoitetta. Voit käyttää reseptien suunnittelun tietolähteitä ja funktioita saadaksesi oikein muotoillun sähköpostiosoitteen.

[![Sähköpostikohteen sähköpostin tietolähteen määrittäminen](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Huomautu:** SMTP (Simple Mail Transfer Protocol) -palvelimen on oltava määritettynä ja käytettävissä. Voit määrittää SMTP-palvelimen valitsemalla Finance and Operationsissa **Järjestelmänhallinta** &gt; **Asetukset** &gt; **Sähköposti** &gt; **Sähköpostiparametrit**.

### <a name="archive-destination"></a>Arkistokohde

Voit lähettää tällä asetuksella tulosteen joko Microsoft SharePoint -kansion tai Microsoftin Azuren tallennustilaan. Lähetä tuloste valitun asiakirjatyypin mukaan määritettyyn kohteeseen valitsemalla **Käytössä**-asetukseksi **Kyllä**. Valittavana on vain asiakirjatyyppejä, joiden ryhmäksi on valittu **Tiedosto**. Asiakirjatyypit määritetään valitsemalla **Organisaation hallinta** &gt; **Tiedoston hallinta** &gt; **Tiedostotyypit**. ER-kohteiden määritys on sama kuin tiedostonhallintajärjestelmän määritys.

[![Tiedostotyypit-sivu](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

Sijainti määrittää, mihin tiedosto tallennetaan. Kun **Arkisto**-kohde on otettu käyttöön, määrityksen suorittamisen tulokset voidaan tallentaa työarkistoon. Voit tarkastella tuloksia kohteessa **Organisaation hallinta** &gt; **Sähköinen raportointi** &gt; **Sähköisen raportoinnin arkistoidut työt**. **Huomautus:** Finance and Operationsin työarkiston tiedostotyypin voi valita kohdassa **Organisaation hallinta** &gt; **Työtilat** &gt; **Sähköinen raportointi** &gt; **Sähköisen raportoinnin parametrit**.

#### <a name="sharepoint"></a>SharePoint

Voit tallentaa tiedoston määritettyyn SharePoint-kansioon. SharePoint-oletuspalvelimen määritetään valitsemalla **Organisaation hallinto** &gt; **Tiedoston hallinta** &gt; **Tiedostonhallintaparametrit** **SharePoint**-välilehdessä. Kun SharePoint-kansio on määritetty, voit valita sen kansioksi, johon ER-tuloste tallennetaan kyseiselle tiedostotyypille. 

[![SharePoint-kansion valitseminen](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azuren tallennustila

Kun asiakirjatyypin sijainniksi on määritetty **Arkistointihakemisto**, voit tallentaa tiedoston Azuren tallennustilaan.

### <a name="file-destination"></a>Tiedostokohde

Jos valitset **Käytössä**-asetukseksi **Kyllä**, avaamis- tai tallennusikkuna avautuu, kun määritys on valmis.

### <a name="screen-destination"></a>Näyttökohde

Jos määrität **Käytössä**-kentän arvoksi **Kyllä**, tulosteen esikatselu luodaan. Voit tarkastella joitakin tiedostotyyppejä, kuten XML, TXT tai PDF, suoraan selainikkunassa. Muiden tiedostotyyppien, kuten Microsoft Excel tai Word, osalta käytetään Microsoft Office Online -palvelua.

### <a name="power-bi-destination"></a>Power BI -kohde

Kun määrität **Käytössä**-kentän arvoksi **Kyllä**, voit käyttää omaa sähköisen raportoinnin ER-konfiguraatiota tietojen siirron järjestämiseen omasta Finance and Operations -esiintymästä Microsoft Power BI -palveluihin. Siirretyt tiedostot tallennetaan Microsoft SharePoint Server -esiintymään, joka on konfiguroitu tähän tarkoitukseen. Lisätietoja on ohjeaiheessa [Finance and Operations -tietojen lähettäminen Power BI:hin sähköisen raportoinnin määritysten avulla](general-electronic-reporting-report-configuration-get-data-powerbi.md) **Vihje:** voit ohittaa oletustoiminnan (eli määrityksen valintaikkunan) luomalla päätulostekohteelle kohdeviittauksen ja tiedostokohteen ja poistamalla sitten kaikki kohteet käytöstä.

## <a name="security-considerations"></a>Tietojen suojaamisesta
ER-kohteissa on käytössä kahdenlaisia oikeuksia ja tehtäviä. Yhdellä tyypillä hallitaan mahdollisuutta ylläpitää yritykselle määritettyjä yleisiä kohteita (eli se hallitsee **Sähköisen raportoinnin kohteet** -sivun käyttöoikeutta). Toisella hallitaan sovelluksen käyttäjän mahdollisuutta ohittaa suorituksen aikana ER-kehittäjän tai ER-toimintokonsultin määrittämiä kohdeasetuksia.

| Rooli (AOT-nimi)                     | Roolin nimi                                  | Velvollisuus (AOT-nimi)                     | Velvollisuuden nimi                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Sähköisen raportoinnin kehittäjä             | ERFormatDestinationConfigure        | Määritä sähköisen raportoinnin muodon kohde                |
| ERFunctionalConsultant              | Sähköisen raportoinnin toiminnallinen konsultti | ERFormatDestinationConfigure        | Määritä sähköisen raportoinnin muodon kohde                |
| PaymAccountsPayablePaymentsClerk    | Ostoreskontran maksuliikenneassistentti            | ERFormatDestinationRuntimeConfigure | Määritä sähköisen raportoinnin muodon kohde ajon aikana |
| PaymAccountsReceivablePaymentsClerk | Myyntireskontran maksuliikenneassistentti         | ERFormatDestinationRuntimeConfigure | Määritä sähköisen raportoinnin muodon kohde ajon aikana |

> ![Huomautus] Edellisissä tehtävissä käytettiin kahta oikeutta. Näiden oikeuksien nimet vastaavat tehtävien nimiä: **ERFormatDestinationConfigure** ja **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Usein kysyttyjä kysymyksiä
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Olen tuonut sähköisiä määrityksiä ja näen ne Sähköisen raportoinnin konfiguraatiot -sivulla Miksi ne eivät kuitenkaan ole näkyvissä Sähköisen raportoinnin kohteet -sivulla?

Varmista, että olet valinnut ensin **Uusi** ja sitten määrityksen **Viittaus**-kentässä. **Sähköisen raportoinnin kohteet** -sivulla on näkyvissä on vain määritykset, joille on määritetty kohteet.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Onko olemassa jonkin tapa, jolla voi määrittää, mitä Azure Storage -tiliä ja Azure Blob -säilöä käytetään?

Nro Käytössä on tiedostonhallintajärjestelmälle määritetty ja siinä käytettävä Azure Blob -oletussäilö.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Minkä takia kohdeasetuksissa on tiedostokohde? Mitä tällä asetuksella tehdään?

**Tiedosto**-kohteen avulla hallitaan valintaikkunaa. Jos otat tämän kohteen käyttöön tai jos määrityksellä ei ole määritetty lainkaan sijaintia, tulostetiedoston luonnin jälkeen avautuu avaamis- tai tallennusikkuna.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Saisinko esimerkin sellaiseen toimittajatiliin viittaavasta kaavasta, johon voin lähettää sähköpostia?

Kaava on ER-määrityskohtainen. Jos esimerkiksi käytät ISO 20022 tilisiirto -määritystä, voit hakea liitetyn toimittajatilin kaavalla **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** tai **model.Payments.Creditor.Identification.SourceID**.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Yhdessä muotomäärityksessäni on useita tiedostoja, jotka on ryhmitelty yhteen kansioon (esimerkiksi Kansio1 sisältää tiedostot Tiedosto1, Tiedosto2 ja Tiedosto3). Miten määritän kohteet siten, että Kansio1.zip-tiedostoa ei luoda lainkaan, Tiedosto1 lähetetään sähköpostitse ja Tiedosto2 lähetetään SharePointiin ja että voin avata tiedoston Tiedosto3 heti, kun määritys on suoritettu?

Edellytyksenä on, että muotoa voi käyttää ER-määrityksissä. Jos sinulla on muoto, avaa **Sähköisen raportoinnin kohde** -sivu ja luo uusi viittaus tähän määritykseen. Tarvitset seuraavaksi neljä tiedostokohdetta, eli yhden kullekin tulosteosalle. Luo ensimmäinen tiedostokohde, anna sille nimi, kuten **Kansio**, ja sitten kansiota määrityksessä edustava tiedostonimi. Valitse sitten **Asetukset** ja varmista, että kaikki kohteet on poistettu käytöstä. Kansiota ei luoda tähän tiedostokohteeseen. Koska tiedostojen ja pääkansioiden välillä on hierarkkisia riippuvuuksia, tiedostot toimivat oletusarvoisesti samalla tavoin. Niitä ei toisin sanoen lähetetä mihinkään. Voit ohittaa tämän oletustoiminnan luomalla vielä kolme tiedostosijaintia eli yksi kullekin tiedostolle. Ota kunkin tiedoston kohdeasetuksissa käyttöön kohde, johon tiedosto on lähetettävä.

## <a name="see-also"></a>Lisätietoja

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)




