---
title: Kolmannen osapuolen sovellusten upottaminen
description: Tässä ohjeaiheessa käsitellään kolmannen osapuolen sovellusten upottamista laajentamaan tuotteen toimintoja.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 89f101bcf33080f6a73664fe7c3fe6719de04a4e
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488231"
---
# <a name="embed-third-party-apps"></a>Kolmannen osapuolen sovellusten upottaminen

[!include [banner](../includes/banner.md)]

Monet asiakkaat käyttävät useita sovelluksia liiketoiminnan harjoittamiseen. Osa sovelluksista on kolmannen osapuolen verkkosovelluksia, jotka toimivat yhdessä Finance and Operations -sovellusten kanssa. Jos haluat antaa entistä sujuvamman käyttökokemuksen, voit käyttää **Koko sivun sovellukset** -toimintoa, kun haluat upottaa nämä kolmannen osapuolen sovellukset suoraan Finance and Operations -sovelluksiin (jos kolmannen osapuolen sovellukset sallivat upottamisen). Näin käyttäjät voivat käyttää tarvitsemiaan sivustoja ja sovelluksia ilman, että heidän tarvitsee vaihtaa välilehtiä tai ikkunoita.

Ennen kuin voit upottaa kolmannen osapuolen sovellukset tuotteeseen, ota ominaisuuksien hallinnassa käyttöön **Koko sivun sovellukset**. Sen jälkeen voit upottaa kolmannen osapuolen sovelluksen tai sivuston jollais seuraavista tavoista. Nämä menetelmät ovat analogisia menetelmille, joita käytetään kaaviosovellusten upottamiseen Microsoft Power Apps -sovelluksista Finance and Operations -sovelluksiin.

- Upota sovellus tai sivusto aiemmin luodulle sivulle uutena välilehtenä (pivot-välilehti, pikavälilehti, lehti tai työtilan osa).
- Luo sovellukselle tai sivustolle uusi koko sivun kokemus koontinäytössä.

## <a name="embed-a-website-on-an-existing-page"></a>Upota sivusto aiemmin luodulle sivulle

Käytä tätä menettelyä, jos haluat täydentää järjestelmässä olevaa sivua upotetulla sovelluksella.

1. Avaa sivu, johon haluat upottaa sovelluksen.
2. Avaa **Lisää sovellus** -ruutu:

    1. Valitse **Asetukset** ja sitten **Mukauta** avataksesi **Mukauttaminen**-työkalurivin.
    2. Valitse **Lisää \> Lisää sovellus**.

3. Valitse sivun alue, johon haluat lisätä sovelluksen. Alueen on oltava *välilehtisäilö* pivot-välilehdelle, pikavälilehdelle, lehdelle tai työtilan osalle.
4. Valitse **Sivusto**.
5. Määritä upotettu sovellus seuraavasti:

    - **Nimi** – Kirjoita teksti, joka näkyy upotetun sovelluksen sisältävässä välilehdessä. Usein tämä teksti on sovelluksen nimi.
    - **URL** – Määritä sovelluksen sijainti.

    > [!IMPORTANT]
    > - Turvallisuussyistä URL-osoitteen on käytettävä HTTPS-protokollaa.
    > - Sovelluksen tai verkkosivuston asetukset on määritettävä niin, että ne sallivat upottamisen.

6. Valitse **Tallenna**, jos haluat upottaa sovelluksen sivulle. Sovellus lisätään ryhmän viimeiseksi välilehdeksi tai osaksi.
7. Vahvista, että sovellus näkyy odotetulla tavalla. Jos sovellusta ei hahmonneta, katso [Vianmääritys](#troubleshooting)-osa jäljempänä tässä ohjeaiheessa.
8. Avaa näkymän valitsin ja valitse joko **Tallenna** (jos sovellus liitetään nykyiseen näkymään) tai **Tallenna nimellä** (jos haluat tallentaa sovelluksen eri näkymään).

    Jos sivulla ei ole näkymän valitsinta (esimerkiksi sivu on valintaikkuna tai työtila), voit ohittaa tämän vaiheen.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Upota sivusto koko sivun kokemuksena koontinäytöstä

Käytä tätä menettelyä, jos upotettava sovellus ei liity aiemmin luotuun sivuun tai jos haluat vain koko sivun kokemuksen sovellukselle Finance and Operations -sovelluksessa.

1. Avaa koontinäyttö.
2. Tee valinta ja pidä se valittuna koontinäytössä (tai napsauta hiiren kakkospainikkeella), valitse sitten **Mukauta** ja valitse lopuksi **Lisää sivu**.
3. Valitse **Lisää sivu** -ruudussa **Sivusto**.
4. Määritä upotettu sovellus seuraavasti:

    - **Nimi** – Kirjoita teksti, jonka pitäisi näkyä upotetulle sovellukselle lisätyssä ruudussa koontinäytössä. Usein tämä teksti on sovelluksen nimi.
    - **URL** – Määritä sovelluksen sijainti.

    > [!IMPORTANT]
    > - Turvallisuussyistä URL-osoitteen on käytettävä HTTPS:ää.
    > - Sovelluksen tai verkkosivuston asetukset on määritettävä niin, että ne sallivat upottamisen.

5. Lisää sovellus koontinäyttöön uutena ruutuna valitsemalla **Tallenna**.
6. Valitse uusi ruutu koontinäytöstä ja vahvista, että sovellus näkyy odotetulla tavalla. Jos sovellusta ei hahmonneta, lisätietoja on jäljempänä tässä aiheessa kohdassa [Vianmääritys](#troubleshooting).

## <a name="sharing-embedded-apps"></a>Upotettujen sovellusten jakaminen

Kun olet upottanut sovelluksen käyttämällä jotakin aiemmissa osissa kuvatuista menetelmistä, voit jakaa näkymän järjestelmän muiden käyttäjien kanssa. Voit jakaa upotetun sovelluksen jollain seuraavista tavoista:

- **Julkaise näkymä (suositus):** Jos upotettu sovellus on tallennettu näkymään, sen suositeltu ja ensisijainen jakotapa on julkaista näkymä käyttäjille, joilla on soveltuvat käyttöoikeusroolit kohteena olevissa yrityksissä. Silloin vain toivotut käyttäjät näkevät upotetun sovelluksen kyseisellä sivulla. Lisätietoja näkymän julkaisemisesta on kohdassa [Julkaisunäkymät](saved-views.md#publishing-views).

    Voit myös julkaista sovelluksen, joka on upotettu koko sivun käyttökokemuksena koontinäytöstä. Koontinäytössä valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) sovellukseen liittyvä ruutu, valitse **Mukauta** valitse sitten **Julkaise sivu**. *Näkymien julkaiseminen* -kokemusta muistuttava kokemus näytetään, ja käyttöoikeudet, joihin julkaisu tehdään, voidaan valita. Jos päivityksestä 10.0.21 alkaen **Tallennettujen näkymien parannetut yritystuki** -ominaisuus on otettu käyttöön, sovellus voidaan julkaista myös toivottuihin yrityksiin.

- **Kopioi mukauttaminen**: Jos sivu ei tue näkymiä (esimerkiksi valintaikkunat tai työtilat), tai koko sivun sovelluskokemusta varten, voit kopioida mukautuksen asianmukaisille käyttäjille. Lisätietoja on kohdassa [Mukauttamisen jakaminen](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Upotettujen sovellusten tarkasteleminen

Voit tarkastella Finance and Operations -sovelluksien sivulle upotettua sovellusta avaamalla sivun, jolla on upotettu sovellus. Muista, että joillakin sivuilla upotettuja sovelluksia voi käyttää vakiomuotoisen toimintoruudun **Power Apps** -painikkeen avulla. Vaihtoehtoisesti ne voivat tulla näkyviin suoraan sivulla uutena välilehtenä, pikavälilehtenä, lehtenä tai työtilan uutena osana.

## <a name="editing-or-removing-embedded-apps"></a>Upotettujen sovellusten muokkaaminen tai poistaminen

Kun sovellus on upotettu sivulle, saatat joutua muokkaamaan sen konfiguraatiota (esimerkiksi vaihtamalla osion otsikkoa tai URL-osoitetta). Voit se pitää poistaa sivulta. Voit muokata upotetun sovelluksen konfiguraatiota tai poistaa sen kokonaan seuraavien menetelmien avulla.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Aiemmin luotuihin sivuihin upotetut sovellukset

1. Avaa sivu, jolle sovellus on upotettu.
2. Valitse **Asetukset** ja sitten **Mukauta** avataksesi **Mukauttaminen**-työkalurivin.
3. Valitse **Valintatyökalu** ja valitse sitten upotettu sovellus.
4. Jos haluat muokata sovellusta, tee tarvittavat muutokset sen konfiguraatioon ja valitse sitten **Tallenna**.

    Voit myös poistaa sovelluksen valitsemalla **Poista**.

5. Tallenna tai julkaisen näkymä uudelleen. Huomaa, että jos poistut sivulta tallentamatta näkymää erikseen, mitään **Muokkaa sivustoa** -ruudussa suorittamistasi toimenpiteistä ei ylläpidetä.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Koontinäytöstä upotetut sovellukset

1. Avaa koontinäyttö.
2. Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) upotettuun sovellukseen liittyvä ruutu ja valitse sitten **Mukauta**.
3. Jos haluat muokata sovellusta, valitse **Muokkaa sivua**. Tee tarvittavat muutokset **Muokkaa sivustoa** -ruudussa sovelluksen konfiguraatioon ja valitse sitten **Tallenna**.

    Voit myös poistaa sovelluksen valitsemalla **Poista sivu**.

## <a name="appendix"></a>Liite

### <a name="troubleshooting"></a>Vianmääritys

Jos sivustoa ei hahmonneta oikein sen jälkeen, kun se on upotettu Finance and Operation s-ovellukseen, tai jos näyttöön tulee virhesanoma, jossa todetaan, että URL-osoitteen yhteys evättiin, sivusto on todennäköisesti määritetty estämään itsensä upotettaminen iFrameen. Seuraavia ohjeita noudattamalla voit määrittää, voidaanko sivusto upottaa.

1. Avaa käyttämäsi selaimen kehittäjän työkalut.
2. Etsi ja valitse vastaus **Verkko**-välilehdestä upotetusta sivustosta.
3. Etsi **Otsikot**-välilehdessä **Vastausten otsikot** -kohdassa kohtaa **x-kehys-vaihtoehdot**. Jos **x-kehys-vaihtoehdot** on olemassa vastausten otsikoissa ja sen arvona on **DENY** tai **SAMEORIGIN**, sivustoa ei voi tällä hetkellä upottaa. Sinun on työskenneltävä sovelluksen omistajan kanssa, jotta se voidaan upottaa turvallisesti.

### <a name="developer-modeling-a-website-on-a-form"></a>[Kehittäjä] Sivuston mallinnus lomakkeelle

Vaikka tämä ohjeaihe on kohdistunut kolmannen osapuolen sovellusten tai sivustoihin upottamiseen mukauttamisen kautta, kehittäjät voivat myös upottaa ne lomakkeeseen Visual Studio -kehittämiskokemusta käyttäen. Lisää vain **WebsiteHostControl** -ohjausobjekti lomakkeeseen. Ohjausobjektin käytettävissä olevat metatietojen ominaisuudet tarjoavat samat ominaisuudet kuin personointikokemuskin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
