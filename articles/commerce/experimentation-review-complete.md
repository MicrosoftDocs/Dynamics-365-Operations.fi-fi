---
title: Variaation määrittäminen ja kokeen päättäminen
description: Tässä artikkelissa käsitellään onnistuneen variaation korottamista ja kokeen päättämistä Dynamics 365 Commercessa.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942734"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variaation määrittäminen ja kokeen päättäminen

Tässä artikkelissa käsitellään kokeessa parhaan tuloksen tuottaneen variaation korottamista ja kokeen päättämistä. Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä artikkeleissa.

[ ![Kokeilun käyttäjän siirtymä – arviointi ja päättäminen.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Kun [koe on suoritettu](experimentation-run-monitor.md) ja on kerätty riittävästi tietoa sen määrittämiseen, mitä variaatiota halutaan käyttää live-sivustossa, variaatio korotetaan ja koe lopetetaan.

## <a name="promote-a-variation"></a>Variaation korottaminen
Kolmannen osapuolen palvelussa suoritettuun kokeeseen liittyvien tietojen ja analyysien avulla voi päättää, millä variaatiolla saatiin parhaat tulokset. Sen voi sitten korottaa korvaamalla live-sivuston nykyisen sisällön voittajavariaatiolla siten, että se on kaikkien käyttäjien käytettävissä.

Voittajavariaatio korotetaan seuraavasti: 

1. Valitse Commercen sivustonmuodostimen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe.
1. Valitse komentopalkissa **Päätä koe**.
1. Valitse **Päätä koe** -valintaikkunassa **Arvioi kokeen tiedot**. Voit arvioida avautuvassa kolmannen osapuolen palvelussa mittareita ja määrittää, mikä variaatio suoriutui parhaiten.
1. Valitse **Päätä koe** -valintaikkunassa voittajavariaatio ja valitse sitten **Seuraava**.
1. Avaa kolmannen osapuolen palvelu ja pysäytä kokeilu.
1. Valitse sivustonmuodostimessa **Päätä**. jolloin alkuperäinen live-sivusto korvataan ja voittajavariaatio julkaistaan. Sen jälkeen kyseinen variaatio on kaikkien sivuston käyttäjien käytettävissä. 

> [!NOTE]
> Jos valitset nykyisen live-sivun säilyttämisen etkä julkaise variaatiota, valitse **Julkaise alkuperäinen sivu uudelleen**.

## <a name="delete-your-experiment"></a>Kokeen poistaminen
Vaikka Commercessa päättynyttä koetta ei ole pakko poistaa, sen voi poistaa, mikä säästää tilaa ja siistii työntilaa. 

Valmiin kokeen voi poistaa Commercen sivustonmuodostimessa seuraavasti:

1. Valitse Commercen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe. 
    > [!NOTE]
    > Jos koe on edelleen aktiivinen, lopeta koe kolmannen osapuolen palvelussa ennen jatkamista.
1. Poista variaatiosisältö live-sivustosta valitsemalla komentopalkissa **Peruuta julkaisu**.
1. Poista koe valitsemalla **Poista**.

## <a name="previous-step"></a>Edellinen vaihe
[Kokeilun suoritus ja seuranta](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
