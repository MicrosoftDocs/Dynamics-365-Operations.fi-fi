---
title: Sarjoitettujen tuotteiden parannukset myyntipisteessä (POS)
description: Tässä aiheessa on luettelo parannuksista, jotka on tehty sarjoitettuihin tuotteisiin ajan säästämiseksi ja tehokkuuden parantamiseksi.
author: ShalabhjainMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: fbd1d9c71ece77cbf4c6ecb741eb6d5e3e3455d9
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028152"
---
# <a name="point-of-sale-pos-improvements-for-serialized-products"></a>Sarjoitettujen tuotteiden parannukset myyntipisteessä (POS)

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Yleiskatsaus

Commerce Headquarters -sovelluksen asetusten perusteella tuotteita voi luokitella sarjoitetuiksi tai ei-sarjoitetuiksi. Kun tuotteet esitetään sarjoitettuna, kullekin nimikkeelle voidaan määrittää yksilöllinen luku, joka auttaa takuiden ja nimikkeiden jäljittämisessä ja omistajuuden vahvistamisessa. Vaikka sarjanumeroiden antaminen sarjoitetuille tuotteille oli mahdollista Modern/Cloud Point of Sale -sovelluksissa, toimintoon on tehty parannuksia, jotta kassanhoitajat voivat säästää aikaa ja työskennellä tehokkaammin.

## <a name="pos-improvements"></a>Myyntipistesovelluksen parannukset

- **Sarjanumeroita ei tarvita ennen uloskuittausta** – aikaisemmin, jos kassanhoitaja lisäsi sarjoitetun tuotteen tapahtumaan, tämän piti antaa sarjanumero. Tämä vaatimus oli ongelmallinen asiakashallintaskenaarioissa, jos kassanhoitajilla ja myyntiedustajilla oli mahdollisuus lisämyyntiin. Tuotteet päivitettiin usein ostoskoriin maksuvaiheeseen saakka. Järjestelmä pyysi siis kassanhoitajalta sarjanumeroa aina, kun kassanhoitaja lisäsi uuden tuotteen. Sarjanumeron valintaikkunassa on nyt **Lisää myöhemmin** -painike. Myyntiedustajat voivat siis lisätä nimikkeen tapahtumaan ja antaa sarjanumeron myöhemmin. Myyntiedustajat voivat lisätä ja vaihtaa sarjoitettuja nimikkeitä ostoskärryyn nopeasti ja syöttää sarjanumerot juuri ennen uloskuittausta. Jos millekään sarjoitetulle tuotteelle ei ole annettu sarjanumeroa, tapahtumaa tekevä kassanhoitaja saa virheilmoituksen. Ilmoitus kehottaa kassanhoitajaa syöttämään puuttuvat sarjanumerot ennen jatkamista.

    Kunkin sarjoitetun tuotteen tapahtumarivin, jolta puuttuu sarjanumero, alle tulee esiin kommentti. Kommentissa ilmaistaan, että nimikkeen sarjanumero puuttuu. Kassanhoitaja löytää siis nimikkeet, joilta sarjanumerot puuttuvat nopeasti.

    Uusi **Lisää sarjanumero** -toiminto tarjoaa myös sarjanumeron nimikkeille, joilla sellaista ei ole. Kun numero on syötetty, sitä ei voi muokata. Kassanhoitajan on mitätöitävä rivi ja lisättävä tuote uudelleen.
    
- **Asiakastilausten tekeminen ei edellytä sarjanumeroita** – asiakastilauksen voi tehdä yhdessä myymälässä ja täyttää toisessa. Asiakastilauksia tekevän kassanhoitajan ei tarvitse syöttää sarjanumeroa. Sarjanumero lisätään keräily- tai noutovaiheessa. Sarjanumero on kuitenkin annettava kaikille rivinimikkeille, joille on valittu **Nouto liikkeestä** -toimitustyyppi. Muussa tapauksessa tapahtuma ei onnistu.
- **Sarjoitettuja tuotteita ei koosteta tapahtumanäytöllä** – **Koosta tuotteet** -asetus **Toimintoprofiili**-sivun **Pääte**-kenttäryhmässä mahdollistaa saman, ei-sarjoitetun tuotteen koostamisen tapahtumanäytöllä. Kun tuotteet koostetaan, ne on helpompi nähdä tapahtumaruudukossa. Koska sarjanumerot ovat tavallisesti yksilöiviä ja myyntiedustajien ei tarvitse kirjoittaa sarjanumeroita ennen uloskuittausta, **Koosta tuotteet** -asetus ei koske sarjoitettuja tuotteita. Sarjoitettuja tuotteita ei yhdistetä tapahtumanäytöllä, jos **Koosta tuotteet** -asetus on valittuna.
- **Mahdollisuus etsiä kirjauskansioita sarjanumeron mukaan** – Kirjauskansioissa voi nyt tehdä hakuja myös sarjanumeroiden mukaan. Se tehdään avaamalla kirjauskansiotoiminto ja painamalla sovelluspalkissa Tarkennettu haku -painiketta. Lisää suodatin -painikkeella voi lisätä suodattimen myös sarjanumerohakuun.


[!INCLUDE[footer-include](../includes/footer-banner.md)]