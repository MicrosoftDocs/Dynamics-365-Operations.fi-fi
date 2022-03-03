---
title: Pakolliset päivitykset
description: Tässä ohjeaiheessa on luettelo Microsoft Dynamics 365 Financelle suunnitelluista ja julkaistuista pakollisista päivityksistä.
author: VStamberg
ms.date: 01/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: vastrup
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 663b7d3162af6d385bc9c445b1e98cf5f74a1471
ms.sourcegitcommit: f2a78e0d7d461ca843ac2f9abff7690275db9196
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8105561"
---
# <a name="regulatory-updates"></a>Pakolliset päivitykset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on luettelo pakollisista päivityksistä, jotka on suunniteltu ja julkaistu Dynamics 365 Financen tukemissa lokalisaatioissa. Toimitusajankohdat voivat muuttua ja ennakoidut toiminnot voivat olla erilaisia tai niitä ei ehkä julkaista. Lisätietoja on kohdassa [Microsoftin käytäntö](https://go.microsoft.com/fwlink/p/?linkid=2007332). 

Pakolliset päivitykset ovat toimintoja, jotka tukevat uudet tai muuttuneet maakohtaiset lainsäädännöt. Lisätietoja muista suunnitelluista tai julkaistuista maakohtaisista ominaisuuksista on [Dynamics 365:n ja Power Platformin julkaisusuunnitelmissa](/business-applications-release-notes/index).

Microsoft pyrkii toteuttamaan uudet lainsäädännölliset vaatimukset mahdollisimman aikaisin. Toimituspäivämäärä riippuu lain ilmoituspäivästä, vaatimuksien saatavuudesta paikallisilta viranomaisilta, oikeellisuustarkistustyöklaujen saatavuudeta sekä muutoksen koosta ja monimutkaisuudesta.

On tarkoitus toimittaa säännöstenmukaisuuden päivitykset yhden version palvelupäivityksissä, jotka julkaistaa siten, että asiakkaat olisivat valmiina voimaantulopäivänä (tapahtumapohjaisille säännöspäivityksille) tai ensimmäisenä pakollisena raportoinnin määräaikana (raportointiin liittyville säännöspäivityksille). Asiakkaat ja kumppanit voivat esikatsella säännöspäivityksiä Preview Early Adoption Program (PEAP) -ohjelmassa.

Siltä varalta, että ilmoituspäivämäärä on myöhässä, tai vaatimukset tai oikeellisuustarkistustyökalut saadaan myöhässä tai muutos on poikkeuksellisen suuri tai monimutkainen, säännöspäivitystä ei ehkä voida julkaista kuukausittaisen päivityksen yleisen saatavuuden päivämäärään mennessä. Tällöin pakollinen päivitys toimitetaan hotfix-korjauksina asiaankuuluville kuukausittaisille päivityksille.

Pakolliset päivitykset, jotka julkaistaan osana kuukausittaista päivitystä, on merkitty vain julkaisuversiolla. Pakolliset päivitykset, jotka toimitetaan joko hotfix-korjauksina tai osana julkaisun esikatselua, voidaan tunnistaa lyhenteiden HF ja PEAP avulla. 

Seuraavassa taulukossa on uusimpien säännöspäivitysten suunnitelmat.   

|Maa tai alue|Vapautuspäivä|Julkaisuversio|Pakollinen päivitys|
|--------------------|---------------|-------|-------| 
|      Itävalta         |   Elokuu 2021      | 10.0.22      |   ALV-ilmoitus XML-muodossa ja esikatselu Excelissä   |
|      Itävalta         |   Syyskuu 2021      | 10.0.22HF      |   Intrastat-muoto päivitetään vuodesta 2022 alkaen – alkuperämaasta ja kumppanin ALV-tunnuksista tulee pakollisia lähetyksissä   |
|      Belgia        |   2021. lokakuuta      | 10.0.22HF     |   Intrastat-tapahtumakoodit muuttuvat kaksinumeroisiksi vuodesta 2022 alkaen  |
|      Brasilia         |   Elokuu 2021      | 10.0.22      |   NF-e NT2020.006 – Digitaalisen alustan välittäjän tunnus (asettelu- ja vahvistussääntöjen päivitykset)   |
|      Brasilia         |   2021. joulukuuta         | 10.0.22, 10.0.23, 10.0.24         |    SPED-verotuksen asettelu 2022  |
|      Tšekin tasavalta         |   2021. lokakuuta         | 10.0.23HF         |     Intrastat-muoto päivitetään vuodesta 2022 alkaen – alkuperämaasta ja kumppanin ALV-tunnuksista tulee pakollisia lähetyksissä  |
|      Tanska         |   2021. joulukuuta         | 10.0.22HF         |    Intrastat-muoto päivitetään alkaen 2022  |
|      Viro         |   2021. joulukuuta      | 10.0.22HF      |   Intrastat-muoto päivitetään vuodesta 2022 alkaen – alkuperämaasta ja kumppanin ALV-tunnuksista tulee pakollisia lähetyksissä  |
|      Suomi         |   marraskuu 2021         | 10.0.22HF         |    Intrastat-muoto päivitetään alkaen vuodesta 2022.  |
|      Saksa        |   Elokuu 2021       | 10.0.22HF      |   Intrastat-muoto INSTAT XML päivitetään vuodesta 2022 alkaen. Intrastat-muoto TXT ei ole enää käytettävissä 1.7.2021 alkaen  |
|      Saksa        |   2021. lokakuuta       | 10.0.23      |   ALV-ilmoitus XML-muodossa ja esikatselu Excelissä (uusi rakenne, jossa verokoodivaluutassa olevat summat voidaan suorittaa valmista käänteisen verovelvollisuuden toimintoa käyttäen muissa kuin DE:n yrityksissä, ja usean yrityksen verotapahtumat voidaan kerätä yhteen)  |
|      Italia         |   marraskuu 2021         | 10.0.22HF, 10.0.23HF, 10.0.24         |    Sähköinen laskutus rajat ylittäviä tapahtumia varten  |
|      Meksiko         |   marraskuu 2021      | 10.0.22      |   Carta de Porte -täydennys CFDI-asiakirjoissa   |
|      Meksiko         |   2021. joulukuuta      | 10.0.24      |   Carta de Porte -täydennyksen versio 2.0  |
|      Alankomaat        |   2021. lokakuuta      | 10.0.22HF      |   Kaksinumeroiset tapahtumakoodit Intrastat-tiedostomuodossa vuodesta 2022 alkaen  |
|      Uusi-Seelanti         |   Elokuu 2021      | 10.0.22    |   GST-ilmoituslomake GST101A  |
|      Norja        |   marraskuu 2021      | 10.0.24      |   ALV-ilmoitusmuoto vuodelle 2022 ja suora lähetys – Dynamics 365 Finance |
|      Oman         |   Elokuu 2021      | 10.0.22      |   ALV-ilmoitus – versio 1 |
|      Puola          |   2021. lokakuuta     | 10.0.23, 10.0.24     |   JPK_V7M – uusi rakenneversio tammikuusta 2022 alkaen |
|      Puola          |   marraskuu 2021     | 10.0.24HF     |   Vuosiraportti kaupallisten tapahtumien maksupäivistä |
|      Puola          |   2021. lokakuuta     | 10.0.24     |   EU-myyntilistan sähköinen muoto (VAT-UE) |
|      Venäjä          |   2021. lokakuuta     | 10.0.22HF, 10.0.23, 10.0.24    |   Muutoksia myynteihin, ostokirjapitoon ja laskunkirjauskansioihin|
|      Venäjä          |   2021. lokakuuta     | 10.0.24HF    |   Muutoksia liitteitä sisältävien ALV-ilmoitusten muotoihin|
|      Venäjä          |   marraskuu 2021     | 10.0.24    |   Liittovaltion kirjanpidon standardit 6/2020 (käyttöomaisuus)|
|      Saudi-Arabia          |   marraskuu 2021     | 10.0.22HF, 10.0.23    |   Sähköisten laskujen luominen Saudi-Arabiassa – vaihe 1|
|      Saudi-Arabia          |   marraskuu 2021     | 10.0.22HF, 10.0.23HF, 10.0.24    |   Retail – sähköinen laskutus Saudi-Arabiassa – vaihe 1|
|      Espanja          |   2021. lokakuuta     | 10.0.23    |    ALV-ilmoituksen malli 303 txt-muodossa ja esikatselu Excelissä|
|      Espanja          |   Syyskuu 2021     | 10.0.22    |    Intrastat-muoto päivitetään vuoden 2022 ilmoituksia varten – alkuperämaasta ja kumppanin ALV-tunnuksista tulee pakollisia lähetyksissä|
|      Ruotsi          |   2021. lokakuuta     | 10.0.22HF    |    Intrastat-muoto päivitetään vuodesta 2022 alkaen – alkuperämaasta ja kumppanin ALV-tunnuksista tulee pakollisia lähetyksissä. Käyttöön tulevat kaksinumeroiset tapahtumakoodit.|
|      Yhdistynyt kuningaskunta          |   Elokuu 2021     | 10.0.22    |    UK – MTD-petostentorjunta 2021)|



## <a name="additional-resources"></a>Lisäresurssit
- Lisätietoja kaikista suunnitelluista ja vapautettavasta maakohtaisista säännösten päivityksistä on kohdassa [Maakohtaisten säännösten päivitysten etsiminen](search-for-regulatory-updates.md). (Kirjautuminen on pakollista.)
- Lisätietoja tuetuista lokalisaatiosta on [kansainvälisessä tuotesaatavuusoppaassa](https://aka.ms/dynamics_365_international_availability_deck).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
