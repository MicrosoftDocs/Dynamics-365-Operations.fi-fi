---
title: Siirtymishaku
description: "Tässä artikkelissa kerrotaan, miten hakutoiminto käyttää sivuja Microsoft Dynamics-365 operaatioille."
author: aneesmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 87fed576f8cf358520d94f5cd5b326ff9801913a
ms.lasthandoff: 03/31/2017


---

# <a name="navigation-search"></a>Siirtymishaku

Tässä artikkelissa kerrotaan, miten hakutoiminto käyttää sivuja Microsoft Dynamics-365 operaatioille.

Työvaiheiden Dynamics 365 tarjoaa monenlaisia teollisuuden ja verticals toimintoja. Sovellus sisältää useita sivuja, joiden avulla voit suorittaa erilaisia tehtäviä ja alueiden. Voit nopeasti etsiä sivuja, sinun on suoritettava tehtävät, voit käyttää hakutoimintoa siirtyminen. Kun haluat käyttää tätä toimintoa, valitse **hakukuvake**, jolloin **hakukenttä** tukee näkyviin. Tämän jälkeen voit kirjoittaa hakukenttään yhden sanan tai useita sanoja. Järjestelmä hakee heti syöttämiäsi sanoja vastaavat sivut sovelluksesta. Jos syötät esimerkiksi sanat toimittajan lasku, järjestelmä näyttää sanoja vastaavat tulokset. **Huomautus:** **Hakukentän** avulla voit etsiä sivut ja siirtyä niille. Sen avulla ei voi etsiä tiettyjä tietoja tai toimintoja. 

[![Etsi-ruutuun](./media/search-box.png)](./media/search-box.png) siirtyminen hakutoiminto toimii myös erinomainen tapa voit siirtyä nopeasti tiettyyn sivuun. Esimerkiksi, jos olet Ostoreskontra virkailija joka usein käyttää **maksukirjauskansion** sivun, voit kirjoittaa hakuruutuun "maksukirjauskansion". Koska syöte on täsmälleen sivun otsikkoa, sivulla näkyy hakutulosten yläpuolella ja voit nopeasti siirtyä siihen. 

[![haku-for--maksukirjauskansio](./media/searching-for-payment-journal.png)](./media/searching-for-payment-journal.png) 

Hakutulosten luettelossa näkyy sivun otsikko sekä siirtyminen polku. Näin sivun sijainti sovelluksessa saadaan selville. Toiminnon avulla pystytään myös määrittämään kahden tai useamman tulosluettelossa olevan sivun erot. Kun sivua haetaan, syötettä ja sivun otsikkoa sekä sivun siirtymispolkua verrataan toisiinsa. Esimerkiksi, jos kirjoitat "saatava" ** ** hakuruutuun näet tulokset sivut käytettävissä olevat saamiset alue--vaikka sivujen otsikot eivät sisällä sanaa "saatava". 

[![search-for--word-saatavat](./media/search-for-the-word-receivable.png)](./media/search-for-the-word-receivable.png) 

Hallinnan ja tietoturvan suhteen siirtyminen etsiä toimintoja vain pinnat:

-   sivut, jotka ovat käytössä nykyisessä konfiguraatiossa (konfigurointiavainten kautta)
-   sivut, joiden käyttöoikeus käyttäjällä on käyttäjäroolin perusteella.

Hakutulosluettelo sisältää 10 kohdetta. Jos tuloksissa ei ole hakemaasi sivua, yritä tarkentaa tai päivittää syötettä. Siirtymishakutoimintoa on helppo kehittää, sillä valikon vaihtoehtojen käyttöönoton ja niiden hakutuloksissa näkymisen välillä ei käytännössä ole viivettä. Valikon vaihtoehdot ovat automaattisesti haettavissa, jos ne on linkitetty siirtymisruudusta tai koontinäytöstä. Siirtymishakutoiminto sisältää myös käyttäjien toivoman tehokäyttäjille tarkoitetun toiminnon, joka on mahdollisuus siirtyä sivulle nopeasti teknisen lomakkeen nimen avulla. Monet käyttäjät tuntevat järjestelmän ja käsittelemiensä lomakkeiden tarkat nimet hyvin. Jos olet tällainen käyttäjä, voit syöttää hakukenttään **lomake:** ja tämän jälkeen etsittävän lomakkeen nimen. Jos syötät esimerkiksi **lomake: vendinvoice**, hakutuloksissa näkyvät kaikki sivut, joiden lomakkeen nimi alkaa sanalla **vendinvoice**. 

[![haku-varten-lomakkeen-vendinvoice](./media/search-for-form-vendinvoice.png)](./media/search-for-form-vendinvoice.png)


