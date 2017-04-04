---
title: SEPA-tilisiirron yleiskatsaus
description: "Tässä artikkelissa on yleisiä tietoja ISO 20022 tilisiirroista, jotka sisältävät yhden euron maksuja alue (SEPA) tilisiirroista ja muita sähköisiä maksuja toimittajille. SEPA-hyvityksen siirto on maksu euroina yritykseltä tai yksittäisiä toisen yrityksen tai yksittäisen tietyntyyppisiä. Ohjeessa kerrotaan myös, miten määrittää ja välittää luoton maksun siirtotiedosto."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>SEPA-tilisiirron yleiskatsaus

Tässä artikkelissa on yleisiä tietoja ISO 20022 tilisiirroista, jotka sisältävät yhden euron maksuja alue (SEPA) tilisiirroista ja muita sähköisiä maksuja toimittajille. SEPA-hyvityksen siirto on maksu euroina yritykseltä tai yksittäisiä toisen yrityksen tai yksittäisen tietyntyyppisiä. Ohjeessa kerrotaan myös, miten määrittää ja välittää luoton maksun siirtotiedosto.

## <a name="what-is-a-credit-transfer-message"></a>Mikä on viestin siirto luotto?
Sanoman siirto luotto on pyyntö, joka siirtää varoja lukuunsa velkojan lähettää aloitteen tehnyt osapuoli (yritys). Viestejä monta tilisiirron maa-/ aluekohtaiset- ja pankki-kohtaisten toteutusten. Jotkin niistä käytetään yhden maan sisällä, ja joitakin standardeja on tulossa. Yksi vakiintunut yleinen standardi on ISO 20022 ja sen aloittamista viestit, kuten-tilisiirrolla. Seuraavassa kuvassa on suhteita ja valitun luotto siirtää viestejä kattavuus. 
![Siirto luotto](./media/credit-transfer.jpg) hyvitys siirtää viestejä\[/tekstitys\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Mitä ovat ISO 20022- ja SEPA-maksut?
Euroopan komissio loi yhtenäinen euromaksualueen (SEPA:n) ja sen perusteella kaikkia sähköisiä maksuja pidetään kotimaan maksuina riippumatta siitä, missä maassa tai millä alueella henkilö, yritys tai organisaatio ja pankki sijaitsevat. Ei ole eroa kansallisia maksuja ja rajat ylittävistä euromääräisistä maksuista. SEPA sisältää 28 jäsenvaltioiden Euroopan unionin (EU), ja myös Islannin, Liechtensteinin, Norjan, Sveitsin, Monaco, ja San Marino. SEPA auttaa muodostamaan yksittäisen markkinan maksutapahtumille Euroopan talousalueella (ETA). SEPA:n odotetaan lopulta vähentävän sitä maksumuotojen määrää, joiden kanssa pankkien, liikeyritysten ja yksityishenkilöiden on toimittava. Euroopan komissio määritti SEPA-maksujen oikeudellisen perustan maksupalveludirektiivin avulla. Euroopan maksuneuvosto (EPC) tukee SEPA-aluetta seuraavilla toimilla:

-   Se määrittää sähköisten SEPA-maksujen standardit käyttämällä XML-pohjaista rahoitusalan sanomavälitysjärjestelmää (ISO 20022).
-   Se luo euromaksujen käsittelysäännöt ja -ohjeistuksen.

Eurooppalaisista pankeista muodostuva EPC kehittää SEPA-maksuvälineiden kaupallista ja teknistä ympäristöä. Käytössä on kolme SEPA-maksutyyppiä:

-   Tilisiirrot
-   Suoraveloitukset
-   Kortit

## <a name="what-is-a-sepa-credit-transfer"></a>Mikä SEPA-tilisiirto on?
SEPA-tilisiirto on toisen yrityksen tai henkilön toiselle yritykselle tai henkilölle suorittama maksu. Maksujen on oltava euromääräisiä ja niissä on oltava kummankin osapuolen kansainvälinen tilinumero (IBAN) ja BIC (Bank Identifier Code) -koodi. (Society for Worldwide Interbank Financial Telecommunication käytetään myös nimitystä BIC-koodi \[SWIFT\] koodia.) Lisäksi kustannukset on jaettava molempien osapuolten välillä. Osapuolten välisissä tilisiirroissa on käytettävä EPC:n määritysten mukaisia XML-tiedostoja, jotka vastaavat ISO 20022 -maksukäsittelystandardeja ja XML-muotoa.

## <a name="how-is-a-credit-transfer-implemented"></a>Miten hyvityksen siirto on toteutettu?
Luoton siirto maksumuoto Euroopan maissa on toteutettu sähköisen raportoinnin (ER) ja menetelmät maksujen toimintojen avulla Dynamics 365 operaatioille. Muutama luotto siirtää muotoja, joita käytetään muilla alueilla edelleen käyttää vanhaa maksun yhteydessä. Monessa muussa muodossa kesken on kaksitoista ISO 20022 luoton siirto tiedostomuotoja, jotka ovat käytettävissä. Nämä vientimuodot SEPA ISO 20022 XML-standardin mukaisia. Niitä käytetään luomaan-euro maat/alueet, joissa niitä käytetään ja euron maksut SEPA luotto siirtää järjestelmän Rulebook, EPC vapauttaa versio 8.2 määriteltyä maksunsiirtojen. Ennen kuin otat tilisiirroista, ota yhteyttä pankin saada ohjelmisto, joka edellyttää sähköisen maksuliikenteen tiedostojen lataaminen. XML-tiedostoja, jotka sisältävät maksumääräykset pankkiin siirtää ohjelmiston avulla.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Luoton siirto missä muodoissa tällä hetkellä tueta Dynamics 365 työvaiheiden?
Aina siirry jaettujen resurssikirjasto Microsoft Dynamics Lifecycle Services (LCS) ja tarkastella uusimmat käytettävissä olevat tiedostot, joiden käyttöomaisuuden tyyppi **GER kokoonpano**. Seuraava on linkki aiheeseen, jossa kerrotaan, miten luodaan LCS-säilö, tarkista käytettävissä olevat kokoonpanot ja tuoda valitut konfiguroinnit-osassa, "Mitä minun pitää määrittäminen?".

## <a name="what-do-i-have-to-set-up"></a>Mitä asetuksia on määritettävä?
-   Ennen kuin voit luoda tiedostoja tilisiirto, vähintään yksi aktiivinen luoton siirto määritys on tuoda ER-kokoonpanoissa. Lisätietoja on ohjeaiheessa [ladata sähköisen raportoinnin Lifecycle Services-kokoonpanojen](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Kun maksettava maksutavat, valitse **yleisen sähköisen raportoinnin** -valintaruutu ja valitse sopiva hyvitys siirron muodossa (esimerkiksi **ISO 20022-tilisiirrolla (AT)**) kuin vienti-muotokonfiguraatioon.
-   On myös määritettävä Dynamics 365 työvaiheiden oikeudellisen yksikön ja pankkitilin tietoja.
-   Tilinumerot, IBANs ja joskus myös SWIFT koodit (BICs) tai muut tunnukset ovat voimassa-tilisiirrolla maksujen luominen edellyttää. Tämän vuoksi on määritettävä ne toimittajan pankkitilin ja organisaatio, joka pyytää siirto pankkitilille.
-   Lisätiedot voivat olla tarpeen esimerkiksi osapuolet, jotka ovat tarkoitettu viestin siirto luotto numerot arvonlisävero (ALV). Nämä tiedot on määritettävä toimittajat ja oikeushenkilön kun sitä pyydetään.
-   Jotkin tilit ostoreskontran maksutavoista, lähinnä ISO 20022-pohjainen maksutavat, saattavat vaatia lisäasetuksia, **maksun muodossa koodin joukot**, kuten **palvelun tyyppi** = **SLEV**. Näitä koodeja käytetään kuin muut tunnisteet maksutapahtumien maksujen käsittelyn aikana. Oletusarvot maksuehtojen koodit, kuten **luokan tarkoitus**, **kulu tuottavat**, **paikallisen laitteen** ja **palvelutasolla** voidaan määrittää kahdella tavalla. Ensimmäinen paikka on **asiakkaiden maksettavien maksujen kirjauskansion otsikko** ja toinen **tilit maksettavat maksut menetelmät**. Maksun kirjauskansion rivien luonnin yhteydessä maksun maksukirjauskansion ylätunnisteen asettaa arvot ovat siirretään kirjauskansion riville, jos ei ole asetettu, maksutavat kentän arvoista käytetään.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Mitkä parametrit ovat käytettävissä luotaessa hyvityksen siirron maksut?
Tietyt parametrit riippuu luotto siirron muodossa. Seuraavassa taulukossa esitetään parametrit, jotka ovat käytettävissä, kun toimittajan maksukirjauskansio luodaan ISO 20022 luoton maksun siirtotiedosto Saksassa. Käytettävissä olevien vaihtoehtojen avulla **tausta-ajo** -välilehdessä, voit suorittaa maksun luominen komentojonotilassa.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kenttä</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Erävaraus</td>
<td>Tämän valintaruudun valinta sisällyttää erävaraustunnisteen XML-tiedostoon.</td>
</tr>
<tr class="even">
<td>Käsittelypäivä</td>
<td>Anna päivämäärä, jolloin pankki käsittelee maksut.</td>
</tr>
<tr class="odd">
<td>Muoto</td>
<td>Valitse maksusuoritustietojen muoto maan tai alueen tai pankin vaatimusten mukaan:
<ul>
<li><strong>Strd</strong> – valitsemalla tämän vaihtoehdon voit käyttää jäsennellyssä muodossa, kun yksi maksurivi täsmäytetään yhteen laskuun. Tämä vaihtoehto ei ole käytettävissä, Ranskan, Saksan ja Alankomaiden maa-/ aluekohtaiset vientimuodot.</li>
<li><strong>Ustrd</strong> – Tällä vaihtoehdolla valitaan jäsentämätön muoto, kun maksu tilitetään useille laskuille. Tilitettyjen laskujen laskunumerot yhdistetään ja niitä käytetään maksusuoritustietoina. ISO 20022 noudattaen suuntaviivojen rakenteeton maksun tiedot on rajoitettu 140 merkkiä.</li>
</ul></td>
</tr>
<tr class="even">
<td>Laskujen määrä</td>
<td>Laskujen määrä, että <strong>maksuehdotuksen</strong> raportti tulostetaan kirjauskansiosta.</td>
</tr>
<tr class="odd">
<td>Järjestysnumero</td>
<td>Anna järjestysnumero, jolla tiedosto tunnistetaan. Sarjanumero näkyy <strong>osallistumishuomautus</strong> raportti.</td>
</tr>
<tr class="even">
<td>Tulosta osallistumishuomautus</td>
<td>Tulosta <strong>Osallistumishuomautus</strong>-raportin valitsemalla tämä valintaruutu.</td>
</tr>
<tr class="odd">
<td>Tulosta valvontaraportti</td>
<td>Tulosta maksutiedot sisältävä raportti valitsemalla tämä valintaruutu.</td>
</tr>
<tr class="even">
<td>Tulosta lähetekirje</td>
<td>Tulosta <strong>Maksuehdotus</strong>-raportti valitsemalla tämä valintaruutu.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Mitä lyhenteet IBAN ja BIC tarkoittavat?
Kansainvälisen pankkitilin numero (IBAN) ja (pankin Identifier Code, BIC) käytetään monissa maissa ja alueilla eri puolilla maailmaa tahansa tilin. Näitä ovat 34 SEPA maat/alueet. BIC-Anna **SWIFT-koodi** kenttä ja IBAN- **IBAN** kenttä. Saajan pankkitilin numero ja asiakkaan pankkitilin nämä kentät sijaitsevat **Lisätunnus** -pikavälilehdessä **pankkitilin** -välilehdessä **Pankkitilit** sivulla. BIC käyttöön SEPA-maksut ei ole enää voimassa.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Miten maksutiedosto siirretään pankkiin?
Kun maksut, maksutiedoston luodaan ja sinua pyydetään tallentamaan sen web-selaimessa käytettävissä missä tahansa sijainnissa. Seuraava vaihe on lähettää XML-tiedoston pankkiin. Tämä prosessi vaihtelee pankeittain. Lähetä tiedostot pankkiin käsiteltäviksi pankin ohjeiden mukaisesti.


