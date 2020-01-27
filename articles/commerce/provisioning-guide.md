---
title: Commercen esikatseluympäristön valmisteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen esikatseluympäristön.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934745"
---
# <a name="provision-a-commerce-preview-environment"></a>Commercen esikatseluympäristön valmisteleminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen esikatseluympäristön.

Ennen kuin aloitat, kannattaa lukaista tämän koko ohjeaiheen läpi. Näin saat käsityksen siitä, millainen prosessi on ja mitä tämä ohjeaihe sisältää.

> [!NOTE]
> Jos sinulle ei ole vielä myönnetty Dynamics 365 Commerce Preview -sovelluksen käyttöoikeutta, voit pyytää esiversion käyttöoikeuden [Commerce-sivuston](https://aka.ms/Dynamics365CommerceWebsite) avulla.

## <a name="overview"></a>Yleiskatsaus

Jotta voit laatia Commerce Preview -ympäristön onnistuneesti, sinun on luotava projekti, jolla on tietty tuotteen nimi ja tyyppi. Ympäristöllä ja Retail Cloud Scale Unit (RCSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, kun myöhemmin valmistelet sähköistä kaupankäyntiä. Tämän ohjeaiheen ohjeissa kuvataan kaikki vaaditut vaiheet, jotka sinun on suoritettava, ja parametrit, joita sinun on käytettävä.

Kun olet onnistuneesti valmistellut Commercen esikatseluympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen valmistelemiseksi. Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida. Voit aina suorittaa valinnaiset vaiheet myöhemmin.

Katso lisätietoja Commercen esikatseluympäristön määrittelystä kohdasta sen jälkeen, kun olet valmistellut sen [Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md). Jos haluat lisätietoja valinnaisten ominaisuuksien määrittämisestä Commercen esikatseluympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md).

Jos haluat lisätietoja valmistelun vaiheista tai jos kohtaat ongelmia, kerro se Microsoftille [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmän](https://aka.ms/Dynamics365CommercePreviewYammer) kautta.

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commerce Preview -ympäristön:

- Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus
- Sinut on hyväksytty Dynamics 365 Commerce Preview -ohjelmaan.
- Sinulla on projektin luomisessa vaaditut **Mahdolliset myyntiä edeltävät toimet**- tai **Siirrä, luo ratkaisuja ja opi** -kohtien oikeudet.
- Olet **Ympäristövastaava**- tai **Projektin omistaja** -roolin jäsen projektissa, jolle valmistelet ympäristöä.
- Sinulla on järjestelmänvalvojan oikeudet Microsoft Azure -tilausta varten, tai ota yhteyttä tilauksen järjestelmänvalvojaan, joka voi suorittaa puolestasi järjestelmänvalvojan oikeudet vaativat kaksi vaihetta.
- Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.
- Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.
- Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus. (Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)

### <a name="find-your-azure-ad-tenant-id"></a>Etsi Azure AD-vuokraajan tunnus

Azure AD -vuokraajasi tunnus on yleisesti yksilöllinen GUID-tunnus, joka muistuttaa tätä esimerkkiä: **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Azure AD -vuokraajan tunnuksen etsiminen Azure-portaalin avulla

1. Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).
1. Varmista, että oikea hakemisto on valittu.
1. Valitse vasemmalla olevasta valikosta **Azure Active Directory**.
1. Valitse **Hallinta**-kohdasta **Ominaisuudet**. Azure AD -vuokraajan tunnus näkyy **hakemistotunnus**-kohdassa.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>Azure AD -vuokraajan tunnuksen etsiminen OpenID Connectin metatietojen avulla

Luo OpenID-URL-osoite korvaamalla **\{OMA\_TOIMIALUEESI\}**, kuten `microsoft.com`. Esimerkiksi toimialueesta `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` tulee `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Siirry siihen OpenID-URL-osoitteeseen, joka sisältää toimialueesi.

    Azure AD-vuokraajan tunnus näkyy usean ominaisuuden arvoissa.

1. Etsi **valtuutustieto\_päätepiste** ja pura GUID-tunnus, joka näkyy heti `login.microsoftonline.com/`in jälkeen.

### <a name="find-your-azure-ad-security-group-id"></a>Azure AD -suojausryhmän tunnuksen etsiminen

Azure AD -suojausryhmän tunnus on tämän esimerkin kaltainen GUID: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

Tässä menettelyssä oletetaan, että olet sen ryhmän jäsen, jolle yrität löytää tunnuksen.

1. Avaa [Graph-työkalu](https://developer.microsoft.com/graph/graph-explorer#).
1. Valitse **Kirjaudu sisään Microsoftin avulla** ja kirjaudu sisään tunnistetietojen avulla.
1. Valitse vasemmalta **Näytä lisää näytteitä**.
1. Ota oikeanpuoleisesta ruudusta käyttöön **ryhmät**.
1. Sulje oikeanpuoleinen ruutu.
1. Valitse **kaikki ryhmät, joihin kuulun**.
1. Etsi **Vastauksen esikatselu** -kentästä ryhmäsi. Suojausryhmän tunnus näkyy **Tunnus**-ominaisuuden alla.

## <a name="provision-your-commerce-preview-environment"></a>Commercen esikatseluympäristön valmisteleminen

Näissä ohjeissa kerrotaan, miten Commerce Preview -ympäristö tarjotaan. Kun olet suorittanut ne onnistuneesti, Commerce Preview -ympäristö on valmiina konfigurointia varten. Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.

> [!IMPORTANT]
> Esikatselun käyttö on sidottu esikatselusovelluksessa määrittämääsi LCS-tiliin ja organisaatioon. Sinun on käytettävä samaa tiliä Commerce Preview -ympäristön tarjoamiseen. Jos sinun on käytettävä Commerce Preview -ympäristössä eri LCS-tiliä tai -vuokraajaa, sinun on annettava kyseiset tiedot Microsoftille. Yhteystiedot ovat jäljempänä tämän ohjeaiheen [ Commerce Preview -ympäristön tuki](#commerce-preview-environment-support) -osiossa.

### <a name="grant-access-to-e-commerce-applications"></a>Sähköisen kaupankäynnin sovellusten käyttöoikeuden myöntäminen

> [!IMPORTANT]
> Henkilön, joka kirjautuu sisään, on oltava Azure AD -vuokraaja-järjestelmänvalvoja , jolla on Azure AD -vuokraajan tunnus. Jos tätä vaihetta ei suoritettu loppuun, jäljellä olevat valmisteluvaiheet epäonnistuvat.

Jos haluat valtuuttaa sähköisen kaupankäynnin sovellukset käyttämään Azure-tilausta, toimi seuraavasti.

1. Kokoa URL-osoite seuraavassa muodossa:

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Kopioi ja liitä URL-osoite selaimeesi tai tekstieditoriin ja korvaa **\{AAD\_-\_VUOKRAAJAN\}** tunnus Azure AD -vuokraajasi tunnuksella. Avaa sitten URL-osoite.
1. Kirjaudu sisään Azure AD -valintaikkunassa ja vahvista, että haluat myöntää **Dynamics 365 Commerce (esikatselu)** -sovellukselle tilauksesi käyttöoikeuden. Sinut ohjataan sivulle, joka osoittaa, onko toimenpide onnistunut.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Tarkista, että esiversio-ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön LCS:ssä

Toimi seuraavasti tarkistaaksesi, että esiversio-ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön LCS:ssä.

1. Kirjaudu sisään [LCS-portaaliin](https://lcs.dynamics.com) käyttämällä samaa LCS-tiliä, jota käytit pyytämällä esikatselun käyttöoikeutta.
1. Vieritä LCS:n kotisivua oikeaan reunaan ja valitse **Esiversio-ominaisuuksien hallinta** -ruutu.

    ![Esiversion hallinta -ruutu](./media/preview1.png)

1. Vieritä **Yksityisen esiversion ominaisuudet** -kohtaan ja vahvista, että seuraavat ominaisuudet ovat käytettävissä ja että ne on otettu käyttöön:

    - Sähköisen kaupankäynnin arviointi
    - Commerce Preview -ohjelman ympäristöt

    ![Yksityisen esiversion ominaisuudet](./media/preview2.png)

1. Jos nämä ominaisuudet eivät näy luettelossa, ota yhteyttä Microsoftiin ja anna työsähköpostiosoitteesi, LCS-tilisi ja vuokralaisen tiedot. Yhteystiedot löydät [ Commerce Preview -ympäristön tuki](#commerce-preview-environment-support) -osiosta.

### <a name="create-a-new-project"></a>Luo uusi projekti

Noudata seuraavia vaiheita luodaksesi uuden projektin LCS:ssä.

1. Luo projekti valitsemalla LCS-aloitussivulla plusmerkki (**+**).
1. Noudata oikeanpuoleisessa ruudussa jotakin näistä vaiheista:

    - Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.
    - Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.

1. Syötä mallin nimi, kuvaus ja toimiala.
1. Valitse **Tuotenimi** -kentässä **Dynamics 365 Retail**.
1. Valitse **Tuoteversio**-kentässä **Dynamics 365 Retail**.
1. Valitse **Metodologia**-kentässä **Dynamics Retail -implementointimetodologia**.
1. Valinnainen: Voit tuoda rooleja ja käyttäjiä aiemmin luodusta projektista.
1. Valitse **Luo**. Projektinäkymä avautuu.

### <a name="add-the-azure-connector"></a>Azure-yhdistimen lisääminen

Voit lisätä Azure-yhdistin LCS-projektiin noudattamalla seuraavia ohjeita.

1. Noudata seuraavia ohjeita:

    - Jos olet kumppani, valitse **Projektin asetukset** -ruutu oikeassa reunassa.
    - Jos olet asiakas, valitse ylävalikosta **Projektin asetukset**.

1. Valitse **Azure-yhdistimet**.
1. Lisää Azure-yhdistin valitsemalla**Lisää**.
1. Kirjoita nimi.
1. Anna Azure-tilauksen tunnus.
1. Ota **Määritä Azuren resurssienhallinta (ARM)** -valinta käyttöön.
1. Varmista, että **Azure-tilauksen AAD-vuokraajan toimialue (tai tunnus)** -arvo on määritetty oikein. Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.
1. Valitse **Seuraava**.
1. Noudata sivulle tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet. Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.

    1. Kirjaudu [Azure-portaalin osoitteessa](https://portal.azure.com/).
    1. Varmista, että oikea hakemisto on valittuna, ja valitse sitten vasemmalla olevasta valikosta **Tilaukset**.
    1. Etsi oikea tilaus luettelosta ja valitse se. Käytä hakutoimintoa tarpeen mukaan.
    1. Valitse valikosta **Käytön valvonta (IAM)**.
    1. Valitse **Lisää** oikealla olevassa **Lisää roolin määritys** -kohdassa. **Lisää roolin määritys** -ruutu avautuu.
    1. Valitse **Rooli**-kentästä **Osallistuja**.
    1. Jätä **Määritä käyttöoikeus** -kenttään oletusarvo, **Azure AD -käyttäjä, ryhmä tai palvelun päätieto**.
    1. Syötä **Valitse**-kohtaan **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Valitse luettelosta **Dynamics-käyttöönoton palvelut Services \[käytössä wsfed\]**.
    1. Valitse **Tallenna**.

1. Valitse **Seuraava**.
1. Noudata sivulle tulevia ohjeita ja myönnä tilaukselle tarvittavien sovellusten käyttöoikeudet. Ota tarvittaessa yhteys Azure-tilauksen järjestelmänvalvojaan.
1. Valitse **Seuraava**.
1. Valitse **Azure-alue**-kohdassa **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.
1. Valitse **Yhdistä**. Azure-yhdistin näkyy luettelossa.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Tuo Commerce Preview -esittelyalustan laajennus

Voit tuoda Commerce Preview-demokannan laajennuksen projektiin noudattamalla seuraavia ohjeita.

1. Avaa projektin kotisivu valitsemalla projektin nimi yläreunassa.
1. Noudata seuraavia ohjeita:

    - Jos olet kumppani, valitse **Omaisuuskirjasto** -ruutu oikeassa reunassa.
    - Jos olet asiakas, valitse ylävalikosta **Omaisuuskirjasto**.

1. Valitse vasemmalla olevasta luettelosta **Käyttöönotettava ohjelmistopaketti**.
1. Valitse **Tuo**.
1. Valitse **Commerce Preview -esittelyn peruslaajennus** **Jaettu resurssikirjasto** -kohdan resurssiluettelosta.
1. Valitse **Kerää**. Sinut siirretään resurssikirjastoon ja laajennuksen tulisi näkyä luettelossa.

Seuraavassa kuvassa näkyvät toiminnot, jotka on tehtävä LCS-**resurssikirjasto**-sivulla.

![Commerce Preview -esittelyalustan laajennuksen tuominen](./media/import.png)

### <a name="deploy-the-environment"></a>Käyttöönottoympäristö

Määritä ympäristö näiden ohjeiden avulla.

> [!NOTE]
> Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan. Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce (esikatselu) - esittely (10.0.6 ja Platform-päivitys 30)** näkyy suoraan **Ympäristön nimi** -kentän yläpuolella. Katso vaiheen 8 jälkeen näkyvää kuvaa.

1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse **+ Lisää** lisätäksesi ympäristön.
1. Valitse **Tuoteversio**-kentässä **10.0.6**.
1. Valitse **Ympäristön versio** -kentässä **Platform Update 30**.

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. Valitse **Seuraava**.
1. Valitse **Esittely** ympäristötopologiaksi.

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. Valitse **Dynamics 365 Commerce (Esikatselu) - Esittely** ympäristötopologiaksi. Jos olet määrittänyt aiemmin yhden Azure-yhdistimen, sitä käytetään tässä ympäristössä. Jos olet määrittänyt useita Azure-yhdistimiä, voit valita käytettävän yhdistimen: **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat**tai **Länsi-Yhdysvallat 2**. (Parhaan päästä päähän-suorituskyvyn saavuttamiseksi suosittelemme valitsemaan **Länsi-Yhdysvallat 2**.)

    ![Ympäristötopologia 2 valitseminen](./media/project3.png)

1. Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla. Älä muuta Lisäasetukset-kohtaa.

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. Säädä VM:n kokoa tarpeen mukaan. (Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)
1. Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.
1. Valitse **Seuraava**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**. Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.

    Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön. Ympäristön työnkulut kestävät jonkin aikaa. Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.

1. Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.

### <a name="initialize-rcsu"></a>RCSU:n alustaminen

Alusta RCSU-osoite seuraavien ohjeiden avulla.

1. Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.
1. Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**. Näkyviin tulee ympäristön tietojen näkymä.
1. Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.
1. Valitse **Vähittäismyynti**-välilehdestä **Alusta**. Näkyviin tulee RCSU-alustusparametrien näkymä.
1. Valitse **Alue**-kohdassa **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.
1. Valitse **Versio**-kentässä **Määritä versio** -luettelosta ja määritä sitten **9.16.19262.5** näyttöön tulevassa kentässä. Muista määrittää tarkka versio, joka on ilmoitettu tässä. Muussa tapauksessa sinun on päivitettävä RCSU oikeaan versioon myöhemmin.
1. Ota käyttöön **Laajennuksen käyttäminen** -vaihtoehto.
1. Valitse laajennusluettelosta **Commerce Preview -esittelyn peruslaajennus**.
1. Valitse **Alusta**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**. Palaat **Vähittäismyynnin hallinta** -näkymään, jossa on valittuna **Vähittäismyynti**-välilehti. RCSU on asetettu jonoon valmistelua varten.
1. Varmista ennen jatkamista, että RCSU:si tila on **Onnistunut**. Alustus kestää noin kahdesta viiteen tuntia.

### <a name="initialize-e-commerce"></a>Sähköisen kaupankäynnin alustaminen

Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.

1. Tarkista esikatselun suostumus **sähköisen kaupankäynnin (esikatselu)**-välilehdestä ja valitse sitten **Asetukset**.
1. Kirjoita **Sähköisen kaupankäynnin vuokraajan nimi** -kenttään nimi. Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.
1. Valitse **Retail Cloud Scale -yksikön nimi** -kentässä RCSU-luettelosta. (Luettelossa pitäisi olla vain yksi vaihtoehto.)

    **Sähköisen kaupankäynnin paikkatieto** -kenttä määritetään automaattisesti, eikä arvoa voi muuttaa.

1. Jatka valitsemalla **Seuraava**.
1. Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.
1.  **AAD-suojausryhmän järjestelmänhallinta** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain. Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake. Valitse luettelosta suojausryhmä.
2.  **AAD-turvallisuusryhmä luokituksille ja arvosteluvalvoja** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain. Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake. Valitse luettelosta suojausryhmä.
1. Jätä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetus päälle.
1. Jos olet jo suorittanut Microsoft Azure Active Directoryn (Azure AD) suostumusvaiheen, joka on kuvattu kohdassa Myönnä käyttöoikeudet verkkokaupan sovelluksiin, valitse valintaruutu vahvistaaksesi suostumuksesi. Jos et ole vielä suorittanut tätä vaihetta, sinun on tehtävä se ennen alustuksen jatkamista. Avaa suostumus-valintaikkuna ja suorita vaihe valitsemalla valintaruudun vieressä olevassa tekstissä oleva linkki.
1. Valitse **Alusta**. Palaat **Vähittäismyynnin hallinta** -näkymään, jossa on valittuna **Sähköinen kaupankäynti (esiversio)**-välilehti. Sähköisen kaupankäynnin alustaminen on aloitettu.
1. Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **Alustaminen onnistui**.
1. Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:

    * **Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.
    * **Sähköisen kaupankäynnin hallintatyökalu** – linkki sivuston hallintatyökaluun.

## <a name="commerce-preview-environment-support"></a>Commercen esikatseluympäristön tuki

Jos valmisteluvaiheiden suorittamisen aikana on ongelmia, saat apua [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmästä](https://aka.ms/Dynamics365CommercePreviewYammer).

Jos kohtaat ongelmia yrittäessäsi käyttää Yammer-ryhmää, voit ottaa yhteyttä Microsoftiin sähköpostitse osoitteella <Dynamics365Commerce@microsoft.com>. Tätä sähköpostiosoitetta ei seurata aktiivisesti. Varaudu viiveeseen vastausta odottaessasi.

## <a name="next-steps"></a>Seuraavat vaiheet

Jatkaaksesi käyttöönotto- ja määritysprosessia Commercen esikatseluympäristön määrittelystä, katso [Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Lisäresurssit

[Commercen esikatseluympäristön yleiskuvaus](cpe-overview.md)

[Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md)

[Valinnaisten ominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md)

[Commercen esikatseluympäristön usein kysytyt kysymykset](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)

[Dynamics 365 Retailin ohjeresurssit](../retail/index.md)
