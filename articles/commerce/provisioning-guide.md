---
title: Dynamics 365 Commerce -arviointiympäristön valmisteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8cda79a6be1aca7ad3826b9409e110524e6560e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969898"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce -arviointiympäristön valmisteleminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit valmistella Microsoft Dynamics 365 Commercen arviointiympäristön.

Ennen kuin aloitat, suosittelemme, että tarkistat tämän aiheen nopeasti, jotta saat käsityksen prosessin vaatimista aiheista.

> [!NOTE]
> Commercen arviointiympäristöt eivät ole yleisesti saatavana, ja ne myönnetään kumppaneille ja asiakkaille pyyntökohtaisesti. Pyydä lisätietoja Microsoft-kumppanilta.

## <a name="overview"></a>Yleiskuvaus

Commercen arviointiympäristön onnistunut valmistelu edellyttää sellaisen projektin luontia, jossa on tietty tuotteen nimi ja tyyppi. Ympäristöllä ja Commerce Scale Unit (CSU) -ratkaisulla on myös joitakin tiettyjä parametreja, joita on käytettävä, jos oletat valmistelevasi sähköisen kaupankäynnin myöhemmin. Tämän ohjeaiheen ohjeissa kuvataan kaikki vaiheet, joita tarvitaan valmisteluun, ja parametrit, joita on käytettävä.

Kun olet onnistuneesti valmistellut Commercen arviointiympäristön, sinun on suoritettava muutama valmistelun jälkeinen vaihe sen käyttöönottamista varten. Jotkin vaiheet ovat valinnaisia. Tämä riippuu siitä, mitä järjestelmän alueita haluat arvioida. Voit aina suorittaa valinnaiset vaiheet myöhemmin.

Lisätietoja Commercen arviointiympäristön määrittämistä valmistelun jälkeen on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md). Lisätietoja Commercen arviointiympäristön valinnaisten ominaisuuksien määrittämisestä on kohdassa [Commercen arviointiympäristön valinnaisten ominaisuuksien määrittäminen](cpe-optional-features.md).

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on oltava käytössä, ennen kuin voit määrittää Commercen arviointiympäristön:

- Sinut on otettu mukaan arviointiohjelmaan ja sinulle on annettu kapsiteettia arviointiympäristöä varten.
- Sinulla on Microsoft Dynamics Lifecycle Services -portaalin (LCS) käyttöoikeus
- Olet aiemmin luotu Microsoft Dynamics 365 -kumppani tai -asiakas ja pystyt luomaan Dynamics 365 Commerce -projektin.
- Sinulla on Microsoft Azure -tilauksen järjestelmänvalvojan käyttöoikeus tai olet yhteydessä tilauksen järjestelmänvalvojaan, joka voi avustaa tarvittaessa.
- Sinulla on käytettävissä Azure Active Directory (Azure AD) -vuokralaisen tunnus.
- Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää sähköisen kaupankäynnin järjestelmänvalvojien ryhmänä, ja sinulla on ryhmän tunnus.
- Olet luonut Azure AD -käyttöoikeusryhmän, jota voidaan käyttää arviot ja arvostelut -moderaattorien ryhmänä, ja sinulla on ryhmän tunnus. (Tämä suojausryhmä voi olla sama kuin verkkokauppajärjestelmän järjestelmänvalvojaryhmä.)

Huomaa, että tämä luettelo ei ole täydellinen. Jos ongelmia esiintyy, ota yhteys Microsoft-kumppaniin.

## <a name="provision-your-commerce-evaluation-environment"></a>Commercen arviointiympäristön valmisteleminen

Näissä ohjeissa käsitellään Commercen arviointiympäristö valmistelua. Kun olet suorittanut ne onnistuneesti, Commercen arviointiympäristö on valmis määritettäväksi. Kaikki tässä kuvatut toiminnot tapahtuvat LCS-portaalissa.

### <a name="create-a-new-project"></a>Luo uusi projekti

Noudata seuraavia vaiheita luodaksesi uuden projektin LCS:ssä.

1. Luo projekti valitsemalla LCS-aloitussivulla plusmerkki (**+**).
1. Noudata oikeanpuoleisessa ruudussa jotakin näistä vaiheista:

    - Jos olet kumppani, valitse **Siirrä, luo ratkaisuja ja opi**.
    - Jos olet asiakas, valitse **Mahdolliset myyntiä edeltävät toimet**.

1. Syötä mallin nimi, kuvaus ja toimiala.
1. Valitse **Tuotenimi** -kentässä **Dynamics 365 Commerce**.
1. Valitse **Tuoteversio**-kentässä **Dynamics 365 Commerce**.
1. Valitse **Metodologia**-kentässä **Dynamics Retail -implementointimetodologia**.
1. Valinnainen: Voit tuoda rooleja ja käyttäjiä aiemmin luodusta projektista.
1. Valitse **Luo**. Projektinäkymä avautuu.

### <a name="add-the-azure-connector"></a>Azure-yhdistimen lisääminen

Lisää Azure Connector LCS-projektiin kohdassa [Azure Resource Manager (ARM) -perehdytyksen suorittaminen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding) olevien ohjeiden mukaan.

### <a name="deploy-the-environment"></a>Käyttöönottoympäristö

Määritä ympäristö näiden ohjeiden avulla.

> [!NOTE]
> Vaiheita 6, 7 ja/tai 8 ei ehkä tarvitse suorittaa, koska sivut, joilla on yksi vaihtoehto, ohitetaan. Kun olet **Ympäristön parametrit** -näkymässä, varmista, että teksti **Dynamics 365 Commerce - esittely (10.0.* x* ja Platform-päivitys *xx*)** näkyy suoraan **Ympäristön nimi** -kentän yläpuolella. Katso tiedot vaiheen 8 jälkeen näkyvästä kuvasta.

1. Valitse päävalikosta **Pilvipalveluympäristöt**.
1. Valitse **+ Lisää** lisätäksesi ympäristön.
1. Valitse **Sovelluksen versio** -kentässä uusin versio. Jos sinulla on erityinen tarve valita jokin muu sovellusversio kuin uusin versio, älä valitse vanhempaa versiota kuin **10.0.14.**
1. Käytä **Käyttöympäristön versio** -kentässä käyttöympäristö versiota, joka valitaan automaattisesti valitsemaasi sovellusversioon. 

    ![Sovelluksen ja ympäristön versioiden valitseminen](./media/project1.png)

1. Valitse **Seuraava**.
1. Valitse **Esittely** ympäristötopologiaksi.

    ![Ympäristötopologia 1 valitseminen](./media/project2.png)

1. Anna ympäristön nimi **Ympäristön käyttöönotto** -sivulla. Älä muuta Lisäasetukset-kohtaa.

    ![Ympäristön käyttöönotto -sivu](./media/project4.png)

1. Säädä VM:n kokoa tarpeen mukaan. (Suosittelemme VM:n varastointiyksikköä \[SKU\] **D13 v2**.)
1. Tarkista hinnoittelu- ja lisensointiehdot ja valitse sitten valintaruutu, jos hyväksyt ne.
1. Valitse **Seuraava**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Ota käyttöön**. Sinut siirretään **Pilvipalveluympäristöt**-näkymään ja ympäristösi pitäisi näkyä luettelossa.

    Pyydetty ympäristö näkyy jonossa. Tämän jälkeen se otetaan käyttöön. Ympäristön työnkulut kestävät jonkin aikaa. Tarkista tilanne, kun aikaa on kulunut noin kuudesta yhdeksään tuntiin.

1. Varmista ennen jatkamista, että ympäristösi tila on **Otettu käyttöön**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Alusta Commerce Scale Unit (pilvi)

Alusta CSU seuraavien ohjeiden avulla.

1. Valitse **Pilvipalveluympäristöt**-näkymässä luettelosta ympäristösi.
1. Valitse oikealla olevasta ympäristön näkymästä **Täydet tiedot**. Näkyviin tulee ympäristön tietojen näkymä.
1. Valitse **Ympäristön ominaisuudet** -kohdassa **Hallitse**.
1. Valitse **Commerce**-välilehdestä **Alusta**. Näkyviin tulee CSU-alustusparametrien näkymä.
1. Valitse **Alue**-kentässä alue, joka on sama alue tai lähellä sitä aluetta, jossa ympäristö otettiin käyttöön.
1. Älä tee muutoksia **Versio**-kenttään.
1. Valitse **Alusta**.
1. Kun tietojen oikeellisuus on vahvistettu käyttöönoton vahvistussivulla, valitse **Kyllä**. **Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **Commerce**-välilehti on valittuna. CSU on asetettu jonoon valmistelua varten.
1. Varmista ennen jatkamista, että CSU:si tila on **Onnistunut**. Alustus kestää noin kahdesta viiteen tuntia.

Jos **Hallinta**-linkki ei ole ympäristön tietonäkymässä, ota yhteys Microsoftin yhteyshenkilöön.

Seuraava virhesanoma saattaa tulla näyttöön käyttöönottoprosessin aikana:

> Arviointiympäristöjen (esittely/testi) on rekisteröitävä Scale Unit Connector -sovellus \<application ID\> headquarters-sovelluksessa.

Jos CSU-alustus epäonnistuu ja näyttöön tulee tämä virhesanoma, merkitse muistiin sovelluksen tunnus, joka on yleinen yksilöivä tunnus (GUID) ja rekisteröi CSU-käyttöönottosovellus Commerce headquarters -sovelluksessa noudattamalla seuraavan osan ohjeita.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>Rekisteröi CSU-käyttöönottosovellus Commerce headquarters -sovelluksessa (jos pakollinen).

Rekisteröi CSU-käyttöönottosovellus Commerce headquarters -sovelluksessa seuraavasti.

1. Siirry Commerce headquarters -sovelluksessa kohtaan **Järjestelmän hallinta \> Asetukset \> Azure Active Directory -sovellukset**.
1. Kirjoita vastaanottamasi CSU-alustuksen virhesanoman sovellustunnus **Asiakastunnus**-sarakkeeseen.
1. Kirjoita **Nimi**-sarakkeeseen mikä tahansa kuvaava teksti (esimerkiksi **CSU Eval**).
1. Kirjoita **Käyttäjätunnus**-sarakkeeseen **RetailServiceAccount**.
1. Yritä CSU-alustusta ja käyttöönottoa uudelleen LCS:stä.

### <a name="initialize-e-commerce"></a>Sähköisen kaupankäynnin alustaminen

Alusta sähköinen kaupankäynti seuraavien ohjeiden avulla.

1. Tarkista arviointiversion suostumus **Sähköinen kaupankäynti**-välilehdessä ja valitse sitten **Asetukset**.
1. Anna **Sähköisen kaupankäynnin ympäristön nimi** -kenttään nimi. Ota huomioon, että tämä nimi näkyy joissakin sähköisen kaupankäynnin esiintymään vievissä URL-osoitteissa.
1. Valitse **Commerce Scale Unitin nimi** -kentässä CSU-luettelosta. (Luettelossa pitäisi olla vain yksi vaihtoehto.)

    **Sähköisen kaupankäynnin maantieteellinen alue** -kenttä täytetään automaattisesti.

1. Jatka valitsemalla **Seuraava**.
1. Kirjoita **Tuetut isäntänimet** -kenttään mikä tahansa kelvollinen toimialue, kuten `www.fabrikam.com`.
1. Anna **Järjestelmänvalvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake. Valitse luettelossa oikea käyttöoikeusryhmä.
1.  Anna **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä** -kentässä käytettävän käyttöoikeusryhmän nimen kaksi ensimmäistä kirjainta ja näytä sitten hakutulokset valitsemalla suurennuslasikuvake. Valitse luettelossa oikea käyttöoikeusryhmä.
1. Jätä **Ota luokitukset ja arvostelupalvelu käyttöön** -asetuksen arvoksi **Kyllä**.
1. Valitse **Alusta**. **Commercen hallinta** -näkymä tulee uudelleen näkyviin, kun **e-Commerce**-välilehti on valittuna. Sähköisen kaupankäynnin alustaminen on aloitettu.
1. Ennen kuin jatkat, odota, kunnes sähköisen kaupankäynnin alustamisen tila on **Alustaminen onnistui**.
1. Merkitse oikeassa alakulmassa olevassa **Linkit**-kohdassa seuraavien linkkien URL-osoitteet:

    * **Sähköisen kaupankäynnin sivusto** – linkki verkkokaupan sivustosi juureen.
    * **Commerce-sivuston luontiohjelma** – linkki sivuston hallintatyökaluun.

## <a name="next-steps"></a>Seuraavat vaiheet

Tietoja Commercen arviointiympäristön valmistelu- ja määritysprosessin jatkamisesta on kohdassa [Commercen arviointiympäristön määrittäminen](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -arviointiympäristön yleiskuvaus](cpe-overview.md)

[Dynamics 365 Commerce -arviointiympäristön määritykset](cpe-post-provisioning.md)

[BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä](cpe-bopis.md)

[Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset](cpe-optional-features.md)

[Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (pilvi)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]