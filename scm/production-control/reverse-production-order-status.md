---
title: Muuta tuotantotilauksen tila
description: "Tässä aiheessa on kuvattu tuotantotilauksen tilan palauttamista."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5578732c1738d6a04b5028d677f0ac4bb3c71e53
ms.lasthandoff: 03/31/2017


---

# <a name="reverse-the-production-order-status"></a>Muuta tuotantotilauksen tila

Tässä aiheessa on kuvattu tuotantotilauksen tilan palauttamista. 

Tuotantotilauksen tilan palauttaminen siirtää itse tilauksen ja kaikki reititykseen liittyvät operaatiot takaisin tuotannon elinkaaren edelliseen vaiheeseen. Esimerkki: Tuotantotilauksen tila on **Ajoitettu** ja palautat tilaksi **Luotu**. Tällöin järjestelmän on ensin vaihdettava tilaksi **Arvioitu** eli tilaan, joka on juuri ennen **Ajoitettu**-tilaa. Tämän jälkeen tila voidaan vaihtaa haluamaasi **Luotu**-tilaan. **Huomautus:** Jos tilauksesi on edennyt **Ilmoita valmiiksi** -tilaan, voit yhä palauttaa sen aiempaan tilaan. Sinun on kuitenkin suoritettava arviointi ja työvaiheiden ajoitus, töiden ajoitus tai molemmat ajoitustyypit uudelleen, jotta tilauksen tiedot päivittyvät. Tämä vaihe on pakollinen, sillä myös jäljellä olevat nimikkeen kulutuksen ja operatiivisten resurssien kulutuksen varaukset on palautettava. Tämän artikkelin loppuosassa selostetaan, mitä tapahtuu, kun tuotantotilauksen tila palautetaan seuraavilla tavoilla:

-   **Arvioitu**-tilasta **Luotu**-tilaan
-   **Ajoitettu**-tilasta **Arvioitu**-tilaan
-   **Vapautettu**-tilasta **Ajoitettu**-tilaan
-   **Aloitettu**-tilasta **Vapautettu**-tilaan

## <a name="from-estimated-to-created"></a>Arvioitu-tilasta Luotu-tilaan
Kun tuotantotilaus palautetaan **Arvioitu**-tilasta **Luotu**-tilaan, järjestelmä poistaa nimikkeen kulutuksen, joka on laskettu nimikkeille tuoterakenteessa. Tuotantorivin varastotapahtumat poistetaan, ja tuotantotilauksen tuoterakennerivien **Jäljellä oleva tila** -kentän asetukseksi palautetaan **Päättynyt**. Kun **Johdetut ostot**- ja **Johdettu tuotanto** -vaihtoehdot valitaan, kaikki pohjana olevat osto- tai tuotantotilaukset poistetaan. Jos olet arvioinut tuotantotilauksen kustannuksia tai varannut nimikkeitä manuaalisesti niin, että niitä voi käyttää tuotannossa, nämä tapahtumat poistetaan.

## <a name="from-scheduled-to-estimated"></a>Ajoitettu-tilasta Arvioitu-tilaan
Kun tuotantotilaus palautetaan **Ajoitettu**-tilasta **Arvioitu**-tilaan, järjestelmä poistaa ajoitetun aloitus- ja päättymispäivän sekä -ajan. Ajoituksen yhteydessä tehdyt kapasiteettivaraukset ja työn ajoituksen yhteydessä luodut työt poistetaan. Kaikki työvaiheiden ja töiden ajoituksesta **Tuotantotilauksen tiedot** -sivulle kirjatut tiedot palautetaan.

## <a name="from-released-to-scheduled"></a>Vapautettu-tilasta Ajoitettu-tilaan
Kun tuotantotilaus palautetaan **Vapautettu**-tilasta **Ajoitettu**-tilaan, vain tilakentän arvo muuttuu.

## <a name="from-started-to-released"></a>Aloitettu-tilasta Vapautettu-tilaan
Kun tuotantotilaus palautetaan **Aloitettu**-tilasta **Vapautettu**-tilaan, kaikki valmiiksi ilmoitetut nimikkeet palautetaan. Jos materiaalia on kerätty tai tuotantoon liittyy saapuvia tai lähteviä toimituksia, myös nämä asetukset palautetaan. Tuotantotilauksen tuoterakennerivien **Jäljellä oleva tila** -kentän arvo muuttuu **Päättynyt**-tilasta **Materiaalikulutus**-tilaan. Jos aika on rekisteröity tai määrät on raportoitu valmiiksi tuotantoreitityksen työvaiheille, nämä asetukset palautetaan. **Jäljellä oleva tila** -kentän arvo muuttuu tuotantoreitityksessä **Päättynyt**-tilasta **Reitityksen kulutus** -tilaan. Kaikkien käsittelyssä oleviksi kirjattujen nimikkeiden tai keskeneräisten töiden asetukset palautetaan. **Tuotantotilauksen tiedot** -sivulla olevat kentät, joissa näkyy aloitettu tai valmiiksi ilmoitettu määrä, palautetaan. Myös kyseisten tapahtumien päivämäärät palautetaan.


