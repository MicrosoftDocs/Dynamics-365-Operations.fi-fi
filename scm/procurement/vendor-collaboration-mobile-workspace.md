---
title: "Toimittaja mobile yhteistyötila Microsoft Dynamics-365-toiminnot app"
description: "Toimittaja mobile yhteistyötilan, jossa toimittajien pysyvät ostotilaukset, jotka on lähetetty ne hyväksyttäväksi ja tarkastelutietoja uusien ja päivitettyjen ostotilausten ja yhteystiedot ajan tasalla."
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

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Toimittaja mobile yhteistyötila Microsoft Dynamics-365-toiminnot app

Toimittaja mobile yhteistyötilan, jossa toimittajien pysyvät ostotilaukset, jotka on lähetetty ne hyväksyttäväksi ja tarkastelutietoja uusien ja päivitettyjen ostotilausten ja yhteystiedot ajan tasalla.

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
<td>Lue Microsoft Dynamics-365 toimintojen mobiilien</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Toimintojen mobiilien Dynamics 365</a></td>
</tr>
<tr class="even">
<td>Työvaiheiden Dynamics 365</td>
<td>Muista, että käytät ympäristössä, jossa on Microsoft Dynamics-365-version toimintoja 1611 ja päivittää toimia ympäristön Microsoft Dynamics 3 (marraskuu-2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Kannettava laite, joka on asennettu toiminnot app for Dynamics-365</span></td>
<td><span style="color: #000000;">Lataa mobile app myymälä toiminnot app for Dynamics-365.</span></td>
</tr>
<tr class="even">
<td>Hotfix-korjauksen kt 3215650</td>
<td>Asentaa korjaustiedoston käyttöön työtilat, jotka toimitetaan Dynamics 365 operaatioille.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Hotfix-korjauksen kt 3216943</span> </span></td>
<td>Asentaa korjaustiedoston käyttöön toimittajan mobiili yhteistyötilan.</td>
</tr>
<tr class="even">
<td>Toimittaja käyttäjä on pääsy toimittajan yhteistyö web-liittymän operaatioille 365 Dynamics ja määritettävä toimittajakäyttäjän yhteistyö.</td>
<td>Ja toimittaja-yhteistyö web-liittymän käsitellä seuraavissa ohjeaiheissa kuvatut toimet.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Käytä toimittajan yhteistyö ulkoisten toimittajien kanssa</a></li>
<li><a href="manage-vendor-collaboration-users.md">Toimittajayhteistyön käyttäjien hallinta</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Määritä ja ylläpidä toimittajayhteistyötä</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Toimittajan yhteistyön avulla voit käsitellä asiakkaiden Dynamics 365 operaatioille</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Yleiskuvaus
Toimittaja mobile yhteistyötilan pitää toimittajien uusista ostotilauksista ilmoittanut, että he voivat nähdä ja vastata Dynamics-365-ostotilausten toimintoja web-asiakasohjelman.  

**Huomautus:** tulee käyttää mobile workspace täydennyksenä toimittaja-yhteistyö web-liittymä, mutta ei korvaa.  

Toimittajien voit tarkastella toimittajan mobiili yhteistyötilan, uusille ostotilauksille, jotka on lähetetty hyväksyttäviksi. Se näyttää ostotilauksen tiedoista, kuten tuotteiden määrä ja pyydetty toimituspäivät. Hintatietoja ei ole saatavilla siten, että kunkin toimittajan.  

Kun käyttäjä kirjautuu toimittajana, he näkevät mitkä ostotilaukset on vastattu tai mitkä ostotilaukset jotka yhä odottavat asiakkaan toimia. Toimittaja voi olla ehdotettu toiseen, joka ei ole vielä sovitaan asiakkaan kanssa siten, että asiakkaan toiminta odottaa ostotilauksen toimituspäivää. Toimittajan Katso myös luettelo ostotilauksista, jotka on vahvistettu, mutta ei ole vielä toimitettu.  

Ostotilaus vastaamaan toimittajalla on toimittajan yhteistyö web-liittymä, joka on käytettävissä Dynamics-365 toimintoja web-asiakasohjelman avulla. Tämä on myös mistä toimittajan hankkia lisätietoja tilaus, kuten liitetiedostoja, toimitusosoite riville ja kulut, jotka liittyvät toimittajaan.  

Toimittajan tarkastella tiettyä käyttöoikeusroolia, mikä Kontakti henkilöiden on rekisteröity toimittaja. Käyttöoikeusrooli toimittaja voit tarkastella minkä tahansa käyttäjän pyynnöstä, joka on jätetty tilaa.  

Uuden yhteystiedon luominen ja uusien käyttäjien pyyntöjen lähettämisestä tulee tehdä toimittajan yhteistyö käyttöliittymässä käytettävissä olevien toimintojen web-asiakasohjelman Dynamics-365.  

Mobiili työtilaan, jossa toimittaja voi

-   Näytä uusi toimittajalle ostotilauksia.
-   Näytä ostotilausten toimittajan vastannut ja jotka odottavat asiakkaan toimia.
-   Näytä ostotilaukset, jotka on vahvistettu valtion ja ei ole vastaanotettu kokonaan.
-   Näytä yhteyshenkilön tiedot, jotka on rekisteröity toimittajatilin (vaatii lisää käyttöoikeusroolin).
-   Näytä tiedot ja seuraa käyttäjän pyynnöstä toimittajan lähettämän (vaatii lisää käyttöoikeusroolin) tila.

## <a name="get-started"></a>Aloittaminen
Matkaviestimen aloittaminen:

1.  Mobile app-myymälä, lataa ja asenna toiminnot app for Microsoft Dynamics-365.
2.  Käynnistä sovellus laitteen.
3.  Anna URL-osoitteesi Dynamics 365.
4.  Kirjoita Kirjaudu yritys. Esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinua pyydetään käyttäjänimeä ja salasanaa Microsoft Dynamics-365, tilin toimintoja varten. 

Kun olet kirjautunut app, näkyvät työtiloja ei ole. Voit tarkastella mobiili sovellusten työtilat, haluttu työtilat on ensin julkaistava toiminnot app for Dynamics-365. Tarvitset järjestelmän hallinto-oikeuden julkaista työtilan.

1.  Käynnistä Dynamics 365 operaatioille.
2.  Siirry **järjestelmän hallinta**&gt;**asennus**&gt;**järjestelmäparametrit**.
3.  Valitse **hallinta mobile app**.
4.  Valitse työtilan **toimittaja, yhteistyössä** julkaista mobile platform.
5.  Valitse **julkaista työtilan**.
6.  Päivitä laitteesi on julkaistu työtilat.
7.  Valitse **toimittaja, yhteistyössä** työtila. Seuraavalla sivulla sinun tulee.

[![Toimittaja-yhteistyö-mobile-sovellus](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Yhteyshenkilöt
**Yhteystiedot** -sivulla voit nähdä kaikki yhteystiedot, jotka on määritetty toimittajatili. Se näyttää yhteyshenkilön nimi ja ensisijainen sähköposti käyttäjät alias, jos sellainen on käytettävissä. Se näyttää myös, onko yhteyshenkilön käyttäjätili on aktiivinen. Kun olet valinnut yhteystiedon, tarkastella yhteystietoja, kuten mitä oikeussubjektien henkilö toimii yhteyshenkilönä, ja yhteystiedot, kuten puhelinnumero tai toinen sähköpostiosoite.

## <a name="user-requests"></a>Käyttäjäpyynnöt
**Pyynnöt** sivulla näet kaikki käyttäjä pyytää, että olet lähettänyt toimittaja-yhteistyö web-liittymän kautta ja seurata tilan avulla. Kun valitset käyttäjän pyynnöstä, voit nähdä mitä pyydettiin, Lisää tai Poista käyttäjä käytöstä, muuttaa suojausasetuksia, ja on käyttäjän käyttöoikeusroolit, joilla on vaadittu.

## <a name="purchase-orders-ready-for-review"></a>Ostotilausten valmis tarkistettavaksi
**Ostotilaukset valmis tarkistettavaksi** sivun avulla näet kaikki ostotilaukset, jotka on lähetetty asiakkaalle ja joihin ei ole vastattu. Voit tarkastella valitun tilauksen, mitkä tuotteet on tehty pyyntö ja kun toimittamaan tietoja. Hintatietoja on käytettävissä vain, jos tämä on määritetty toimittajalle.  

Näet, onko ostotilauksen huomautusten tai liitetiedostoja. Avaamaan liitteitä, sinun on käytettävä toimittaja-yhteistyö web-asiakasohjelmassa. Valitse **ostotilausrivi** nähdäksesi kaikki rivit, joiden tiedot. Huomaa, että kunkin rivin ilmaisin näkyy onko liitteitä tai muistiinpanoja, vai onko toimitusosoitteen, joka on eri kuin mitä näkyy otsikon.  

Vastata ostotilauksen on käytettävä toimittajan yhteistyö-web-asiakasohjelmassa.

## <a name="awaiting-customer-action"></a>Odottaa asiakkaan toimintoa
**Odottavat asiakkaan toimia** löydät sivun avulla ostotilaukset, jotka sinä tai joku muu yrityksesi, joka on myös toimittaja, yhteistyössä oikeus ovat vastanneet. Ostotilaukset näkyvät vain tässä luettelossa, jos asiakas tarvitsee tehdä jonkin seuraavista toimista ostotilauksen.

-   Jos ostotilauksen hylättiin, asiakkaan joko lähetetty päivitetään ja Lähetä uudelleen tai Peruuta tilaus ja Lähetä uudelleen. Ostotilaus lähetetään uudelleen, kun se katoaa **odottavat asiakkaan toimia** sivulla.
-   Jos ostotilauksen hyväksyttiin muutokset, asiakkaan on alkuperäinen tilaus ja Lähetä tarkistettavaksi- tai päivitä muutokset ja vahvista heti. Molemmissa tapauksissa ostotilauksen katoaa **odottavat asiakkaan toimia** sivulla.
-   Jos ostotilauksen hyväksyttiin ja se tulee **odottavat asiakkaan toimia** sivulla, se on koska ostotilausta ei automaattisesti vahvistettiin hyväksymisen kierron. Se odottaa Ostoedustaja vahvistettu järjestyksen muuttaminen. Yleensä ostotilauksen katsottava asiakkaan ja toimittajan välisen sopimuksen heti, jona Toimittaja hyväksyy tilauksen. Siirretään ostotilauksen vahvistettu valtion olisi muodollisuus.

Lisätiedot näkyviin valitsemalla ostotilauksen vastauksen tietoja. Näet tiedot ja jokaisen rivin vastaus. Rivin tila näyttää mitä seuraavat vastaukset on annettu.

-   Hyv.
-   Hylätty
-   Hyväksytty muutosten kera
-   Korvataan ja korvaava
-   Aikataulu/rivi on jaettu

Huomaa, että ilmaisin näyttää **toimenpide**= Kyllä/ei, jota käytetään osoittamaan, että rivejä ei toimiteta. Tämä voi johtua siitä, että rivi on hylätty tai korvaamista, jossa alkuperäisen rivin ei odoteta toimitetaan tai rivi on jaettu useiksi riveiksi aikataulun ja alkuperäisen viivan odotetaan toimitetaan järjestyksessä vastaanotettujen pyydetyllä tavalla.  

Tilauksen rivin vastaus tehdyt muutokset näkyvät ladatun muistiinpanot ja liitteet, jotka näet toimittaja-yhteistyö web-liittymän avulla.

## <a name="open-confirmed-orders"></a>Vahvistettu Avoimet tilaukset
Kun asiakas on vahvistanut ostotilauksen, mikä tarkoittaa ostotilaus muutetaan vahvistettu valtion se näkyy vahvistettu Avoin tilaus. Se pysyy luettelossa, kunnes se on rekisteröity vastaanotetuksi asiakkaan.


