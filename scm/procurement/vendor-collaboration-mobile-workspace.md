---
title: "Toimittajayhteistyön mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja toimittajayhteistyön mobiilityötilasta. Työtilan avulla toimittajat pysyvät ajan tasalla ostotilauksia, jotka on lähetetty heille hyväksyttäväksi. He voivat myös tarkastella uusia ja päivitettyjä ostotilauksia ja yhteyshenkilöitä koskevia tietoja."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 20e4c77bc47bffc3474559e3b9933b87e947e178
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017


---

# Toimittajayhteistyön mobiilityötila
<a id="vendor-collaboration-mobile-workspace" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **toimittajayhteistyön** mobiilityötilasta. Työtilan avulla toimittajat pysyvät ajan tasalla ostotilauksia, jotka on lähetetty heille hyväksyttäväksi. He voivat myös tarkastella uusia ja päivitettyjä ostotilauksia ja yhteyshenkilöitä koskevia tietoja.

Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.

## Yleiskuvaus
<a id="overview" class="xliff"></a> 
**Toimittajayhteistyön** mobiilityötila pitää toimittajat ajan tasalla uusista ostotilauksista, jotta he voivat nähdä ja vastata ostotilauksiin Microsoft Dynamics 365 for Finance and Operationsin Enterprise edition -www-asiakasohjelmassa. 

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

## Edellytykset
<a id="prerequisites" class="xliff"></a>
Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.

### Edellytykset, jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys
<a id="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update" class="xliff"></a> 
Jos Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys on otettu organisaatiossa käyttöön, järjestelmänvalvojan on julkaistava **Toimittajayhteistyö** mobiilityötila. Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611, johon on asennettu vähintään ympäristöpäivitys 3
<a id="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later" class="xliff"></a>
Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operationsin versio 1611, jossa on vähintään ympäristöpäivitys 3, järjestelmänvalvojan on toteutettava seuraavat edellytykset. 

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
<li>Lataa KB 3216943 Microsoft Dynamicsin elinkaaripalveluista (LCS).</li>
<li>Asenna binaaripäivitys, joka toimitetaan käyttöönottopakettina. Tietoja käyttöönottopaketista on kohdassa <a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Käyttöönottopaketin käyttö</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>KB 4013633 on oltava asennettu.</td>
<td>Järjestelmänvalvoja</td>
<td>KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>käytettävissä olevan varaston</strong> mobiilityötilan. Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Lataa metatietojen hotfix-korjaus LCS:stä</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</li><li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Toimittajayhteistyö</strong>-mobiilityötila on julkaistava.</td><td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
<tr class="even">
<td>Toimittajakäyttäjällä on oltava käyttöoikeus toimittajayhteistyön web-liittymään WWW-asiakasohjelmassa sekä määritettävä toimittajayhteistyön käyttäjä.</td><td>Hankintahenkilöstö ja järjestelmänvalvoja</td>
<td>Noudata seuraavien ohjeaiheiden vaiheita määrittääksesi toimittajayhteistyön web-liittymän käyttöä varten.
<ul>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-external-vendors/">Toimittajayhteistyön käyttäminen ulkoisten toimittajien kanssa</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/manage-vendor-collaboration-users/">Toimittajayhteistyön käyttäjien hallinta</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/set-up-and-maintain-vendor-collaboration/">Toimittajayhteistyön määrittäminen ja hallinta</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations/">Toimittajayhteistyön käyttäminen Dynamics 365 for Finance and Operations -asiakkaiden kanssa</a></li>
</ul></td>
</tr>
</tbody>
</table>

## Mobiilisovelluksen lataaminen ja asentaminen
<a id="download-and-install-the-mobile-app" class="xliff"></a>

Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## Kirjautuminen mobiilisovellukseen
<a id="sign-in-to-the-mobile-app" class="xliff"></a>
1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna oman Microsoft Dynamics 365:n URL-osoite.
4.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
5.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

    [![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## Toimittajayhteistyön mobiilityötilan käyttäminen
<a id="use-the-vendor-collaboration-mobile-workspace" class="xliff"></a>
Kun valitset **Toimittajayhteistyö**-työtilan, näet seuraavat vaihtoehdot.

![Toimittajayhteistyön mobiilityötila](./media/vendor-collaboration-mobile-app.png)

**Toimittajayhteistyö**-työtila sisältää seuraavat sivut.

### Yhteyshenkilöt
<a id="contacts" class="xliff"></a>
**Yhteystiedot** -sivulla näet kaikki yhteyshenkilöt, jotka on määritetty toimittajan tilille. Siinä näkyy yhteyshenkilön nimi, ensisijainen sähköpostiosoite ja käyttäjän tunnus, jos yhteyshenkilöllä on sähköpostitunnus. Sivu näyttää myös, onko yhteyshenkilön käyttäjätili aktiivinen. Kun valitset henkilön, näet yhteystiedot, kuten yritykset, joiden yhteyshenkilö hän on. Näet myös yhteystiedot, kuten puhelinnumero tai vaihtoehtoisen sähköpostiosoitteen.

### Käyttäjäpyynnöt
<a id="user-requests" class="xliff"></a>
**Käyttäjäpyynnöt**-sivulla näet toimittajayhteistyön web-liittymän kautta lähettämäsi käyttäjäpyynnöt ja niiden tilan. Voit myös seurata pyyntöjen tilaa. Kun valitset käyttäjäpyynnön, näet pyynnön sisällön, voit lisätä tai poistaa käyttäjän käytöstä, muuttaa suojausasetuksia ja nähdä, mitä käyttöoikeusrooleja käyttäjälle on pyydetty.

### Tarkastuskelpoiset ostotilaukset
<a id="purchase-orders-ready-for-review" class="xliff"></a>
**Tarkastuskelpoiset ostotilaukset** -sivulla näet kaikki ostotilaukset, jotka asiakas on lähettänyt ja joihin ei ole vielä vastattu. Voit tarkastella tiettyjä tilauksen tietoja, kuten mitä tuotteita pyyntöön kuuluu ja milloin tuotteet tulee toimittaa. Hintatiedot ovat saatavilla myös kunkin toimittajan määrityksistä riippuen.

Näet myös, onko ostotilauksella huomautuksia tai liitetiedostoja. Avataksesi huomautuksia ja liitteitä sinun on käytettävä toimittajayhteistyön web-liittymän WWW-asiakasohjelmaa. Valitse **Ostotilausrivi** nähdäksesi kaikki rivit ja niillä olevat tiedot. Huomaa, että kullakin rivillä on ilmaisin, joka näyttää, onko rivillä huomautuksia tai liitetiedostoja, tai onko rivin toimitusosoite eri, kuin mitä otsikossa näytetään.

Ostotilaukseen voi vastata vain toimittajayhteistyön web-liittymän WWW-asiakasohjelmassa.

### Odottaa asiakkaan toimintoa
<a id="awaiting-customer-action" class="xliff"></a>
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

### Avoimet vahvistetut tilaukset
<a id="open-confirmed-orders" class="xliff"></a>
Kun asiakas on vahvistanut ostotilauksen, (ts. ostotilaus on siirretty **Vahvistettu** -tilaan), se näkyy avoimissa vahvistetuissa tilauksissa. Se pysyy luettelossa, kunnes se on rekisteröity asiakkaan vastaanottamaksi.

