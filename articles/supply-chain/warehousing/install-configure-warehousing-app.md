---
title: Microsoft Dynamics 365 for Finance and Operationsin asentaminen ja määrittäminen &#8211; varastointi
description: Tässä ohjeaiheessa kerrotaan, miten asennat ja määrität Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5e99351d79cb5898c6d5565d3d3197a8fe860df
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559183"
---
# <a name="install-and-configure-microsoft-dynamics-365-for-finance-and-operations-8211-warehousing"></a>Microsoft Dynamics 365 for Finance and Operationsin asentaminen ja määrittäminen &#8211; varastointi

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> Tässä ohjeaiheessa käsitellään pilvikäyttöönottojen varastoinnin määrittämistä. Lisätietoja varastoinnin määrittämisestä paikallisissa käyttöönotoissa on kohdassa [Varastointi paikallisissa käyttöönottoja](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


Tässä ohjeaiheessa kerrotaan, miten asennat ja määrität Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen.

Finance and Operations – varastointi on sovellus, joka on saatavilla Windows Storesta ja Googlen Play Storesta. Finance and Operationsin nykyiselle versiolle tämä sovellus on saatavana erillisenä komponenttina, joka tarkoittaa itsenäistä käyttöönottoa sellaisissa laitteissa, joita käytetään fyysisen varastoinnin tehtävissä. Jotta voisit käyttää sovellusta Finance and Operations -ympäristössäsi, sinun on ladattava sovellus kuhunkin laitteeseen ja määrittää se muodostamaan yhteys Finance and Operations -ympäristöösi. Tässä aiheessa kuvataan, miten sovellus asennetaan laitteisiin. Artikkelissa kerrotaan myös, miten voit määrittää sovelluksen yhteyden Finance and Operations -ympäristöösi.

## <a name="prerequisites"></a>Edellytykset
Sovellus on saatavilla Android- ja Windows-käyttöjärjestelmille. Jos haluat käyttää tätä sovellusta, sinulla on oltava jokin seuraavista tuetuista käyttöjärjestelmistä asennettuna laitteeseen. Sinulla on myös oltava jokin seuraavista tuetuista Finance and Operationsin versioista. Seuraavan taulukon tietojen avulla voit arvioida, tukeeko laitteisto- ja ohjelmistoympäristösi asentamista.

| Ympäristö                    | Versio                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (kaikki versiot)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, versio 1611 <br>-tai- <br>Microsoft Dynamics AX:n versio 7.0/7.0.1 ja Microsoft Dynamics AX platform update 2 ja hotfix-korjaus KB 3210014 |

## <a name="get-the-app"></a>Hanki sovellus
-   Windows (UWP)
     - [Finance and Operationsin varastointisovellus Windows-kaupassa](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operationsin varastointisovellus Google Play Storessa](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery on poistettu, joten Finance and Operationsin varastointisovellusta ei voi enää ladata kyseisestä sijainnista.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Verkkosovelluksen luominen Azure Active Directoryssa
Jotta sovellus toimisi tietyn Finance and Operations -palvelimen kanssa, sinun täytyy rekisteröidä verkkopalvelusovellus Azure Active Directoryssä Finance and Operationsin vuokraajassa. Tietoturvasyistä on suositeltavaa luoda verkkopalvelusovellus jokaiselle laitteelle, jota käytät. Luo verkkopalvelusovellus Azure Active Directoryssä (Azure AD) seuraavasti:

1.  Siirry selaimessa osoitteeseen <https://portal.azure.com>.
2.  Kirjoita nimi ja salasana käyttäjälle, jolla on Azure‑tilauksen käyttöoikeus.
3.  Valitse Azure Portalin vasemmassa siirtymisruudussa **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Varmista, että Finance and Operations käyttää kyseistä Active Directory -esiintymää.
5.  Valitse luettelossa **sovelluksen rekisteröinnit**. [![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  Valitse yläruudussa **uuden sovelluksen rekisteröinti**. Ohjattu **Lisää sovellus** -toiminto käynnistyy.
7.  Anna sovellukselle nimi ja valitse **verkkosovellus tai verkon ohjelmointirajapinta**. Anna kirjautumisen URL-osoite, joka on verkkosovelluksen URL-osoite. Tämä URL-osoite on sama kuin käyttöönoton URL-osoite, mutta sen loppuun lisätään oauth. Valitse **Luo**. [![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Valitse luettelossa uusi sovellus. [![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Muista **sovelluksen tunnus**, sillä tarvitse sitä myöhemmin. **Sovelluksen tunnusta** kutsutaan myöhemmin **asiakastunnukseksi**.
10. Valitse **asetusruudussa** **avaimet**. Luo avain antamalla avaimen kuvaus ja kesto **salasanojen** osiossa. 
11. Valitse **tallennus** ja kopioi avain. Tähän avaimeen viitataan myöhemmin nimellä **Asiakkaan salasana**. [![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)

## <a name="create-and-configure-a-user-account-in-finance-and-operations"></a>Finance and Operationsin käyttäjätilin luominen ja määrittäminen
Jotta Finance and Operations voisi käyttää Azure AD -sovellustasi, sinun on suoritettava seuraavat määritysvaiheet:

1.  Luo Finance and Operationsin käyttäjä, joka vastaa varastointisovelluksen käyttäjän tunnistetietoja.
    1.  Siirry Finance and Operationsissa kohtaan **Järjestelmän hallinta** &gt; **Yleinen** &gt; **Käyttäjät**.
    2.  Luo uusi käyttäjä.
    3.  Määritä Warehouse-mobiililaitteen käyttäjä, kuten seuraavassa kuvakaappauksessa. [![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Liitä Azure Active Directory -sovelluksesi Warehousing-sovelluksen käyttäjään.
    1.  Valitse Finance and Operationsissa **Järjestelmän hallinta** &gt; **Asetukset** &gt; **Azure Active Directory -sovellukset**.
    2.  Luo uusi rivi.
    3.  Anna **Asiakastunnus** (saatu edellisessä osassa), anna sille nimi ja valitse aiemmin luotu käyttäjä. Suosittelemme kaikkien laitteiden merkitsemistä niin, että voit helposti poistaa niiden Finance and Operationsin käyttöoikeuden tällä sivulla siltä varalta, että ne ovat kadonneet. [![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Määritä sovellus
Sinun on määritettävä sovellus laitteessa muodostaaksesi yhteyden Finance and Operations -palvelimeen Azure AD -sovelluksen kautta. Toimi seuraavasti.

1.  Siirry sovelluksessa kohtaan **Yhteysasetukset**.
2.  Tyhjennä **Demotila**-kenttä. <br>[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Kirjoita seuraavat tiedot: 
    + **Azure Active -asiakkaan tunnus** – asiakkaan tunnus saadaan vaiheessa 9 kohdassa Verkkopalvelusovelluksen luominen Active Directoryssa. 
    + **Azure Active directory -asiakkaan salasana** – Asiakkaan salasana saadaan vaiheessa 11 kohdassa Verkkopalvelusovelluksen luominen Active Directoryssa. 
    + **Azure Active directory -resurssi** - Azure AD -resurssi esittää Finance and Operationsin pääkansion URL-osoitetta. **Huomautus**: Älä lopeta tätä kenttää vinoviivalla (/). 
    + **Azure Active directory -vuokraaja** - Azure AD -vuokraajaa käytetään Finance and Operations -palvelimen kanssa: `https://login.windows.net/your-AD-tenant-ID`. Esimerkki: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Huomautus**: Älä lopeta tätä kenttää vinoviivalla (/). 
    + **Yritys** – Anna Finance and Operationsin yritys, johon haluat muodostaa sovelluksella yhteyden. <br>[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Valitse **Takaisin** -painike sovelluksen vasemmassa yläkulmassa. Sovellus muodostaa nyt yhteyden Finance and Operations -palvelimeen ja fyysisen varaston työntekijän kirjautumisnäyttö avautuu. <br>[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Lisätietoja Dynamics 365 for Finance and Operations – varastoinnin määrittämisestä lukemaan viivakoodeja mobiililaitteen kameralla on kohdassa [Viivakoodien lukeminen kameran avulla Dynamics 365 for Finance and Operations – varastoinnissa](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Poista laitteen käyttöoikeudet
Jos laite katoaa tai vaarantuu, laitteen Finance and Operationsin käyttöoikeuden on poistettava. Seuraavat vaiheet kuvaavat suositeltavaa prosessia käyttöoikeuksien poistamiseksi.

1.  Valitse Finance and Operationsissa **Järjestelmän hallinta** &gt; **Asetukset** &gt; **Azure Active Directory -sovellukset**.
2.  Poista rivi, joka vastaa laitetta, jonka haluat poistaa. Muista irrotetun laitteen **asiakastunnus**, sillä tarvitset sitä myöhemmin.
3.  Kirjaudu Azure-portaalin osoitteessa <https://portal.azure.com>.
4.  Valitse vasemmassa valikossa **Active Directory** ja varmista, että olet oikeassa hakemistossa.
5.  Valitse luettelossa ensin **sovelluksen rekisteröinnit** ja sitten määritettävä sovellus. Avautuvalla **asetusten** sivulla on määritystiedot.
6.  Varmista, että sovelluksen **asiakastunnus** on sama kuin tämän osan vaiheessa 2.
7.  Valitse yläruudussa **Poista**.
8.  Valitse vahvistussanomassa **Kyllä**.
