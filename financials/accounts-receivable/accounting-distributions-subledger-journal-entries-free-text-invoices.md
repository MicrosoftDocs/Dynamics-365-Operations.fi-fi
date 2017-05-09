---
title: "Vapaatekstilaskujen kirjanpidolliset jaot ja alatason kirjauskansion merkinnät"
description: "Kirjanpidollisia jakoja käytetään määritettäessä summan käsittely, kuten esimerkiksi se, miten tuottoa, veroa tai maksua käsitellään vapaatekstilaskussa. Jokaisella määrällä, joka on huomioitava vapaatekstilaskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e7a40509a50d7c059574c85952501f8a7a926e0f
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a>Vapaatekstilaskujen kirjanpidolliset jaot ja alatason kirjauskansion merkinnät

[!include[banner](../includes/banner.md)]


Kirjanpidollisia jakoja käytetään määritettäessä summan käsittely, kuten esimerkiksi se, miten tuottoa, veroa tai maksua käsitellään vapaatekstilaskussa. Jokaisella määrällä, joka on huomioitava vapaatekstilaskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako.

<a name="accounting-distributions"></a>Kirjanpidolliset jaot
------------------------

Seuraavilla Vapaatekstilasku-sivun painikkeilla voit tarkastella ja mahdollisesti muokata kirjanpidollisia jakoja kullekin vapaatekstilaskun summalle.

-   **Jaa summat** – Tarkastele ja muuta yksittäisen rivin ja sen alarivien, kuten verojen tai kulujen, kirjanpidollisia jakoja. Voit tarkastella ja muuttaa alarivin kirjanpidollisia jakoja myös suoraan Arvonlisäverotapahtumat- tai Kulutapahtumat-sivulla.
    -   Muuta vapaatekstilaskun otsikon summia, kuten kuluja tai valuutan pyöristyssummia.
    -   Muuta vapaatekstilaskun rivisummia.
-   **Näytä jakaumat** – Näytä asiakirjan kaikkien rivien kirjanpidolliset jaot. Et voi muuttaa kirjanpidollisia jakoja tästä näkymästä.
    -   Näytä otsikon ja rivien summat.

## <a name="distributing-amounts"></a>Summien jakaminen
Kun annat vapaatekstilaskun, jokainen määrä jaetaan seuraavasti.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Kirjoita rahasumma</th>
<th>Mistä päätili näytetään</th>
<th>Tärkeysjärjestys, joka määrittää, mikä oletusarvoinen taloushallinnon dimensio tulee näkyviin.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vapaatekstilaskun rivi</td>
<td>Vapaatekstilaskurivin kirjanpitotili.</td>
<td><ol>
<li>Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</li>
<li>Jos päätili ei ole kohdistustili, käytä vapaatekstilaskun rivillä taloushallinnon dimension oletusmallia.</li>
<li>Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</li>
<li>Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</li>
</ol></td>
</tr>
<tr class="even">
<td>Käyttöomaisuustunnuksen ja arvomallin yhdistelmän vapaatekstilaskun rivi
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Huomautus </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vapaatekstilaskun rivin päätili on käyttöomaisuuden poistotili.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Vapaatekstilaskurivin kirjanpitotili.</td>
<td><ol>
<li>Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</li>
<li>Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Vapaatekstilaskun alennussumman</td>
<td>Asiakkaan alennusten päätili -kenttä Käteisalennukset-sivulla.</td>
<td><ol>
<li>Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</li>
<li>Jos päätili ei ole kohdistustili, käytä vapaatekstilaskun rivillä taloushallinnon dimension oletusmallia.</li>
<li>Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</li>
<li>Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</li>
</ol></td>
</tr>
<tr class="even">
<td>Vapaatekstilaskun arvonlisäveron summa</td>
<td>Maksettava arvonlisävero -kenttä Kirjanpidon kirjausryhmät -sivulla.</td>
<td><ol>
<li>Käytä taloushallinnon dimensioita, jotka on määritetty vapaatekstilaskun rivisummassa tai maksurivin summan jaossa.</li>
<li>Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</li>
<li>Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Vapaatekstilaskun maksurivin summa</td>
<td>Kredit-tili-kenttä Kulujen koodi -sivulla.</td>
<td><ol>
<li>Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</li>
<li>Jos päätili ei ole kohdistustili, käytä vapaatekstilaskun rivillä taloushallinnon dimension oletusmallia.</li>
<li>Käytä taloushallinnon dimension oletusarvoja vapaatekstilaskun rivillä.</li>
<li>Käytä Tilikartta-sivun kirjanpitotilin taloushallinnon dimension oletusarvoja.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Verojen jakaminen
verojen kirjanpidollisia jakoja ei voi luoda ennen verojen laskentaa. Jotta voit laskea arvonlisäverot, sinun on suoritettava jokin seuraavista Vapaatekstilasku-lomakkeen tehtävistä:
-   Näytä arvonlisävero.
-   Näytä laskun summa.
-   Näytä kassavirta.
-   Näytä koko vapaatekstilaskun kirjanpidolliset jaot.
-   Näytä alareskontran kirjauskansio.

## <a name="subledger-journals-for-free-text-invoices"></a> Vapaatekstilaskujen alareskontran kirjauskansiot
Ennen kuin kirjaat vapaatekstilaskun, voit tarkastella laskun koko kirjanpitokirjausta, joka sisältää hyvitykset ja veloitukset, jotta voit varmistaa, että lasku kirjataan oikeille tileille. Tämä kirjanpitomerkinnän koko näkymä tunnetaan nimellä alareskontran kirjauskansio. Jos alareskontran kirjauskansiovienti on virheellinen esikatselussa, et voi muuttaa sitä ennen kuin kirjaat vapaatekstilaskun. Sen sijaan sinun on muutettava kirjanpidollisia jakoja tai kirjausprofiilia. Kirjanpidollisia jakoja käytetään määrittämään yksi kirjanpitomerkinnän puolista, debet tai kredit. Alareskontran kirjauskansion kirjanpitoviennin vastakirjaus luodaan kirjausprofiileista, kuten asiakastilistä tai verosta.




