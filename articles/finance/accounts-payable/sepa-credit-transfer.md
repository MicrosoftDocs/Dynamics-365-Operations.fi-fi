---
title: SEPA-tilisiirron yleiskatsaus
description: Tässä artikkelissa on yleisiä tietoja ISO 20022 -tilisiirroista, jotka sisältävät yhtenäisen euromaksualueen (Single Euro Payments Area, SEPA) tilisiirrot ja muut toimittajille suoritettavat sähköiset maksut. SEPA-tilisiirto on tietyntyyppinen toisen yrityksen tai henkilön toiselle yritykselle tai henkilölle suorittama euromääräinen maksu. Aiheessa selitetään myös tilisiirron maksutiedoston määrittäminen ja siirtäminen.
author: sunfzam
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "11124"
- intro-internal
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc37dde8829abdd26a224adbd788538834f4d320
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984024"
---
# <a name="sepa-credit-transfer-overview"></a>SEPA-tilisiirron yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on yleisiä tietoja ISO 20022 -tilisiirroista, jotka sisältävät yhtenäisen euromaksualueen (Single Euro Payments Area, SEPA) tilisiirrot ja muut toimittajille suoritettavat sähköiset maksut. SEPA-tilisiirto on tietyntyyppinen toisen yrityksen tai henkilön toiselle yritykselle tai henkilölle suorittama euromääräinen maksu. Aiheessa selitetään myös tilisiirron maksutiedoston määrittäminen ja siirtäminen.

## <a name="what-is-a-credit-transfer-message"></a>Mikä on tilisiirron sanoma?
Tilisiirron sanoma on pyyntö, jonka aloittava osapuoli (oma yrityksesi) lähettää siirtääkseen varoja omalta tililtään velkojan tilille. Tilisiirron sanomille on useita maa/aluekohtaisia ja pankkikohtaisia toteutuksia. Jotkin niistä käytetään yhden maan/alueen sisällä, ja joistakin on muodostumassa standardeja. Yksi vakiintunut yleinen standardi on ISO 20022 ja sen aloitussanomat, kuten Tilisiirto. Seuraavassa kuvassa esitetään valittujen tilisiirron sanomien suhteet ja kattavuus. 
![Tilisiirto.](./media/credit-transfer.jpg) Tilisiirron sanomat 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Mitä SEPA- ja ISO 20022 -maksut ovat?
Euroopan komissio loi yhtenäinen euromaksualueen (SEPA:n) ja sen perusteella kaikkia sähköisiä maksuja pidetään kotimaan maksuina riippumatta siitä, missä maassa tai millä alueella henkilö, yritys tai organisaatio ja pankki sijaitsevat. Kansallisten ja kansainvälisten maksujen välillä ei ole eroja. SEPA koostuu 28 Euroopan unionin (EU) jäsenvaltiosta sekä Islannista, Liechtensteinista, Norjasta, Sveitsistä, Monacossa ja San Marinosta. SEPA auttaa muodostamaan yksittäisen markkinan maksutapahtumille Euroopan talousalueella (ETA). SEPA:n odotetaan lopulta vähentävän sitä maksumuotojen määrää, joiden kanssa pankkien, liikeyritysten ja yksityishenkilöiden on toimittava. Euroopan komissio määritti SEPA-maksujen oikeudellisen perustan maksupalveludirektiivin avulla. Euroopan maksuneuvosto (EPC) tukee SEPA-aluetta seuraavilla toimilla:

-   Se määrittää sähköisten SEPA-maksujen standardit käyttämällä XML-pohjaista rahoitusalan sanomavälitysjärjestelmää (ISO 20022).
-   Se luo euromaksujen käsittelysäännöt ja -ohjeistuksen.

Eurooppalaisista pankeista muodostuva EPC kehittää SEPA-maksuvälineiden kaupallista ja teknistä ympäristöä. Käytössä on kolme SEPA-maksutyyppiä:

-   Tilisiirrot
-   Suoraveloitukset
-   Kortit

## <a name="what-is-a-sepa-credit-transfer"></a>Mikä SEPA-tilisiirto on?
SEPA-tilisiirto on toisen yrityksen tai henkilön toiselle yritykselle tai henkilölle suorittama maksu. Maksujen on oltava euromääräisiä ja niissä on oltava kummankin osapuolen kansainvälinen tilinumero (IBAN) ja BIC (Bank Identifier Code) -koodi. (BIC-koodi tunnetaan myös nimellä \[SWIFT\] Society for Worldwide Interbank Financial Telecommunication) -koodi. Lisäksi osapuolien on jaettava tapahtumakustannukset. Osapuolten välisissä tilisiirroissa on käytettävä EPC:n määritysten mukaisia XML-tiedostoja, jotka vastaavat ISO 20022 -maksukäsittelystandardeja ja XML-muotoa.

## <a name="how-is-a-credit-transfer-implemented"></a>Miten tilisiirto tehdään?
SEPA-tilisiirron maksumuoto toteutetaan Euroopan maissa käyttämällä Microsoft Dynamics 365 Financen sähköistä raportointia (ER) ja maksutapatoimintoa. Muilla alueilla käytetään edelleen joitakin tilisiirron muotoja, jotka käyttävät vanhaa maksukehystä. Muiden muotojen lisäksi saatavilla on kaksitoista ISO 20022 -tilisiirron tiedostomuotoa. Nämä vientimuodot ovat SEPA ISO 20022 XML -standardin mukaisia. Niiden avulla muodostetaan ei-euromääräiset maksun siirrot maille/alueille, joissa niitä käytetään sekä euromääräiset maksut sen mukaisesti, mitä EPC:n SEPA-tilisiirtojen sääntökirjan versiossa 8.2 määritetään. Ennen tilisiirtojen käyttöönottoa omasta pankista on pyydettävä ohjelmisto, joka tarvitaan sähköisten pankkitiedostojen lataamiseen. Maksutoimeksiannot sisältävät XML-tiedostot siirretään tällä ohjelmistolla pankkiin.

## <a name="what-credit-transfer-formats-are-currently-supported"></a>Mitä tilisiirron muotoja tuetaan tällä hetkellä?
Tarkista Microsoft Dynamics Lifecycle Services (LCS) -palvelun jaetusta omaisuuskirjastosta luettelo uusimmista käytettävissä olevista tiedostoista, joiden tyyppi on **GER-konfigurointi**. Seuraavassa osassa, "Mitä asetuksia on määritettävä?", on linkki ohjeaiheeseen, jossa kerrotaan, miten luot LCS-säilön, josta voit tarkastaa käytettävissä olevat konfiguraatiotiedostot ja tuoda haluamasi tiedostot.

## <a name="what-do-i-have-to-set-up"></a>Mitä asetuksia on määritettävä?
-   Ennen tilisiirtotiedostojen luontia vähintään yksi aktiivinen tilisiirtomääritys on tuotava sähköisen raportoinnin määrityksiin. Ohjeet löydät artikkelista [Lataa sähköisen raportoinnin konfiguraatiot Lifecycle Servicesistä](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Valitse ensin **Yleinen sähköinen raportointi** -valintaruutu ja sitten ISO-tilisiirtomuoto (esim. **ISO 20022 Tilisiirto (AT)**) vientimuodon määritykseksi, kun määrität ostoreskontran maksutavan.
-   Myös yrityksen ja pankkitilin tiedot on määritettävä.
-   Tilisiirtomaksujen luomiseen tarvitaan pankkitilin numero, IBAN-koodi ja toisinaan SWIFT-koodi (BIC) tai muu tunnus. Tämän vuoksi on ne on määritettävä toimittajan pankkitilille sekä ja siirtoa pyytävän organisaation pankkitilille.
-   Jotkin lisätiedot voivat olla pakollisia, kuten arvonlisäveronumerot (ALV-numero) osapuolille, joihin tilisiirron sanomassa viitataan. Nämä tiedot on määritettävä toimittajille ja yritykselle pyydettäessä.
-   Jotkin ostoreskontran maksutavat, jotka ovat enimmäkseen ISO 20022 -pohjaisia maksutapoja, voivat vaatia lisäasetuksia **Maksumuodon koodijoukot** -kohdassa, kuten **Palvelutyyppi** = **SLEV**. Näitä koodeja lisätunnisteina maksutapahtumille maksujen käsittelyssä. Maksukoodien oletusarvot, kuten **luokan tarkoitus**, **kulun haltija**, **paikallinen väline** ja **palvelutaso**, voidaan määrittää kahdessa paikassa. Ensimmäinen paikka on **Ostoreskontran maksukirjauskansion otsikko** ja toinen on **Ostoreskontran maksutavat**. Maksun kirjauskansion rivien luonnin yhteydessä maksun maksukirjauskansion otsikkoon asetetut maksukoodin arvot siirretään kirjauskansion riville; jos asetusta ei ole määritetty, käytetään arvoja Maksutavat-kohdasta.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Mitä parametreja voi käyttää tilisiirtomaksujen luontiin?
Parametrien tarkka luettelo riippuu tilisiirron muodosta. Seuraavassa taulussa on luettelo parametreista, joilla Saksaa koskeva ISO 20022 -tilisiirtomaksun tiedosto luodaan toimittajan maksukirjauskansiossa. Käyttämällä **Suorita taustalla** -välilehden asetuksia voit muodostaa maksun erätyötilassa.

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
<li><strong>Strd</strong> – Tällä vaihtoehdolla valitaan rakenteinen muoto, kun yksi maksurivi tilitetään yhdelle laskulle. Tämä vaihtoehto ei ole käytettävissä Saksan, Ranskan tai Alankomaiden maa- ja aluekohtaisissa vientimuodoissa.</li>
<li><strong>Ustrd</strong> – Tällä vaihtoehdolla valitaan jäsentämätön muoto, kun maksu tilitetään useille laskuille. Tilitettyjen laskujen laskunumerot yhdistetään ja niitä käytetään maksusuoritustietoina. ISO 20022 -ohjeiden mukaisesti jäsentämättömien maksusuoritetietojen pituus on rajoitettu 140 merkkiin.</li>
</ul></td>
</tr>
<tr class="even">
<td>Laskujen määrä</td>
<td>Anna laskujen lukumäärä, joista <strong>Maksuehdotus</strong>-raportti tulostetaan.</td>
</tr>
<tr class="odd">
<td>Järjestysnumero</td>
<td>Anna järjestysnumero, jolla tiedosto tunnistetaan. Järjestysnumero näkyy <strong>Osallistumishuomautus</strong>-raportissa.</td>
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
International Bank Account Number (IBAN)-numeroa ja Bank Identifier Code (BIC) -koodia käytetään kaikkien tilien tunnistamiseen monessa maassa/alueella ympäri maailman. Näihin kuuluvat 34 SEPA maata/aluetta. Anna BIC **SWIFT-koodi** -kenttään ja IBAN-koodi **IBAN**-kenttään. Laskuttajan pankkitilin ja asiakkaan pankkitilin kentät sijaitsevat **Lisätunnus**-pikavälilehdessä **Pankkitilit**-sivun **Pankkitili**-välilehdessä. BIC-koodin käyttö SEPA-maksuissa ei ole enää pakollista.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Miten maksutiedosto siirretään pankkiin?
Maksuja muodostettaessa muodostetaan maksutiedosto, ja sinua pyydetään tallentamaan se selaimesta sopivaan sijaintiin. Tämä XML-tiedosto lähetetään seuraavaksi pankkiin. Tämä prosessi vaihtelee pankeittain. Lähetä tiedostot pankkiin käsiteltäviksi pankin ohjeiden mukaisesti.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
