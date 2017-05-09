---
title: "Toimittajayhteistyön mobiilityötila Microsoft Dynamics 365 for Operations -sovellusta varten"
description: "Toimittajasi voivat käyttää toimittajayhteistyön mobiilityötilaa pysyäkseen ajan tasalla heille hyväksyttäväksi lähetetyistä ostotilauksista sekä tarkastellakseen uusien ja päivitettyjen ostotilausten ja yhteyshenkilöiden tietoja."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Toimittajayhteistyön mobiilityötila Microsoft Dynamics 365 for Operations -sovellusta varten

Toimittajasi voivat käyttää toimittajayhteistyön mobiilityötilaa pysyäkseen ajan tasalla heille hyväksyttäväksi lähetetyistä ostotilauksista sekä tarkastellakseen uusien ja päivitettyjen ostotilausten ja yhteyshenkilöiden tietoja.

<a name="prerequisites"></a>Edellytykset
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lue Microsoft Dynamics 365 for Operations -mobiiliympäristöstä</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operations -mobiiliympäristö</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Varmista, että käytössäsi on ympäristö, johon on asennettu Microsoft Dynamics 365 for Operations -versio 1611 sekä Microsoft Dynamics for Operations ympäristöpäivitys 3 (Marraskuu 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobiililaite, johon on asennettu Dynamics 365 for Operations -sovellus</span></td>
<td><span style="color: #000000;">Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.</span></td>
</tr>
<tr class="even">
<td>Hotfix-korjaus KB 3215650</td>
<td>Asenna korjaustiedosto ottaaksesi käyttöön työtilat, jotka toimitetaan Dynamics 365 for Operationsissa.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Hotfix-korjaus KB 3216943</span> </span></td>
<td>Asenna hotfix-korjaus, jos haluat ottaa toimittajayhteistyön mobiilityötilan käyttöön.</td>
</tr>
<tr class="even">
<td>Toimittajakäyttäjällä on oltava käyttöoikeus toimittajayhteistyön web-liittymään Dynamics 365 for Operationsissa sekä määritettävä toimittajayhteistyön käyttäjä.</td>
<td>Noudata seuraavien ohjeaiheiden vaiheita määrittääksesi toimittajayhteistyön web-liittymän käyttöä varten.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Toimittajayhteistyön käyttäminen ulkoisten toimittajien kanssa</a></li>
<li><a href="manage-vendor-collaboration-users.md">Toimittajayhteistyön käyttäjien hallinta</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Määritä ja ylläpidä toimittajayhteistyötä</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Toimittajayhteistyön käyttäminen Dynamics 365 for Operations -asiakkaiden kanssa</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Yleiskuvaus
Toimittajayhteistyön mobiilityötila pitää toimittajat ajan tasalla uusista ostotilauksista, jotta he voivat nähdä ja vastata ostotilauksiin Dynamics 365 for Operationsissa.  

**Huomautus:** mobiilityötilaa tulee käyttää täydennyksenä toimittajayhteistyön web-liittymään, ei sen sijasta.  

Toimittajayhteistyön mobiilityötilassa toimittajasi voivat tarkastella uusia, hyväksyttäväksi lähetettyjä ostotilauksia. Se näyttää ostotilauksen tiedot, kuten tuotteet, määrän ja pyydetyt toimituspäivät. Hintatiedot ovat saatavilla kunkin toimittajan määrityksistä riippuen.  

Kun käyttäjä kirjautuu toimittajana, hän näkee, mihin ostotilauksiin on saatu vastaus ja mitkä ostotilaukset odottavat vielä asiakkaan toimia. Toimittaja voi ehdottaa toista toimituspäivää, jota asiakas ei ole vielä hyväksynyt, joten ostotilaus odottaa asiakkaan toimia. Toimittaja näkee myös luettelon ostotilauksista, jotka on vahvistettu, mutta joita ei ole vielä toimitettu.  

Toimittaja voi vastata ostotilauksiin toimittajayhteistyön web-liittymässä, joka on saatavilla Dynamics 365 for Operationsin web-asiakasohjelmassa. Tässä toimittaja saa myös lisätietoja tilauksesta, kuten liiteasiakirjat, rivikohtaiset toimitusosoitteet ja toimittajaan liittyvät maksut.  

Jos toimittajalla on erityinen käyttöoikeusrooli, tämä voi tarkastella, mitkä yhteyshenkilöt on rekisteröity toimittajan tiliin. Samalla käyttöoikeusroolilla toimittaja voit tarkastella minkä tahansa lähetetyn käyttäjäpyynnön tilaa.  

Uudet yhteyshenkilöt ja uudet käyttäjäpyynnöt on luotava Dynamics 365 for Operationsin web-asiakasohjelman toimittajayhteistyöliittymässä.  

Mobiilityötilassa toimittajasi voi:

-   Tarkastella uusia toimittajalle lähetettyjä ostotilauksia.
-   Tarkastella ostotilauksia, joihin toimittaja on vastannut ja jotka odottavat asiakkaan toimintoa.
-   Tarkastella ostotilauksia, jotka ovat vahvistetussa tilassa, mutta niitä ei ole täysin vastaanotettu.
-   Tarkastella toimittajatiliin liitettyjen yhteyshenkilöiden tietoja (vaatii ylimääräisen käyttöoikeusroolin).
-   Tarkastella käyttäjän lähettämän pyynnön tietoja ja tilaa (vaatii ylimääräisen käyttöoikeusroolin).

## <a name="get-started"></a>Aloittaminen
Voit aloittaa käytön mobiililaitteessa seuraavasti:

1.  Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.
2.  Käynnistä sovellus laitteessa.
3.  Anna Dynamics 365 -URL-osoitteesi.
4.  annan yritys, johon kirjaudutaan. Kirjoita esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinulta pyydetään Microsoft Dynamics 365 for Operations -tilisi käyttäjänimeä ja salasanaa. 

Kun olet kirjautunut sovellukseen, työtiloja ei näy. Jotta voit tarkastella mobiilisovelluksessa työtiloja, halutut työtilat on ensin julkaistava Dynamics 365 for Operationsiin. Tarvitset järjestelmänvalvojan oikeuden työtilan julkaisemiseen.

1.  Käynnistä Dynamics 365 for Operations.
2.  Valitse **Järjestelmän hallinta** &gt; **Asetukset** &gt; **järjestelmän parametrit**.
3.  Valitse **Hallitse mobiilisovellusta**.
4.  Valitse **Toimittajayhteistyö**-työtila julkaistaksesi mobiiliympäristöön.
5.  Valitse **Julkaise työtila**.
6.  Päivitä laitteesi nähdäksesi julkaistut työtilat.
7.  Valitse **Toimittajayhteistyö**-työtila. Seuraava sivu aukeaa.

[![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Yhteyshenkilöt
**Yhteystiedot** -sivulla näet kaikki yhteyshenkilöt, jotka on määritetty toimittajan tilille. Se näyttää yhteyshenkilön nimen ja ensisijaisen sähköpostiosoitteen sekä käyttäjän aliaksen, jos sellainen on. Se näyttää myös, onko yhteyshenkilön käyttäjätili aktiivinen. Kun valitset yhteyshenkilön, näet sen tiedot, kuten minkä yritysten yhteyshenkilö on kyseessä sekä yhteystietoja, kuten puhelinnumeron tai toisen sähköpostiosoitteen.

## <a name="user-requests"></a>Käyttäjäpyynnöt
**Käyttäjäpyynnöt**-sivulla näet toimittajayhteistyön web-liittymän kautta lähettämäsi käyttäjäpyynnöt ja niiden tilan. Kun valitset käyttäjäpyynnön, näet pyynnön sisällön, voit lisätä tai poistaa käyttäjän käytöstä, muuttaa suojausasetuksia ja nähdä, mitä käyttöoikeusrooleja käyttäjälle on pyydetty.

## <a name="purchase-orders-ready-for-review"></a>Tarkastuskelpoiset ostotilaukset
**Tarkastuskelpoiset ostotilaukset** -sivulla näet kaikki ostotilaukset, jotka on lähetetty asiakkaalle ja joihin ei ole vastattu. Voit tarkastella tiettyjä tilauksen tietoja, kuten mitä tuotteita pyyntöön kuuluu ja milloin tilaus tulee toimittaa. Hintatiedot ovat käytettävissä vain, jos ne on määritetty toimittajalle.  

Näet, onko ostotilauksella huomautuksia tai liitetiedostoja. Jos haluat avata liitetiedostot, sinun on käytettävä web-asiakasohjelman toimittajayhteistyö-osaa. Valitse **Ostotilausrivi** nähdäksesi kaikki rivit, joilla on lisätietoja. Huomaa, että kullakin rivillä on ilmaisin, joka näyttää, onko rivillä huomautuksia tai liitetiedostoja, tai onko rivin toimitusosoite eri, kuin mitä otsikossa näytetään.  

Ostotilaukseen voi vastata vain toimittajayhteistyön web-asiakasohjelmassa

## <a name="awaiting-customer-action"></a>Odottaa asiakkaan toimintoa
**Odottaa asiakkaan toimintoa** -sivulta löydät ostotilaukset, johon sinä tai joku muu yrityksesi työntekijä, jolla on käyttöoikeus toimittajayhteistyö-liittymään, on vastannut. Ostotilaukset näkyvät tässä luettelossa vain, jos asiakkaan on tehtävä jokin seuraavista toimista ostotilaukselle.

-   Jos ostotilaus on hylätty, asiakkaan on joko päivitettävä lähetettyä tilausta ja lähetettävä se uudelleen, tai peruutettava tilaus ja lähetettävä se uudelleen. Kun ostotilaus lähetetään uudelleen, se katoaa **Odottaa asiakkaan toimintoa** -sivulta.
-   Jos ostotilaus on hyväksytty muutosten kera, asiakkaan on päivitettävä alkuperäinen tilaus ja lähetettävä se uudelleen tarkistettavaksi, tai päivittää siihen pyydetyt muutokset ja vahvistettava se heti. Molemmissa tapauksissa ostotilaus katoaa **Odottaa asiakkaan toimintoa** -sivulta.
-   Jos ostotilaus on hyväksytty ja se näkyy **Odottaa asiakkaan toimintoa** -sivulla, ostotilausta ei ole vahvistettu automaattisesti, kun se on hyväksytty. Se odottaa ostoedustajaa muuttamaan tilauksen vahvistetuksi. Yleensä ostotilausta käsitellään sopimuksena asiakkaan ja toimittajan välillä heti, kun toimittaja hyväksyy tilauksen. Ostotilauksen siirtäminen vahvistettuun tilaan on siis muodollisuus.

Vastauksen lisätiedot tulevat näkyviin valitsemalla ostotilauksen. Näet rivin lisätiedot ja kunkin rivin vastauksen. Rivin tila näyttää, mikä seuraavista vastauksista on annettu.

-   Hyv.
-   Hylätty
-   Hyväksytty muutosten kera
-   Korvattu/Korvaava
-   Jaa aikatauluksi/Aikataulurivi

Huomaa, että ilmaisin on **Toimitus**= Kyllä/ei, jota käytetään osoittamaan, että rivejä ei toimiteta. Tämä voi johtua siitä, että rivi on hylätty tai korvattu siten, että alkuperäisiä rivejä ei odoteta toimittavan, tai rivi on jaettu useampaan aikatauluriviin, eikä alkuperäistä riviä odoteta toimitettavaksi pyydetyllä tavalla ja pyydetyssä järjestyksessä.  

Kaikki tilausriville tehdyt muutokset näytetään, pois lukien ladatut huomautukset ja liitetiedostot, jotka näet toimittajayhteistyön web-liittymässä.

## <a name="open-confirmed-orders"></a>Avoimet vahvistetut tilaukset
Kun asiakas on vahvistanut ostotilauksen, eli ostotilaus on siirretty vahvistettuun tilaan, se näkyy avoimissa vahvistetuissa tilauksissa. Se pysyy luettelossa, kunnes se on rekisteröity asiakkaan vastaanottamaksi.


