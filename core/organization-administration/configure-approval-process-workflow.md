---
title: "Määrittää hyväksymisprosessin työnkulku"
description: "Määritä hyväksyntäprosessin ominaisuudet seuraavan menettelyn avulla."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 579e393ef64bc5ad72d129ac08ac215c524d5c55
ms.lasthandoff: 03/31/2017


---

# <a name="configure-an-approval-process-in-a-workflow"></a>Määrittää hyväksymisprosessin työnkulku

Määritä hyväksyntäprosessin ominaisuudet seuraavan menettelyn avulla.

Määrittämään sen hyväksymisprosessi työnkulkueditori hyväksynnän elementti hiiren kakkospainikkeella ja valitse sitten **ominaisuudet** avaamiseen **ominaisuudet** lomake.
Hyväksyntäprosessin nimeäminen
-------------------------

Seuraavia ohjeita noudattamalla voit nimetä hyväksyntäprosessin.
1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Kirjoita hyväksyntäprosessin yksilöivä nimi **Nimi**-kenttään.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Määritä, milloin järjestelmä käsittelee asiakirjaa automaattisesti
Voit määrittää järjestelmän siten, että se käsittelee automaattisesti asiakirjan, jos tietyt ehdot täyttyvät. Järjestelmä voi hyväksyä esimerkiksi kuluraportit, joiden kokonaissummat ovat alle 100 USD. Noudata seuraavia ohjeita määrittääksesi, milloin järjestelmä käsittelee asiakirjaa.
1.  Valitse vasemmasta ruudusta **Automaattiset toiminnot**.
2.  Merkitse **Ota käyttöön automaattiset toiminnot** -valintaruutu.
3.  Click **Add condition**.
4.  Määritä ehto.
5.  Voit tarvittaessa määrittää useita ehtoja.
6.  Voit tarkistaa, onko ehdot määritetty oikein käymällä läpi seuraavat ohjeet:
    1.  Valitse **Testi**, jolloin **Testaa työnkulun ehto** -lomake tulee näyttöön.
    2.  Valitse tietue lomakkeen **Tarkista ehto** -alueelta.
    3.  Valitse **Testi**. Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.
    4.  Valitse **OK** tai **peruuttaa** palaa **ominaisuudet** muodossa.

7.  Valitse **Automaattinen loppuunvientitoiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan asiakirjalle.

## <a name="specify-when-notifications-are-sent"></a>Määritä, milloin ilmoitukset lähetetään
Voit lähettää käyttäjille ilmoituksia, kun asiakirja on hyväksytty, hylätty, delegoitu tai eskaloitu, tai kun muutosta on pyydetty. Toimi seuraavasti määrittääksesi, milloin ilmoitukset lähetetään, ja kenelle ne lähetetään.
1.  Valitse vasemmasta ruudusta **Ilmoitukset**.
2.  Valitse tapahtuman vieressä oleva valintaruutu, jos haluat lähettää siihen liittyviä ilmoituksia:
    -   **Edustaja** – kun asiakirja on määritetty toiselle käyttäjälle hyväksyntää varten.
    -   **Eskaloi** – kun määritetty käyttäjä ei ole reagoinut asiakirjan annetussa ajassa.
    -   **Hyväksy** – kun asiakirja on hyväksytty.
    -   **Hylkää** – kun asiakirja on hylätty.
    -   **Pyydä muutosta** – kun määritetty käyttäjä on pyytänyt muutosta lähetettyyn asiakirjaan.

3.  Valitse sen tapahtuman rivi, jonka valitsit vaiheessa 2.
4.  Valitse **Ilmoitusteksti**-välilehti.
5.  Kirjoita tekstiruutuun ilmoitusteksti.
6.  Voit mukauttaa tekstiä lisäämällä siihen paikkamerkkejä, jotka korvataan sopivilla tiedoilla, kun ne näytetään käyttäjille. Paikkamerkkejä voit lisätä seuraavasti:
    1.  Napsauta tekstiruutua kohdassa, johon haluat lisätä paikkamerkin.
    2.  Napsauta **Lisää paikkamerkki** -painiketta.
    3.  Valitse näyttöön tulevasta luettelosta lisättävä paikkamerkki.
    4.  Valitse **Lisää**.

7.  Lisää käännöksiä ilmoituksen valitsemalla **käännökset**. Käy näyttöön tulevassa lomakkeessa läpi seuraavat vaiheet:
    1.  Click **Add**.
    2.  Valitse näyttöön tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    3.  Kirjota tekstisi **Käännetty teksti** -tekstiruutuun.
    4.  Voit mukauttaa tekstiä lisäämällä paikkamerkkejä.
    5.  Valitse **Sulje**.

8.  Valitse **Vastaanottaja**-välilehti.
9.  Määritä, kenelle ilmoitukset lähetetään Valitse jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 10.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Vaihtoehto</th>
    <th>Ilmoituksen vastaanottajat</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>Osallistuja</strong></td>
    <td>Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</td>
    <td><ol>
    <li>Valittuasi <strong>Osanottaja</strong> napsauta <strong>Rooliperustainen</strong>-välilehti.</li>
    <li>Valitse <strong>Osallistujan tyyppi</strong>-luettelosta ryhmän tai roolin tyyppi, jolle ilmoituksia lähetetään.</li>
    <li>Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle ilmoituksia lähetetään.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><strong>Työnkulun käyttäjä</strong></td>
    <td>Nykyiseen työnkulkuun osallistuvat käyttäjät</td>
    <td><ol>
    <li>Valittuasi <strong>Työnkulun käyttäjä</strong> napsauta <strong>Työnkulun käyttäjä</strong>-välilehteä.</li>
    <li>Valitse <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulkuun.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><strong>User</strong></td>
    <td>Tietyt Microsoft Dynamics-365 toimintoja käyttäjille</td>
    <td><ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Microsoft Dynamics-365 toimintoja käyttäjille. Valitse käyttäjät, joille ilmoituksia lähetetään, ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. Toista vaiheet 3-9 kullekin tapahtumalle, jonka valitsit vaiheessa 2.

## <a name="specify-a-final-approver"></a> Lopullisen hyväksyjän määrittäminen
Voit halutessasi määrittää lopullisen hyväksyjän skenaarioissa, joissa hyväksyjä on henkilö, joka lähetti asiakirjan hyväksyttäväksi. Määritä lopullinen hyväksyjä käymällä läpi seuraavat vaiheet.
1.  Napsauta vasemmassa ruudussa **Lisäasetukset**.
2.  Valitse **Käytä lopullista hyväksyjää** -valintaruutu.
3.  Valitse luettelosta käyttäjä, joka on lopullinen hyväksyjä.

## <a name="set-a-time-limit"></a>Aikarajan määrittäminen
Noudata seuraavia ohjeita, jos hyväksyntäprosessi on suoritettava tietyn ajan kuluessa.
| **Huomautus **                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tässä vaiheessa valitsemasi asetukset korvaavat asetukset, jotka olet valinnut kunkin hyväksyntävaiheen **Määritys**- ja **Eskalointi**-kohdissa. |

1.  Napsauta vasemmassa ruudussa **Lisäasetukset**.
2.  Valitse **Aseta aikaraja työnkulun****elementille** -valintaruutu.
3.  Merkitse **Kesto**-kenttään aika, johon mennessä hyväksyntäprosessi on suoritettava. Valitse jompikumpi seuraavista vaihtoehdoista:
    -   **Tunti**: Määritä tuntimäärä, jonka kuluessa hyväksyntäprosessi on suoritettava. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    -   **Päivä**: Määritä päivien lukumäärä, jonka kuluessa hyväksyntäprosessi on suoritettava. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    -   **Viikko**: Määritä viikkomäärä, jonka kuluessa hyväksyntäprosessi on suoritettava.
    -   **Kuukausi** – Valitse päivä ja viikko, johon mennessä hyväksyntäprosessi on suoritettava. Voit esimerkiksi määrittää, että hyväksyntäprosessi on suoritettava kuukauden kolmannen viikon perjantaihin mennessä.
    -   **Vuosi** – Valitse päivä, viikko ja kuukausi, johon mennessä hyväksyntäprosessi on suoritettava. Voit esimerkiksi määrittää, että hyväksyntäprosessi on suoritettava joulukuun kolmannen viikon perjantaihin mennessä.

4.  Jos aikaraja ylittyy, järjestelmä käsittelee asiakirjan automaattisesti. Valitse **Toiminto**-luettelosta toiminto, jonka haluat järjestelmän suorittavan.

## <a name="specify-which-actions-are-available-to-the-user"></a>Määritä käyttäjän käytettävissä olevat toiminnot
Kun asiakirja on määritetty käyttäjälle hyväksymistä varten, käyttäjän pitää suorittaa asiakirjan toimenpide. Käy läpi seuraavat vaiheet määrittääksesi, mitä toimintoja käyttäjät voivat tehdä lähetetylle asiakirjalle.
1.  Napsauta vasemmassa ruudussa **Lisäasetukset**.
2.  Valitse **Hyväksy** valintaruudun valinta, jos käyttäjä voi hyväksyä asiakirjan.
3.  Valitse **hylätä** valintaruutu on valittuna käyttäjä voi hylätä asiakirjan.
4.  Valitse **Pyydä muutosta** käyttäjän valintaruutu voit pyytää muutoksia asiakirjaan.
5.  Valitse **edustaja** valintaruudun valinta, jos käyttäjä voi määrittää asiakirjan toisen käyttäjän hyväksyttäväksi.

**Huomautus**: **Ota työluettelon toiminnot käyttöön yritysportaalissa** -valintaruutu on poistettu.

## <a name="configure-the-approval-steps"></a> Hyväksyntävaiheiden konfiguroiminen
Hyväksyntäprosessi koostuu hyväksymisvaiheista. Lisää hyväksyntäprosessiin vaiheita ja määritä vaiheet tekemällä seuraava menettely.
1.  Kaksoisnapsauta hyväksyntäprosessia työnkulun editorissa. Työnkulun editori näyttää hyväksyntäprosessin vaiheet.
2.  Hyväksyntävaihe lisätään vetämällä vaihe **Työnkulun elementit** -alueelta alustalle.
3.  Lisätietoja hyväksyntävaiheen konfiguroimisesta on kohdassa [Hyväksyntävaiheen konfiguroiminen](http://axhelp.dynamics.com/en/wiki/configure-an-approval-step/).




