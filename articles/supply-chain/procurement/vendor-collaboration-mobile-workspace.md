---
title: Toimittajayhteistyön mobiilityötila
description: Tässä ohjeaiheessa on tietoja toimittajayhteistyön mobiilityötilasta. Työtilan avulla toimittajat pysyvät ajan tasalla ostotilauksia, jotka on lähetetty heille hyväksyttäväksi. He voivat myös tarkastella uusia ja päivitettyjä ostotilauksia ja yhteyshenkilöitä koskevia tietoja.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: riluan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2c81a5a1bf34706254479a99af253b2b8d743828
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246690"
---
# <a name="vendor-collaboration-mobile-workspace"></a>Toimittajayhteistyön mobiilityötila

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **toimittajayhteistyön** mobiilityötilasta. Työtilan avulla toimittajat pysyvät ajan tasalla ostotilauksia, jotka on lähetetty heille hyväksyttäväksi. He voivat myös tarkastella uusia ja päivitettyjä ostotilauksia ja yhteyshenkilöitä koskevia tietoja.

Tämä mobiilityötila on tarkoitettu käytettäväksi Finance and Operations -mobiilisovelluksen kanssa.

## <a name="overview"></a>Yleiskuvaus 
**Toimittajayhteistyö**-mobiilityötila pitää toimittajat ajan tasalla uusista ostotilauksista, jotta he voivat tarkastella ostotilauksia ja sitten vastata niihin verkkoasiakasohjelmassa. 

>[!NOTE]
> Huomautus: mobiilityötilaa tulee käyttää täydennyksenä toimittajayhteistyön web-liittymään, ei sen sijasta. 

**Toimittajayhteistyön mobiilityötilassa** toimittajasi voivat tarkastella heille hyväksyttäväksi lähetettyjä uusia ostotilauksia. Se näyttää ostotilauksen tiedot, kuten tuotteet, määrät ja pyydetyt toimituspäivät. Hintatiedot ovat saatavilla myös kunkin toimittajan määrityksistä riippuen. 

Käyttäjä, joka kirjautuu toimittajana, näkee, mihin ostotilauksiin on saatu vastaus ja mitkä ostotilaukset odottavat vielä asiakkaan toimia. Esimerkiksi ostotilaus voi odottaa asiakkaan toimintoa, koska toimittaja ehdottaa toista toimituspäivää, jota asiakas ei ole vielä hyväksynyt. Toimittaja näkee myös luettelon ostotilauksista, jotka on vahvistettu mutta joita ei ole vielä toimitettu. 

Toimittajan pitää vastata ostotilauksiin toimittajayhteistyön web-liittymässä web-asiakasohjelmassa. Toimittaja saa siinä myös lisätietoja tilauksesta, kuten liiteasiakirjat, rivikohtaiset toimitusosoitteet ja toimittajaan liittyvät maksut. 

Toimittajat, joilla on erityinen käyttöoikeusrooli, voivat tarkastella, mitkä yhteyshenkilöt on rekisteröity toimittajan tiliin. Samalla käyttöoikeusroolilla toimittaja voit tarkastella minkä tahansa lähetetyn käyttäjäpyynnön tilaa. 

WWW-asiakasohjelman toimittajayhteistyön web-liittymää käytetään uusien yhteyshenkilöiden luomiseen ja uusien käyttäjäpyyntöjen lähettämiseen. 

**Toimittajayhteistyön** mobiilityötilan avulla toimittaja voi suorittaa nämä tehtävät:

-   Tarkastele uusia toimittajalle lähetettyjä ostotilauksia.
-   Tarkastele ostotilauksia, joihin toimittaja on vastannut ja jotka odottavat asiakkaan toimintoa.
-   Tarkastele ostotilauksia, jotka on vahvistettu mutta vain osittain vastaanotettu.
-   Näytä toimittajatiliin rekisteröidyt yhteyshenkilön tiedot. (Tehtävä edellyttää lisätietoja käyttöoikeusroolille.)
-   Tarkastele käyttäjän lähettämän pyynnön tietoja ja seurata pyynnön tilaa. (Tehtävä edellyttää lisätietoja käyttöoikeusroolille.)

## <a name="prerequisites"></a>Edellytykset
Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Managementin käytön edellytykset
Jos Supply Chain Management on otettu käyttöön organisaatiossasi, järjestelmänvalvojan on julkaistava **Toimittajayhteistyö**-mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611 ja Platform update 3 tai uudempi
Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operationsin versio 1611 ja Platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

<table>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Rooli</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 3216943 on otettava käyttöön, jos käytät ympäristön päivitystä 3.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 3216943 on binaaripäivitys, joka on pakollinen, jos käytät ympäristön päivitystä 3. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen tämän KB-päivityksen.
<ol>
<li>Lataa KB 3216943 Microsoft Dynamics Lifecycle Services (LCS) -palvelusta.</li>
<li>Asenna binaaripäivitys, joka toimitetaan käyttöönottopakettina. Tietoja käyttöönottopaketista on kohdassa <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Käyttöönottopaketin käyttö</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>KB 4013633 on oltava asennettu.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>käytettävissä olevan varaston</strong> mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Lataa metatietojen hotfix-korjaus LCS:stä</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Toimittajayhteistyö</strong>-mobiilityötila on julkaistava.</td><td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
<tr class="even">
<td>Toimittajakäyttäjällä on oltava käyttöoikeus toimittajayhteistyön web-liittymään WWW-asiakasohjelmassa sekä määritettävä toimittajayhteistyön käyttäjä.</td><td>Hankintahenkilöstö ja järjestelmänvalvoja</td>
<td>Noudata seuraavien ohjeaiheiden vaiheita määrittääksesi toimittajayhteistyön web-liittymän käyttöä varten.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Toimittajayhteistyön käyttäminen ulkoisten toimittajien kanssa</a></li>
<li><a href="manage-vendor-collaboration-users.md">Toimittajayhteistyön käyttäjien hallinta</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Toimittajayhteistyön määrittäminen ja hallinta</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Toimittajayhteistyön käyttäminen Supply Chain Managements -asiakkaiden kanssa</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen

Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen
1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna Microsoft Dynamics 365:n URL-osoite.
4.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
5.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

    [![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Toimittajayhteistyön mobiilityötilan käyttäminen
Kun valitset **Toimittajayhteistyö**-työtilan, näet seuraavat vaihtoehdot.

![Toimittajayhteistyön mobiilityötila](./media/vendor-collaboration-mobile-app.png)

**Toimittajayhteistyö**-työtila sisältää seuraavat sivut.

### <a name="contacts"></a>Yhteyshenkilöt
**Yhteystiedot** -sivulla näet kaikki yhteyshenkilöt, jotka on määritetty toimittajan tilille. Siinä näkyy yhteyshenkilön nimi, ensisijainen sähköpostiosoite ja käyttäjän tunnus, jos yhteyshenkilöllä on sähköpostitunnus. Sivu näyttää myös, onko yhteyshenkilön käyttäjätili aktiivinen. Kun valitset henkilön, näet yhteystiedot, kuten yritykset, joiden yhteyshenkilö hän on. Näet myös yhteystiedot, kuten puhelinnumero tai vaihtoehtoisen sähköpostiosoitteen.

### <a name="user-requests"></a>Käyttäjäpyynnöt
**Käyttäjäpyynnöt**-sivulla näet toimittajayhteistyön web-liittymän kautta lähettämäsi käyttäjäpyynnöt ja niiden tilan. Voit myös seurata pyyntöjen tilaa. Kun valitset käyttäjäpyynnön, näet pyynnön sisällön, voit lisätä tai poistaa käyttäjän käytöstä, muuttaa suojausasetuksia ja nähdä, mitä käyttöoikeusrooleja käyttäjälle on pyydetty.

### <a name="purchase-orders-ready-for-review"></a>Tarkastuskelpoiset ostotilaukset
**Tarkastuskelpoiset ostotilaukset** -sivulla näet kaikki ostotilaukset, jotka asiakas on lähettänyt ja joihin ei ole vielä vastattu. Voit tarkastella tiettyjä tilauksen tietoja, kuten mitä tuotteita pyyntöön kuuluu ja milloin tuotteet tulee toimittaa. Hintatiedot ovat saatavilla myös kunkin toimittajan määrityksistä riippuen.

Näet myös, onko ostotilauksella huomautuksia tai liitetiedostoja. Avataksesi huomautuksia ja liitteitä sinun on käytettävä toimittajayhteistyön web-liittymän WWW-asiakasohjelmaa. Valitse **Ostotilausrivi** nähdäksesi kaikki rivit ja niillä olevat tiedot. Huomaa, että kullakin rivillä on ilmaisin, joka näyttää, onko rivillä huomautuksia tai liitetiedostoja, tai onko rivin toimitusosoite eri, kuin mitä otsikossa näytetään.

Ostotilaukseen voi vastata vain toimittajayhteistyön web-liittymän WWW-asiakasohjelmassa.

### <a name="awaiting-customer-action"></a>Odottaa asiakkaan toimintoa
**Odottaa asiakkaan toimintoa** -sivulta löydät ostotilaukset, johon sinä tai joku muu yrityksesi työntekijä, jolla on käyttöoikeus toimittajayhteistyö-liittymään, on vastannut. Ostotilaukset näkyvät tässä luettelossa vain, jos asiakkaan on tehtävä jokin seuraavista toimista ostotilaukselle.

-   Jos ostotilaus on hylätty, asiakkaan on joko päivitettävä alkuperäistä tilausta tai peruutettava se ja lähetettävä se uudelleen. Kun ostotilaus lähetetään uudelleen, sitä ei enää näy **Odottaa asiakkaan toimintoa** -sivulta.
-   Jos ostotilaus on hyväksytty muutosten kera, asiakkaan on joko päivitettävä alkuperäinen tilaus ja lähetettävä se uudelleen tarkistettavaksi tai päivitettävä siihen pyydetyt muutokset ja vahvistettava se heti. Molemmissa tapauksissa ostotilausta ei enää nähdä **Odottaa asiakkaan toimintoa** -sivulla.
-   Jos ostotilaus on hyväksytty mutta se näkyy **Odottaa asiakkaan toimintoa** -sivulla, ostotilausta ei ole vahvistettu automaattisesti, kun se on hyväksytty. Se odottaa ostoedustajaa muuttamaan tilauksen tilaksi **Vahvistettu**. Yleensä ostotilausta pidetään sopimuksena asiakkaan ja toimittajan välillä heti, kun toimittaja hyväksyy tilauksen. Siksi päivityksen **Vahvistettu** -tila on yleensä vain muodollisuus.

Vastauksen lisätiedot tulevat näkyviin, kun valitset ostotilauksen. Näet rivin lisätiedot ja kunkin rivin vastauksen. Rivin tila näyttää, mikä seuraavista vastauksista on annettu.

-   Hyv.
-   Hylätty
-   Hyväksytty muutosten kera
-   Korvattu/Korvaava
-   Jaa aikatauluksi/Aikataulurivi

Huomaa, että **Toimitus**-kentän arvo **Kyllä** tai **Ei** osoittaa, toimitetaanko rivit. Riviä ei mahdollisesti voi toimittaa seuraavista syistä:

- Rivi hylättiin.
- Korvaus tehtiin, eikä alkuperäisen rivin toimitusta odoteta vastaanotetun tilauksen pyynnön mukaisena.
- Rivi on jaettu useisiin aikatauluriveihin, eikä alkuperäisen rivin toimitusta odoteta vastaanotetun tilauksen pyynnön mukaisena.

Kaikki tilausriville tehdyt muutokset näytetään. Ladattuja huomautuksia ja liitteitä ei kuitenkaan näytetä. Tarkastellaksesi huomautuksia ja liitteitä sinun on käytettävä toimittajayhteistyön web-liittymän WWW-asiakasohjelmaa.

### <a name="open-confirmed-orders"></a>Avoimet vahvistetut tilaukset
Kun asiakas on vahvistanut ostotilauksen, (ts. ostotilaus on siirretty **Vahvistettu** -tilaan), se näkyy avoimissa vahvistetuissa tilauksissa. Se pysyy luettelossa, kunnes se on rekisteröity asiakkaan vastaanottamaksi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]