---
title: Myyntipisteen offline-toimintojen tarjoaminen
description: "Tässä artikkelissa on tietoja Retail Modern POS -sovelluksen offline-tilasta, jossa myyntipisteen laite siirtyy automaattisesti kanavatietokannasta offline-tietokantaan, jos Retail Server ei ole käytettävissä. Artikkeli sisältää myös offline-tilan yleisiä asetustietoja sekä kertoo, miten offline-tietokannan ja kanavatietokannan välinen tietojen synkronointi tapahtuu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>Myyntipisteen offline-toimintojen tarjoaminen

Tässä artikkelissa on tietoja Retail Modern POS -sovelluksen offline-tilasta, jossa myyntipisteen laite siirtyy automaattisesti kanavatietokannasta offline-tietokantaan, jos Retail Server ei ole käytettävissä. Artikkeli sisältää myös offline-tilan yleisiä asetustietoja sekä kertoo, miten offline-tietokannan ja kanavatietokannan välinen tietojen synkronointi tapahtuu.

<a name="overview"></a>Yleiskuvaus
--------

-Moderni Retail POS-kohdan myynti (POS)-laite siirtyy offline-tilassa aina, kun retail-palvelin ei ole käytettävissä. Siksi retail palvelimen kanssa yhteys katkeaa, jos Retail POS-Sovelluksen Moderni siirtyy automaattisesti offline-tietokantaa. Jos tietopyyntö ei onnistu myyntitapahtuman yhteydessä offline-profiilissa määritetyn aikakatkaisuvälin aikana, Retail Modern POS vaihtaa automaattisesti offline-tietokantaan ja jatkaa myyntitapahtumaa. Kun myyntipisteen laite on offline-tilassa, Retail Modern POS yrittää muodostaa yhteyden uudelleen Retail Serveriin offline-profiilissa määritetyn uudelleen yhdistämisen yrityksen aikavälin perusteella. Tämä uudelleen yhdistämisen yritys tapahtuu vain tapahtuman alussa.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Retail Modern POS -sovelluksen yhteystilan määrittäminen

Retail Modern POS -sovelluksen tilan otsikko osoittaa nykyisen yhteyden tilan. **Yhteyden tila** -ikkunassa näkyy offline-tietokantasynkronoinnin edellisen yrityksen tila. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Online- ja offline-tilan manuaalisessa vaihtamisessa käytettävän painikkeen luominen

Voit lisätä painikkeen Retail Modern POS -sovellukseen. Tämän jälkeen online- ja offline-tilan voi vaihtaa manuaalisesti. Luo painike myyntipisteen toiminnolle **917 – Tietokantayhteyden tila**. Tämän painikkeen nimi on **Katkaise yhteys**, kun Retail Modern POS on yhteydessä vähittäismyynnin palvelimeen, ja **Yhdistä**, kun yhteys on katkaistu. Tämän painikkeen avulla toi tarkastella yhteyttä sekä katkaista tai muodostaa yhteyden Retail Serveriin. [![Retail POS-sovelluksen Moderni katkaisupainike](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Asennus
POS-laite (register) offline-tuki käyttöön määrittämällä **tue offline-tilassa** asetuksella **Kyllä** - **rekisteröidä** sivulla. Uuden entiteetin kanavan tietokanta luodaan ja myymälän kanavan tietojen ryhmään. Tämän jälkeen suoritetaan kaikki pakolliset jakeluaikataulut offline-tietokannan tietopakettien luomiseksi. Seuraavaksi Asenna Retail POS-Sovelluksen Moderni offline-version. Asennusprosessi Luo offline-tietokantaa. Asenna Microsoft SQL Server-2014 Express lisäksi, jos se on tarpeen. Offline-tietojen synkronointi alkaa, kun Retail Modern POS -sovellukseen kirjaudutaan ensimmäisen kerran.

## <a name="data-synchronization"></a>Tietojen synkronointi
Päätiedot lähetetään offline-tietokantaan Retail-ajastuksen avulla. Oletusarvoisesti tietojen muutokset lähetetään jakeluaikataulun suorittamisen jälkeen sekä kanavatietokantaan että offline-tietokantaan. Retail Modern POS sisältää asynkronoinnin ja synkronoinnin kirjaston, joka lataa kaikki käytettävissä olevat tietopaketit ja lisää ne offline-tietokantaan. Jos tapahtumia on luotu offline-tilassa, Retail Modern POS myyntipiste lataa ne vähittäismyynnin palvelimeen, josta ne voidaan lisätä kanavatietokantaan. Offline-tietojen synkronointi voidaan tehdä vain, jos Retail Modern POS on käynnissä. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


