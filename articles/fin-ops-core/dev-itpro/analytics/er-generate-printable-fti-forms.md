---
title: Luo tulostettavia FTI-lomakkeita
description: Tässä ohjeaiheessa käsitellään, miten sähköisen raportoinnin (ER) runkoa käsitellään siten, että tulostettavan vapaatekstilaskun (FTI) lomakkeita luodaan Microsoft Office -asiakirjoina.
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 168cef1b5f5d48cb739b08fa395c1bcd62089494
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686723"
---
# <a name="generate-printable-fti-forms"></a>Tulostettavien FTI-lomakkeiden luominen

[!include[banner](../includes/banner.md)]

Sähköisen raportoinnin (ER) runko sallii sinun luoda tulostettavan vapaatekstilaskun (FTI) lomakkeita Microsoft Office -asiakirjoina. Tässä aiheessa on tietoja siitä, miten voit luoda omia konfiguraatioita sekä tietoja käytettävissä olevien kokoonpanomallien yksityiskohdista.

## <a name="overview"></a>Yleiskuvaus

Sen lisäksi, että voit olemassa olevan kyvyn avulla tulostaa FTI-lomakkeita käyttämällä Microsoft SQL Server Reporting Servicesiä (SSRS), voit nyt käyttää ER-runkoa. Voit hallita tulostettavia FTI-lomakkeita Microsoft Office Excelissä ja Wordissa. Voit myös muokata asettelua, tietojen kulkua ja muotoilua vaatimustesi mukaan muuttamatta koodia.

> [!NOTE]
> Jos haluat aloittaa yleiskuvalla tulostettavien FTI-lomakkeiden ratkaisun olemassa olevista ER-kokoonpanoista, voit siirtyä suoraan osioon **Lataa malli ER-konfiguraatioista tulostettavien FTI-lomakkeiden luomiseksi** myöhemmin tässä ohjeessa.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Luo muokatut kokoonpanot FTI-tulostettaville lomakkeille
Osana räätälöityä ratkaisua tulostettaviin FTI-lomakkeisiin sinun on luotava joukko ER-kokoonpanoja.

### <a name="configure-the-er-data-model"></a>ER-kohteiden tietomallien määrittäminen
Sovelluksesi on sisällytettävä ER-kohteiden tietomallin konfiguraatio, joka sisältää tietomallin, joka kuvaa asiakkaan laskutuskauden yrityksen liiketoiminta-aluetta. Vaatimuksena on, että tietomallin nimen täytyy olla **CustomersInvoicing**. Lisätietoja ER-tietomallien suunnittelusta on kohdassa [ER Toimialuekohtaisen tietomallin suunnitteleminen](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>ER-tietomallien kartoituksen määrittäminen
Sovelluksessasi on oltava ER-tietomallien kartoitus CustomersInvoicing-tietomallia varten. Mallin määritys voi olla joko ER-tietomallin konfiguraatio tai ER-tietomallin kartoituksen konfiguraatio. Joka tapauksessa mallikartoituksen juuren kuvaajan nimen on oltava **FreeTextInvoice**.

Kartoituksen tulee sisältää seuraavat tietolähteet:

- Tietolähteen tyyppi: **Taulukkotietueet**

    - Tämän tietolähteen nimen on oltava **CustInvoiceJour**.
    - Sen on viitattava CustInvoiceJour-sovellustaulukkoon.
    - Sitä käytetään ajon aikana siirryttäessä sovelluksesta ER-malliin, joka kartoittaa luettelon laskuista, jotka on valittu tulostettavaksi.

- tietolähteen tyyppi: **Esine**

    - Tämän tietolähteen nimen on oltava **PrintMgmtPrintSettingDetail**.
    - Sen on viitattava **PrintMgmtPrintSettingDetail** -sovellusluokkaan.
    - Sitä käytetään ajon aikana siirrettäessä sovelluksesta ER-mallin tarkat kartoitustiedot tulostuksen hallinnan asetuksista ER-muotoon, joka on käynnissä.

Sovelluksen integrointi ER - kehykseen löytyy **ERPrintMgmtReportFormatSubscriber** -luokasta (ER Application Suite -integraation malli) sovelluksen lähdekoodissa.

Lisätietoja ER-mallimääritysten suunnittelusta on kohdassa [ER-mallin yhdistämismääritysten määrittäminen ja tietolähteiden valinta niille](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>ER-muodon määrittäminen
Sovellusesiintymässäsi sinulla on oltava ER-muotokonfiguraatio, jota käytetään, kun luodaan FTI-lomakkeita. 

> [!NOTE]
> Tämä muotoiluasetus on luotava CustomersInvoicing-tietomallissa ja sen on käytettävä mallinkartoitusta, jolla on **FreeTextInvoice**-juuren kuvaaja.

Lisätietoja ER-mallien määrittämisestä on kohdassa [ER Muotomäärityksen luominen (marraskuu 2016)](tasks/er-format-configuration-2016-11.md). Lisätietoja OpenXML-muotoisia raportteja muodostavien ER-muotojen suunnittelusta on kohdassa [ER Konfiguraation suunnitteleminen luomaan OPENXML-muotoisia raportteja (marraskuu 2016)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Tulostuksenhallinnan määrittäminen
Voit luoda FTI-lomakkeita ER-kehyksen avulla käyttämällä ER-muotoja samalla tavalla kuin SSRS-raportteja. Voit liittää ER-mallin myyntisaamisten FTI:t , katso **Myyntisaamiset** \> **Asetukset** \> **Lomakkeet** \> **Lomakkeiden asetukset** \> **Yleinen** \> **Tulostuksen hallinta** \> **Vapaatekstilasku** \> **Alkuperäinen**. Voit yhdistää ER-muodon tiettyyn asiakkaaseen tai laskuun noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.
2. Valitse FTI, joka yhdistetään ER-muotoon, ja avaa **Tulostuksenhallinnan asetukset** -sivu.
3. Määritä soveltamisala valitsemalla asiakirjataso laskujen käsittelyä varten.
4. Valitse ER-muoto määrätyn asiakirjatason mukaan

![Tulostuksenhallinnan asetukset](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Vain ER-muodot, jotka käyttävät **FreeTextInvoice**-juuren kuvaajaa **CustomersInvoicing** -tietomallia näkyvät **Raportin muodon haku** -kentässä valitulle muodolle.

## <a name="generate-fti-forms"></a>Luo FTI-lomakkeet
FTI-lomakkeet luodaan käyttämällä ER-muotoja samaan tapaan kuin SSRS-raportit muodostetaan.

Luodaksesi FTI-lomakkeita, voit valita laskut joko alueen tai valinnan mukaan. 

![Laskuvalinta](media/FTIbyGER-InvoiceSelection.png)

![Laskun esikatselu](media/FTIbyGER-InvoiceExcelPreview.png)

Kun käytät ER-muotoja tulostamalla FTI-lomakkeita tällä tavalla, käytetään oletusarvoisia ER-tiedostojen kohteita. Et voi muuttaa kohdetta. Lisätietoja ER-muotojen ER-kohteiden määrittämisestä on kohdassa [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md).

Voit myös luoda FTI-lomakkeita, kun lähetät FTI:n, laittamalla valinnan **Tulosta lasku** päälle ja laittamalla **Käytä tulostuksen hallintakohteet** pois päältä.

> [!NOTE]
> Kun käytät ER-muotoja tulostamalla FTI-lomakkeita tällä tavalla, käytetään oletusarvoisia ER-tiedostojen kohteita. Voit muuttaa oletuskohteen ajon aikana, jos kohde on jo määritetty. Muuttaaksesi kohdetta sinulla on oltava seuraava suojauksen etuoikeus:
>
> - **Nimi:** ERFormatDestinationRuntimeMaintain
> - **Otsikko:** Ylläpidä sähköisen raportoinnin muodon kohdetta ajon aikana

![Sähköisen raportoinnin kohde](media/FTIbyGER-ERFileDestinationSetting.png)

![Sähköisen raportoinnin muodon kohde](media/FTIbyGER-ERFileDestinationUsage.png)

ER-kehys tukee tällä hetkellä seuraavia kohteita tuotetuille asiakirjoille:

- **Ladattu tiedosto** – Luodut lomakkeet ovat käytettävissä myös kuin ladattavat tiedostot tallennetaan selaimella.
- **Näyttö** – Microsoft 365 Exceliä käytetään FTI-lomakkeiden esikatseluun Excel-muodossa.
- **SharePoint-kansio** – Luodut lomakkeet tallennetaan asiakirjojen hallintajärjestelmän asetusten perusteella.
- **Sovellusarkisto** – Luodut lomakkeet tallennetaan liitteinä suorituslokin tietueina Microsoft Azure -varastoon.
- **Sähköposti** – Luodut lomakkeet lähetetään sähköpostiliitteinä.

> [!NOTE]
> Et voi lähettää FTI-lomakkeita, jotka on luotu suoraan tulostimeen, koska Dynamics-tulostusreititysagenttia käyttävää suoraa tulostusta ei tällä hetkellä tueta.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Lataa esimerkki ER-kokoonpanoista tulostettavien FTI-lomakkeiden luomiseksi
Voit ladata esimerkkejä ER-kokoonpanoista käytettäväksi mallina FTI-ratkaisussasi. Konfiguraatiot tallennetaan jaettujen käyttöomaisuuksien kirjastossa Microsoft Dynamics Lifecycle Services:ssä (LCS). Konfiguraatioihin sisältyy:

- **Asiakaslaskutusmalli** Konfiguraatio sisältää määritettävän tietomallin ja mallin määrityksen.
- **Asiakkaan FTI-raportti (GER)** konfiguraatio sisältää esimerkkimallin.

> [!NOTE]
> Nämä kokoonpanot on luotu näytteiksi selventämään mahdollisia skenaarioita. Näiden kokoonpanojen tulevaisuus riippuu tämän arvioinnin tuloksista ja vastaanotetusta palautteesta.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Ominaisuuksia, jotka ovat käytössä ER-esimerkkimuodossa
ER-formaatin näytteessä Excel-tiedostoa käytetään mallina FTI-lomakkeiden luomiseen.

![Muodon suunnittelija](media/FTIbyGER-ERFormat.png)

Tällä hetkellä tämä ER-muoto tukee seuraavia ominaisuuksia luoda FTI-lomakkeita:

- FTI-lomakkeet on muodostettu sekä alkuperäisiä kirjattuja laskuja, että alkuperäisiä laskuja varten, joita ei ole vielä kirjattu. Korjattuja laskujen ja hyvityslaskuja ei tueta.
- FTI-lomakkee on luotu laskun kielellä. Luotujen lomakkeiden arvojen ja päivämäärien muoto perustuu käyttäjän asiakkaan paikallisverkon asetuksiin.
- Luodut laskut näyttävät tietojen virheilmoituksia, jos käsiteltävissä laskuissa ei ole rivejä.
- Luodut laskutusotsikot perustuvat paperimuotoon, joka on valittu FTI-lomakkeelle **Myyntisaamiset**-sivulle. Yrityksen tiedot näkyvät luodun laskun lomakkeen otsikossa vain, jos paperimuoto on tyhjä.
- Luodut laskulomakkeet näyttävät yritykselle ja asiakkaalle verovapaita numeroita, kun FTI-lomakkeelle on valittu oikea vaihtoehto **Myyntisaamisten parametrit** -sivulle.
- Luotujen laskujen rivit ja laskun kokonaissummat näyttävät oletuslaskun rahalliset tiedot laskun rekisteröintivaluutassa.
- luodun laskun kokonaismäärän osa voi näyttää rahallisia tietoja eurovaluutasta ja laskujen rekisteröintivaluutasta, kun **Tulosta summa euroina** -vaihtoehto on otettu käyttöön **Myyntisaamisten parametrit** -sivulla.
- Luodut laskulomakkeet näyttävät kaikki saatavilla olevat prosessilaskuilmoitukset **Myyntisaamisten parametrit** -sivulla. Huomautukset sisältyvät sekä koko laskuun että jokaisen laskun riville.
- Luodut laskulomakkeet sisältävät asiakkaan FTI-lomakkeen ja laskutuskielet, kun ne on määritetty AR-lomakkeiden luetteloon.
- Tulostusasetusten mukaan tuotetuissa laskuissa on mukautettu alatunnistekirja, kun se on määritetty laskutuskielen, ER-muodon ja FTI-asiakirjan soveltamisalueelle.
- Luotujen laskujen lomakkeiden kokonaissumma sisältää käytettävissä olevat kassa-alennustiedot.
- Luotujen laskujen lomakkeiden maksutietoryhmä sisältää mahdolliset käytettävissä olevat maksuaikataulun yksityiskohdat.
- Luotujen laskujen lomakkeiden merkintäosuus sisältää kaikki tehdyt maksutapahtumat.
- Luodut laskulomakkeet sisältävät myyntiverotiedot **Myyntimääritelmä**-asetuksen **Myyntisaamisten parametrit** -sivulla. Tämä osio voi näyttää verotiedot joko vain laskun rekisteröintivaluutassa tai laskurekisteröintivaluutassa ja yrityksen kirjanpitoarvossa samanaikaisesti.
- Luodut laskulomakkeet näyttävät suoraveloitusilmoituksen yksityiskohtia. Esimerkiksi he osoittavat, milloin laskuille on valittu maksutapa, jolla on pakollinen suoraveloitusvaltuutuksen tunnus, kun käsittelylasku on rekisteröity eurovaluutalla ja kun laskuille on määritetty suoraveloitusvaltuutuksen tunnusnumero.
- Luodut laskut näyttävät kaikki ennakkomaksutiedot, jotka ovat saatavilla lähetetyille laskuille.
- Luodut laskulomakkeet voidaan lähettää sähköpostiviestin liitteenä laskuasiakkaalle. Asianmukaisen ER-tiedoston määränpää on määritettävä käytettävän ER-muotoon.

### <a name="countryregion-specific-features"></a>Maa-/aluekohtaiset ominaisuudet 
ER-muotoon on sisällytetty seuraavat maa- tai aluekohtaiset ominaisuudet, jotka osoittavat, kuinka erityisiä vaatimuksia voidaan käsitellä ER-kokoonpanoissa.

#### <a name="norway"></a>Norja
Yritysrekisterin termi asetetaan luodun laskusivun otsikkoon, kun lasku käsitellään oikeussubjektille, joka on konfiguroitu seuraavalla tavalla:

- Norjan maa/alue-konteksti käytössä.
- **Tulosta Foretaksregisteret** -parameteri on aktiivinen myyntidokumenteissa.

#### <a name="spain"></a>Espanja
**Kassaperusteisen kirjanpitomenetelmän erityisjärjestelmä** -termi asetetaan luodun laskusivun otsikkoon, kun lasku käsitellään oikeussubjektille, joka on määritetty seuraavasti:

- Espanjan maa/alue-konteksti käytössä.
- Kassaperusteisen kirjanpitojärjestelmän erityisjärjestelmä on otettu käyttöön laskujen käsittelypäivänä.

Kun käytettävissä on kassa-alennuksen yksityiskohdat, kuten kassa-alennusmäärä ja laskutilin nettomäärä, ne esitetään laskutetun lomakkeen laskun kokonaissummassa, kun se on käsitelty oikeussubjektille, joka on määritetty seuraavasti:

- Espanjan maa/alue-konteksti käytössä.
- **Laskuun lasketaan käteisalennus** on päällä laskuvaihtoehdossa (**Yleiset pääkirjaparametrit** \> **Myyntivero**).

#### <a name="italy"></a>Italia
Tavaroiden alennusluku sisältyy laskutetun laskun laskutuslinjoihin, kun sitä käsitellään oikeussubjektille, joka on määritetty käyttäen maa- tai aluekontekstia Italiassa.

#### <a name="finland"></a>Suomi
Luotujen laskujen lomakkeen lisäksi Giron rahansiirtolomakkeita voidaan tuottaa seuraavasti:

- Sellaiselle oikeushenkilölle, joka käyttää maata/aluekonttoria Suomelle ja jolla on vähintään yksi pankkitili, joka on merkitty nimellä **Giro-tili** ja **Pankkikoodi**. 
- Laskusta, joka on merkitty vaaditulla tavalla **suomalainen** liittyvä maksuliike.

![Tilisiirtolomake](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> Esimerkki ER-muodosta on konfiguroitu valinnaisesti generoimaan Giron rahansiirtoliput erillisessä laskentataulukossa.

> [!NOTE]
> Sinun on ensin asennettava fontti, jota käytetään viivakoodin generoimiseen paikallisessa koneessa, jossa esitelty Excel-muodossa luotu laskulomake.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>Määritä sähköpostien kohteet ER-formaatin avulla
Käytä seuraavia elementtejä ER-muotoa sähköpostiosoitteiden määrittämiseen:

- Asiakkaan yhteyshenkilön sähköpostiosoitetta voi käyttää seuraavan ER-lausekkeen kautta: **model.InvoiceBase.Contact.ElectronicMail**.
- Sähköpostiaiheen tekstiä voi käyttää seuraavan ER-lausekkeen kautta: **Emailing.TxtToUse.Subject**.
- Sähköpostielimen tekstiä voi käyttää seuraavan ER-lausekkeen kautta: **Emailing.TxtToUse.Body**.

![Kohdeasetukset](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Sähköpostin aiheen ja kehon oletusteksti on määritetty ER-mallinäytteessä. Kieli määräytyy lomakkeen etiketeistä. Tätä oletustekstiä käytetään sähköpostiviesteissä, jos muokattua organisaation sähköpostimallia, jolla on ennalta määritetty **ERFTITMP**-tunnus, ei ole lisätty..

> [!NOTE]
> **ERFTITMP** sähköpostimallin tunnus on määritetty ER-mallinäytteessä. Sitä voidaan muuttaa tarpeen mukaan uudessa ER-muodossa, joka on luotu tästä otosmuodosta.

Jos organisaation sähköpostimalli on ennalta määritetty **ERFTITMP** ID-tunnus on lisätty oikeushenkilölle, jolle käsittelyt laskut on, sähköpostiviestin mallia ja kehon tekstiä käytetään sähköpostin luomiseen. 

![Organisaation sähköpostimallit](media/FTIbyGER-EmailTemplate.png)

![Lataa sähköpostimalli](media/FTIbyGER-EmailTemplateBody.png)

**Emailing.TxtToUse.Subject**-näytteen ER-muotoinen ER-lauseke on määritetty korvaamaan paikkamerkin %1 mahdolliset esiintymät käsittelylaskun tunnuksella.

**Emailing.TxtToUse.Body** näyteformaatin lauseke on määritetty paikanvaraajille seuraaville korvauksille:

- %1 korvataan asiakkaan yhteyshenkilön nimellä.
- %2 korvataan yrityksen nimellä.
- %3 korvataan asiakkaan nimellä.
- %4 korvataan yrityksen yhteyshenkilön nimellä.
- %5 korvataan yrityksen yhteyshenkilön tittelillä.
- %6 korvataan yrityksen yhteyshenkilön sähköpostiosoitteella.

![Sähköposti](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Lisäresurssit
[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
