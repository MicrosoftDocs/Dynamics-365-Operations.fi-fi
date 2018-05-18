---
title: "Hyväksyntävaiheen lisääminen työnkulkuun"
description: "Tässä ohjeaiheessa kerrotaan, miten hyväksyntävaiheen ominaisuudet määritetään."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d2fc157b54401463bbabf1e3f6d5dddc6bda9631
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-approval-step-in-a-workflow"></a>Hyväksyntävaiheen lisääminen työnkulkuun

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten hyväksyntävaiheen ominaisuudet määritetään.

Hyväksyntävaihe konfiguroidaan työnkulkueditorissa napsauttamalla hyväksyntävaihetta hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**, joka avaa **Ominaisuudet**-sivun. Sitten voit määrittää seuraavien ohjeiden avulla hyväksyntävaiheen ominaisuudet.

## <a name="name-the-step"></a>Vaiheen nimeäminen
Kirjoita näiden ohjeiden avulla nimi hyväksyntävaiheelle.

1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Kirjoita **Nimi**-kenttään hyväksyntävaiheen yksilöivä nimi.

## <a name="enter-a-subject-line-and-instructions"></a>Aiherivin ja ohjeiden määrittäminen
Sinun on luotava aiherivi ja ohjeet käyttäjille, jotka on määritetty hyväksyntävaiheeseen. Esimerkiksi jos olet konfiguroimassa ostoehdotusten hyväksyntävaiheen, vaiheelle määritetty käyttäjä näkee aiherivin ja ohjeet **Ostoehdotukset**-sivulla. Aiherivi näytetään sivulla olevalla viestirivillä. Käyttäjä voi sitten avata ohjeet napsauttamalla viestirivin kuvaketta. Seuraavia ohjeita noudattamalla voit määrittää aiherivin ja ohjeet.

1.  Napsauta vasemmassa ruudussa **Perusasetukset**.
2.  Kirjoita aiherivi **Työnimikkeen aihe** -kenttään.
3.  Voit mukauttaa aiheriviä lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat ilmoitusta, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:
    1.  Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.
    2.  Napsauta **Lisää paikkamerkki** -painiketta.
    3.  Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4.  Valitse **Lisää**.

4.  Aiherivin käännökset voit lisätä seuraavasti:
    1.  Napsauta **Käännökset**-painiketta.
    2.  Valitse esiin tulevalla sivulla **Lisää**.
    3.  Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4.  Kirjota tekstisi **Käännetty teksti** -kenttään.
    5.  Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 3 mukaisesti.
    6.  Valitse **Sulje**.

5.  Kirjoita ohjeet **Työnimikkeen ohjeet** -kenttään.
6.  Voit mukauttaa ohjeita lisäämällä paikkamerkkejä. Kun käyttäjät tarkastelevat ohjeita, paikkamerkit korvataan asianmukaisilla tiedoilla. Paikkamerkkejä voit lisätä seuraavasti:
    1.  Napsauta tekstiruudussa kohtaa, johon haluat lisätä paikkamerkin.
    2.  Napsauta **Lisää paikkamerkki** -painiketta.
    3.  Valitse esiin tulevasta luettelosta lisättävä paikkamerkki.
    4.  Valitse **Lisää**.

7.  Ohjeiden käännökset voit lisätä seuraavasti:
    1.  Napsauta **Käännökset**-painiketta.
    2.  Valitse esiin tulevalla sivulla **Lisää**.
    3.  Valitse esiin tulevasta luettelosta kieli, jolla kirjoitat tekstin.
    4.  Kirjota tekstisi **Käännetty teksti** -kenttään.
    5.  Voit mukauttaa tekstiä lisäämällä paikkamerkkejä vaiheen 6 mukaisesti.
    6.  Valitse **Sulje**.

## <a name="assign-the-approval-step"></a>Hyväksyntävaiheen liittäminen
Seuraavia ohjeita noudattamalla voit määrittää käyttäjät, joille hyväksyntävaihe määritetään.

1.  Valitse vasemmasta ruudusta **Määritys**.
2.  Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 3.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Vaihtoehto</th>
    <th>Käyttäjät, joille hyväksyntävaihe on määritetty</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Osallistuja</td>
    <td>Käyttäjät, jotka on määritetty tiettyyn ryhmään tai rooliin</td>
    <td><ol>
    <li>Valittuasi <strong>osallistujan</strong>, valitse <strong>Rooliperustainen</strong>-välilehdellä <strong>Osallistujan tyyppi</strong> -luettelosta ryhmän tai roolin tyyppi, jolle vaihe määritetään.</li>
    <li>Valitse <strong>Osallistuja</strong>-luettelosta, ryhmä tai rooli, jolle vaihe määritetään.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarkia</td>
    <td>Tietyssä organisaatiohierarkiassa olevat käyttäjät</td>
    <td><ol>
    <li>Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle vaihe määritetään.</li>
    <li>Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta. Nämä nimet edustavat käyttäjiä, joille vaiheen voi määrittää. Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste: <ol>
    <li>Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</li>
    <li>Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>. Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</li>
    </ol></li>
    <li>Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille vaihe määritetään: <ul>
    <li><strong>Määritä kaikille noudetuille työntekijöille</strong> – Vaihe määritetään joukon kaikille käyttäjille.</li>
    <li><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Vaihe määritetään vain joukon viimeiselle työntekijälle.</li>
    <li><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Vaihetta ei liitetä niille joukon käyttäjille, jotka täyttävät määritetyn ehdon. Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Työnkulun käyttäjä</td>
    <td>Nykyisen työnkulun käyttäjät</td>
    <td><ul>
    <li>Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Käyttäjä</td>
    <td>Tietyt Microsoft Dynamics 365 for Finance and Operations -käyttäjät</td>
    <td><ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät. Valitse käyttäjät, joille vaihe liitetään ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

3.  Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on suorittaa toimintoja tai vastata asiakirjoihin, jotka ovat hyväksyntävaiheessa. Valitse jompikumpi seuraavista vaihtoehdoista:
    -   **Tunnit** – Määritä käyttäjän vastausaika tunteina. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    -   **Päivät** – Määritä käyttäjän vastausaika päivinä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    -   **Viikot** – Määritä käyttäjän vastausaika viikkoina.
    -   **Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee antaa vastaus. Voit esimerkiksi haluta, että käyttäjä vastaa kuukauden kolmannen viikon perjantaihin mennessä.
    -   **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee antaa vastaus. Voit esimerkiksi haluta, että käyttäjä vastaa joulukuun kolmannen viikon perjantaihin mennessä.

    Jos käyttäjä reagoi asiakirjaan aikarajan puitteissa, asiakirja on erääntynyt. Erääntyneet asiakirjat eskaloidaan, sivun **Eskalointi**-alueessa valitsemiesi asetusten mukaan.
4.  Jos olet määrittänyt hyväksyntävaiheen useille käyttäjille tai käyttäjäryhmälle, valitse **Valmistumiskäytäntö**-välilehdessä jokin seuraavista vaihtoehdoista:
    -   **Yksi hyväksyjä** – Asiakirjan toimenpiteen valitsee ensimmäinen hyväksyntäpyyntöön vastaava henkilö. Esimerkiksi Sam on lähettänyt 15 000 dollarin kuluraportin. Kuluraportti on liitetty Suelle, Joelle ja Billille. Jos Sue on ensimmäinen asiakirjaan reagoiva henkilö, hänen valintansa on se, jota asiakirjaan sovelletaan. Jos Sue hylkää asiakirjan, se hylätään ja lähetetään takaisin Samille. Jos Sue hyväksyy asiakirjan, se lähetetään Annille hyväksyttäväksi. 

    ![Työnkulku, jolla on hyväksyntäprosessi](./media/workflow_multipleusersinstep.gif)

    -   **Suurin osa hyväksyjistä** – Asiakirjan toimenpide määräytyy sen mukaan, miten suurin osa hyväksyjistä vastaa hyväksyntäpyyntöön. Esimerkiksi Sam on lähettänyt 15 000 dollarin kuluraportin. Kuluraportti on liitetty Suelle, Joelle ja Billille. Jos Sue ja Jo ovat ensimmäiset vastauksen antaneet hyväksyjät, asiakirjan toimenpide määräytyy sen mukaan, miten he vastaavat pyyntöön.
        -   Jos Sue hyväksyy asiakirjan mutta Jo hylkää sen, asiakirja hylätään ja se lähetetään takaisin Samille.
        -   Jos molemmat Sue ja Jo hyväksyvät asiakirjan, se lähetetään Annille hyväksyttäväksi.
    -   **Prosenttiosuus hyväksyjistä** – Asiakirjan toimenpide määräytyy sen mukaan, miten vastaajien tietty prosenttiosuus vastaa pyyntöön. Esimerkiksi Sam on lähettänyt 15 000 dollarin kuluraportin. Kuluraportti on liitetty Suelle, Joelle ja Billille, ja olet määrittänyt prosenttiarvoksi **50**. Jos Sue ja Jo ovat ensimmäiset hyväksyjät, jotka vastaavat pyyntöön, heidän valitsemaansa toimintoa sovelletaan kohdistetaan asiakirjaan, koska hyväksyjien 50 prosentin vaatimus on täytetty.
        -   Jos Sue hyväksyy asiakirjan mutta Jo hylkää sen, asiakirja hylätään ja se lähetetään takaisin Samille.
        -   Jos molemmat Sue ja Jo hyväksyvät asiakirjan, se lähetetään Annille hyväksyttäväksi.
    -   **Kaikki hyväksyjät** – Kaikkien hyväksyjien on hyväksyttävä asiakirja. Muutoin työnkulku keskeytyy. Esimerkiksi Sam on lähettänyt 15 000 dollarin kuluraportin. Kuluraportti on liitetty Suelle, Joelle ja Billille. Jos Sue ja Joe hyväksyvät asiakirjan, mutta Bill hylkää sen, asiakirja hylätään ja se lähetetään takaisin Samille. Jos Sue, Jo ja Bill hyväksyvät asiakirjan, se lähetetään Annille hyväksyttäväksi.

## <a name="specify-when-the-approval-step-is-required"></a>Määritä, milloin hyväksyntävaihetta tarvitaan
Voit määrittää, milloin hyväksyntävaihetta tarvitaan Hyväksyntävaihe voi olla edellytys aina, tai se voi olla pakollinen vain, jos tietyt ehdot täyttyvät.

### <a name="the-approval-step-is-always-required"></a>Hyväksyntävaihe on aina pakollinen

Noudata seuraavia ohjeita, jos haluat hyväksyntävaiheen olevan aina pakollinen.

1.  Valitse vasemmasta ruudusta **Ehto**.
2.  Valitse **Suorita aina tämä vaihe**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Hyväksyntävaihe on pakollinen vain tietyissä tilanteissa

Määrittämäsi hyväksyntävaiheet saattavat olla pakollisia vain, kun tietyt ehdot täyttyvät. Jos esimerkiksi määrität hyväksyntävaihetta ostoehdotuksen työnkululle, haluat ehkä, että hyväksyntävaihe suoritetaan vain, jos ostoehdotuksen kokonaissumma on suurempi kuin 10 000 dollaria. Noudata seuraavia ohjeita, jos haluat määrittää tilanteet, joissa hyväksyntävaihe on pakollinen.

1.  Valitse vasemmasta ruudusta **Ehto**.
2.  Valitse **Suorita tämä vaihe vain, kun seuraava ehto täyttyy**.
3.  Määritä ehto.
4.  Kirjoita kaikki muut tarvittavat ehdot.
5.  Voit tarkistaa, onko ehdot määritetty oikein seuraavien ohjeiden avulla:
    1.  Valitse **Testi**.
    2.  Valitse tietue **Testaa työnkulun ehto** -sivun **Tarkista ehto** -alueella.
    3.  Valitse **Testi**. Järjestelmä arvioi, täyttääkö tietue määrittämäsi ehdot.
    4.  Palaa **Ominaisuudet**-sivulle valitsemalla **OK** tai **Peruuta**.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Erääntyneen asiakirjan toimenpiteiden määrittäminen
Jos käyttäjä reagoi asiakirjaan aikarajan puitteissa, asiakirja on erääntynyt. Erääntyneen asiakirjan voi eskaloida tai määrittää automaattisesti toisen käyttäjän hyväksyttäväksi. Seuraa näitä ohjeita, jos haluat eskaloida erääntyneet asiakirjat.

1.  Valitse vasemmasta ruudusta **Eskalointi**.
2.  Luo eskalointipolku valitsemalla **Käytä eskalointipolkua** -valintaruutu. Järjestelmä määrittää asiakirjan automaattisesti eskalointipolussa luetelluille käyttäjille. Seuraava taulukko on esimerkki eskalointipolusta.

    | Järjestys | Eskalointipolku      |
    |----------|----------------------|
    | 1        | Määritä rooliin: Donna     |
    | 2        | Määritä rooliin: Erin      |
    | 3        | Viimeinen toimi: Hylkäys |

    Tässä esimerkissä järjestelmä määrittää erääntyneen asiakirjan Donnalle. Jos Donna ei vastaa määräajassa, järjestelmä määrittää asiakirjan Erinille. Jos Erin ei vastaa määräajassa, järjestelmä hylkää asiakirjan.
3.  Voit lisätä käyttäjän eskalointipolkuun valitsemalla **Lisää eskalaatio**. Valitse **Määrityksen tyyppi** -välilehdellä jokin seuraavan taulukon vaihtoehdoista ja noudata vaihtoehdon toimia ennen siirtymistä vaiheeseen 4.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Vaihtoehto</th>
    <th>Käyttäjät, joille asiakirja eskaloidaan</th>
    <th>Lisävaiheet</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarkia</td>
    <td>Tietyssä organisaatiohierarkiassa olevat käyttäjät</td>
    <td><ol>
    <li>Valittuasi <strong>hierarkian</strong>, valitse <strong>Hierarkian valinta</strong> -välilehdellä <strong>Hierarkian tyyppi</strong> -luettelosta hierarkian tyyppi, jolle asiakirja eskaloidaan.</li>
    <li>Järjestelmän on noudettava käyttäjien nimijoukko hierarkiasta. Nämä nimet edustavat käyttäjiä, joille asiakirjan voi eskaloida. Noudata näitä ohjeita määrittääksesi järjestelmän noutamien käyttäjänimien joukon aloituspiste ja lopetuspiste: <ol>
    <li>Määritä aloituspiste valitsemalla henkilö <strong>Alku</strong>-luettelosta.</li>
    <li>Määritä lopetuspiste valitsemalla <strong>Lisää pysäytysehto</strong>. Määritä sitten ehto, joka ilmaisee, missä kohtaa hierarkiaa järjestelmä lopettaa nimien noutamisen.</li>
    </ol></li>
    <li>Määritä <strong>Hierarkian asetukset</strong> -välilehdellä, mille valitun joukon käyttäjille asiakirja eskaloidaan: <ul>
    <li><strong>Määritä kaikille noudetuille työntekijöille</strong> – Asiakirja eskaloidaan joukon kaikille käyttäjille.</li>
    <li><strong>Määritä vain viimeksi noudetulle käyttäjälle</strong> – Asiakirja eskaloidaan vain joukon viimeiselle työntekijälle.</li>
    <li><strong>Jätä pois käyttäjät, joilla on seuraava ehto</strong> – Asiakirjaa ei eskaloida niille joukon käyttäjille, jotka täyttävät määritetyn ehdon. Määritä ehto valitsemalla <strong>Lisää ehto</strong>.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Työnkulun käyttäjä</td>
    <td>Nykyisen työnkulun käyttäjät</td>
    <td><ul>
    <li>Valittuasi <strong>työnkulun käyttäjän</strong>, valitse <strong>Työnkulun käyttäjä</strong> -välilehdessä <strong>Työnkulun käyttäjä</strong> -luettelosta käyttäjä, joka osallistuu työnkulun.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Käyttäjä</td>
    <td>Tietyt Finance and Operations -käyttäjät</td>
    <td><ol>
    <li>Valittuasi <strong>käyttäjän</strong>, napsauta <strong>Käyttäjä</strong>-välilehteä.</li>
    <li><strong>Käytettävissä olevat käyttäjät</strong>: luettelo sisältää kaikki Finance and Operations -käyttäjät. Valitse käyttäjät, joille asiakirja eskaloidaan ja siirrä nämä käyttäjät <strong>Valitut käyttäjät</strong> -luetteloon.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  Määritä **Aikaraja**-välilehden **Kesto**-kenttään kuinka paljon aikaa käyttäjällä on suorittaa toimintoja tai vastata asiakirjoihin. Valitse jompikumpi seuraavista vaihtoehdoista:
    -   **Tunnit** – Määritä käyttäjän vastausaika tunteina. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    -   **Päivät** – Määritä käyttäjän vastausaika päivinä. Valitse sitten kalenteri, jota organisaatio käyttää ja määritä organisaation työviikon tiedot.
    -   **Viikot** – Määritä käyttäjän vastausaika viikkoina.
    -   **Kuukaudet** – Valitse päivä ja viikko, johon mennessä käyttäjän tulee antaa vastaus. Voit esimerkiksi haluta, että käyttäjä vastaa kuukauden kolmannen viikon perjantaihin mennessä.
    -   **Vuodet** – Valitse päivä, viikko ja kuukausi, johon mennessä käyttäjän tulee antaa vastaus. Voit esimerkiksi haluta, että käyttäjä vastaa joulukuun kolmannen viikon perjantaihin mennessä.

5.  Toista vaiheet 3 ja 4 jokaiselle käyttäjälle, joka lisätään eskalointipolkuun. Käyttäjien järjestystä voi muuttaa.
6.  Jos eskalointipolun käyttäjät eivät vastaa asiakirjaan ajoissa, järjestelmä suorittaa asiakirjan toimenpiteen automaattisesti. Voit määrittää järjestelmän suorittaman toimenpiteen valitsemalla **Toimenpide**-rivin ja sitten valitsemalla **Lopetustoiminto**-välilehdellä toimenpiteen.





