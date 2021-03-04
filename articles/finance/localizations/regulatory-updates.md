---
title: Pakolliset päivitykset
description: Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 Financelle suunnitelluista ja julkaistuista pakollisista päivityksistä.
author: ShylaThompson
manager: AnnBe
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 46e9b3c3d47207715d0eee689913073d363f3af3
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517497"
---
# <a name="regulatory-updates"></a>Pakolliset päivitykset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on luettelo pakollisista päivityksistä, jotka on suunniteltu ja julkaistu Dynamics 365 Financen tukemissa lokalisaatioissa. Toimitusajankohdat voivat muuttua ja ennakoidut toiminnot voivat olla erilaisia tai niitä ei ehkä julkaista. Lisätietoja on kohdassa [Microsoftin käytäntö](https://go.microsoft.com/fwlink/p/?linkid=2007332). 

Pakolliset päivitykset ovat toimintoja, jotka tukevat uudet tai muuttuneet maakohtaiset lainsäädännöt. Lisätietoja muista suunnitelluista tai julkaistuista maakohtaisista ominaisuuksista on [Dynamics 365:n ja Power Platformin julkaisusuunnitelmissa](https://docs.microsoft.com/business-applications-release-notes/index).

Microsoft pyrkii toteuttamaan uudet lainsäädännölliset vaatimukset mahdollisimman aikaisin. Toimituspäivämäärä riippuu lain ilmoituspäivästä, vaatimuksien saatavuudesta paikallisilta viranomaisilta, oikeellisuustarkistustyöklaujen saatavuudeta sekä muutoksen koosta ja monimutkaisuudesta.

On tarkoitus toimittaa säännöstenmukaisuuden päivitykset yhden version palvelupäivityksissä, jotka julkaistaa siten, että asiakkaat olisivat valmiina voimaantulopäivänä (tapahtumapohjaisille säännöspäivityksille) tai ensimmäisenä pakollisena raportoinnin määräaikana (raportointiin liittyville säännöspäivityksille). Asiakkaat ja kumppanit voivat esikatsella säännöspäivityksiä Preview Early Adoption Program (PEAP) -ohjelmassa.

Siltä varalta, että ilmoituspäivämäärä on myöhässä, tai vaatimukset tai oikeellisuustarkistustyökalut saadaan myöhässä tai muutos on poikkeuksellisen suuri tai monimutkainen, säännöspäivitystä ei ehkä voida julkaista kuukausittaisen päivityksen yleisen saatavuuden päivämäärään mennessä. Tällöin pakollinen päivitys toimitetaan hotfix-korjauksina asiaankuuluville kuukausittaisille päivityksille.

Pakolliset päivitykset, jotka julkaistaan osana kuukausittaista päivitystä, on merkitty vain julkaisuversiolla. Pakolliset päivitykset, jotka toimitetaan joko hotfix-korjauksina tai osana julkaisun esikatselua, voidaan tunnistaa lyhenteiden HF ja PEAP avulla. 

Seuraavassa taulukossa on uusimpien säännöspäivitysten suunnitelmat.   

|Maa tai alue|Vapautuspäivä|Julkaisuversio|Pakollinen päivitys|
|--------------------|---------------|-------|-------|
|      Itävalta         |   2020. syyskuuta      | 10.0.15      |   ALV-ilmoituksen muoto U30 on päivitetty vuoden 2020 raportointia varten   |
|      Bahrain         |   2020. kesäkuuta      | 10.0.13      |   Laskun kirjoittamisen takaraja (GCC)   |
|      Bahrain         |   2020. syyskuuta      | 10.0.13      |   Bahrainin projektilasku   |
|      Bahrain         |   2020. kesäkuuta      | 10.0.13      |   Bahrainin ALV-ilmoitus - ota käyttöön tapahtuman kuvaus   |   
|      Brasilia         |   Elokuu 2020      | 10.0.14, 10.0.13      |   ADRCST-ilmoituksen PR   |
|      Brasilia         |   Toukokuun 2020.      | 10.0.13      |   SPED ECF -asettelu 6   |
|      Brasilia         |   Heinäkuu 2020      | 10.0.13      |   SPED-verotus – tietue C176 – RS-tila   |
|      Brasilia         |   2020. lokakuuta      | 10.0.16, 10.0.15HF, 10.0.14HF, 10.0.13HF      |   NF-e NT2019.001 v1.51 - Tarkistussääntöjen käyttöönotto etukoodin yhteydessä Distrito Federalin mukaan   |
|      Brasilia         |   2020. lokakuuta      | 10.0.16      |   SPED-verotus - asettelu 015   |
|      Brasilia         |   marraskuu 2020      | 10.0.15HF      |   SPED-verotus, ICMS/IPI-tietue, C176-päivitys RS-tilalle   |
|      Brasilia         |   2020. lokakuuta      | 10.0.16      |   DRCST-ilmoituksen SC - SEF 262/2020   |
|      Brasilia         |   2020. lokakuuta      | 10.0.16      |   SPED-verotus, ICMS/IPI-tietue, C176   |
|      Tšekin tasavalta      |   Heinäkuu 2020      | 10.0.13      |   ALV-valvontailmoituksen muutokset XML-rakenteessa (laskulistaus)   |
|      Tšekin tasavalta         |   Heinäkuu 2020      | 10.0.13      |   ALV-ilmoitus XML-muodossa, ALV-ilmoituksen esikatselu Excelissä ja ALV-valvontailmoituksen XML-muodot veroilmoitusmalliin perustuvana   |
|      Eurooppa        |   Elokuu 2020       | 10.0.14      |   Siirrä kumppanin ALV-tunnus Intrastatiin  |
|      Suomi         |   Heinäkuu 2020       | 10.0.13      |   Suomen sähköisten laskujen tuki  |
|      Intia         |   Heinäkuu 2020      | 10.0.13      |   Myytyjen tuotteiden TCS osaa kohti 206C (1H) - raja kertyneiden tapahtumien PAN-kohtainen raja.  |
|      Intia         |   Elokuu 2020, kesäkuu 2020      | 10.0.13      |   Hyvitys-/veloituslasku vientilaskulle  |
|      Intia         |   Elokuu 2020      | 10.0.13      |   Sähköinen lasku, GST-vero  |
|      Intia         |   Heinäkuu 2020      | 10.0.13      |   Uusi GSTR (ANX-1 ja ANX-2), offline-työkalu (beetaversio)  |
|      Intia         |   2020. lokakuuta      | 10.0.14HF, 10.0.13HF      |   Intian varaston siirtotilauksen GST:n sähköinen lasku|
|      Intia         |   2020. lokakuuta      | 10.0.14HF, 10.0.13HF      |   Intian GST:n sähköinen lasku ja useita GSTIN-rekisteröintejä|
|      Intia         |   2020. syyskuuta      | 10.0.13HF      |   Ennakonpidätyksen määrä 3/5 desimaalina|
|      Intia         |   2020. syyskuuta      | 10.0.14HF      |   Numerosarjaryhmä GSTNSG, tapahtumatyyppi GST-lasku määritetään verotietojen 0073 GST-viitenumerojärjestysryhmälle|
|      Italia         |   Heinäkuu 2020      | 10.0.13      |   Muutokset Italian sähköisten laskujen, FatturaPA, muodossa |
|      Malesia         |   Heinäkuu 2020      | 10.0.13      |   SST-raportti |
|      Meksiko         |   2020. syyskuuta      | 10.0.13HF      |   CFDI URL -rakenne, joka perustuu Anexo 20 -asiakirjaan |
|      Alankomaat         |   2020. lokakuuta      | 10.0.16     |   Intrastat-muoto päivitetään alkaen 2021 |
|      Norja         |   Elokuu 2020      | 10.0.14     |   SAF-T - Tosite-arvon mukasen ryhmittelytason tapahtumat on raportoitava Tapahtuma-elementtitasolla Kirjauskansio-tason sijaan |
|      Puola          |   2020. syyskuuta     | 10.0.14     |   Puola: JPK-V7M (VDEK), Excel-muoto - korvaa SSRS-raportin  |
|      Puola          |   Heinäkuu 2020     | 10.0.15, 10.0.14HF, 10.0.13     |   Vapaaehtoisen jaetun maksun parannukset |
|      Puola          |   2020. lokakuuta     | 10.0.13HF     |   Pakollisen jaetun maksun parannukset |
|      Puola          |   marraskuu 2020     | 10.0.16, 10.0.15, 10.0.14, 10.0.13     |   JPK-V7M (VDEK) - Myyntiasiakirjan tyyppi FP ja RO vähittäismyyntitapahtumia varten |
|      Puola          |   2020. syyskuuta     | 10.0.15     |   Puola: JPK-V7M (VDEK) - poista lukitus mahdollisuudesta suorittaa raportin luominen osien mukaan |
|      Puola          |   2020. lokakuuta     | 10.0.16     |   JPK-V7M (VDEK) -raportti - Vapaaehtoinen jaettu maksu -parametrin käyttö |
|      Venäjä          |   Elokuu 2020     | 10.0.14    |   Kirjanpidon raportoinnin muoto muuttuu vuodesta 2020 alkaen  |
|      Venäjä          |   Heinäkuu 2020     | 10.0.13    |   Poistojen laskenta hankintakustannuksen perusteella ja merkittävät korjaukset käytettäessä poistobonusta verokirjanpidossa  |
|      Venäjä          |   marraskuu 2020     | 10.0.16    |   ALV-ilmoituksen muoto päivitetään versioon 5.07 alkaen vuoden 2020 neljännen neljännesvuoden raportoinnista|



## <a name="additional-resources"></a>Lisäresurssit
- Etsi kaikki suunnitellut ja julkaistut pakolliset päivitykset [Lifecycle Service – ongelmahaussa](https://lcs.dynamics.com/Logon/Index) (pakollinen kirjautuminen).
- Lisätietoja tuetuista lokalisaatiosta on [kansainvälisessä tuotesaatavuusoppaassa](https://aka.ms/dynamics_365_international_availability_deck).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]