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
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30870ea17ea73e48467698166ba14a9184f5a3b1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144809"
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

