---
title: Toimittajayhteistyön määrittäminen ja hallinta
description: Tässä artikkelissa kerrotaan, kuinka voit toimittajayhteistyön Dynamics 365 Supply Chain Managementissa. Tässä kerrotaan myös, miten uudet toimittajayhteistyön käyttäjät valmistellaan ja miten näiden käyttäjien käyttöoikeusrooleja hallitaan.
author: GalynaFedorova
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 19fafb21e879d7436678bdb3c29d1a3d7e2330d7
ms.sourcegitcommit: bad64015da0c96a6b5d81e389708281406021d4f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023757"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Toimittajayhteistyön määrittäminen ja hallinta

[!include [banner](../includes/banner.md)]

Toimittajayhteistyöliittymästä saadaan rajoitettu joukko tietoja ostotilauksista, laskuista ja lähetysvarastosta ulkoisille toimittajakäyttäjille. Tässä käyttöliittymässä toimittaja voi myös vastata tarjouspyyntöihin sekä tarkastella ja muokata yrityksen perustietoja.

Tässä artikkelissa kerrotaan, kuinka voit toimittajayhteistyön Dynamics 365 Supply Chain Managementissa. Tässä kerrotaan myös, miten määritetään työnkulku uusien toimittajayhteistyön käyttäjien valmistelulle ja miten näiden käyttäjien käyttöoikeusrooleja hallitaan.

## <a name="set-up-vendor-collaboration-security-roles"></a>Toimittajayhteistyön käyttöoikeusroolien määrittäminen

Hankinta-asiantuntija tai toimittaja, jolla on riittävät käyttöoikeudet, voi pyytää yhteyshenkilön valmistelua käyttäjäksi ottamalla asetuksen **Valmistele toimittajakäyttäjä** käyttöön yhteyshenkilötietueessa. Valmisteluprosessin aikana valitaan uuden ulkoisen käyttäjän käyttöoikeudet ja lähetetään uutta toimittajakäyttäjää koskeva pyyntö. On tärkeää määrittää oikein käyttöoikeudet, jotka ovat valittavissa toimittajakäyttäjäpyynnössä. Muutoin toimittajille voidaan myöntää käyttöoikeudet tietoihin, joihin ei pitäisi päästä käsiksi Supply Chain Managementissa.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Määritä käyttöoikeusroolit, jotka ovat valittavissa, kun yhteyshenkilön osalta käytetään uutta käyttäjää koskevaa pyyntöä

1. Valitse **Järjestelmänhallinta** &gt; **Suojaus** &gt; **Ulkoiset roolit**.
2. Valitse **Uusi** ja valitse sitten käyttöoikeusrooli sekä **Toimittaja**-osapuolen rooli.

Voit lisätä roolit **Toimittajan järjestelmänvalvoja (ulkoinen)** ja **Toimittaja (ulkoinen)**, jotka tarjotaan Supply Chain Managementissa. Voit myös käyttää yrityksesi luomia käyttöoikeusrooleja.

Rooli **Toimittajan järjestelmänvalvojan (ulkoinen)** kannattaa määrittää käytettäväksi vain, jos toimittajien pitäisi pystyä luomaan uusia yhteyshenkilöitä, lähettää toimittajayhteistyökäyttäjiä koskevia pyyntöjä, muuttaa käyttäjätietoja ja käsitellä näitä pyyntöjä työnkulun avulla.

Jos aiot määrittää toimittajan yhteyshenkilöt ja käyttäjät manuaalisesti, voit määrittää käyttöön vain roolin **Toimittaja (ulkoinen)**. Tällöin tämä rooli on ainoa rooli, jota toimittajankäyttäjäpyynnöllä voi pyytää.

> [!NOTE]
> **SystemUser**-rooli myönnetään automaattisesti, kun luot uuden käyttäjätilin manuaalisesti. Siksi kyseinen rooli on poistettava ja **SystemExternalUser**-rooli määritettävä. Jos uusia käyttäjätilejä luodaan työnkululla, joka käynnistetään toimittajakäyttäjän uuden käyttäjän valmistelua koskevalla pyynnöllä, määritetään vähintään yksi niistä rooleista, jotka on määritetty toimittajayhteistyötä varten, sekä **SystemExternalUser**-rooli.

#### <a name="vendor-admin-external-security-role"></a>Toimittajan järjestelmänvalvojan (ulkoinen) käyttöoikeusrooli

**Toimittajan järjestelmänvalvoja (ulkoinen)** -roolia voi käyttää ulkoisilla toimittajilla, jotka ylläpitävät yhteystietoja ja tekevät uusien toimittajayhteistyön käyttäjien valmistelua koskevia pyyntöjä. Ulkoiset käyttäjät, joilla on tämä käyttöoikeusrooli, voivat suorittaa seuraavia tehtäviä:

- Tarkastele ja muokkaa yhteyshenkilötietoja, kuten henkilön tehtävänimikettä, sähköpostiosoitetta ja puhelinnumeroa.
- Lisää uusi tai aiemmin luotu yhteyshenkilö toimittajatileihin, joille he toimivat yhteyshenkilönä.
- Poista mikä tahansa heidän luomansa yhteyshenkilö.
- Ota yhteyshenkilön ja toimittajatilin välinen yhteys käyttöön tai poista se käytöstä. Kun yhteyshenkilön ja toimittajatilin välinen yhteys on pois käytöstä, yhteyshenkilöön ei voi viitata uusissa ostotilauksissa tai muissa asiakirjoissa.
- Estä tai salli yhteyshenkilön asiakirjojen käyttöoikeudet toimittajatilille yksilöllisessä toimittajayhteistyön käyttöliittymässä. Kun yhteyshenkilön ja toimittajatilin välinen yhteys ei ole käytössä, toimittajatilille yksilöllisten asiakirjojen käyttöoikeudet kielletään aina.
- Pyydä yhteyshenkilölle uutta käyttäjätiliä **Valmistele käyttäjä** -toiminnolla.
- Pyydä, että yhteyshenkilön käyttäjätili poistetaan käytöstä.
- Pyydä, että yhteyshenkilön käyttäjätiliä muokataan käyttöoikeusroolien lisäämiseksi tai poistamiseksi.
- Näytä tarjouspyynnöt.

#### <a name="vendor-external-security-role"></a>Toimittajan (ulkoinen) käyttöoikeusrooli

**Toimittaja (external)** -roolia voi käyttää ulkoisilla toimittajilla, jotka käsittelevät ostotilauksia. Ulkoiset käyttäjät, joilla on tämä käyttöoikeusrooli, voivat suorittaa seuraavia tehtäviä:

- Vastaa ostotilauksiin ja tarkastele niiden tietoja.
- Ylläpidä toimittajayhteistyön laskuja.
- Näytä tavaralähetysvarasto.
- Tarkastele tarjouspyyntöjä ja vastaa niihin.
- Tarkastele toimittajatietoja.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Mahdollisten toimittajien aktivoinnissa käytettävien käyttöoikeusroolien määrittäminen

Mahdollisen toimittajan rekisteröintipyynnöllä luotavien toimittajien aktivointia varten on määritettävä ulkoinen käyttöoikeusrooli. Tämä rooli määritetään uusille käyttäjille sen valmisteluprosessin aikana, jota ohjataan tyypin **Käyttäjäpyynnön työnkulku (ympäristö)** työnkululla. Lisätietoja on myöhemmin tässä artikkelissa osassa [Toimittajayhteistyön käyttäjäpyyntöjen käsittelyn työnkulkujen määrittäminen](#set-up-workflows-to-process-vendor-collaboration-user-requests).

Tietoja mahdollisten toimittajien aktivoinnista: [Toimittajien aktivointi](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Määritä käyttöoikeusrooli, jota käytetään, kun uutta mahdollisen toimittajan käyttäjää koskeva pyyntö lähetetään

1. Valitse **Järjestelmänhallinta** > **Suojaus** > **Ulkoiset roolit**.
2. Valitse **Uusi** ja valitse sitten käyttöoikeusrooli sekä **Mahdollinen toimittaja**-osapuolen rooli.

Sinun kannattaa lisätä **Mahdollinen toimittaja (ulkoinen)** -rooli, joka tarjotaan Supply Chain Managementissa.

Käyttöoikeusrooli myöntää käyttöoikeuden vain uuden toimittajan ohjattuun rekisteröintitoimintoon.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Toimittajayhteistyön käyttäjäpyyntöjen käsittelyn työnkulkujen määrittäminen

Sen varmistamiseksi, että kaikki merkitykselliset tehtävät suoritetaan ja että asianmukaiset hyväksynnät annetaan, on määritettävä työnkulkuja toimittajayhteistyön käyttäjiä koskevien pyyntöjen käsittelemistä varten.

Toimittajayhteistyön käyttäjiä koskevia pyyntöjä lähettävät joko ulkoiset toimittajat, joilla on **Toimittajan järjestelmänvalvoja (ulkoinen)** -käyttöoikeusrooli tai sitä vastaavat käyttöoikeudet, tai oman yrityksen hankinta-asiantuntijat. Niitä voidaan luoda myös mahdollisten toimittajien rekisteröintiä koskevien pyyntöjen perusteella toimittajan aktivointiprosessin yhteydessä.

Pyyntötyyppejä on kolme.

- Uuden käyttäjän valmistelua koskeva pyyntö
- Olemassa olevan käyttäjän käytöstä poistamista koskeva pyyntö
- Olemassa olevan käyttäjän käyttöoikeusroolien muuttamista koskeva pyyntö

Lisätietoja toimittajayhteistyön käyttäjiä koskevista pyynnöstä: [Toimittajayhteistyön käyttäjien hallinta](manage-vendor-collaboration-users.md).

Luo vähintään kaksi työnkulkua, jotta voit käsitellä kaikkia kolmea toimittajayhteistyön käyttäjiä koskevien pyyntöjen tyyppejä. Uudet työnkulut luodaan **Käyttäjän työnkulut** -sivulla.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Esimerkki uusien käyttäjien valmistelun ja käyttöoikeusroolien muokkaamisen työnkulusta

Voit asettaa haaroitusehdon työnkulun alkuun toimittajakäyttäjäpyyntöjen käsittelyä, uusien käyttäjien luontia ja käyttöoikeusroolien muokkaamista varten. Tällä tavoin käytetään työnkulun eri haaroja sen mukaan, koskeeko pyyntö uuden käyttäjän luomista vai olemassa olevan käyttäjän muokkaamista.

Voit määrittää tämän haaroituksen luomalla uuden tyypin **Käyttäjäpyynnön työnkulku (ympäristö)** työnkulun. Tämän työnkulun haarat voivat sisältää seuraavia elementtejä.

#### <a name="branch-to-provision-new-users"></a>Uusien käyttäjien valmistelun haara

1. Määritä hyväksyntätehtävä henkilölle, joka vastaa sen hyväksymisestä, että uusille käyttäjille myönnetään käyttöoikeudet toimittajayhteistyön tietoihin.
2. Määritä tehtävä henkilölle, joka on vastuussa uusien Microsoft Azure Active Directory (Azure AD) -käyttäjätilien pyytämisestä Azure-portaalissa. Käytä tässä vaiheessa esimääritettyä **Lähetä Azuren yritystenvälisen yhteistyön käyttäjäkutsu** -tehtävää. Yritystenvälisen yhteistyön käyttäjät voidaan viedä automaattisesti Azure AD:hen. Käytä ennalta määritettyä **Valmistele Azure AD:n yritystenvälisen yhteistyön käyttäjä** -toimintoa. Lisätietoja: [Yritystenvälisen yhteistyön käyttäjien vienti Azure AD:hen](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Määritä hyväksyntätehtävä henkilölle, joka suorittaa lataukset Azureen. Jos tiliä ei luoda onnistuneesti, tämä henkilö hylkää tehtävän ja lopettaa työnkulun. Tämän hyväksyntätehtävän voi ohittaa, jos olet sisällyttänyt vaiheen, joka vie uudet käyttäjätilit automaattisesti Azureen yritystenvälisen yhteistyön sovelluksen ohjelmointirajapinnan kautta.
4. Lisää automaattinen tehtävä, joka valmistelee uuden käyttäjän. Käytä tässä vaiheessa esimääritettyä **Käyttäjän automatisoitu valmistelu** -tehtävää.
5. Lisää tehtävä, joka ilmoittaa uudesta käyttäjästä. Saatat haluta lähettää uudelle käyttäjälle tervetulosähköpostin, joka sisältää Supply Chain Managementin URL-osoitteen. Tässä sähköpostissa voi käyttää mallia, joka luodaan **Sähköpostiviestit**-sivulla ja valitaan sitten **Käyttäjätyönkulun parametrit** -sivulla. Tämä malli voi sisältää **%portalURL%**-tunnisteen. Kun tervetulosähköposti luodaan, tämä tunniste korvataan Supply Chain Management vuokraajan URL-osoitteella.

    > [!NOTE]
    > Tätä työnkulkua voidaan käyttää useissa skenaarioissa, joihin liittyy käyttäjien aktivointia. Sitä voidaan käyttää esimerkiksi silloin, kun mahdolliset toimittajat tai yhteyshenkilöt tarvitsevat toimittajayhteistyön tilin. Siksi sähköposti kannattaa muotoilla yleiseksi lausunnoksi, jota voi käyttää moniin tarkoituksiin.

#### <a name="branch-to-modify-security-roles"></a>Haara käyttöoikeusroolien muokkausta varten

1. Määritä hyväksyntätehtävä henkilölle, joka on vastuussa käyttöoikeusroolien muutosten hyväksymisestä.
2. Lisää automaattinen tehtävä, joka lisää tai poistaa asianmukaiset käyttöoikeusroolit. Käytä tässä vaiheessa **Käyttäjän automatisoitu valmistelu** -tehtävää.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Esimerkki työnkulusta, jolla käyttäjä poistetaan käytöstä

Luo tyypin **Poista käyttäjäpyynnön työnkulkuympäristö** työnkulku ja lisää sitten seuraavat tehtävät.

1. Määritä hyväksyntätehtävä henkilölle, joka on vastuussa käyttäjien käytöstä poistoa koskevien pyyntöjen hyväksymisestä. Voit lisätä ehtoja tämän hyväksymisvaiheen automatisoimiseksi.
2. Lisää automaattinen tehtävä, joka poistaa käyttäjän käytöstä. Käytä tässä vaiheessa **Käyttäjän automatisoitu käytöstä poisto** -tehtävää.
3. Lisää tarvittavat puhdistustehtävät. Voit esimerkiksi lisätä tehtävän, joka poistaa tilin hakemistostasi Azure-portaalissa.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Tietyn toimittajan toimittajayhteistyön käyttöönotto

Ennen kuin luot käyttäjätilin henkilölle, joka tulee käyttämään toimittajayhteistyötä, sinun on määritettävä kyseinen toimittaja siten, että se voi käyttää toimittajayhteistyötä. Lisätietoja tästä on kohdassa [Toimittajayhteistyö ulkoisten toimittajien kanssa](vendor-collaboration-work-external-vendors.md).

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Uusien toimittajayhteistyön käyttäjien valmistelun vianmääritys

Uudet toimittajayhteistyön käyttäjät valmistellaan työnkululla, joka määritetään käsittelemään tyypin **Valmistele toimittajakäyttäjä** toimittajayhteistyön käyttäjiä koskevat pyynnöt.

Jos uuden toimittajayhteistyön käyttäjän sähköpostiosoitteen toimialue on rekisteröity vuokraajaksi Azuressa (eli se on hallittu toimialuetili), sähköpostiosoitteen on oltava aiemmin luotu Azure AD -tili. Muussa tapauksessa valmisteluprosessia ei voi suorittaa.

Lisätietoja prosessista, jota käytetään Azure AD:n tilinhallinnan **Lähetä Azuren yritystenvälisen yhteistyön käyttäjäkutsu** -tehtävässä: [Azure Active Directoryn yritysten välinen yhteistyö](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Lisäresurssit

[Toimittajayhteistyö ulkoisten toimittajien kanssa](vendor-collaboration-work-external-vendors.md)

Katso lyhyt video aktivointiprosessista: [Uuden toimittajan aktivointi](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
