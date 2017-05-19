---
title: "Asenna ja määritä Microsoft Dynamics 365 for Operations - Warehousing"
description: "Tässä aiheessa kuvataan, miten asennat ja määrität Microsoft Dynamics 365 for Operations - Warehousing -sovelluksen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bbf6df8d43889e7a62bfe28921997c45c8b4c632
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Asenna ja määritä Microsoft Dynamics 365 for Operations - Warehousing

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, miten asennat ja määrität Microsoft Dynamics 365 for Operations - Warehousing -sovelluksen.

Microsoft Dynamics 365 for Operations - Warehousing on sovellus, joka on saatavilla Windows Storesta ja Googlen Play Storesta. Microsoft Dynamics 365 for Operationsin nykyiselle versiolle tämä sovellus on saatavana erillisenä komponenttina, joka tarkoittaa itsenäistä käyttöönottoa sellaisissa laitteissa, joita käytetään fyysisen varastoinnin tehtävissä. Jotta voisit käyttää sovellusta Dynamics 365 for Operations -ympäristössäsi, sinun on ladattava sovellus kuhunkin laitteeseen ja määrittää se muodostamaan yhteys Dynamics 365 for Operations -ympäristöösi. Tässä aiheessa kuvataan, miten sovellus asennetaan laitteisiin. Artikkelissa kerrotaan myös, miten voit määrittää sovelluksen yhteyden Dynamics 365 for Operations -ympäristöösi.

## <a name="prerequisites"></a>Edellytykset
Sovellus on saatavilla Android- ja Windows-käyttöjärjestelmille. Jos haluat käyttää tätä sovellusta, sinulla on oltava jokin seuraavista tuetuista käyttöjärjestelmistä asennettuna laitteeseen. Sinulla on myös oltava jokin seuraavista tuetuista Dynamics 365 for Operations -versioista. Seuraavan taulukon tietojen avulla voit arvioida, tukeeko laitteisto- ja ohjelmistoympäristösi asentamista.

| Ympäristö                    | Versio                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (kaikki versiot)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations -versio 1611 -TAI- Microsoft Dynamics Dynamics AX -versio 7.0/7.0.1 ja Microsoft Dynamics AX -ympäristön päivitys 2 sekä hotfix KB 3210014 |

## <a name="get-the-app"></a>Hanki sovellus
-   Windows (UWP) - [Dynamics 365 for Operations - Warehousing Windows Storessa](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Warehousing Google Play Storessa](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Luo Active Directoryyn WWW-palvelusovellus
Jotta sovellus toimisi tietyn Dynamics 365 for Operations -palvelimen kanssa, sinun täytyy rekisteröidä verkkopalvelusovellus Azure Active Directoryssä Dynamics 365 for Operations -vuokralaisessa. Tietoturvasyistä on suositeltavaa luoda verkkopalvelusovellus jokaiselle laitteelle, jota käytät. Luo WWW-palvelusovellus Azure Active Directoryssa (Azure AD) seuraavasti:

1.  Siirry web-selaimessa osoitteeseen <https://manage.windowsazure.com>.
2.  Kirjoita nimi ja salasana käyttäjälle, jolla on Azure‑tilauksen käyttöoikeus.
3.  Valitse Azure Portalissa vasemmassa siirtymisruudussa **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-active-directory-example](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  Valitse ruudukossa Active Directory -esiintymä, jota Dynamics 365 for Operations käyttää.
5.  Valitse yläreunan työkalurivissä **Sovellukset**. [![wh-02-active-directory-applications](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  Valitse alaosan ruudussa **Lisää**. Ohjattu **Lisää sovellus** -toiminto käynnistyy.
7.  Anna sovellukselle nimi ja valitse **WWW-sovellus ja/tai web-API-liittymä**. [![wh-03-active-directory-add-application](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Kirjoita kirjautumisen URL-osoite, joka on sovelluksen URL-osoite vuokraajassasi (Operationsin pääkansion URL-osoite). Kirjautumisen URL-osoitetta ei tällä hetkellä aktiivisesti käytetä sovelluksen todennukseen, mutta se on pakollinen kenttä. Kirjoita sama URL-osoite App ID URI -kenttään. [![wh-04-ad-add-properties](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  siirry **Konfiguroi** -välilehteen. [![wh-05-ad-configure-app](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Vieritä alas, kunnes näet **Muiden sovellusten käyttöoikeudet** -osan. Valitse **Lisää sovellus**. [![wh-06-ad-app-add-permissions](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Valitse luettelossa **Microsoft Dynamics ERP**. Valitse **Suorita tarkistus** -painike sivun oikeassa yläkulmassa. [![wh-07-ad-select-permissions](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. Valitse **Edustajan käyttöoikeudet** -luettelossa kaikki valintaruudut. Valitse **Tallenna**. [![wh-08-ad-delegate-permissions](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Merkitse muistiin seuraavat tiedot:
    -   **Asiakastunnus** - kun vierität sivua ylös, näet **Asiakastunnus** -kentän.
    -   **Avain** - Luo **Avaimet**-osassa avain valitsemalla kesto ja kopioi avain. Tähän avaimeen viitataan myöhemmin nimellä **Asiakkaan salasana**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Luo ja määritä käyttäjätili Dynamics 365 for Operationsissa
Jotta Dynamics 365 for Operations voisi käyttää Azure AD -sovellustasi, sinun on suoritettava seuraavat määritysvaiheet:

1.  Luo uusi käyttäjätili Dynamics 365 for Operations -vuokraajan Azure Active Directory -hakemistossa. Tämän käyttäjätilin tarkoituksena on käyttää Warehousing-sovelluksen erityistä mukautettua palvelua, jonka Dynamics 365 for Operations -palvelin tarjoaa. Kun olet suorittanut tämän vaiheen, sinulla on WMDP-käyttäjän tunnistetiedot, jotka koostuvat WMDP-sähköpostiosoitteesta ja WMDP-salasanasta. Lisätietoja käyttäjien lisäämisestä Azure AD -hakemistoon ja Dynamics 365 for Operationsiin on tässä oppaassa: [Rekisteröi Microsoft Dynamics 365 for Operations -tilaus](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Luo Dynamics 365 for Operations -käyttäjä, joka vastaa Warehousing-sovelluksen käyttäjän tunnistetietoja.
    1.  Siirry Dynamics 365 for Operationsissa kohtaan **Järjestelmän hallinta** &gt; **Yleinen** &gt; **Käyttäjät**.
    2.  Luo uusi käyttäjä.
    3.  Määritä Warehouse-mobiililaitteen käyttäjä, kuten seuraavassa kuvakaappauksessa. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Liitä Azure Active Directory -sovelluksesi Warehousing-sovelluksen käyttäjään.
    1.  Siirry Dynamics 365 for Operationsissa kohtaan **Järjestelmän hallinta** &gt; **Asetukset** &gt; **Azure Active Directory -sovellukset**.
    2.  Luo uusi rivi.
    3.  Anna **Asiakastunnus** (saatu edellisessä osassa), anna sille nimi ja valitse aiemmin luotu käyttäjä. Suosittelemme kaikkien laitteiden merkitsemistä niin, että voit helposti poistaa niiden käyttöoikeuden Dynamics 365 for Operationsiin tällä sivulla siltä varalta, että ne ovat kadonneet. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Määritä sovellus
Sinun on määritettävä sovellus laitteessa muodostaaksesi yhteyden Dynamics 365 for Operations -palvelimeen Azure AD -sovelluksen kautta. Toimi seuraavasti.

1.  Siirry sovelluksessa kohtaan **Yhteysasetukset**.
2.  Tyhjennä **Demotila**-kenttä. [![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Anna seuraavat tiedot:- **Azure Active Directory -asiakastunnus** – Asiakastunnus saadaan vaiheessa 13 ohjeessa "Luo Active Directoryyn WWW-palvelusovellus". - **Azure Active Directory -asiakkaan salasana** – Asiakkaan salasana saadaan vaiheessa 13 ohjeessa "Luo Active Directoryyn WWW-palvelusovellus". - **Azure Active Directory -resurssi** – Azure Active Directory -resurssi esittää Dynamics 365 for Operationsin pääkansion URL-osoitetta. **Huomautus**: Älä lopeta tätä kenttää vinoviivalla (/). - **Azure Active Directory -vuokralainen** – Azure Active Directory -vuokralaista käytetään Dynamics 365 for Operations -palvelimen kanssa: https://login.windows.net/&lt;your-AD-tenant-ID&gt;. Esimerkiksi: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Huomautus**: Älä lopeta tätä kenttää vinoviivalla (/). - **Yritys** – Anna Dynamics 365 for Operationsin yritys, johon haluat muodostaa sovelluksella yhteyden. [![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valitse **Takaisin** -painike sovelluksen vasemmassa yläkulmassa. Sovellus muodostaa nyt yhteyden Dynamics 365 for Operations -palvelimeen ja fyysisen varaston työntekijän kirjautumisnäyttö näytetään. [![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Poista laitteen käyttöoikeudet
Jos laite katoaa tai vaarantuu, laitteen käyttöoikeudet Dynamics 365 for Operationsiin pitää poistaa. Seuraavat vaiheet kuvaavat suositeltavaa prosessia käyttöoikeuksien poistamiseksi.

1.  Siirry Dynamics 365 for Operationsissa kohtaan **Järjestelmän hallinta** &gt; **Asetukset** &gt; **Azure Active Directory -sovellukset**.
2.  Poista rivi, joka vastaa laitetta, jonka haluat poistaa. Kirjoita muistiin poistetun laitteen **Asiakastunnus**.
3.  Kirjaudu sisään Azure classic -portaalissa osoitteessa <https://manage.windowsazure.com>.
4.  Valitse **Active Directory** -kuvake vasemmalla olevassa valikossa ja valitse sitten haluamasi kansio.
5.  Valitse yläosan valikosta **Sovellukset**, ja valitse sitten sovellus, jonka haluat määrittää. **Pika-aloitus** -sivu näkyy, ja siinä on kertakirjauksen tiedot ja muut määritystiedot.
6.  Valitse **Konfiguroi**-välilehti, vieritä alaspäin ja varmista, että sovelluksen **Asiakastunnus** on sama kuin tämän osan vaiheessa 2.
7.  Napsauta työkalurivin **Poista**-painiketta.
8.  Valitse vahvistussanomassa **Kyllä**.





