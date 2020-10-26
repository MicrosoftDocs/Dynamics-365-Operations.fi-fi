---
title: Arvonlisäveron kirjanpidon kirjausryhmien määrittäminen
description: Arvonlisävero lasketaan ja kirjataan kirjanpidon kirjausryhmien päätileille.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1481b714d089994c1f00189cdaba3ca328f00577
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983104"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Arvonlisäveron kirjanpidon kirjausryhmien määrittäminen

[!include [banner](../../includes/banner.md)]

Arvonlisävero lasketaan ja kirjataan kirjanpidon kirjausryhmien päätileille. Kirjanpidon kirjausryhmät liitetään kuhunkin arvonlisäverokoodiin. Voit määrittää kullekin arvonlisäverokoodille kirjanpidon kirjausryhmät käyttämällä kaikissa arvonlisäverokoodeissa yhtä kirjanpidon kirjausryhmää tai liittämällä arvonlisäverokoodeille useita kirjanpidon kirjausryhmiä. Tässä tallenteessa käytetään esittely-yritystä DEMF. 

1. Siirry kohtaan **siirtymisruutu > Moduulit > Vero > Asetukset > Arvonlisävero > Kirjanpidon kirjausryhmät**.
2. Valitse **Uusi**.
3. Kirjoita arvo **Kirjanpidon kirjausryhmä** -kenttään.
4. Kirjoita **Kuvaus**-kenttään arvo.
5. Valitse **Maksettava arvonlisävero** -kentässä päätili lähtevälle arvonlisäverolle, joka maksetaan veroviranomaiselle. Arvonlisäverot kerätään veroviranomaisen puolesta, kun verollisia tavaroita ja palveluja myydään.  
6. Valitse **Saatava arvonlisävero** -kentässä päätili saapuvalle arvonlisäverolle, joka vastaanotetaan veroviranomaiselta. Toimittajat keräävät verot veroviranomaisen puolesta, kun verollisia tavaroita ja palveluja ostetaan. Tämä kenttä ei ole käytettävissä, jos Käytä arvonlisäverotuksen sääntöjä -vaihtoehto on valittu **Kirjanpitoparametrit**-sivulla. Sen sijaan toimittajille maksettavat arvonlisäverot hyvitetään samalta tililtä kuin ostot.   
7. Valitse **Käyttöverokulu**-kentässä päätili niille vähennettäville käyttöveroille, joita veroviranomainen ei peri tai joita toimittajat eivät raportoi veroviranomaiselle osana EU:n käännettyä GOT/HS-veroa. Tapahtumassa käytettävän **arvonlisäveroryhmän** **arvonlisäverokoodin** **Käyttövero**-vaihtoehto on valittava. Tämä kenttä ei ole käytettävissä, jos **Käytä arvonlisäverotuksen sääntöjä** -vaihtoehto on valittu **Kirjanpitoparametrit**-sivulla.   
8. Valitse **Maksettava käyttövero** -kentässä päätili veroviranomaiselle maksettavien saapuvien käyttöverojen kirjaamista varten. **Arvonlisäveroryhmän** **arvonlisäverokoodin** **Käyttövero**-vaihtoehto on valittava, kun **käyttövero** kirjataan. Jos **Kirjanpidon parametrit** -sivun **Käytä arvonlisäverotuksen sääntöjä** -vaihtoehto on valittu, vastakirjaus kirjataan tapahtuman kulutilille.   
9. Valitse **Tilitystili**-kentässä päätili, jolle **Maksettava käyttövero**- ja **Saatava arvonlisävero** -kentässä määritettyjen kirjanpitotilien nettosaldo kirjataan. Saldo luodaan, kun arvonlisäveron tilitys ja työn kirjaaminen suoritetaan.  Jos tilityskauden veroviranomainen on liitetty toimittajan tiliin, saldo kirjataan sen sijaan toimittajan tiliin.
10. Valitse **Toimittajan käteisalennus** -kentässä päätili, jonne tähän kirjanpidon kirjausryhmän liitetyn arvonlisäverokoodin käteisalennukset kirjataan. Tämä kenttä on valinnainen. Jos tiliä ei ole syötetty, käytetään **Käteisalennuksen koodit** -kohdan päätiliä. **Kirjanpidon kirjausryhmä** -kohdassa kannattaa ehkä käyttää eri tilejä, jos käytössä on arvonlisäveroryhmien Mitätöi käteisalennuksen arvonlisävero -kohta.  
11. Valitse **Asiakastapauksen alennus** -kentässä päätili, jonne tähän **kirjanpidon kirjausryhmän** liitetyn **arvonlisäverokoodin** käteisalennukset kirjataan. Tämä kenttä on valinnainen. Jos tiliä ei ole syötetty, käytetään **Käteisalennuksen koodit** -kohdan päätiliä. **Kirjanpidon kirjausryhmä** -kohdassa kannattaa ehkä käyttää eri tilejä, jos käytössä on **arvonlisäveroryhmien** Mitätöi käteisalennuksen arvonlisävero -kohta.  
12. Valitse **Tallenna**.

