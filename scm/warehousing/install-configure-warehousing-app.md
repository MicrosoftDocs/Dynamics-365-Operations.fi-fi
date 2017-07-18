---
title: "Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen asentaminen ja määrittäminen"
description: "Tässä ohjeaiheessa kerrotaan, miten asennat ja määrität Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: 2e6b0fb81396eef945dbce3be8aee17c9fd455bc
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen asentaminen ja määrittäminen

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten asennat ja määrität Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen.

Finance and Operations – varastointi on sovellus, joka on saatavilla Windows Storesta ja Googlen Play Storesta. Finance and Operationsin nykyiselle versiolle tämä sovellus on saatavana erillisenä komponenttina, joka tarkoittaa itsenäistä käyttöönottoa sellaisissa laitteissa, joita käytetään fyysisen varastoinnin tehtävissä. Jotta voisit käyttää sovellusta Finance and Operations -ympäristössäsi, sinun on ladattava sovellus kuhunkin laitteeseen ja määrittää se muodostamaan yhteys Finance and Operations -ympäristöösi. Tässä aiheessa kuvataan, miten sovellus asennetaan laitteisiin. Artikkelissa kerrotaan myös, miten voit määrittää sovelluksen yhteyden Finance and Operations -ympäristöösi.

## <a name="prerequisites"></a>Edellytykset
Sovellus on saatavilla Android- ja Windows-käyttöjärjestelmille. Jos haluat käyttää tätä sovellusta, sinulla on oltava jokin seuraavista tuetuista käyttöjärjestelmistä asennettuna laitteeseen. Sinulla on myös oltava jokin seuraavista tuetuista Finance and Operationsin versioista. Seuraavan taulukon tietojen avulla voit arvioida, tukeeko laitteisto- ja ohjelmistoympäristösi asentamista.

| Ympäristö                    | Versio                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (kaikki versiot)                                                                                                                                                   |
| Finance and Operations | Microsoft Finance and Operations versio 1611 <br>-tai- <br>Microsoft Dynamics Dynamics AX:n versio 7.0/7.0.1 ja Microsoft Dynamics AX -ympäristöpäivitys 2 ja hotfix-korjaus KB 3210014 |

## <a name="get-the-app"></a>Hanki sovellus
-   Windows (UWP): [Finance and Operationsin varastointisovellus Windows-kaupassa](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android:
    - [Finance and Operationsin varastointisovellus Google Play Storessa](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)
    - [Finance and Operationsin varastointisovellus Zebra App Galleryssa](https://appgallery.zebra.com/showcase/apps/146?type=showcase)

## <a name="create-a-web-service-application-in-active-directory"></a>Luo Active Directoryyn WWW-palvelusovellus
Jotta sovellus toimisi tietyn Finance and Operations -palvelimen kanssa, sinun täytyy rekisteröidä verkkopalvelusovellus Azure Active Directoryssä Finance and Operationsin vuokralaisessa. Tietoturvasyistä on suositeltavaa luoda verkkopalvelusovellus jokaiselle laitteelle, jota käytät. Luo WWW-palvelusovellus Azure Active Directoryssa (Azure AD) seuraavasti:

1.  Siirry web-selaimessa osoitteeseen <https://manage.windowsazure.com>.
2.  Kirjoita nimi ja salasana käyttäjälle, jolla on Azure‑tilauksen käyttöoikeus.
3.  Valitse Azure Portalissa vasemmassa siirtymisruudussa **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Valitse ruudukossa Finance and Operationsin käyttämä Active Directory -esiintymä.
5.  Valitse yläreunan työkalurivissä **Sovellukset**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Valitse alaosan ruudussa **Lisää**. Ohjattu **Lisää sovellus** -toiminto käynnistyy.
7.  Anna sovellukselle nimi ja valitse **WWW-sovellus ja/tai web-API-liittymä**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Anna kirjautumisen URL-osoite, joka on verkkosovelluksen URL-osoite. Tämä URL-osoite on sama kuin käyttöönoton URL-osoite, mutta sen loppuun lisätään oauth. Anna sovelluksen tunnuksen URI. Tämä arvo on pakollinen, mutta sitä ei tarvita todennuksessa. Varmista, että tämä sovellustunnuksen URI on URI-jäljitelmä, kuten https://contosooperations/wmapp, sillä käyttöönoton URL-osoitteen käyttö voi aiheuttaa kirjautumisongelmia muissa ADD-sovelluksissa, kuten Excel-lisäosassa. [![WH-04-AD-add-properties3](./media/WH-04-AD-add-properties3.png)](./media/WH-04-AD-add-properties3.png)
9.  siirry **Konfiguroi** -välilehteen. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Vieritä alas, kunnes näet **Muiden sovellusten käyttöoikeudet** -osan. Valitse **Lisää sovellus**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Valitse luettelossa **Microsoft Dynamics ERP**. Valitse **Suorita tarkistus** -painike sivun oikeassa yläkulmassa. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Valitse **Edustajan käyttöoikeudet** -luettelossa kaikki valintaruudut. Valitse **Tallenna**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Merkitse muistiin seuraavat tiedot:
    -   **Asiakastunnus** - kun vierität sivua ylös, näet **Asiakastunnus** -kentän.
    -   **Avain** - Luo **Avaimet**-osassa avain valitsemalla kesto ja kopioi avain. Tähän avaimeen viitataan myöhemmin nimellä **Asiakkaan salasana**.

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Finance and Operationsin käyttäjätilin luominen ja määrittäminen
Jotta Finance and Operations voisi käyttää Azure AD -sovellustasi, sinun on suoritettava seuraavat määritysvaiheet:

1.  Luo uusi käyttäjätili Finance and Operationsin vuokraajan Azure Active Directory -hakemistossa. Tämän käyttäjätilin tarkoituksena on käyttää varastointisovelluksen erityistä mukautettua palvelua, jonka Finance and Operations -palvelin tarjoaa. Kun olet suorittanut tämän vaiheen, sinulla on WMDP-käyttäjän tunnistetiedot, jotka koostuvat WMDP-sähköpostiosoitteesta ja WMDP-salasanasta. Lisätietoja käyttäjien lisäämisestä Azure AD -hakemistoon ja Finance and Operationsiin on seuraavassa oppaassa: [Finance and Operations -tilauksen rekisteröinti](/dynamics365/unified-operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Luo Finance and Operationsin käyttäjä, joka vastaa varastointisovelluksen käyttäjän tunnistetietoja.
    1.  Siirry Finance and Operationsissa kohtaan **Järjestelmän hallinta** &gt; **Yleinen** &gt; **Käyttäjät**.
    2.  Luo uusi käyttäjä.
    3.  Määritä Warehouse-mobiililaitteen käyttäjä, kuten seuraavassa kuvakaappauksessa. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Liitä Azure Active Directory -sovelluksesi Warehousing-sovelluksen käyttäjään.
    1.  Finance and Operationsissa kohtaan **Järjestelmän hallinta** &gt; **Asetukset** &gt; **Azure Active Directory -sovellukset**.
    2.  Luo uusi rivi.
    3.  Anna **Asiakastunnus** (saatu edellisessä osassa), anna sille nimi ja valitse aiemmin luotu käyttäjä. Suosittelemme kaikkien laitteiden merkitsemistä niin, että voit helposti poistaa niiden Finance and Operationsin käyttöoikeuden tällä sivulla siltä varalta, että ne ovat kadonneet. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Määritä sovellus
Sinun on määritettävä sovellus laitteessa muodostaaksesi yhteyden Finance and Operations -palvelimeen Azure AD -sovelluksen kautta. Toimi seuraavasti.

1.  Siirry sovelluksessa kohtaan **Yhteysasetukset**.
2.  Tyhjennä **Demotila**-kenttä. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Kirjoita seuraavat tiedot: 
    + **Azure Active Directory -asiakkaan tunnus** – asiakkaan tunnus saadaan vaiheessa 13 kohdassa Verkkopalvelusovelluksen luominen Active Directoryssa. 
    + **Azure Active Directory -asiakkaan salasana** – Asiakkaan salasana saadaan vaiheessa 13 kohdassa Verkkopalvelusovelluksen luominen Active Directoryssa. 
    + **Azure Active Directory -resurssi** – Azure AD -resurssi esittää Finance and Operationsin pääkansion URL-osoitetta. **Huomautus**: Älä lopeta tätä kenttää vinoviivalla (/). 
    + **Azure Active Directory -vuokralainen** – Azure AD -vuokralaista käytetään Finance and Operations -palvelimen kanssa: https://login.windows.net/your-AD-tenant-ID. Esimerkiksi: https://login.windows.net/contosooperations.onmicrosoft.com. 
    <br>**Huomautus**: Älä lopeta tätä kenttää vinoviivalla (/). 
    + **Yritys** – Anna Finance and Operationsin yritys, johon haluat muodostaa sovelluksella yhteyden. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valitse **Takaisin** -painike sovelluksen vasemmassa yläkulmassa. Sovellus muodostaa nyt yhteyden Finance and Operations -palvelimeen ja fyysisen varaston työntekijän kirjautumisnäyttö avautuu. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Poista laitteen käyttöoikeudet
Jos laite katoaa tai vaarantuu, laitteen Finance and Operationsin käyttöoikeuden on poistettava. Seuraavat vaiheet kuvaavat suositeltavaa prosessia käyttöoikeuksien poistamiseksi.

1.  Finance and Operationsissa kohtaan **Järjestelmän hallinta** &gt; **Asetukset** &gt; **Azure Active Directory -sovellukset**.
2.  Poista rivi, joka vastaa laitetta, jonka haluat poistaa. Kirjoita muistiin poistetun laitteen **Asiakastunnus**.
3.  Kirjaudu sisään Azure classic -portaalissa osoitteessa <https://manage.windowsazure.com>.
4.  Valitse **Active Directory** -kuvake vasemmalla olevassa valikossa ja valitse sitten haluamasi kansio.
5.  Valitse yläosan valikosta **Sovellukset**, ja valitse sitten sovellus, jonka haluat määrittää. **Pika-aloitus** -sivu näkyy, ja siinä on kertakirjauksen tiedot ja muut määritystiedot.
6.  Valitse **Konfiguroi**-välilehti, vieritä alaspäin ja varmista, että sovelluksen **Asiakastunnus** on sama kuin tämän osan vaiheessa 2.
7.  Napsauta työkalurivin **Poista**-painiketta.
8.  Valitse vahvistussanomassa **Kyllä**.





