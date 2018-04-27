---
title: "Työnkulkuominaisuuksien asetusten määrittäminen"
description: "Tässä ohjeaiheessa kerrotaan, miten työnkulun eri ominaisuudet määritetään."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 7ea35d851613a19889392400e31cf8492d5dc799
ms.contentlocale: fi-fi
ms.lasthandoff: 03/23/2018

---

# <a name="configure-workflow-properties"></a>Työnkulkuominaisuuksien asetusten määrittäminen

[!INCLUDE [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten työnkulun eri ominaisuudet määritetään.

Konfiguroidaksesi työnkulun ominaisuudet, avaa työnkulku työnkulkueditorissa. Napsauta Työnkulkueditorin alustaa ja valitse sitten **ominaisuudet** avataksesi **Ominaisuudet**-sivun. Seuraavien ohjeiden avulla voit sitten määrittää työnkulun eri ominaisuudet.

## <a name="name-the-workflow"></a>Työnkulun nimeäminen
Kirjoita näiden ohjeiden avulla nimi työnkululle.

1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Kirjoita **Nimi**-kenttään työnkulun yksilöivä nimi. Oletetaan esimerkiksi, että olet luomassa ostoehdotustyönkulut jokaiselle maalle/alueelle, jossa toimit. Ostoehdotustyönkulut voi nimetä esimerkiksi seuraavasti: **Tanskan ostoehdotukset** tai **Espanjan ostoehdotukset**.

## <a name="specify-the-workflow-owner"></a>Työnkulun omistajan määrittäminen
Työnkulun omistaja on vastuussa työnkulun hallinnasta ja ylläpidosta. Määritä työnkulun omistaja seuraavia ohjeita noudattamalla.

1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Valitse **Omistaja**-luettelosta tämän työnkulun hallinnasta vastaava henkilö.

## <a name="select-an-email-template"></a>Valitse sähköpostimalli.
Valitse näiden ohjeiden avulla sähköpostimalli, jota käytetään työnkulkua koskevien ilmoitusviestin luomiseen.

1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Valitse malli **Työnkulkuilmoitusten sähköpostimallit** -luettelosta.

## <a name="enter-instructions-for-users"></a>Käyttäjien ohjeiden määrittäminen
Voit antaa ohjeita käyttäjille, jotka lähettävät asiakirjoja käsiteltäviksi ja hyväksyttäviksi. Näistä käyttäjistä käytetään myös nimitystä *aloittaja*. Oletetaan, että olet luomassa ostoehdotuksen työnkulkua, jolle kirjoitat ohjeita. Ohjeet ovat sitten niiden henkilöiden tarkasteltavissa, jotka luovat ostoehdotuksia **Ostoehdotukset**-sivulla. Aloittaja voi avata ohjeet näyttöön napsauttamalla työnkulun sanomapalkissa olevaa kuvaketta. Määritä käyttäjien ohjeet seuraavasti.

1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Kirjoita ohjeet **Lähetysohjeet**-kenttään.
3.  Voit mukauttaa ohjeita lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat ohjeita, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:
    1.  Napsauta **Lähetysohjeet**-kenttää määrittääksesi, mihin haluat lisätä paikkamerkin.
    2.  Napsauta **Lisää paikkamerkki** -painiketta.
    3.  Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4.  Valitse **Lisää**.

4.  Ohjeiden käännökset voit lisätä seuraavasti:
    1.  Napsauta **Käännökset**-painiketta.
    2.  Valitse esiin tulevalla sivulla **Lisää**.
    3.  Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4.  Kirjota tekstisi **Käännetty teksti** -kenttään.
    5.  Voit mukauttaa tekstiä lisäämällä paikkamerkkejä. Ohjeet paikkamerkkien asettamisesta ovat vaiheessa 3.
    6.  Valitse **Sulje**.

## <a name="specify-when-this-workflow-is-used"></a>Määritä, milloin tätä työnkulkua käytetään
Voit luoda useita samaan tyyppiin perustuvia työnkulkuja. Voit esimerkiksi luoda ostoehdotustyönkulun kullekin maalle/alueelle, jossa toimit, kuten Tanskan ostoehdotukset ja Espanjan ostoehdotukset. Jos käytössä on useita samaan tyyppiin perustuvia työnkulkuja, määritä, milloin kutakin työnkulkua käytetään. Edellisessä esimerkissä määritetään seuraavat ehdot:

-   Tanskan ostoehdotukset -työnkulkua käytetään, kun maa/alue on DK.
-   Espanjan ostoehdotukset -työnkulkua käytetään, kun maa/alue on ES.

Määritä seuraavien ohjeiden avulla, milloin konfiguroitavaa työnkulkua tulee käyttää.

1.  Valitse vasemmasta ruudusta **Aktivointi**.
2.  Merkitse **Määritä tämän työnkulun suorittamisen ehdot** -valintaruutu.
3.  Valitse **Lisää ehto**.
4.  Määritä ehto.
5.  Kirjoita kaikki muut tarvittavat ehdot.
6.  Voit tarkistaa, onko ehdot määritetty oikein seuraavien ohjeiden avulla:
    1.  Valitse **Testi**.
    2.  Valitse tietue **Testaa työnkulun ehto** -sivun **Tarkista ehto** -alueella.
    3.  Valitse **Testi**. Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot. Jos esimerkiksi olet luomassa Espanjan ostoehdotusten työnkulkua, sivun **Tarkista ehto** -alueella näytetään luettelo ostoehdotuksista. Kun valitset **Testi**, järjestelmä arvioi valitun ostoehdotuksen ja määrittää, onko maa/alue ES.
    4.  Palaa **Ominaisuudet**-sivulle valitsemalla **OK** tai **Peruuta**.

## <a name="specify-when-notifications-are-sent"></a>Määritä, milloin ilmoitukset lähetetään
Kun asiakirja lähetetään käsiteltäväksi, järjestelmä luo työnkulkuinstanssin. Voit lähettää käyttäjille ilmoituksen, kun (tähän työnkulkuun perustuva) työnkulkuinstanssi aloitetaan tai päätetään tai kun työnkulku on valmis tai se pysäytetään virheen vuoksi. Seuraavia ohjeita noudattamalla voit määrittää, milloin ilmoitukset lähetetään.

1.  Valitse vasemmasta ruudusta **Ilmoitukset**.
2.  Merkitse kunkin tapahtuman valintaruutu, jonka tulisi käynnistää ilmoitusten lähettäminen:
    -   **Aloitettu** – Ilmoitukset lähetetään, kun työnkulkuinstanssi aloitetaan.
    -   **Pysäytettiin** – Ilmoitukset lähetetään, kun työnkulkuinstanssi pysäytetään virheen vuoksi.
    -   **Valmis** – Ilmoitukset lähetetään, kun työnkulkuinstanssi valmistuu.
    -   **Peruuttamaton** – Ilmoitukset lähetetään, kun työnkulkuinstanssi pysäytetään peruuttamattoman virheen vuoksi.
    -   **Lopetettu** – Ilmoitukset lähetetään, kun työnkulkuinstanssi lopetetaan.

3.  Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.
4.  Kirjoita **Ilmoitusteksti**-välilehdellä ilmoituksen leipäteksti.
5.  Voit mukauttaa tekstiä lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat tekstiä, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:
    1.  Napsauta kentän kohtaa, johon haluat lisätä paikkamerkin.
    2.  Napsauta **Lisää paikkamerkki** -painiketta.
    3.  Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4.  Valitse **Lisää**.

6.  Tekstien käännökset voit lisätä seuraavasti:
    1.  Napsauta **Käännökset**-painiketta.
    2.  Napsauta esiin tulevalla sivulla **Lisää**-painiketta.
    3.  Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4.  Kirjota tekstisi **Käännetty teksti** -kenttään.
    5.  Voit mukauttaa tekstiä lisäämällä paikkamerkkejä. Ohjeet paikkamerkkien asettamisesta ovat vaiheessa 5.
    6.  Valitse **Sulje**.

7.  Käytä **Vastaanottaja**-välilehden seuraavia asetuksia määrittääksesi henkilöt, joille ilmoitukset lähetetään.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Vaihtoehto</th>
    <th>Ilmoitukset lähetetään näille käyttäjille</th>
    <th>Noudata seuraavia ohjeita lähettääksesi ilmoituksia</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Osallistuja</td>
    <td>Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</td>
    <td><ol>
    <li>Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Osallistuja</strong>-kohtaa.</li>
    <li>Valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</li>
    <li>Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Työnkulun käyttäjä</td>
    <td>Käyttäjät, jotka osallistuvat työnkulkuun</td>
    <td><ol>
    <li>Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Työnkulun käyttäjä</strong>-kohtaa.</li>
    <li>Valitse <strong>Työnkulun käyttäjä</strong> -välilehden <strong>Työnkulun käyttäjä</strong> -luettelosta tämän työnkulun osallistuja.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Käyttäjä</td>
    <td>Tietyt Finance and Operations -käyttäjät</td>
    <td><ol>
    <li>Napsauta <strong>Vastaanottaja</strong>-välilehdessä <strong>Käyttäjä</strong>-kohtaa.</li>
    <li><strong>Käyttäjä</strong>-välilehden <strong>Käytettävissä olevat käyttäjät</strong> -luettelo sisältää kaikki Dynamics 365 for Finance and Operations -käyttäjät. Valitse käyttäjät, joille ilmoituksia lähetetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Toista vaiheet 3-7 kullekin tapahtumalle, jonka valitsit vaiheessa 2.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Kirjoita kommentit työnkulkuun tekemistäsi muutoksista
Noudata seuraavia ohjeita, kun haluat määrittää työnkulkuun tehtyjen muutosten kommentteja.

1.  Valitse vasemmasta ruudusta **Huomautukset**.
2.  Kirjoita kommenttisi **Anna kommentteja työnkulusta** -kenttään.
3.  Tarkista kommenttisi. Kommentteja ei voi muokata lisäämisen jälkeen.
4.  Valitse **Lisää** lisätäksesi kommenttisi **Kommenttihistoria**-alueelle.





