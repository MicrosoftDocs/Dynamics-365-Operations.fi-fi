---
title: ER Kohteiden määrittäminen
description: Tässä menettelyssä esitellään, miten sähköisen raportoinnin (ER) tuloskomponenteille, kuten kansioille tai tiedostoille, voi käyttää eri kohteita.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0073033454c7d3054496fe4c38cdb3cff71d8755
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681874"
---
# <a name="er-configure-destinations"></a>ER Kohteiden määrittäminen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä esitellään, miten sähköisen raportoinnin (ER) tuloskomponenteille, kuten kansioille tai tiedostoille, voi käyttää eri kohteita. Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF. Saksan on yrityksen ensisijaisen osoitteen maa/alue, mutta tässä menettelyssä voit käyttää mitä tahansa yritystä. 

Esimerkissä käytetty muoto on ISO20022 Tilisiirto, mutta voit käyttää mitä tahansa aiemmin tuomaasi muotoa. Huomaa, että tämä menettely on esimerkki yhden tiedoston ja yhden kohteen määrityksestä. Lisätietoja sähköisen raportoinnin kohdehallinnasta löydät Dynamics 365 Finance -sovelluksen ohjeesta.

1. Valitse Organisaation hallinto > Sähköinen raportointi > Sähköisen raportoinnin kohde.
2. Luo muodolle uusi kohdejoukko painamalla Uusi.
3. Valitse Viite-kenttään muoto, jolle haluat konfiguroida kohteet.
    * Jos valittavana ei ole arvoa, et ole tuonut yhtäkään sähköisen raportoinnin muotokonfiguraatiota. Muotokonfiguraatio on tuotava ennen kohteiden määrittämistä.  
4. Luo tiedostokohde napsauttamalla Uusi.
    * Huomaa, että voit luoda yhden tiedostokohteen kullekin samanmuotoiselle tuloskomponentille, kuten kansiolle tai tiedostolle. Voit ottaa käyttöön tai poistaa käytöstä kohteita erikseen asetuksissa.  
5. Kirjoita Nimi-kenttään tuloskomponentin kutsumanimi.
    * On suositeltavaa käyttää kuvaavia nimiä, kuten "Maksutiedosto" tai "Valvontaraportti". Nämä nimet esitetään käyttäjille, kun konfiguraatio ajetaan kohteen asetusten rinnalla.  
6. Valitse Tiedostonimi-kohdassa muotokohtainen tiedosto tai kansio.
7. Valitse Asetukset.
8. Valitse Käytössä-kentässä Kyllä.
    * Kunkin välilehden Käytössä-valintaruutu ottaa tai poistaa kunkin kohteen käytöstä erikseen. Tässä esimerkissä otetaan käyttöön tulostiedoston lähettäminen postin vastaanottajalle, kun tiedosto luodaan.  
9. Määritä sähköpostin vastaanottajat napsauttamalla Muokkaa-painiketta.
10. ValitseLisää.
11. Valitse Tulostuksenhallinnan sähköposti.
12. Valitse Sähköpostilähde-kentässä vaihtoehto.
    * Voit valita sähköpostille eri lähdetyyppejä, kuten asiakas- tai toimittajatyypin Tämä määrittää Sähköpostin lähdetili -kaavan palauttaman argumenttityypin. Sähköpostin lähdetili -kaava, joka kuvaillaan tulevassa vaiheessa, on paikka, jossa sähköpostilähteen sidonta suoritetaan. Valitse Toimittaja, jos kaava palauttaa toimittajatilin. Käytä Toimittaja-arvoa, jos käytät ISO 20022 Tilisiirto -esimerkkikonfiguraatiota.  
13. Valitse Sido sähköpostilähde.
14. Kirjoita Kaava-kohtaan, asiakirjakohtainen viittaus aiemmin valitsemaasi osapuolen tyyppiin.
    * Kirjoittamisen asemesta voit etsiä tietolähdesolmun, joka vastaa osapuolen tiliä ja napsauttaa Lisää tietolähde -painiketta päivittääksesi kaavan. Esimerkki: Jos käytössä on ISO 20022 Tilisiirto -konfiguraatio, toimittajatiliä vastaava solmu on $PaymentsForCoveringLetter'.Creditor.Identification.SourceID. Muussa tapauksessa voit kirjoittaa minkä tahansa merkkijonoarvon, kuten "DE-001", tallentaaksesi kaavan.  
15. Valitse Tallenna.
16. Sulje sivu.
17. Määritä osapuolen yhteystiedot napsauttamalla Muokkaa-painiketta.
18. Valitse Ensisijainen yhteyshenkilö -kentässä Kyllä.
    * Erilaisia vaihtoehtoja voi käyttää ilmaisemaan, mitä yhteyshenkilötyyppiä osapuolen tulisi olla tämän kohteen sähköpostiosoitteessa. Tässä esimerkissä käytetään ensisijaista yhteyshenkilöä.  
19. Valitse OK.
20. Valitse OK.
21. Kirjoita arvo Aihe-kenttään.
22. Valitse OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]