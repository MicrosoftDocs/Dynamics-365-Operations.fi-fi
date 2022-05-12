---
title: Vähittäismyynnin laskelmien numerosarjojen määritys
description: Tässä aiheessa kuvataan, kuinka määritetään numerosarjat, joita tarvitaan vähittäismyynnin laskelmissa Microsoft Dynamics 365 Commercessa.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: db47ca4ee8bac0d55b9a9c732183d2734bce660f
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649197"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Vähittäismyynnin laskelmien numerosarjojen määritys

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan, kuinka määritetään numerosarjat, joita tarvitaan vähittäismyynnin laskelmissa Microsoft Dynamics 365 Commercessa.

Vähittäismyyntilaskelmatyyppejä on kahta eri tyyppiä Dynamics 365 Commercessa: 

- **Tapahtumalaskelmat** on tarkoitettu luotavaksi ja kirjattavaksi usein. Niiden avulla kirjataan myymälän kaikki ei-kirjanpitotapahtumat Dynamics 365 Commerce headquartersiin. 
- **Raportit** on tarkoitus luoda ja kirjata kerran päivässä. Ne sisältävät vain vähittäismyyntiliikkeiden suljetut vuorot, jotka on ladattu Commerce headquartersiin p-työn kautta.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Laskelmien kirjaamisen numerosarjojen määrittäminen

Kun olet määrittänyt vähittäismyyntimyymälän asetukset, Commerce headquarters -sovelluksessa on määritettävä yksilöivä numerosarja, jota käytetään laskelmissa laskelman luontiprosessin aikana.

Laskelmien kirjauksen numerosarjat määritetään Commerce headquartersissa seuraavasti.

1. Siirry kohtaan **Organisaation hallinta \> Numerosarjat \> Numerosarjat**.
1. Luo uusi tietue valitsemalla **Uusi \> Numerosarja**.
1. Anna **Tunnus**-pikavälilehden **Numerosarjan koodi** -kentässä numerosarjan koodi.
1. Syötä **Numerosarjan nimi**-kenttään nimi.
1. Valitse **Laajuuden parametrit** -pikavälilehden **Laajuus**-kentässä **Toimintayksikkö**.
1. Valitse **Toimintayksikkö**-kentästä myymälä, jossa numerosarjaa käytetään.
1. Määritä segmentit **Segmentit**-pikavälilehdessä.
1. Määritä **Viitteet**-pikavälilehdessä **Alue**-kentän arvoksi **Vähittäismyymälä**.
1. Määritä **Viite**-kentän arvoksi **Laskelman numero** ja valitse sitten **OK**.

    ![Numerosarjat-sivun Tunnus, Laajuuden parametrit-, Segmentit- ja Viitteet-pikavälilehdet.](media/retail-statements-num-seq-setup-01.png)

1. Päivitä **Yleiset**-pikavälilehden **Numeroiden kohdistus** -osassa **Pienin** ja **Suurin**-kentät niin, että ne vastaavat **Segmentit**-pikavälilehdessä määritetyn **aakkosnumeerisen** segmentin pituutta.
1. **Suorituskyky**-pikavälilehdessä on suositeltavaa määrittää **Esijako**-asetuksen arvoksi **Kyllä** ja **Numeroiden määrä** -kentän arvoksi **25**.

    ![Yleiset- ja Suorituskyky-pikavälilehdet Numerosarjat-sivulla.](media/retail-statements-num-seq-setup-02.png)

1. Tallenna muutokset ja sulje sivu valitsemalla toimintoruudussa **Tallenna**.
