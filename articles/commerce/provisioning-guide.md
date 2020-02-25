---
title: Dynamics 365 Commercen esiversioympäristön valmistelu
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen esikatseluympäristön.
author: psimolin
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024633"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a>Dynamics 365 Commercen esiversioympäristön valmistelu


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Dynamics 365 Commercen esikatseluympäristön.

Ennen kuin aloitat, suosittelemme, että tarkistat tämän aiheen nopeasti, jotta saat käsityksen prosessin vaatimista aiheista.

> [!NOTE]
> Jos sinulle ei ole vielä myönnetty Dynamics 365 Commerce Preview -sovelluksen käyttöoikeutta, voit pyytää esiversion käyttöoikeuden [Dynamics 365 Commerce -sivuston avulla](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Yleiskatsaus

Jotta voit laatia Commerce Preview -ympäristön onnistuneesti, sinun on luotava projekti, jolla on tietty tuotteen nimi ja tyyppi. Ympäristöllä ja commerce scale unit (CSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, kun myöhemmin valmistelet sähköistä kaupankäyntiä. Tämän ohjeaiheen ohjeissa kuvataan kaikki tarvittavat vaiheet käyttöönoton suorittamiseksi ja parametrit, joita sinun on käytettävä.

Kun olet onnistuneesti valmistellut Commercen esikatseluympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen valmistelemiseksi. Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida. Voit aina suorittaa valinnaiset vaiheet myöhemmin.

Katso lisätietoja Commercen esikatseluympäristön määrittelystä kohdasta sen jälkeen, kun olet valmistellut sen [Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md). Jos haluat lisätietoja valinnaisten ominaisuuksien määrittämisestä Commercen esikatseluympäristöön, katso [Lisäominaisuuksien määrittäminen Commercen esikatseluympäristöä varten](cpe-optional-features.md).

Jos haluat lisätietoja valmistelun vaiheista tai jos kohtaat ongelmia, kerro se Microsoftille [Microsoft Dynamics 365 Commerce Preview Yammer -ryhmän](https://aka.ms/Dynamics365CommercePreviewYammer) kautta.

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commerce Preview -ympäristön:

- Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus
- Olet aiemmin luotu Microsoft Dynamics 365 -kumppani tai -asiakas ja pystyt luomaan Dynamics 365 Commerce -projektin.
- Sinut on hyväksytty Dynamics 365 Commerce Preview -ohjelmaan.
- Sinulla on projektin luomisessa vaaditut **Siirrä, luo ratkaisuja ja opi** -kohtien oikeudet.
- Olet **Ympäristövastaava**- tai **Projektin omistaja** -roolin jäsen projektissa, jolle valmistelet ympäristöä.
- Sinulla on järjestelmänvalvojan oikeudet Microsoft Azure -tilausta varten, tai ota yhteyttä tilauksen järjestelmänvalvojaan, joka voi suorittaa puolestasi järjestelmänvalvojan oikeudet vaativat kaksi vaihetta.
- Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.
- Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.
- Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus. (Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)

## <a name="provision-your-commerce-preview-environment"></a>Commercen esikatseluympäristön valmisteleminen

Näissä ohjeissa kerrotaan, miten Commerce Preview -ympäristö tarjotaan. Kun olet suorittanut ne onnistuneesti, Commerce Preview -ympäristö on valmiina konfigurointia varten. Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.

> [!IMPORTANT]
> Esikatselun käyttö on sidottu Commerce-esikatselusovelluksessa määrittämääsi LCS-tiliin ja organisaatioon. Sinun on käytettävä samaa tiliä Commerce Preview -ympäristön tarjoamiseen. Jos sinun täytyy käyttää Commerce Preview -ympäristössä eri LCS-tiliä tai -vuokraajaa, sinun on annettava kyseiset tiedot Microsoftille. Yhteystiedot ovat jäljempänä tämän ohjeaiheen [ Commerce Preview -ympäristön tuki](#commerce-preview-environment-support) -osiossa.

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
> Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan. Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce - esittely (10.0.* x* ja Platform-päivitys *xx*)** näkyy suoraan **Ympäristön nimi** -kentän yläpuolella. Katso tiedot vaiheen 8 jälkeen näkyvästä kuvasta.

1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse **+ Lisää** lisätäksesi ympäristön.
1. Valitse **Sovelluksen versio** -kentässä uusin versio. Jos sinulla on erityinen tarve valita jokin muu sovellusversio kuin uusin versio, älä valitse vanhempaa versiota kuin **10.0.8.**
1. Käytä **Käyttöympäristön versio** -kentässä käyttöympäristö versiota, joka valitaan automaattisesti valitsemaasi sovellusversioon. 

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. Valitse **Seuraava**.
1. Valitse **Esittely** ympäristötopologiaksi.

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. Valitse **Dynamics 365 Commerce - Esittely** ympäristötopologiaksi. Jos olet määrittänyt aiemmin yhden Azure-yhdistimen, sitä käytetään tässä ympäristössä. Jos olet määrittänyt useita Azure-yhdistimiä, voit valita käytettävän yhdistimen: **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat**tai **Länsi-Yhdysvallat 2**. (Parhaan päästä päähän-suorituskyvyn saavuttamiseksi suosittelemme valitsemaan **Länsi-Yhdysvallat 2**.)

    ![Ympäristötopologia 2 valitseminen](./media/project3.png)

1. Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla. Älä muuta Lisäasetukset-kohtaa.

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. Säädä VM:n kokoa tarpeen mukaan. (Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)
1. Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.
1. Valitse **Seuraava**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**. Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.

    Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön. Ympäristön työnkulut kestävät jonkin aikaa. Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.

1. Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.

### <a name="initialize-the-commerce-scale-unit-csu"></a>Alusta Commerce Scale unit (CSU)

Alusta CSU-osoite seuraavien ohjeiden avulla.

1. Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.
1. Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**. Näkyviin tulee ympäristön tietojen näkymä.
1. Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.
1. Valitse **Commerce**-välilehdestä **Alusta**. Näkyviin tulee CSU-alustusparametrien näkymä.
1. Valitse **Alue**-kohdassa **Itä-Yhdysvallat**, **Itä-Yhdysvallat 2**, **Länsi-Yhdysvallat** tai **Länsi-Yhdysvallat 2**.
1. Valitse **Versio**-kentässä **Määritä versio** -luettelosta ja määritä sitten **9.18.20014.4** näyttöön tulevassa kentässä. Muista määrittää tarkka versio, joka on ilmoitettu tässä. Muussa tapauksessa sinun on päivitettävä RCSU oikeaan versioon myöhemmin.
1. Ota käyttöön **Laajennuksen käyttäminen** -vaihtoehto.
1. Valitse laajennusluettelosta **Commerce Preview -esittelyn peruslaajennus**.
1. Valitse **Alusta**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**. **Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **Commerce**-välilehti on valittuna. CSU on asetettu jonoon valmistelua varten.
1. Varmista ennen jatkamista, että CSU:si tila on **Onnistunut**. Alustus kestää noin kahdesta viiteen tuntia.

### <a name="initialize-e-commerce"></a>Sähköisen kaupankäynnin alustaminen

Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.

1. Tarkista esikatselun suostumus **sähköisen kaupankäynnin**-välilehdestä ja valitse sitten **Asetukset**.
1. Kirjoita **Sähköisen kaupankäynnin vuokraajan nimi** -kenttään nimi. Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.
1. Valitse **Commerce Scale -yksikön nimi** -kentässä CSU-luettelosta. (Luettelossa pitäisi olla vain yksi vaihtoehto.)

    **Sähköisen kaupankäynnin paikkatieto** -kenttä määritetään automaattisesti, eikä arvoa voi muuttaa.

1. Jatka valitsemalla **Seuraava**.
1. Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.
1.  **AAD-suojausryhmän järjestelmänhallinta** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain. Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake. Valitse luettelosta oikea suojausryhmä.
2.  **AAD-turvallisuusryhmä luokituksille ja arvosteluvalvoja** -kenttään, kirjoita haluamasi käyttöoikeusryhmän nimen muutama ensimmäinen kirjain. Tuo hakutulokset näkyviin valitsemalla suurennuslasikuvake. Valitse luettelosta oikea suojausryhmä.
1. Jätä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetus päälle.
1. Valitse **Alusta**. **Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **e-Commerce**-välilehti on valittuna. Sähköisen kaupankäynnin alustaminen on aloitettu.
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

[Dynamics 365 Commercen esikatseluympäristön yleiskuvaus](cpe-overview.md)

[Dynamics 365 Commercen esikatseluympäristön määrittäminen](cpe-post-provisioning.md)

[Valinnaisten ominaisuuksien määrittäminen Dynamics 365 Commercen esikatseluympäristöä varten](cpe-optional-features.md)

[Dynamics 365 Commerce -esikatseluympäristön usein kysytyt kysymykset](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)

