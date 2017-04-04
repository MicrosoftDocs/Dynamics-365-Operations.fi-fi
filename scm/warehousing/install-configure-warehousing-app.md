---
title: "Asenna ja määritä Microsoft Dynamics-365 toimintojen & #8211; Varastointi"
description: "Tässä aiheessa kuvataan, miten Asenna ja määritä Microsoft Dynamics-365 työvaiheiden - varastoinnista."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 231c087ddc976aa552fc9cd6c89188f82a0247d1
ms.lasthandoff: 03/31/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Asenna ja määritä Microsoft Dynamics-365 toimintojen & #8211; Varastointi

Tässä aiheessa kuvataan, miten Asenna ja määritä Microsoft Dynamics-365 työvaiheiden - varastoinnista.

Dynamics 365 työvaiheiden - varastoinnista on sovelluksen käytettävissä Windows Storen ja Googlen Play Store. Microsoft Dynamics-365 toimintojen nykyisen version tämän app on saatavana erillinen komponentti, joka tarkoittaa itsenäisen käyttöönoton sellaisissa laitteissa, fyysisen varastoinnin tehtävien. Dynamics-365-sovellus käyttää toimintojen ympäristön, lataa app kunkin laitteen ja määrittää muodostamaan yhteyttä Dynamics 365 toimia ympäristön. Tässä aiheessa kuvataan, miten sovellus asennetaan laitteita. Artikkelissa kerrotaan myös app muodostaa yhteyttä Dynamics 365 ympäristön toimintojen määrittämisestä.

## <a name="prerequisites"></a>Edellytykset
Sovellus voi käyttää Android ja Windows-käyttöjärjestelmissä. Jos haluat käyttää tätä app, on oltava jokin tuetut käyttöjärjestelmät asennettu laitteeseen. Sinulla on myös oltava jokin seuraavien tuettujen versioiden Dynamics 365 operaatioille. Seuraavan taulukon tietojen avulla voit arvioida, jos laitteisto- ja ohjelmisto-ympäristössä on valmiina tukemaan asentamista.

| Ympäristö                    | Versio                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | 10 Windows (kaikki versiot)                                                                                                                                                   |
| Työvaiheiden Dynamics 365 | Päivitä Microsoft Dynamics-365-toimintojen 1611 - tai - Microsoft Dynamics Dynamics AX: N versio 7.0/7.0.1 ja Microsoft Dynamics AX-platform 2 KB 3210014-korjaustiedoston |

## <a name="get-the-app"></a>Hanki app
-   Windows (UWP) - [toiminnoissa - varastoinnista Windows Store-365 Dynamics](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 työvaiheiden - Google Play Store-varastointi](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Luo Active Directoryyn WWW-palvelusovellus
Tietyn Dynamics 365 palvelimen toimintojen kanssa app jotta sinun täytyy rekisteröityä palvelun verkkosovelluksen Azure Active Directory-toimintojen vuokralaisen osalta Dynamics-365. Tietoturvasyistä on suositeltavaa luoda web service-sovelluksen jokaiselle laitteelle, jota käytät. Luo WWW-palvelusovelluksen Azure Active Directory (Azure AD), tee seuraavat toimet:

1.  Siirry web-selaimessa, <https://manage.windowsazure.com>.
2.  Kirjoita nimi ja salasana, käyttäjä, jolla on Azure ‑tilauksen käyttöoikeuden.
3.  Azure Portalissa vasemmasta siirtymisruudusta valitsemalla **Active Directoryn**. [](./media/wh-01-active-directory-example.png)[![mi-01-aktiivinen-directory-Esimerkki](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Ruudukossa Valitse Active Directory-esiintymään, jota käytetään työvaiheen Dynamics 365.
5.  Valitse yläreunan työkalurivi, **sovelluksia**. [![Mi-02-aktiivinen-directory-sovellukset](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Valitse alaruudun **Lisää**. **Lisätä sovelluksen** ohjattu toiminto käynnistyy.
7.  Sovellus ja valitse nimi **WWW-sovelluksessa tai web-API-Liittymän**. [![Wh-03-Active-Directory-Add-Application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Kirjoita Sign-URL-osoite, joka on palveltava, pääkansion URL toiminnot-sovelluksen URL-osoite. URL-osoite-on parhaillaan ei aktiivisesti käytetä-sovelluksen todennuksen, mutta se on pakollinen kenttä. Kirjoita saman URL-Osoitteen App ID-URI-kenttään. [![Mi-04-ad--ominaisuuksien lisääminen](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Siirry **määrittäminen** välilehti. [![Mi-05-ad-Määritä-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Vieritä alas, kunnes näet **muiden sovellusten käyttöoikeudet** osan. Valitse **lisätä sovelluksen**. [![Wh-06-AD-App-Add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Valitse **Microsoft Dynamics ERP** -luettelosta. Valitse **suorittaa tarkistus** -painiketta sivun oikeassa yläkulmassa. [![Mi-07-ad-select-oikeudet](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. - **Edustajien oikeudet** -luettelon kaikki valintaruudut. Click **Save**. [![Mi-08-ad-edustajien-oikeudet](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Merkitse muistiin seuraavat tiedot:
    -   **Asiakkaan tunnus** - vierittää ylös-sivulla näet **asiakkaan tunnus** näkyviin.
    -   **Avain** - ja **avaimet** jakso ja luo avain kesto valitsemalla Kopioi avaimen. Tämä avain myöhemmin nimitystä **asiakkaan salaisuus**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Luoda ja määrittää käyttäjätilin Dynamics 365 operaatioille
Jotta 365 Dynamics Azure AD-sovelluksen toimintoihin, edellyttää kokoonpanon seuraavasti:

1.  Luo uusi käyttäjätili Azure Active Directory-toimintojen vuokralaisen osalta Dynamics-365. Tämän käyttäjätilin tarkoituksena on käyttää laajemmissa app, joka aiheuttaa palvelimen toimintojen Dynamics-365 erityisiä asiakaspalvelu. Kun olet suorittanut tämän vaiheen, jos sinulla on WMDP käyttäjän tunnistetiedot, jotka koostuvat WMDP-sähköpostiosoite ja salasana WMDP. Lisätietoja käyttäjien lisäämisestä Azure AD perusvaiheet Dynamics 365 toimintoja, ja tässä opetusohjelmassa: [rekisteröityä Microsoft Dynamics-365 toimintojen tilauksen](/dynamics365/operations/dev-itpro/sign-up-preview-subscription).
2.  Luo Dynamics-365 toimintoja käyttäjälle, joka vastaa laajemmissa app käyttäjän tunnistetietoja.
    1.  Siirry Dynamics työvaiheiden 365, **järjestelmän hallinta**&gt;**yhteisen**&gt;**käyttäjät**.
    2.  Luo uusi käyttäjä.
    3.  Määritä fyysisen varastoinnin kannettavan laitteen käyttäjä, kuten seuraava kuva. [![Wh-09-Add-User-Security-Role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Liitä laajemmissa app käyttäjän Azure Active Directory-sovelluksesi.
    1.  Siirry Dynamics työvaiheiden 365, **järjestelmän hallinta**&gt;**asennus**&gt;**Azure Active Directoryyn sovellusten**.
    2.  Luo uusi rivi.
    3.  Anna **asiakkaan tunnus** (saatu viimeisessä osassa), anna sille nimi ja valitse aiemmin luotu-käyttäjä. Suosittelemme kaikkien laitteiden merkitseminen niin, että voit helposti poistaa käyttöoikeuden Dynamics 365 toimille tällä sivulla siltä varalta, että ne ovat kadonneet. [![Mi 10-ad-sovellukset-lomake](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Määritä sovellus
Sinun on määritettävä sovelluksen laitteen muodostaa yhteyden palvelimen toimintojen Azure AD soveltamalla Dynamics-365. Voit tehdä tämän toimimalla seuraavasti.

1.  Siirry app, **yhteysasetukset**.
2.  Tyhjennä **demotila** kenttä. [![Wh-11-App-Connection-Settings-Demo-Mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Anna seuraavat tiedot:- **Azure Active directory-Asiakastunnus** -asiakas ID saadaan vaiheessa 13 "Active Directory-palvelun verkkosovelluksen luominen". - **Azure Active directory-asiakkaan secret** -client-secret saadaan vaiheessa 13 "Active Directory-palvelun verkkosovelluksen luominen". - **Azure Active directory-resurssiin** -Azure Active directory-resurssiin esittää Dynamics 365 toimintojen ensisijaisen URL-osoitteen. **Huomautus**: Älä lopeta tähän kenttään vinoviivan (/). - **Azure Active directory-vuokralaisen** -vuokralaisen Azure Active directory käyttää Dynamics 365 palvelimen toimintoja: https://login.windows.net/&lt;your-AD-vuokralaisen-ID&gt;. Esimerkki: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Huomautus**: Älä lopeta tähän kenttään vinoviivan (/). - **Yritys** -Kirjoita yritys, johon haluat muodostaa sovelluksen toimintojen Dynamics 365. [![Ki 12-app-yhteys-asetukset](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valitse **takaisin** painiketta vasemmassa yläkulmassa hakemus. Sovellus muodostaa yhteyden palvelimen toiminnot oman Dynamics 365 ja fyysisen varaston työntekijän kirjautumisnäyttö näytetään. [![Mi-13-login-näyttö](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Poista laitteen käyttö
Jos menettää tai vaarantuneen, laite käyttää laitteen toimintoja Dynamics 365 on poistettava. Seuraavat vaiheet kuvaavat suositeltavaa prosessia voit poistaa käyttöoikeudet.

1.  Siirry Dynamics työvaiheiden 365, **järjestelmän hallinta**&gt;**asennus**&gt;**Azure Active Directoryyn sovellusten**.
2.  Poista rivi, joka vastaa laitteen, jonka haluat poistaa. Huomautus alas **asiakkaan tunnus** käytetty laite poistetaan.
3.  Kirjaudu sisään Azure classic-portaalissa osoitteessa <https://manage.windowsazure.com>.
4.  Valitse **Active Directoryn** kuvaketta vasemmalla olevasta valikosta ja valitse sitten haluamasi kansio.
5.  Valitse yläosan valikosta **sovelluksia**, ja valitse sitten sovellus, jonka haluat määrittää. **Pika-aloitus** sivu näkyy kertakirjauksen ja muut tiedot.
6.  Valitse **määrittäminen** välilehti, vieritä alas ja varmistaa, että **Asiakastunnus** sovellus on sama kuin vaiheessa 2 Tässä jaksossa.
7.  Valitse **poistaa** -painiketta komentopalkista.
8.  Valitse **Kyllä** vahvistussanomassa.



