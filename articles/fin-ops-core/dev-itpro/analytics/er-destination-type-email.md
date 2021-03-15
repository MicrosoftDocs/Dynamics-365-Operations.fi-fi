---
title: Sähköpostin ER-kohteen tyyppi
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muodon KANSIO- tai TIEDOSTO-osalla määritetään sähköpostikohde.
author: NickSelin
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e2e0da1c724269e0956be2f402b34ff376ed1990
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094101"
---
# <a name="email-er-destination-type"></a>Sähköpostin ER-kohteen tyyppi

[!include [banner](../includes/banner.md)]

Kun sähköisen raportoinnin (ER) muoto suoritetaan, voidaan luoda yksi tai useita lähteviä asiakirjoja. **Kansi**- tai **Tiedosto**-muotokomponentteja käytetään ER-muodoissa lähtevien tiedostojen rakenteen määrittämiseen. Voit määrittää sähköpostikohteen näille tyypeille lähettääksesi lähteviä dokumentteja sähköpostin liitteinä.

Voit määrittää sähköpostikohteen kullekin ER-muodon **Kansio**- tai **Tiedosto**-komponentille. Tällöin **kukin lähtevä asiakirja lähetetään sähköpostitse yksitellen**. Luotu asiakirja toimitetaan sähköpostiviestin liitteenä tämän kohdeasetuksen perusteella. 

> [!NOTE]
> Jos asiakirjaa ei luoda, koska **Käytössä**-lauseke liittyvälle **Tiedosto**-komponentille on määritetty palauttamaan **Epätosi** totuusarvo, sähköpostia ei lähetetä, vaikka sähköpostikohde olisi määritetty ja käytössä komponentille.

Voit myös [ryhmitellä](#grouping) useita **Kansion**- tai **Tiedosto**-komponentteja yhteen ja määrittää sitten sähköposti kohteen kaikille ryhmän sisältämille komponenteille. Tässä tapauksessa kaikki ryhmään kuuluvien komponenttien luomat lähtevät tiedostot **lähetetään yhden sähköposti iestin useina liitteinä**. Kukin luotu asiakirja toimitetaan yksittäisen sähköpostiviestin liitteenä tämän kohdeasetuksen perusteella.

> [!NOTE]
> Jos vähintään yhden asiakirjan on luonut komponenttiryhmässä **Tiedosto**-komponentti, sähköposti lähetetään. Jos ryhmitellyt komponentit eivät luo asiakirjaa, koska **Käytössä**-lauseke kullekin **Tiedosto**-komponentille on määritetty palauttamaan **Epätosi** totuusarvo, sähköpostia ei lähetetä, vaikka sähköpostikohde olisi määritetty ja käytössä kyseiselle komponenttiryhmälle.
>
> **Sähköposti** on ainoa kohde, joka voidaan määrittää komponenttiryhmälle. Jos haluat toimittaa ryhmän sähköpostikohdeasetuksen perusteella lähetettävän asiakirjan, lisää kohdetietue, valitse haluamasi komponentti, ja määritä sitten toinen kohde tälle tietueelle.

Useita komponenttiryhmiä voidaan määrittää yksittäiselle ER-muodon määritykselle. Tällä tavoin voit määrittää sähköpostikohteen jokaiselle komponenttiryhmälle ja sähköpostikohteen jokaiselle komponentille.

## <a name="configure-an-email-destination"></a>Sähköpostikohteen määrittäminen

Jos haluat lähettää tulostetiedoston tai useita tulostetiedostoja sähköpostitse, valitse **Sähköisen raportoinnin kohde** -sivun **Tiedostokohde**-pikavälilehdessä komponentti tai komponenttien ryhmä ruudukosta ja valitse sitten **Asetukset**. Aseta ilmestyvän **Kohdeasetukset**-dialogi-ikkunan **Sähköposti**-välilehdessä **Käytössä**-asetukseksi **Kyllä**. Voit tämän jälkeen määrittää sähköpostin vastaanottajat sekä muokata sähköpostin aihetta ja tekstiä. Voit joko määrittää vakiotekstin sähköpostiviestin aiheelle ja tekstille tai käyttää ER-[kaavoja](er-formula-language.md) luodaksesi sähköpostitekstejä dynaamisesti.

Voit määrittää sähköisen raportoinnin sähköpostiosoitteet kahdella tavalla. Määritys voidaan suorittaa loppuun samalla tavalla kuin Tulostuksenhallinta-ominaisuus suorittaa sen loppuun, tai voit ratkaista sähköpostiosoitteen käyttämällä suoraa viitettä ER-määritykseen kaavan kautta.

[![Sähköpostikohteen Käytössä-asetuksen arvon määrittäminen arvoksi Kyllä](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Sähköpostiosoitteen tyyppi

Jos valitset **Muokkaa** **Vastaanottaja**- tai **Kopio**-kentän vieressä **Kohdeasetukset**-dialogi-ikkunassa, **Sähköposti vastaanottajalle**  -dialogi-ikkuna näytetään. Valitse **Lisää** ja valitse sitten, minkä tyyppistä sähköpostiosoitetta käytetään. Tällä hetkellä tuetaan kahta tyyppiä: **Tulostuksenhallintasähköposti** ja **Määrityssähköposti**.

[![Sähköpostiosoitteen tyypin valitseminen](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Tulostuksenhallinnan sähköposti

Jos valitse sähköpostiosoitteen tyypiksi **Tulostuksenhallintasähköposti**, voit syöttää kiinteitä sähköpostiosoitteita **Sähköposti vastaanottajalle** -dialogi-ikkunaan määrittämällä seuraavat kentät:

- Valitse **Sähköpostin lähde**-kentässä **Ei mikään**.
- Syötä **Lisäsähköpostiosoitteet eroteltuina merkillä ";"** -kenttään kiinteät sähköpostiosoitteet.

Vaihtoehtoisesti voit hankkia sähköpostiosoitteita sen osapuolen yhteystiedoista, jolle luot lähtevän asiakirjan. Jos haluat käyttää muita kuin kiinteitä sähköpostiosoitteita, valitse **Sähköpostin lähde** -kentässä tiedoston kohteen [rooli](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles). Seuraavia rooleja tuetaan:

- Asiakas
- Toimittaja
- Prospekti
- Kontakti
- Kilpailija
- Työntekijä
- Hakija
- Mahdollinen toimittaja
- Ei-sallittu toimittaja

Jos esimerkiksi haluat määrittää sähköpostikohteen toimittajamaksun käsittelyssä käytettävää ER-muotoa varten, valitse **Toimittaja**-rooli.

Kun olet valinnut haluamasi roolin, valitse **Sido**-painike (ketjusymboli) **Sähköpostin lähdetili** -kentän vierestä, jolloin [Kaavasuunnittelija](general-electronic-reporting-formula-designer.md)-sivu aukeaa. Tätä sivua voidaan sen jälkeen käyttää määrittämään kaava, joka palauttaa käsiteltävästä asiakirjasta sähköpostikohteeseen suorituksen aikana sen osapuolen tilinumeron, jolla on määritetty rooli.

> [!NOTE]
> Kaavat ovat ER-määrityskohtaisia.

Syötä **Kaavasuunnittelija**-sivun **Kaava**-kenttään asiakirjakohtainen viite tuettuun rooliin. Sen sijaan, että kirjoittaisit viitteen **Tietolähde**-ruutuun, hae ja valitse tietolähdesolmu, joka edustaa määritetyn roolin tiliä, ja valitse **Lisää tietolähde** kaavan päivittämiseksi. Jos esimerkiksi halutaan määrittää sähköpostikohde määritykselle **ISO 20022 Credit Transfer**, jota käytetään toimittajamaksujen käsittelyyn, toimittajatiliä edustava solmu on `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Sähköpostilähdetilin määritys](./media/er_destinations-emaildefineaddresssource.gif)

Jos määritetyn roolin tilinumerot ovat yksilöllisiä koko Microsoft Dynamics 365 Finance -esiintymässä, **Sähköpostilähteen yritys** -kenttä dialogi-ikuunassa **Sähköposti vastaanottajalle** voi jäädä tyhjäksi.

Voit myös joutua tilanteeseen, jossa [Yleisen osoitekirjan](../../fin-ops/organization-administration/overview-global-address-book.md) eri osapuolet on rekisteröity eri yrityksiin ([oikeushenkilöihin](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) siten, että ne kaikki käyttävät samaa tilinumeroa määritetyn roolin täyttämiseen. Tässä tapauksessa määritetyn roolin tilinumerot eivät ole yksilöiviä koko Finance-esiintymässä. Tämän vuoksi et voi eksplisiittisesti valita osapuolta vain tilinumeron perusteella. On myös määritettävä yritys, jolle osapuoli on rekisteröity määritetyn roolin täyttämiseksi. Valitse **Sido** -painike (ketjusymboli) **Sähköpostin yritys** -kentän vierestä **Sähköposti vastaanottajalle** -dialogi-ikkunassa avataksesi [Kaavasuunnittelija](general-electronic-reporting-formula-designer.md)-sivun. Voit sitten käyttää tätä sivua määrittääksesi kaavan, joka palauttaa suorituksen aikana sen yrityksen koodin, josta halutun lähteen on löydyttävä.

> [!TIP]
> Jos sinun on käytettävä yrityskoodia ER-muodon suorittamiseen, mutta ER-muoto ei anna mitään tietolähdettä, josta yrityskoodi voidaan hankkia, määritä `GetCurrentCompany()`-kaava käyttämällä sisäistä [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md) ER-funktiota.

> [!NOTE]
> Kaavat ovat ER-määrityskohtaisia.

Suorituksen aika käytettävien sähköpostiosoitteiden tyyppi voidaan määrittää valitsemalla **Sähköposti vastaanottajalle** -dialogi-ikkunassa **Muokkaa** **Vastaanottaja**-kentän vieressä **Kohdenna sähköpostiosoite** -pudotusvalikkodialogiruudun avaamiseksi. Määritä sitten seuraavat kentät:

- Valitse **Tarkoitus**-kentässä halutut tarkoitukset. Ohjelma käyttää vain valittujen tarkoitusten sähköpostiosoitteita löytyneen osapuolen yhteyshenkilöistä.
- Määritä **Ensisijainen yhteyshenkilö** -asetuksen arvoksi **Kyllä**, jos haluat käyttää löydetylle osapuolelle määritettyä sähköpostiosoitetta ensisijaisena sähköpostiosoitteena.

> [!NOTE]
> Jos tarkoitukset on valittu **Tarkoitus**-kentässä ja **Ensisijainen yhteyshenkilö** -asetukseksi on samanaikaisesti määritetty **Kyllä**, kaikkia vähintään yhden määritetyn ehdon täyttäviä sähköpostiviestejä käytetään suorituksen aikana.

### <a name="configuration-email"></a>Määrityssähköposti

Valitse sähköpostiosoitteen tyypiksi **Määrityssähköposti**, jos käytössä olevissa määrityksissä on tietolähteissä oleva solmu, joka palauttaa joko yhden sähköpostiosoitteen tai useita sähköpostisosoitteita, jotka erotetaan toisistaan puolipisteillä (;). Voit käyttää kaavasuunnittelijassa [tietolähteitä](general-electronic-reporting.md#FormatComponentOutbound) ja [funktioita](er-formula-language.md#functions) saadaksesi oikein muotoillun sähköpostiosoitteen tai sähköpostiosoitteita, jotka on eroteltu puolipisteillä. Jos esimerkiksi käytät määritystä **ISO 20022 Credit Transfer**, toimittajan ensisijaista sähköpostiosoitetta toimittajan yhteystiedossa edustava solmu, johon saatekirje tulisi lähettää, on `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Sähköpostiosoitteen lähteen määritys](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Ryhmämuodon osat

Jos haluat määritellä komponenttien muotoja ryhmänä, valitse **Sähköisen raportoinnin kohde** -sivun **Tiedostokohde**-pikavälilehdellä komponentit ruudukosta ja valitse sitten **Ryhmittele**.

**Sähköposti** on ainoa aiemmin määritetty kohde, joka on edelleen käytettävissä valituissa komponenteissa. Muita aiemmin määritettyjä kohteita ei ole käytettävissä, koska niitä ei tueta komponenttiryhmälle. Sinulle ilmoitetaan näistä muutoksista tarpeen mukaan.

Aiemmin lisäämääsi tietuetta pidetään luotavan ryhmän otsikkona. Tämä otsikkotietue sisältää ryhmän sähköpostikohteen asetukset. Muut tietueet ovat ryhmän jäseniä, jotka käyttävät ryhmän otsikkotietueen sähköpostin kohdeasetuksia.

Voit purkaa muotokomponenttien ryhmittelyn valitsemalla **Tiedostokohde**-pikavälilehdellä tietueen, joka kuuluu ryhmään, ja valitsemalla sitten **Pura ryhmittely**.

- Jos valitset otsikkotietueen, koko ryhmä puretaan.
- Jos valitset jäsentietueen ja se on ryhmän viimeinen jäsentietue, koko ryhmä puretaan.
- Jos valitset jäsentietueen, joka ei ole ryhmän viimeinen jäsentietue, kyseinen tietue jätetään pois nykyisestä ryhmästä.

Seuraavassa kuvassa näkyy sellaisen ER-muodon rakenne, joka on määritetty tuottamaan zip-muotoinen lähtevä tiedosto, joka sisältää maksukehoitushuomautuksen ja asianmukaiset asiakaslaskut PDF-muodossa.

[![Lähteviö asiakirjoja luovan ER-muodon rakenne](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Seuraavassa kuvassa näkyy tässä aiheessa kuvailtu prosessi yksittäisten komponenttien ryhmittelystä ja **Sähköposti**-kohteen ottamisesta käyttöön uudelle ryhmälle maksukehoitushuomautuksen lähettämiseksi liittyvien asiakaslaskujen kanssa sähköpostin liitteinä.

[![Yksittäisten komponenttien ryhmittely ja Sähköpostikohteen ottaminen käyttöön](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)
- [Sähköisen raportoinnin (ER) kohteet](electronic-reporting-destinations.md)
- [Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]